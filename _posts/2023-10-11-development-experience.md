---
title: "How working as a part-time developer made me a better technical writer"
---

Hello, fellow technical writers. Today, I'll share with you the story of how I gained substantial software development experience while working as a technical writer. The question of how much coding expertise a software technical writer should possess is an ongoing topic of debate, and I personally believe that the answer depends on a lot of factors. In this post, I will share my experience as a part-time developer and explore how this journey has influenced my career as a technical communicator.

I'll share the story of how I started, the things I worked on, how the experience has improved my technical writing, and I will speculate about the doors it has opened for me, professionally. This episode has been the most interesting I've had thus far in my technical career, and I hope that readers will benefit from learning about my experiences and perhaps even consider embarking on something similar in their own careers.

I'll begin with some context. I already had a fair amount of professional writing experience when I began as a technical writer, but I had very little experience coding. About one year into my first technical writing position, I dedicated myself to learning Python, coding for about an hour each morning before starting my workday. After spending several months on the basics, I challenged myself to automate various documentation tasks, such as making repetitive edits to large reference topics. What began as a way to improve my skills as a technical writer evolved into a love of coding.

## Working as a part-time developer

After about six months of basic coding practice, I initiated conversations with various engineering leads about how to progress further as a developer. An engineering manager offered the following opportunity on one of the products that I documented.

### The plan

I could onboard as a developer and spend a small amount of my time each day working on bugs in the development backlog. I would work only on non-urgent tasks, aiding the development team by clearing away old issues, benefiting myself by gaining more experience, and helping the documentation team by making myself into a more effective writer and collaborator. I discussed the proposal with my boss, and she agreed – on the condition that it did not affect my productivity as a technical writer.

Working from home, I spent about 90 minutes each day coding before work. And with any time remaining at the end of my workday, I would return to my development tasks. Determined to work through the problems that I encountered as a developer, I was motivated to complete my writing assignments quickly so that I could revisit the coding challenges that I faced.

### The work

Here are some of the issues I worked on in my first six months:

* Removed unused API endpoints
* Introduced context into RethinkDB functions
* Replaced string-typed context keys with unique types
* Fixed an endpoint that was returning the wrong HTTP error
* Improved logging in various CLI subcommands
* Fixed broken links in the product UI

Of all these experiences, the most helpful thing was learning how to navigate an extremely large code base in my editor. Once I had these experiences under my belt, I was prepared to take on something larger. First, I had the opportunity to work on a telemetry feature for a tool that customers used to migrate between versions of the product. Next, I worked on a similar but much larger feature that exposed key product metrics for a Prometheus server to scrape. In both cases, I was supported by senior developers who offered their help when I got stuck.

While the bug fixes and telemetry feature were low priority and I could take them at my own pace, the Prometheus metrics feature got pulled into a major release vehicle, thus taking on greater importance and urgency. This was a mixed blessing. On the one hand, it meant that I had to plan much more carefully so as not to interfere with my writing responsibilities. This was stressful, and honestly not something that I would recommend. But on the other hand, it meant that I was given a lot more support, and by working closely with a senior developer, I learned at a much quicker pace.

## What I learned

At this point, I want to note that for the majority of the time I worked as a part-time developer, I aspired to transition into a software engineering role. Eventually, I changed my mind, but I bring this up because I want acknowledge that it would have been difficult to remain motivated if I did not possess this goal. Given the nature of this post, I'll focus on how this experience has helped me as a technical communicator.

### Different paces

Working as a developer, I gained an appreciation for the different paces at which technical writing and development proceed. Unlike with writing, I found that when working on code I ran into difficulties at every step. And I discovered that it takes a long time to figure out each problem. This observation is relevant to technical writing for two reasons:

First, if you're a writer aiming to enhance your technical proficiency, it's important not to be discouraged when you find yourself programming at a considerably slower pace than you are accustomed. And I don't mean just in the beginning. I am of the opinion that programming work is simply a slower process than writing. While it is true that you will get faster at resolving issues as you learn, the nature of software development is such that you will encounter roadblocks at nearly every turn. Knowing this, you should not judge your coding acumen relative to the pace with which you are used to writing text.

This observation also engenders an important piece of empathy. The SMEs with whom we work often do not know the answers to the questions we ask them, but in fact need to research and tinker to give us the feedback that we need. While it is true that they have more context, thus making the process considerably faster for them, there is nothing inherent to writing that should exempt us from this activity. If we slow down and do more of the research and tinkering ourselves, we will get a better sense of the questions that we can answer on our own. This will lighten the research burden on our SMEs and garner important goodwill along the way.

### Exposure to the process

Another way that working as a developer has benefited my writing is through exposure to every part of the development process. From the design phase, on through implementation, followed by testing and QA, I observed where writers can be involved in the process and make meaningful contributions. When PRDs and design documents are created, technical writers can open documentation tickets and begin scoping their work. When the implementation work ensues, writers can attend standups and stay in the loop as the features evolve. And then, in anticipation of testing, writers can draft their documentation for early use by the testing team, and benefit from the feedback that testers are likely to share. Admittedly, you don't really need to work as a developer to get involved at all these stages, but in my own experience, working as a developer helped me to better understand the entirety of the process.

### Deploying and testing

The last benefit that I will mention comes from testing the code changes that I made as a developer. When you make a change to your software, you don't simply interact with the product code base. You also deploy and test the changes on your local machine, and it's often not an easy task. In my experience, this can be more challenging than working in the codebase itself. Learning how to do this will benefit your writing because this is precisely what you need to do in order to test whether your documentation is accurate and complete.

This is one of the most important skills I gained while working as a part-time developer. Through learning to deploy and test my software changes, I was able to spin up a technical preview and check whether my documentation mapped onto the reality of the product. Sometimes there are gaps in the information that we receive from our SMEs. What better way to figure out what those gaps are than to test your documentation and discover for yourself what it is missing? As technical writers armed with the ability to test the software ourselves, we can better advocate for our users by identifying the information that our documentation lacks.

## Looking forward

Working as a part-time developer has aided my work as a technical writer, and I suspect that it has given my career a boost as well. It is difficult to know for sure, but I recently changed jobs, and I think that having development work on my resume helped me to stand out and ultimately aided in securing my new role.

I have approximately four years of technical writing experience, most of which have been spent at the same company. I started applying to jobs in June of 2023, in a very competitive market. I applied to around 20 positions and interviewed at four – two start ups and two larger companies. Of these four companies I received an offer from one, a large tech company whose docs team has a great reputation. I was passed over by the two startups, and I withdrew my application from the fourth. In total, it took three months to secure the new job.

With so many recent layoffs, I'm sure that I was up against many candidates with more than four years of technical writing experience. Granted there is a lot more that goes into a resume than years spent on the job, and I am fortunate to posses other strengths, such as a master's degree, a background in professional writing prior to my transition into technical writing, and publicly available writing samples on complex technical subjects. Considering the challenges in the job market for technical writers, I was fortunate to secure interviews and a new position at a reputable company relatively quickly. Furthermore, a number of my interviewers, primarily developers and operations professionals, expressed a strong interest in my development experience.

I think that this post would be incomplete without acknowledging that not everyone will have time in their busy schedules to take on such a project as this and not every company will be willing to extend such an opportunity. Moreover, I believe that technical proficiency is only one among many different strengths that writers can foster to excel in their roles. Diving deeply into development work is not for everybody, and I don't think it's essential to becoming an excellent technical writer. In fact, in many ways it is overkill, as not all the skills learned are directly applicable to writing. But for me, the experience I've shared here unfolded in a way that has proven to be very beneficial, and I wanted to share it in the hope that others may find value in it as well.

One last thing that I will say about my work as a part-time developer is that it has helped me to feel more confident in my role. When I first started as a technical writer, I felt somewhat out of place. Seemingly everyone around me could speak the language of scripting, development, and cloud operations. Working as a developer, I learned to communicate in the same language as my colleagues. This helps my writing, but it also helps me to feel greater confidence at work. And feeling more confident, I am happier overall as well. Spending some time as a developer has been extremely beneficial to me in numerous ways.

I hope that if you're a technical writer who is looking to gain experience as a developer, this post has given you some insight into what this experience could entail.
