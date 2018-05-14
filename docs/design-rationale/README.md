# Design rational
###### Enso
___

### Introduction
This document is an explicit documentation of the reasons behind decisions made during my graduation project. I highlighted the most important decisions during the project and explain the arguments that led to the decision.

### Design Challenge
The (design) challenge I am solving in this project is the following:

##### _“How could the current Enso application give facilitators of design sprints the possibility to configure their own design sprint agendas in the app?”_

The goal of the project is to give the users of the Enso app, facilitators of design sprints, the option to configure their own design sprints in the current Enso application. The users of the app should also be able to edit the configured sprints and delete them if they don't want to use them anymore.

### Background
Enso is an application that helps facilitators of workshops or design sprints to run their workshops. It does that by giving its users a workshop agenda with events, and more tools like energisers to increase the energy level of people participating in a workshop.

The Enso application did not have the option to configure your own design sprints or workshops. The design sprints that are now shown in the application are the ones that were filled into the backend system Enso is working with. These workshops were filled in by hand by one of the team members of the Enso team. This solution worked to test the prototype Enso application, but now that the tests with the prototype were successful we need this functionality to be in the application.

The new feature I am designing and prototyping will speed up the time needed for users of the Enso app to get their workshops in the application. Instead of having to ask someone from the Enso team to add their workshop to the backend system, they can just configure and edit a workshop themselves in the app.

### Problem
The problem I was asked to solve by **MOBGEN | Accenture Interactive** was to design and prototype a new feature for the Enso application that allows its users to configure and edit design sprints and workshops in the application, on both iOS and Android while using a single code base.

### Gems
During the project I made a lot of decisions. I highlight the 7 most important or interesting ones here. These 'gems' in my project were:

1. Concept phase
2. Requirements list
3. Epics & user stories
4. Create sprint flow
5. Edit sprint day flow
6. UX prototype tests
7. Development setup

#### Concept phase
**What was done?**<br />
At the beginning of the project I took a lot of time to define the concept of the project, and to find out what the actual problem was with the Enso application. **MOBGEN | Accenture Interactive** asked me to find a way to enable the users of the Enso application to configure their own sprints in the application. I took a step back to find out how to Enso app was being used already. The app was released internally at **MOBGEN | Accenture Interactive** to test if it was useful or not to use an app in a design sprint, so I could experience how facilitators were actually using the application.

I did an [observation](../concept/research/fly-on-the-wall.md) during a design sprint, and did [interviews](../concept/research/expert-interviews.md) with designers to find out what they thought of the Enso application, and how they were using the application in a workshop. I found out how what the painpoints of the application were, and in what way the facilitators wanted to use the Enso app.

![Fly on the wall photo 5]({{ book.img }}/fotw-5.jpg)
<span style="display: block; font-size: 85%; margin-bottom: 8px; margin-top: -8px;">Enso Fly on the Wall observation</span>

**Which decisions were made?**<br />
I found out that the facilitators liked the idea of using an app for their workshops, where they had an agenda for every day of the workshop. However, I found out that facilitators change their workshop agenda's a lot. Sometimes they change the agenda only a couple minutes before the start of the day, or even during the day. This meant that editing a workshop was more important than creating a workshop, and editing has to be really easy and intuitive.

The concept phase took a couple of weeks, which is quite long, but gave me great insights in what was actually needed for the Enso application. Along with the observations and interviews I did, I also did a competitor analysis, made persona's, empathy maps and a customer journey to find out what the pain points were.

Based on all the research I made the decision that **MOBGEN | Accenture Interactive** was indeed right with what they asked me to do, but they did not think about the editing part of it. Configuring sprints was an important feature that had to be in the app, but editing was at least as important.

___

#### Requirements list
**What was done?**<br />
For the new release of the Enso application **MOBGEN | Accenture Interactive** did not only want the new feature, but also a redesign of the application and some extra features in the application. To give a clear view of what was needed and what priority every feature had, I made a [requirements list](../design/requirements-list/README.md). I applied the [MOSCOW](https://en.wikipedia.org/wiki/MoSCoW_method) method, invented by Dai Clegg, to all the features to create a good overview of what was really important, and what was less important. The requirements were based on all the research I did during the concept phase, and some.

| # | Feature (Epic) | # | Task (User story title) | Priority |
| :-: | :-- | :-: | :-- | :-:
| 1 | Create sprint | 1.1 | Set sprint name | Must |
|   |   | 1.2 | Set sprint challenge | Must |
|   |   | 1.3 | Set sprint start date | Should |
|   |   | 1.4 | Set number of people | Should |
|   |   | 1.5 | Select a sprint team | Won't |
|   |   | 1.6 | Select a sprint template | Must |
|   |   | 1.7 | Select a blank sprint template | Won't |
|   |   | 1.8 | Select number of sprint days in blank template | Won't |
|   |   | 1.9 | Store sprints on the Halo CMS | Won't |
| &mdash; |   |   |   |   |
| 2 | Edit sprint | 2.1 | Edit sprint name | Should |
|   |   | 2.2 | Edit sprint challenge | Should |
|   |   | 2.3 | Edit sprint date | Should |
|   |   | 2.4 | Edit sprint people | Could |
|   |   | 2.5 | Delete created sprint | Should |
| &mdash; |   |   |   |   |
| 3 | Edit agenda | 3.1 | Add events from a predefined list | Must |
|   |   | 3.2 | Remove events from sprint agenda | Must |
|   |   | 3.3 | Edit the events order | Must |
|   |   | 3.4 | Edit the agenda day start time | Should |
| &mdash; |   |   |   |   |
| 4 | Edit event | 4.1 | Edit event title | Won't |
|   |   | 4.2 | Edit event duration | Must |
|   |   | 4.3 | Edit event description | Won't |
|   |   | 4.4 | Edit event tips | Should |
|   |   | 4.5 | Edit event equipment | Should |
|   |   | 4.6 | Edit event visual | Should |
<span style="display: block; font-size: 85%; margin-bottom: 8px; margin-top: -8px;">Enso Epics that were selected for the project</span>

**Which decisions were made?**<br />
Based on the requirements list I made with the features that come from the concept phase, I realized that there were a lot of features that could not be done in the time I had. Initially I thought I had to make a login/sign-up feature to save all user configured sprints in a structured way, and make teams so that participants could join a facilitators team to get a view-only version of the design sprint on their phone. With the requirements list I realized that this was impossible in the time I had. There were also a lot of other requirements that I was not going to do. The Enso team found two other developers who were willing to help with the development of the application. They were assigned to the features I was not going to do.

In the end I selected 4 features (epics) that I was going to make a prototype for. These epics all had to do with creating or editing a workshop, and were doable in the time I had for this project. The requirements list is a very thought out list of everything that should be in the application, that was made with the help of the facilitators at **MOBGEN | Accenture Interactive** and the Business Analyst (Yoav Farbey), who also came up with the idea for the Enso app. The features I ended up with were:

1. create-sprint
2. edit-sprint
3. edit-agenda
4. edit-event

___

#### Epics & user stories
**What was done?**<br />
After defining the scope of the project with the requirements list, I started to write down all the design and functional requirements of each feature in [epics and user stories](../design/epics/README.md). I splitted the features (epics) into smaller features (user stories) that were needed to create the feature. I wrote down a description for every epic, stated what the problem was, listed higher level proposals, and explained the value to users and to **MOBGEN | Accenture Interactive**. Every user story is answering the following question: 'As a [...], I want [...], so that [...]. I placed all these epics and user stories in a Kanban Jira board so that I, but also other people working on the Enso project, had a clear overview of where I was working on.

![Enso Jira Kanban board]({{ book.img }}/enso-jira-kanban-board.png)
<span style="display: block; font-size: 85%; margin-bottom: 8px; margin-top: -8px;">Enso Jira Kanban Board</span>
![Enso Jira Epic 1]({{ book.img }}/enso-jira-epic-1.png)
<span style="display: block; font-size: 85%; margin-bottom: 8px; margin-top: -8px;">Enso Jira Epic part 1</span>
![Enso Jira Epic 2]({{ book.img }}/enso-jira-epic-2.png)
<span style="display: block; font-size: 85%; margin-bottom: 8px; margin-top: -8px;">Enso Jira Epic part 2</span>
![Enso Jira US 1]({{ book.img }}/enso-jira-us-1.png)
<span style="display: block; font-size: 85%; margin-bottom: 8px; margin-top: -8px;">Enso Jira User Story</span>

As showed in the screenshots every Epic has its own User Stories assigned to it. The User Stories are small parts of the Epic that all have to be done to complete the Epic.

**Which decisions were made?**<br />
By describing and thinking through every feature of the application very well I had a good idea of what I had to prototype and how long it would take to develop each feature. I could now create the UX prototype based on the information that was described in the Epics and User Stories. I could use them as a checklist to see if all my designs could do what they actually needed to be able to do. I think the Epics and User Stories for the Enso app are real gems in my project because they are so detailed and high quality. They follow the **MOBGEN | Accenture Interactive** Epic and User Story template that helps to write down User Stories as clear as possible.

___

#### Create sprint flow
**What was done?**<br />
I had to come up with a way to enable the users of the Enso app to configure their own design sprints or workshops in the application. They have to be able to do this as quickly as possible, which meant being selective with the data you request from the users. I wanted as less steps as possible but still getting all the data I needed to create a sprint. I made three versions of how to do this, one where all the inputs are on one screen, one where the application tried to fill in the required fields for you, and one wizard like option where the user gets one input on every screen.

**Which decisions were made?**<br />
The facilitators and UX experts at **MOBGEN | Accenture interactive** preferred the wizard like option, because it is way clearer for the user where he or she has to focus on. It also gives the user a good indication of how much more steps there are in the process because you can give the user a 'step 1 of 5' indicator at the top of the screen. You could not do this with the other options, because you could not really know where the user is in the process.

___

#### Edit sprint day flow
**What was done?**<br />
This screen was challenging in the way that it had a lot of functionality, but that functionality should not be in the way during the actual workshop. On this screen you could add events, remove events, reorder events and mark events as done. I struggled for long to find a good UX pattern I could base this screen on, but found the iOS clock application to be a good example. The clock application had an edit button at the top right part of the screen that activated the 'edit mode' in the application. In that mode the user could click on the red stop sign that had appeared on the left to remove the item, and drag the item around using the handles that had appeared on the right. In the clock application the user could also swipe on items from right to left to remove an item.

**Which decisions were made?**<br />
 I used the same flow on the agenda screen for removing and dragging around, where I used a swipe from left to right to mark an event as done. The edit button in my case also activated an 'add event' button with which the user could add new events to the agenda. This way I had all my four features that had to be on this screen in quick reach for the user. Removing an event and marking it as done were possible without activating the 'edit mode' and reordering and adding an event were possible in the 'edit mode'. In the edit mode it also was hard to accidentally remove an event, because it required two clicks. This is to prevent a misclick from the user that accidentally removes the event.

___

#### UX Prototype tests
**What was done?**<br />
I tested the UX prototype I made that was based on the best practices, on a couple of people and facilitators. Before I tested the Invision prototype I wrote a test plan. The goal of the test plan was to have a good preparation for the test itself, and to make sure I knew what I was going to ask. Part of the testplan was an introduction they advice you to do when conducting user tests, making sure the participant is relaxed and knows what is going to happen. I also told the participants that it was the product I was testing, and not their ability to work with the product. I gave the participants a couple of tasks to complete, but tried to not give any hints away.

**Which decisions were made?**<br />
I made a lot of good assumptions and the participants were enthusiastic about the prototype. They had some feedback points on the prototype however. They wanted the timer button in an event to display the amount of time the event was going to take, and that timer button should be visible in all the screens, since they considered it the most important feature of the application. They also did not seem to understand the home screen if the user already had an active design sprint. The term 'upcoming exercise' was vague for 4 of the 6 participants.

Overall the prototype performed pretty well, and was mostly clear to the participants. I only had to adjust a couple of small details based on the feedback they gave me.

___

#### Development setup
**What was done?**<br />
For the Enso application I constructed a codebase that is maintainable, understandable and extendable. I did this almost from scratch, using the [create-react-native-app](https://github.com/react-community/create-react-native-app) package from Facebook, that gives you the most simple setup for a React Native project. I added a lot of other packages on top of the project, like redux, redux-saga, reselect, recompose and many other packages to enable a certain way of working I applied to the Enso project.

Besides maintainable, understandable and extendable code, the code also had to be clean, clever and modular. I used ESLint and configured it so it would show errors in the code editor if the code was not written correctly.

**Which decisions were made?**<br />
To keep the code maintainable, understandable and extendable I chose to work with the Redux way of working, and used the smart and dumb component philosophy of React. The Redux way of working took care of the maintainability because you split up a lot of functionality in the application. Splitting functionality up in smaller pieces means it is easier to create new pieces to work along with the other pieces. Using this method also allows other developers to develop features that work separately from my features.

The Smart and Dumb component philosophy is a way to separate functionality from layout. Smart components worry about how things **work**, where dumb components worry about how things **look**. Smart components take care of fetching data from a server, transforming that data and sending it to the dumb components that live inside the smart components. Dumb components receive and display that data. They do not have functionality and they certainly do not fetch data from servers or modify data.

To keep the code the same, even with multiple developers working on the project, I installed the ESLint plugin. This plugin checks the way the code is written in the code editor of the developer. It gives the developers live warnings when syntactical or semantical errors are being made. I based the ESLint rules (the errors it checks against) on the Airbnb ESLint configuration.

In the project I worked with Git, and the Gitflow workflow. This means that every feature you make lives on a separate feature branch. When the feature is done you make a pull-request in Bitbucket and assign reviewers to the pull-request. This way nobody is ever making commits directly on the development branch, and the only code on the development branch is code that is thought to be done and working. This means the quality assurance team could test the development branch at any time.

![Enso Bitbucket Pull Request]({{ book.img }}/enso-bitbucket-pull-request.png)
<span style="display: block; font-size: 85%; margin-bottom: 8px; margin-top: -8px;">Enso Bitbucket pull-request</span>

In the above screenshot you see the pull-request for a progress bar I made. I assigned three reviewers to the pull-request, from which two reviewed and approved my code. The pull-request is then merged into development, and the feature is done.

### Conclusion
[Soon more...]
