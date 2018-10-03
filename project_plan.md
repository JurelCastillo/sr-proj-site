---
layout: default
title:  "Welcome to Jekyll!"
date:   2016-02-12 17:50:00
categories: main
---

# Project Plan

# Overview
Intellireview 2.0 2018-19 is a continuation of last year’s group’s attempt at updating Intellireview by Language Intelligence. Intellireview is a web application that allows Language Intelligence to show it’s already translated files to their customers for review. Their customers can then make suggestions, add comments, and edit translated lines to make the translated content more true to the original message. In this way, the customer gets involved in the translation process. Language Intelligence has been using Intellireview for over 10 years. Intellireview was first created in 2006 before HTML5, CSS3, and jQuery. Today, we have made many advances in web development including better cross-browser compatibility and web standards that Language Intelligence is looking employ when building the new Intellireview platform. 

We spent the first 4 weeks refactoring and understanding last year’s group’s code. We decided to take this much time because during the first meeting we had with our sponsor, they informed us of a major blocker for the previous team, the parser (more information later when we get into the deliverables). We wanted to understand as much of the current code as possible so that we don’t have to tear down much of what last year’s group did. We wanted to leverage the work they did, and when testing what was completed, we found that some things were bugged. We fixed those issues. Coincidentally, we also chose a spiral methodology this year, the same as last year’s group. After a meeting with one of the previous group members and an explanation of the file format we are expected to support, we feel ready to commit to project plan.

# Goals and Scope
We first decided to rank all of the requirements on the project description based on its priority. We gave the highest level of priority to those items that we felt were integral to the performance of the application. We ended up deciding we had 4 levels of priority with sublevels for those special cases. We decided what we want to tackle these next 2 semesters based on that priority level. Some of the things that are high priority did not get put in scope, but we decided that if we have time, we will most certainly devote time to those things. We decided to commit to few tasks that can be completed because of the parser. After we decided what is and isn’t in-scope, we determined how likely is that task going to be a blocker for another task, or be blocked by another task and that is our “risk” measure. About every month, because we are using a spiral methodology, we will revisit this “risk” measure and re-analyse in greater detail how and why it could be dangerous to pursue. After that we decided how long each task might take to get a rough timeline estimate. We created an excel spreadsheet with our plan.

This is a list of what is in scope:
* Time Tracking: Tracking the time spent by users in the system, the time they spent working on a project, etc
* Manage Login Credentials: Reset password functionality and allowing users to log into the system.
* Exposed API for projects: The API shall be exposed so that Language Intelligence’s project management system can use it to create projects and view file uploads.
* Sending Automated Emails: Whenever a milestone is reached (users get added to a new project, the customer completes their review, a reviewer completes their review, the translator completes their update, and the project gets marked as complete), an email will be sent out to all the relevant people.
* Accept or Reject changes: The reviewer should be able to accept or reject changes made by the customer
* Allow comments/suggestions: The customer should be able to make comments and suggest changes or edits.
* Fallback mechanism: Since we are doing Translation formats, this is just the default translation format
* Create an audit trail: Track what occured when. Timestamps are included here
* Customize translations format: This is tied to the parser. We believe it could take a while to understand the different translation formats and filters. It is high on our priority list, but the parser is going to be a major blocker for this task.
* Track translation changes: What users changed or made what suggestions. Tied to audit trail and comments/suggestions
* The parser: Takes in an xml or sdlxliff file and converts it into a json object that will be used by the frontend react component. The parser should maintain the structure of the original file. A format or filter can be applied to a file before and after submission, the parser must take that into consideration when building the json. 

And what we think we could possibly commit to if things go smoothly (we factored these in when creating our timeline estimate):
* Concurrent editing: This is very high on our priority list. We want to make sure everything else (mostly the parser) is stable and mostly complete before attempting to tackle this. The moment we feel comfortable taking on additional work, we will add this task in.

These items are out of scope:
* Support ancillary files: We don’t know what this means.
* Find and Replace: We feel like this would take quite a bit of time to implement, and may be pretty difficult.
* Terminology identification: We don’t fully understand what this entails
* Spell checking: Decidedly unenthused by the idea of needing to support this
* Tutorial: This is very low on our priority list. We don’t think this will be very difficult, but we also don’t want to devote a lot of attention to this until the very end when we have the other tasks completed.
* Performance: We put this out of scope, because we don’t know how we would test this. Of course we will be attempting to keep thing pretty quick locally, and even on a server that may be nearby, but without a VPN or dev environment to test this we can’t commit to performance globally.

# Risk analysis
We only analyzed the things we believe may affect the project.
* Time tracking: (Low) If implemented correctly, this is a pretty stand alone function of the system
* Manage Login Credentials: (Low) Pretty stand alone function of the system. The only issue would be if we can’t log into the system to test other things, but we have found a work-around for that already.
* Exposed API: (Low) if its a good api, it will have exposed endpoints.
* Sending automated emails: (Medium) It depends on most of the other parts of the system. We need more information on what is being sent when and by whom from where. This won’t block anything, but will get blocked by other tasks
* Accept or Reject changes: (Low) This is core functionality, but not a lot of things hinge on this task.
* Allow comments/ suggestions: (Medium) This is core functionality, and a lot of things hinge on this task. Suggestions are inline, and comments are on the side bar.
* Audit Trail: (Low) Should boil down to a logger that everyone uses as often as possible.
* The Parser: (High) Literally a blocker for the previous team. Prevented almost all of the core functionality. We are looking at this one with a magnifying glass in case anything happens.
* Concurrent Editing: (High) Core functionality, A lot of other things hinge on this
* Customize Translations Format: (High) Core functionality, probably difficult to implement
* Track Translation changes: (Low) Same as audit trail.

# Scheduling and estimates
Produced a Work Breakdown Structure and used a judgmental combination of the WBS-based estimation with group estimation via Planning Poker. This is assuming 8 hours a week, per person on the task, but each task may have more than one person on it at any given time. Time tracking for example may only have 1 person on it, but The Parser will definitely have at least 2 people working on it at all times. Every 3-5 weeks we will have a demo for our sponsors and allow them to use the system. This will feed into the next month’s work. The project will be tracked using Github’s integrated project management tool. 
Time it would take to complete tasks:
* Time tracking: (1-2 weeks, 1-2 people)
* Manage Login Credentials: (0.5 - 1 week, 1 person)
* Exposed API: (1 -2 weeks, 1-2 people)
* Sending automated emails: (2 - 4 weeks, 2 people)
* Accept or Reject changes: (2 - 3 weeks, 1-2 people)
* Allow comments/ suggestions: (2 - 4 weeks, 2-4 people)
* Audit Trail: (0.5 - 1 week, 1 person)
* The Parser: (7 - 12 weeks, 2-4 people)
* Concurrent Editing: (5 - 10 weeks, 2-4 people)
* Customize Translations Format: (3 - 5 weeks, 2-4 people)
* Track Translation changes: (2 - 3 weeks, 1-2 people)

# Deliverables high level releases and content
* Deliverable 1 - Working Parser
* Deliverable 2 - Scope items 12, 13 (Custom translation formats, default translation format)
* Deliverable 3 - Scope items 1, 8, 9, 10 (Time Tracking, Accepting changes, Commenting, Audit Trail)
* Deliverable 4 - Scope items 3, 5, 6 and possibly Concurrent Editing (This is a stretch deliverable and will be expanded on once deliverable 3 is completed)

# Measurements & Metrics
* Time tracking sheet (Estimated time per task vs. Actual time per task)
  * Important to see how well we estimated
  * Also helps when scheduling and planning Spiral cycles
  * A large difference between estimated time and actual time per task can indicate bad estimation techniques or slippage.
* Function Points
  * Good indicator of how large and complex a module is
  * Team prefers it of KLOC because a high KLOC doesn’t correlate with high complexity
* Defects per module (parser, concurrent editing, etc.) and how long it takes to fix them
  * Important to see what modules have the most errors and how fast we are fixing them
  * Lots of defects can indicate that the module is complex and might need to be reworked or revised by multiple team members
  
# Technical Process
* Our team has elected to use the Spiral Methodology
* Tools & Techniques
  * Each deliverable will come at the end of a loop through our development process. Each loop will follow the pattern of:
    * Determining our next objectives based on Sponsor input
    * Assessing the risks involved in accomplishing those objectives and producing a risk management plan for the current loop
    * Developing and testing a functional prototype that encapsulates the sponsor’s feedback
    * Delivering the prototype, receiving feedback, and planning the next loop.
* Methodology Artifacts
  * Spiral - Risk Management Plan. These will be produced prior to the development phase of each loop, focusing on the risks inherent to the specific objectives we plan to accomplish.
  * UML Diagram. While an overall, domain model diagram has been constructed and will be referred to throughout the project, each loop in our spiral methodology will produce a UML Class Diagram of any subsystem that is developed and the domain model will be updated to capture the domain architecture that has been implemented.
  * Activity Tracker. We will track the work accomplished by all team members to ensure blockers are quickly addressed and work is fairly divided. This will mitigate some of the existing and inherent risks of software development.
  * Time Tracker. Similarly to the Activity Tracker, we will track time spent accomplishing assigned tasks to better estimate the duration of oncoming loops.
