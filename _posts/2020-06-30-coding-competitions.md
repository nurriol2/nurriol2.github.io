---
title:  What I Gained from 3 Different Coding Competitions
permalink:  /2020/06/30/coding-competitions.html
---

Over the last few months, I've been working on building a project portfolio to showcase my abilities as a data scientist. I still have a lot to learn and refine, but I think it's rewarding to work on projects that were once just bullet points in a notebook. 

However, like many others, I suffer from personal project overload. Whenever a new idea comes to mind, it's almost impossible for me to wait until my current project is finished to start a new one. After a while, the half finished projects begin to outnumber the finished ones. 

Requiring something to break up this vicious cycle, I turned to online coding challenges. I consider online coding challenges to be any event that is organized for people with coding skills to solve problems. This definition includes the traditional hackathon and also extends to things like competitive programming.

Online coding challenges offer 2 opportunities that aren't usually available to me when working on most personal projects. The first is a chance to interact with other people with similar interests. Whenever I'm solving a complex problem, I make sense of the hard parts by talking through them. Admittedly, a majority of these conversations are with myself. So, I greatly value collaboration as a way to not only work through a problem, but view it from another (sometimes better) perspective.

The other reason I started integrating online coding challenges into my portfolio development is the strict deadline. Competitive programming competitions, for example, are scored based on the time it takes to solve the puzzles. Having a cutoff means I can't artificially add time to a project's lifespan because I want to work on something new.

I learned a lot from these events and I'd like to share some of that knowledge here. I hope to encourage anyone who is not already participating to try one out. I will include some useful links at the end to help you find your next online coding challenge.

---

# My First Hackathon #
At the end of April, I participated in the [Copenhagen University Remote Bioinformatics Hackathon](https://biohackathon.dk/). I knew very little about hackathons, but I had 3 years of microbiology research experience and finished a handful of courses in machine learning. I felt that this experience was a good enough basis to get started.

My team worked on the *Metabolic Disorders and Changes in Tissues* challenge for this hackathon. The goal was to create a machine learning model to predict fat content percentages in pancreas and liver tissue. For an added challenge, we were tasked with discovering "useful" correlations between metadata and fat percentage.

I was excited to graduate from the artificial problems found in the textbooks to a real world, open ended problem. I was even more eager to code on a team. I treated this hackathon as a litmus test for my ability to perform as a data scientist. *That was my biggest mistake*. 

After hours of anxious coding and apologetic commits, I learned what this hacakthon  was trying to teach me:  **put distance between myself and the problem**. When I stopped treating this hackathon like a performance review I noticed my contributions approaching my expectations.

A good example of this lesson in action happened while I was working on the data pipeline for our mean value prediction model. The data set we were given had a cause of death column and many records contained multiple causes represented as lists. I wanted to unravel these lists so that records with overlapping causes were grouped together in a new data frame. This is a problem I knew I had the skill set to solve. 

But, the function I wrote to transform the data wasn't passing any of the test cases and 90 minutes had already gone by. After taking a short break, I realized that this wasn't a closed-book exam. I wasn't being critically observed under a microscope. I could reach out to my teammates or whiteboard my ideas. *I had Google*. 

I became so desperate to keep my incompetence a secret and fix a problem with *me* that I denied myself almost every resource I had available. Putting that distance between myself and  the problem I had to solve was how I overcame that distraction. I ended up drawing a flow diagram for my function, fixed the bug, and implemented my solution successfully. 

I'm glad to have learned this lesson so early in the "coding gauntlet" that has been the last 3 months of my life. It's a frame of mind that I carried into the next two events and one that is an integral part of my workflow.

I'm only able to put this lesson into words because of the great work by Jose Browne. After reading his article ["On Coding, Ego and Attention"](https://josebrowne.com/on-coding-ego-and-attention/), I was able to understand my experience and present it here.

# Hadamard Help Us on Problem 4 #
Before the dust had settled in Copenhagen, I heard about the [IBM Quantum Experience-May 4th Challenge](https://www.ibm.com/blogs/research/2020/04/ibm-quantum-challenge/). I was fascinated by quantum information in university and looked for research opportunities in that field. Even though I joined a biological physics research lab instead, quantum information and quantum computing has remained one of my peak interests. When I saw a Reddit post about this challenge, I couldn't pass up an opportunity to use real quantum hardware.

The IBM Quantum Experience Challenge was a four day celebration of the first quantum computer that could be programmed over the cloud. The quantum computing community was given 4 problems to solve using the IBM Experience. These problems covered different areas of quantum computing such as the BB84 Protocol. 

The organizers boasted problem 4 as difficult for even quantum computing experts. After working on it for nearly 2 days, I certainly agree; problem 4 demanded my best work and a lot of researching to solve. Luckily, though, [I was able to submit a correct solution](https://www.youracclaim.com/badges/b02f32fa-5633-4b4a-ba81-784758a6df6d) to all of the problems with 8 hours to spare!

The May 4th Challenge cemented the idea that **online coding events can be valuable experiences for rising professionals**. I solved problem 4 by reading through pages of Qiskit documentation, asking the IBM mentors and many fellow Qiskitters for guidance, and a substantial amount of debugging--all against a deadline.  This parallels a vital portion of the new developer experience:  navigating unfamiliar documentation and utilizing mentorship to produce a deliverable *on time*. So by participating in this really fun event, I'm also practicing valuable workplace skills. 

The May 4th Challenge serves as a reminder to me that these coding challenges (and my personal projects) are truly a medium for practicing the skills necessary to succeed in the workplace, *before I get there*. As usual, I'm keeping track of the frameworks and libraries I use throughout these projects but since the May 4th Challenge, I'm also taking note of the soft skills I learned along the way. 

# Competitive Quantum Computing #
The most recent event I participated in was the[ Microsoft Q\# Coding Contest - Summer 2020](https://codeforces.com/blog/entry/77614). Unlike the May 4th Challenge, during the main event I was competing against other quantum computing enthusiasts to see who could solve the problems the fastest. So, collaboration was not allowed during the contest.

Solutions to this challenge were required to be submitted using the Q\# (Q-sharp) programming language. Q\# is a language developed by Microsoft for writing quantum algorithms.

Up until this point, all of my quantum computing coding experience had been using Qiskit. Qiskit is a framework that allows you to write quantum algorithms using Python code. Since Python is a language I'm already familiar with, getting started with Qiskit meant I could focus on the quantum computing concepts, not the code itself.

Q\#, on the other hand, was an entirely new language. Preparing for this event was incredibly fun because in order to do well, I had to practice like I was training for an athletic event. That is, I had to consistently drill the fundamentals (Q\# syntax, control flow, libraries, etc.), memorize plays (or in this context, frequently used quantum circuits), and build up my speed.

To truly master a new programming language takes much longer than the 2 weeks I spent studying. However, I was able to learn enough Q\# to finish 302nd out of 710 participants! Comparing the solutions to my own attempts showed me where I needed to improve, but it was encouraging to know I was on the right track for a few more problems.

The most important take-away from this competition, for me, was **don't be afraid to abandon a solution**. I frequently find myself looking for similarities between the problems I already know how to solve and the ones presented to me. In general, I think using what I know to learn something I don't is a good strategy for demystifying the unknown. 

But on problem B1, I think I would have a better score if I took a fresh approach. During the competition, I was convinced my approach was correct. I did the pen-and-paper calculation ten times over, tested and debugged my code, and everything seemed fine. The test suite, however, told a different story. 

What I failed to do was reference an incredibly similar problem from the warmup round. Instead, I only focused on *forcing* my solution to work. Knowing that I could've performed better by essentially giving up is counterintuitive. But, I don't think I've had enough lessons in stubbornness, yet. So, I'm glad to have this one.

One of the great things about writing code is that it seems like you really can build anything you want, however you want. But in reality, there are some things you can't build with a hammer no matter how hard you try. It's better to give up and use something else.

Moving forward, I'll be sure to differentiate when I'm being stubborn versus when something requires perseverance. In doing so, I hope to improve equally as a problem solver and as a person.

---

# Thanks! # 
I hope you enjoyed this blog. If you did (or even if you didn't) let me know! Feel free to [connect with me on Twitter](https://twitter.com/_ElliotF).

---

# Resources for Online Coding Challenges # 
I found out about the Microsoft Q\# Coding Contest through people I met during the May 4th Challenge. I think that experience speaks to the value of getting started with just *one* event and staying involved. Eventually, you'll hear about other events. Below is a list of some great platforms for getting started with online coding events. The entries are categorized so hopefully you can find one you enjoy. 

*I intend to loosely keep this list up to date.*

## Competitive Programming ##
- [https://codeforces.com/](https://codeforces.com/)
- [https://atcoder.jp/](https://atcoder.jp/)

## Data Science Centric Events ##
- [https://www.drivendata.org/](https://www.drivendata.org/)
- [https://www.datakind.org/](https://www.datakind.org/)
- [https://www.kaggle.com/](https://www.kaggle.com/)

## Hackathons ##
- [https://www.reddit.com/r/hackathons/](https://www.reddit.com/r/hackathons/)
- [https://devpost.com/hackathons](https://www.reddit.com/r/hackathons/)

*If hackathons are more your style, I recommend joining social media communities in your area of interest, too. For example, searching Twitter tags or following Reddit subreddit communities.*