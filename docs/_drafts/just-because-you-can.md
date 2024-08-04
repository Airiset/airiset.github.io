---
title: Just Because You Can Does Not Mean You Should
---
Almost all career programmers will, at some point, be met with one of the most
dauting challenges of software engineering: team work. <!--more--> Whether you
find comfort in isolation or thrive in social circles, working in a team will
be, at first, a challenge for most developers.

This is not true only for programmers, but all activities that require team
work. We are all humans, after all. We tend to form in-groups and out-groups.
We gossip about each other's drama. We build friendships and give birth to
enemies and rivals. History is but humanity's struggle with itself; difference
engenders conflict, and conflict leads to changes.

Just like in most human activities, software developers usually interact with
others, be they developers, users, co-workers, or managers. But most will be
unprepared when they are first entering the industry.

In some ways, programming is more akin to painting than engineering.
Programmers dabble in the art of coding. Alone, afront the digital canvas, a
programmer composes a choreography for their machine to dance to. The
usefulness of their work sometimes is irrelevant. Sometimes, the artwork is
meant as an exploration of certain mediums (programming languages, or
environments) or techniques (be they paradigms or frameworks). Sometimes, the
usefulness of the piece is overshadowed by the effort in composing it.
Sometimes the program is a stroke of genius, complete and (impressive?).
Most of the time, the program is of little use, and unfinished. The code is
written by the programmer for themselves, and rarely does it go to others.

Used to the individual nature of the task, programmer's are usually unprepared
once they begin to program in groups. Code in group projects is inpersonal,
and thus initially unnatural to those who first code on their own. This is
something I myself experienced many times. The differences in expectation of
each mode of programming are vast. However in time, I got used to team work.

One of the first lesson's I believe programmer's new to this mode of coding is
to learn to be respectful of their team mates. By this, I do not mean respect
as in admiration, the kind that has to be earned. Rather, I mean the minimum
modicum of respect of another person's boundaries and of their opinions. I
learnt this lesson early, back in my third year of university, in an
introductory course to software engineering practices.

For many students in my program, this was a first taste of what working in the 
industry would be like. Most of the grade was allocated to the course's final 
project. In this project, groups of five to six students would partner with a 
company/organization of their choice. Groups would use the skills they learned
in class to develop a product as specified by the partner. Having not worked
any internships yet, I was excited at the opportunity. I was quick to recruit
friends and classmates who I knew shared in the excitement. We picked out a
partner and quickly setup a group structure. I was the de-facto leader, and the
main point of communication with the partner. Our partner, Bob, asked us to
upgrade an app he had previous students develop for him. The main features
requested by Bob were improving the mobile app's UI, friend requests, and
messages between users. The app was implemented in Reach Native, and the 
business logic was managed by a Django backend. We decided to split into
two teams, one to work on the frontend and another on the backend, with
sub-teams composed of members of both teams each tasked with implementing
a feature. All looked well. I had great expectations for our team. But
everything changed soon enough.

I woke up late that Sunday. On my inbox, I saw a notice from the course
instructor about a new member to our team. Let's call this person David. He
had also requested to be partnered with the same company, but had no team of
his own. Instead, he became the seventh member of our team. 

We were all quick to meet together and welcome David to the team, and gave him
the choice of being part of the frontend or the backend team. Soon, I was 
impressed with David's skill. He was quite talented, the sort of 10x software 
engineer programmer's love to mythologize about. David built a quick prototype 
of the upgrades to show to Bob. We all saw great potential in his skills. We
chose to have him work as a full-stack developer, to give him enough room for
him to apply his talents.

Jumping into the backend was no easy task. As expected of computer science
students, the codebase lacked almost any documentation. None of the API
endpoints had any descriptions on what input they expected or what they
returned. Comments were rare, and all the ones we found consisted solely of
non-working code that was commented out but left in place for all of us to see.
The initial setup of the project was slow, but we started adding the features
little by little.

We noticed that David stopped contributing to the project. He refused to go 
over the unreadable mess that was the backend. After a week of attempting to
convince him to give the backend a try, all progress stopped due to David's
refusal to contribute. A meeting was called. A lively debate between David and
the rest of the team spurred off. David insisted on a full rewrite of the
backend, something I felt would distract us from working on the features we
were requested to implement. I claimed that on top of delays, there was much
to learn from attempting to understand the backend. In fact, that was something
I was already working on, having documented the behaviour of half of the
existing backend. I insisted that understanding the "legacy" system would be a
small hickup, but would be a good learning experience. The team agreed. David
still did not.

A few weeks passed, and David still refused to work on the legacy backend. We
began to make progress, with some of the needed endopoints implemented, and
some older bugs we had discovered were fixed. In our meetings, David kept
insisting on a rewrite. I insisted to David that was not what Bob had agreed
to. Shockingly, David said that we didn't "owe" anything to Bob since he was
not paying us, which I found quite disrespectful. Few days after that meeting,
it would be the mid-term Reading Week, and I was glad for a short break. We
agreed to a pause to development so that we could catch up on our other classes
and study for midterm examinations.

After a short week of studying and resting (mostly resting than studying, to
be frank), I felt refreshed and ready to go back on developing the app. I was
not expecting any surprises, especially not the one David had for us. Turns
out that during Reading Week, David had performed a complete rewrite of the
backend. There was a problem, however. The new backend could not be plugged
in as a replacement of the old one. The API endpoints were different and
returned different values to the legacy backend, and we could not incorporate
the features we spent weeks working on because David chose to use a
completely different framework.

Personally, I felt insulted. I was livid at the arrogance that David had
displayed. However, I was wise to not show it. I tried giving David's backend
a try, but as I read through it, David's claim that his code was much
"cleaner" and "well-documented" were clearly blown out of proportion. The
endpoints were clear, but the code lacked documentation. The framework relied
on convention for its configuration, so it would take a while for me to
understand the new codebase and rewrite what we had already developed to work
on the new backend. Moreover, the frontend team would need to rewrite how they
handled the requests to and responses from the new backend. It would be a
couple of weeks lost to accomodate David's work, which would delay us all from
completing what Bob had requested from us.

I talked to some of my teammates about this, and they agreed it would be a
waste of time. We convened a new meeting with David. We told David we would
not move forward with his backend and keep working on the old one. He was
clearly angry, and he refused to contribute anything else in the project, as,
in his opinion, he had "done all the work." We went to the professor and the
teaching assistants for help, but no one could convince David to work on the
project.

I was getting exhausted of dealing with David. Instead, we had him
do something completely unrelated to the codebase. We needed a fast way of
deploying a debugging version of the backend so that it could be tested in
conjunction with the mobile app, so I asked David to use his talents to setup
a CI/CD pipeline. He swiftly got it to work, but for some reason chose to host
it on his own domain. We tried to tell him to build something we could hand-off
to Bob, but our pleas fell on deaf ears. He even went on to speak to the TA,
claiming that he had done all the work and we had done nothing, which was
patently false, given that he had yet to touch the old backend or the mobile
app.

We were able to get all the features working on the app and old backend. We
made a presentation for Bob and the class instructor on what we built. In
David's opinion, we had not achieved nothing, but I was satisfied with the
features we had built. For a small project for a course, it was a good learning
experience. My other teammates, except for David, agreed.

If there is one thing I learnt about working in teams, is to never act like
David. He may have been a talented developer, but his arrogance and single
mindedness prevented him from being useful like the rest of us. I hope one
day, David learns that lesson. I wish him the best on his future endeavours,
but I am glad I don't have to work with him any time in the foreseeable future.
If you are reading this, David, know this: team work will always be hard if
you piss off your team mates. Do not do that if you wish to be successful.

