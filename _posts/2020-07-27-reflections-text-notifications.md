---
title:  Reflections On Automating Text Notifications with Python
permalink:  blog/2020/07/27/coding-competitions.html
---

I'm embarrassed to admit that it took me almost a year to notice the opportunity for this project. But thanks to the great work ethic and dedication from my director, the team has had personalized text reminders every day since I started in 2019. It wasn't until a week ago that a slight mishap kickstarted this whole project.

In this post, I'll go over exactly what motivated me to build this program, explain some of the design decisions I made, and list future updates.

[Github Repository](https://github.com/nurriol2/work_notifier)

--- 

# Getting Started

One of the nice perks of my current job are the daily text message reminders from my director letting us know who is working and at what time(s). It saves me the trouble of logging into my Google account and checking the schedule. Additionally, they allow the team to instantly notify our director if there's a conflict or mistake. 

Since I started in 2019, these reminders have been sent to us personally from my director. For a few months, the messages were sent to each team member individually, which must've been tedious. Recently we transitioned to group texting, but even then the process is prone to human error.

For example, last week (from the time of writing) my director almost forgot to send out the reminders. Myself and much of the team had already checked the online schedule and planned accordingly. Nonetheless, my director apologized for sending out reminders so late and was lenient about any short notice conflicts. I thought this was especially nice of them.

It was at this moment that I realized how quickly a minor mistake could've turned into a logistical nightmare. I've automated simple tasks with Python before, so I felt confident that I could do the same here. After a few days of coding, the first version is finished. The project repository can be found [here](https://github.com/nurriol2/work_notifier). 

# Design Decisions and Why I Made Them

During the planning phase, I thought a lot about *what* I would make to solve this problem. On one hand, I could build a generalized, full-stack web application that anyone with a similar problem could use. But, did I really *need* to?

If you read my last post [What I Gained from 3 Different Coding Competitions](https://elliot.bearblog.dev/coding-competitions-blog/), you might already have a sense of how much I value seeing a project through to the end. But that end isn't always clear when working on personal projects and that's what kills momentum. 

For this project, I decided to define my end as the minimum viable product (MVP). That is, the most basic *thing* that fully accomplishes everything I want it to do. I defined my MVP as something that would accomplish the following, in order:

1. Be usable with absolutely no extra effort from my audience (e.g. my director)
2. Emulate the behavior I expect from the personalized reminders
3. Is extensible 

After a few days of coding, I think I succeeded! Some examples of real text messages from the project can be seen at the Github link above.

I was able to automate running the script by using cron. On Unix systems, cron is a software utility that allows users to schedule "jobs", which are essentially bash commands, to run at specified times and intervals. If you'd like to learn more about cron, I recommend this video by [Corey Schafer](https://www.youtube.com/watch?v=QZJ1drMQz1A&t=0s). The cron table was fairly easy to set up and quickly eliminated the heart of my problem:  humans forget. 

I abstracted away many of the remaining pieces through several interacting modules. For example, a single module handles parsing the selected Google Sheet for everyone's hours while another handles fetching and preprocessing that Google Sheet.

Building my MVP in this way allows me to "sell" this project as a solution, rather than a neat trick. That is, I can definitively say to my director, "Here's something that fixes what's broken". I think this is an important micro-lesson for an aspiring data scientist like myself. 

I think an under emphasized part of being a data scientist is being able to produce and sell solutions to problems. The machine learning algorithms and advanced programming skills are incredibly important tools, but to a business client they are just neat tricks. At the end of the day, an actionable solution is more valuable than a clever algorithm.

*It is here that I'd like to thank J. S. and S. H. for helping me debug the parsing algorithm. I couldn't have done it without you!*

# Future Improvements

I mentioned in the last section that I wanted there to be no input effort for my audience to use this project. I was only able to accomplish this because I built this project to specifically shift a lot of the "start up 
cost" to myself.

As can be seen in the README at the Github, setting up credentials with Twilio and Google Cloud is pretty tedious. Luckily, once it is done you (probably) won't have to set it up again and the responsibility falls on you to ensure the cron table is formatted correctly for your needs.

Streamlining this process has the highest priority for future iterations of this project. While it's entirely possible to "sell" this solution by setting it up on your machine and taking full responsibility for its function, there's something to be said about putting a product in the client's hands. 

To that end, I think a web application that allows you to log in with your Google account would be the ultimate goal. If you have suggestions, I'd love to hear them! Let me know [@_ElliotF](https://twitter.com/_ElliotF). 

---

I had a lot of fun with this automation project. My focus must return to a larger data science project for the time being. But, I will make small improvements in the source code whenever I can. Check back here for updates! When the time is right, I'll fully develop an application.

Thank you for reading this far. I hope you enjoyed seeing my thoughts on this project. Please feel free to [connect with me on Twitter](https://twitter.com/_ElliotF).