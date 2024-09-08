---
layout: post
title: The Encyclopedia Agatha
subtitle: How I Made My Profile Picture

categories: [Rust]
---

_The Encyclopedia Agatha_ is a web app tool to generate visualizations of an
_insect-like, digital creature called an `eBug`._

When I started this blog, I wanted the logo to be (or represent) something that
I made.

Based on this decision, I thought of a few options.
I could:

- Take a photograph
- Upload a drawing or painting
- Design a logo in [Krita](https://krita.org/en/)
- [Build a paint-like program from scratch](https://www.youtube.com/watch?v=czfvHUw4sks) then draw a logo with it
- [Learn to model a character in Blender](https://www.youtube.com/watch?v=jnj2BL4chaQ&list=PLn3ukorJv4vuU3ILv3g3xnUyEGOQR-D8J&ab_channel=GrantAbbitt)

Each of these options seemed fun in their own way.
I can still build these projects in the future.

But, to me, none of these options felt like they were a good fit to get a first
draft _done_.
I'm trying to get more things _done_ these days.

I gave myself a week to make a decision.
During that week, I considered the originality, clarity, and customizability of
different ideas.

I also thought about:

1. Having a fun way to shout out friends throughout my blog
2. Thanking people (in a fun and unique way) for contributing to the blog
3. How this project could automatically generate a logo for me

Next, I graded (more like vibe checked) each option based on how fast I
estimated finishing a proof of concept and a minimum viable product.

Thankfully, in the 11th hour, a conversation with [#e850...](_Coming Soon_)
sparked the idea to combine my fascination with insects and arachnids with my
love for a game called [Dwarf Fortress](https://www.bay12games.com/dwarves/?).

I had it...

_The Encyclopedia Agatha!_

(Can you tell I've been reading _Foundation_?)

The Encyclopedia Agatha is a web tool for generating unique, insect-like,
digital creatures called `eBugs` for all of your friends and family!

I talk about the technical details in [this post](https://elliotsmaker.space/2024-09-08-agatha-technical-details/).
But, generally speaking, `eBugs` are silly visualizations based on a _SHA-256 hash_
of an input `Message`, under the hood.

After making a list of features to define the boundaries of a proof of concept
and a minimum viable product, I started prioritizing responsibilities. I think
the hardest part to learn will be understanding [PlasCAD](https://github.com/David-OConnor/plascad).
I prefer to [eat the frog](https://elliotsmaker.space/2024-09-08-agatha/) in most situations.
But learning the details of a new tool before getting something on the screen
is not a good way to get things _done_ - (at least, in my own experience)).

I list the methods I chose to _emulate_ PlasCAD's behaviour in [this post](https://elliotsmaker.space/2024-09-08-agatha-technical-details/)
about The Encyclopedia Agatha's technical features.

Let's get coding.
