---
layout: post
title: "A case study on calendar designing for managers"
date: 2013-12-24 01:51:46 +0700
comments: true
sharing: true
categories: [Product Design, Casestudy, UX]
---

# A case study about designing calendar page for managers.

## The situation
As a business student, I certainly do not act like one. Long gone the day I stick around school, do some HBR case studies and discuss group projects with my mates. Once I taste the triumphant feeling of building stuffs from scratch, especially after building the UI at the coolest online ticket platform in Vietnam, [ticketbox.vn](http://ticketbox.vn "ticketbox"), there's no going back.

So when opportunity presented itself, I immediately jumped and took a shot at part-time front-end/interface designing for another Singapore startup called Beensprout. This time, the focus is about social networking for non-profit organisations. My first task was to put together a calendar page for non-profit admin.

A little bit background about Beensprout targeted users. There are two types of users: the organisers and the volunteers. The calendar page is mainly for organisers to manage different activities they have. Yet, even among organisers, there're different levels of authority. We have org admins, people who overlook the whole organisation's activity. We also have activity managers, who take care of specific activities within the organisation. At the lowest power level, we have event helpers whose tasks are to coordinate with activity managers to hold successful events.

## Initial stupid sketching excitement
The calendar I was tasked to design targets at org admins. The general instruction from my boss was just to "help them manage events". So with stupid enthusiasm, I popped open my [Paper53 app](http://www.fiftythree.com/paper "paper53") and sketched some interesting ideas.

![Version 1](http://i.imgur.com/wJAKIKl.jpg "Version 1")

![Version 2](http://i.imgur.com/ECySf1K.jpg "Version 2")


The idea behind prototype 1 was that org admins could color-code activities and filtered displayed activities using a tagging system. However, I quickly faced the problem of too many activities per day, which would rainbow-ize days with lots of activities, making it very difficult for users to tell what activities they have exactly.

For the second prototype, I wanted to explore a different option where org admins could track the exact progress of each activity. This was achieved by not using a standard calendar but instead limiting the timeframe to a weekly basis and giving each activity a row of its own.

Yet, after the sketching excitement was over, I realized my fatal mistakes: both options were made from my assumption about the users, without any input from real org admins.

## Fix it or it just becomes another Dribbble shot.
To prevent the DRIBBBLISATION of design (Padday has an [awesome post](http://insideintercom.io/the-dribbblisation-of-design/) about it), I took a step back and use what I learn from Ryan Singer of 37Signals when designing a web app. There were three high-level questions that I wanted to answer:

- What is the single task that the users are here for?
- How do users get to this page?
- What next after this step?

The answer to the first question seemed simple: org admins wanted to "manage" all activities and the calendar page should help them to do that. But there's one thing I didn't understand: What did org admins mean when they said they wanted to "manage"? What activities were they involved in? Did they decide what time an activity should happen? If yes, at what level of time detail could they interfere? Week? Day? Hour? Different time perspectives would certainly affect how flexible the calendar should be.

Seeing many potential questions similar to the one above, I decided to go back to the users for some chit chats. It turned out that my assumption about org admins wanting to look at detailed activities to help them schedule events was plain wrong. Scheduling activities was actually done by activity managers, which meant there would be a different calendar page for that.

To org admins, what they care about was not how detailed the activities were displayed, which rendered both my prototypes useless. Rather org admins wanted to have an overview of how "busy" the organisations were. The org admins believed that the more activities an organisation had, which meant more days were filled up with events, the healthier the growth of the organization.

For the second question, at that time, users could access the calendar page through a left hand side navigation via the "Activities" label, which my previous colleague had reserved when he built the page architect. But "Activities" didn't seem so clear to users about its functionality.

Could the label change to "Activities overview"? And how else can org admins reached the calendar page? Could the calendar page be the landing page? Sort of like the dashboard in other web apps to provide an overview to users?

For this I didn't really arrive at a good copy writing solution and had to leave it there for the moment. This was part of a bigger problem in navigation and I just didn't want to digress myself. A separate problem should deserve its own time and researches before proposing any fix. Thus, I would have to push the problem to parking zone and come back later.

Then, there was still one big question left to answer: what should the users do next? Based on previous interviews, after the initial overview, org admins needed to chat with activity managers to check their event progress. Sometimes they needed to add a new activity and assign certain organisers to handle that activity. The UI then needed to facilitate org admins to find these tasks easily.

Optimally, actions should be built-in to the context so that they provides a natural and smooth transition from task to task.

## Final objectives & design
With these inputs, I set out to decide my calendar page. Again, important ballpoints:

- Show healthy growth of the organisations through "filled/busy" days.
- Smart linking to next actions, including creating new activities, assigning organisers to activities, communicating to certain activity managers.

Now that I have real user inputs, it becomes easier to create and justify which wireframes should be the final.

![Version 3](http://i.imgur.com/smT1tlZ.jpg "This prototype only shows days with event at a glance, the users can still checkout detailed activity with the search bar.")

Another 2 iterations and I finally arrived at a [final prototype](murmuring-journey-2056.herokuapp.com), which is currently implemented at our Beensprout Beta page.

![Final prototype no search](http://i.imgur.com/G54P3zY.jpg "Each day now owns a progress bar to show org admins how busy a day is.")


![Final prototype with search](http://i.imgur.com/Ys90QVu.jpg "Org admin can still track detailed activities for actions like contacting the current activity manager, checking out activity time for a surprise crash.")

*Ps: the calendar styling is done with [clndr.js](http://kylestetz.github.io/CLNDR/ clndr.js), a js plugin that allow you to flexibly define the calendar markup. I highly recommend this plugin for customized calendar design.*