---
title:  Learning Rust A Pattern Matching Exercise
permalink:  til/rust-pattern-matching-exercise.html
---

I'm working through ["Take your first steps with Rust"](https://docs.microsoft.com/en-us/learn/paths/rust-first-steps/). This series isn't the traditional starting point for learning Rust, but it's working for me. 

In the **"Handle errors in Rust"** section, there was an exercise that gave me more trouble than I was expecting. In this post, I'll be solving the problem and sharing some notes.

If you don't want spoilers for the answer, I encourage you to stop now, work through the tutorial yourself, and come back. The specific problem can be found by [clicking here](https://docs.microsoft.com/en-us/learn/modules/rust-error-handling/4-exercise-use-option-type).

# The Problem

In this exercise, we need to complete the function `build_full_name` so it returns a person's full name. A person's full name follows this template:  

`First Name (Middle Name) Last Name`

Full name data is stored in the following `struct`:

```
// Copied from exercise with my own comments

struct Person {
    first:  String,
    middle:  Option<String>,
    last:  String, 
}
```

Notice that `middle` is an `Option<String>` type. That is because we assume that every person has a first and last name. *But not every person will have a middle name*. Either `middle` will be `Some(...)` when a person does have a middle name or `None` when a person does not have a middle name. We need `build_full_name` to handle both possibilities. 

# The Solution(s)

I can see there are 2 ways to solve this problem because this module introduces 2 ways to do pattern matching in Rust.

I think the intended solution is to use an `if let` statement. In Rust, an `if let` statement is a way to do pattern matching that is more concise than `match`.

I think the solution using `if let` would be:

```
// Inside `build_full_name`

if let Some(dummy_variable) = &person.middle {
    full_name.push_str(dummy_variable);
    full_name.push_str(" ");
}
```

--- 

## Note: The advantage of `if let`

With an `if let` statement, I have the ability to execute an entire code block when the variant matches the pattern. So if the procedure I needed to do on match was multiple steps or very complex, I could contain that entire procedure in this code block. 

It's *possible* do the same thing using `match` but, as we'll see in a moment, it's kind of awkward to write - for a Rust beginner like myself, at least. I haven't seen many examples where match arms did more than a single task.

---

## Note:  A dummy variable catches the general `Some()` case

I think this is something that will come with practice, but it's a good reminder for myself to write it out here. To match the general `T` type (as opposed to a specific instance of the type `T`), you pass a dummy variable to `Some(...)`. Each solution to this problem has examples of this dummy variable.


Here is the second solution I thought of by asking myself, "What is the equivalent `match` syntax for the above `if let` statement?"

```
match &person.middle {
    Some(dummy_variable) => {full_name.push_str(dummy_variable);
    full_name.push_str(" ");}, 
    _ => {}, 
}
```
As can be seen above, I simply wrapped the same 2 steps in a codeblock and set it as the result of the `Some()` variant match arm.

We're using a dummy variable to match with `&person.middle` since we don't know the middle name beforehand.

---

## Note:  Do match arms "usually" execute entire blocks?

As I'm writing this, I realize that it might not be unusual for a match arm to execute a codeblock. I'm certainly a Rust beginner, so my perception about what is (un)common could be skewed by the fact that I just haven't read enough Rust code yet.

Actually, I see that there has been a tiny hint hidden in plain sight:  the wildcard arm! Up until now, I've been blindly accepting that the syntax for "do nothing" in pattern matching is `_ => {}`. This arm is saying "on wildcard cases, **execute this empty code block**. I have definitely seen this syntax scattered throughout different Rust codes. So, maybe it's not too unusual.

---

## Note: Why is it "obvious" that the `Some()` variant takes `&String`, not `String`?

While I haven't gotten to the references section in this tutorial series, yet, I started learning the absolute basics of references from other Rust guides.

So, I think there are 2 ways of answering this question. The first (and easiest) way is to incorrectly use `String` let the compiler correct you.

The other way I thought about this was by considering the `Some(...)` variant case. The `struct` would look something like: 

```
// Mental model of `Person` for the `Some()` variant case

struct Person {
    first:  String,
    middle:  String, // Note the change here
    last:  String, 
}
```
Because the person we're considering does have a middle name. Then, that `String` is owned by the `struct`. So, I can only pass a reference to the data to the pattern matching. Also, `build_full_name` has extra hints that passing a reference might be the right thing to do:

```
// Copied from exercise with my own comments

fn build_full_name(person: &Person) -> String {
    let mut full_name = String::new();
    full_name.push_str(&person.first); // A reference is being passed here
    ...
```
---

# Conclusion

The official answer for this question can be viewed by [clicking here](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=67db8775239bbd297229bdea23a438e2%3Fazure-portal%3Dtrue).

The official answer differs slightly from what I wrote. I notice that in the official solution `middle` is passed as a reference to `push_str`.

```
// Copied from exercise

...

if let Some(middle) = &person.middle {
    full_name.push_str(&middle); // Passing a reference
    full_name.push_str(" ")
}
...
```

But in my solution, I do not pass a reference.

```
if let Some(dummy_variable) = &person.middle{
        full_name.push_str(dummy_variable); // Not passing a reference
        full_name.push_str(" ");
    }
```

Both solutions build and run without any warnings or errors on Rust Playground and on my local machine. I think I should learn more about ownership in Rust and come back to this question.






