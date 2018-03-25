# Design Brief 📫
###### Configuration of Design Sprints in Enso
___

### Introduction
During my internship at MOBGEN from September 2017 until the end of January of 2018 I have worked on several projects. One of them was an application that helps the facilitator of a design sprint run through their design sprint workshop. The application is a prototype that is used to test if the idea behind the app is useful to a facilitator. It is also used to discover how to further develop it and how to put the application into the market. After some research and a lot of testing by Yoav (who is the founding father of Enso) and also by me and the rest of the Enso team, it became clear that new features were necessary to make the application actually useful. In the current version, the prototype, it is not possible to create your own design sprint as a user. Managing your own design sprints by the user is the most important feature in the new release.

MOBGEN is an Amsterdam based app developer but also has two offices in Spain. One in A Coruna and another one in Malaga. The company is very internationally oriented, and I work together with people from all over the world. That is also the reason to write documents like this one in English. MOBGEN was acquired by Accenture in June 2016 and via Accenture it has a giant pool of very big clients. Examples are: Shell, KPN, ABN AMRO and AEGON. MOBGEN is still an independent company inside the Accenture brand, with it’s own clients and offices, and has around 200 employees.

### Problem
The prototype of the application, named Enso, is being used extensively in design sprints given at MOBGEN. The facilitators of MOBGEN say it is a great tool that allows them to focus more on the design sprint itself instead of on the planning and structuring of the workshop.[^1] The application takes care of that for them. MOBGEN sees that the application is adding value to the company, but also has a point of criticism: the application can only be used internally at MOBGEN. **The reason the application is currently only usable internally at MOBGEN because when someone want to add a sprint, he or she has to contact Yoav and ask him to add the agenda to the Halo Backend System.**

The most important features of Enso are the sprint agenda, the timer, the list of energisers and the shopping list. The sprint agenda is the planning for the design sprint the facilitator wants to host. The week is divided in days and the days have events.

![Screenshots of the Enso application]({{ book.img }}/enso.png)

MOBGEN and the facilitators at MOBGEN would like to see a feature where users of the application, facilitators, can build their own agendas without having to use a separate backend system. This means we have to make the facilitators able to configure their own sprints in the application.

### Context
#### Stakeholders
##### Facilitators
The target audience of the application are people that are facilitating or participating in a design sprint. The first group are the people that are facilitating these design sprint workshops, we call them facilitators. The facilitators are facilitating the workshop and want to create an agenda that reflects their needs and wants. They also want to adjust the agenda when needed, for example when one of the events can not take place because equipment is missing or broke down. Facilitators want to be in full control of the content in their design sprint agenda, and want to be able to change it whenever and wherever they are. (This information comes from the Enso user tests[^1])

##### Participants
On the other hand we have the people that are joining and participating in a design sprint, these people can be clients, but also colleagues of the facilitator. These users have a different role and want to do different things than the facilitator. We call this group participants. The participants want to see the agenda and read back what events were about. They also want to know when they have lunch and at what time the day ends. Both the facilitators and participants are users of the application. (This information comes from the Enso user tests[^1])

##### MOBGEN
Finally we have MOBGEN as a stakeholder in the project. MOBGEN is the company that finances the project, and allows me to work on it. In a conversation with the board of MOBGEN[^2], they made clear that they want their brand to come forward into the app and to be able to use the application as a marketing tool. With the application they want to emphasize their leading position in the area of design sprints.

#### Trends
Design sprint are a trend in the current creative businesses. The methodology was created by Google Ventures, and was used to improve Google Chrome, Gmail and Google Search. The design sprint methodology is now also used by other big companies like Facebook, Slack and Airbnb[^3]. The method is used by these big companies because: “Companies are getting better and quicker results with the design sprint methodology than with the design thinking process” as Jonathan Courtney states[^4]. It is important to state that design thinking and design sprints are two separate methodologies. The same goes for agile/scrum, design sprints are not part of agile/scrum, but can be really useful in that workflow. The design sprint is a short period of time, mostly 3 or 5 days, where a team together with the client creates a tested prototype.

There are a lot of trends in and around mobile app development. One of them is React Native, the technology that has been used to build the prototype application of Enso[^5]. React Native covers both the iOS and Android platforms, and the code that is written is pure JavaScript which can be used on the web as well. With React Native it is possible for one developer to build an iOS, Android and a web interface with just one language.

Another trend is Progressive Web Apps. This trend is quite new and is not workable yet on iOS, but Apple is working on an update of the iOS software to make this possible[^6]. Progressive Web Apps are expected to be a big thing because of the following reasons: It’s faster than a native application, it does not require an install procedure from the App or Play store and you have access to offline functionalities with service workers.[^7]

#### Opportunities
The area we aim to serve with the application currently only has one big active competitor. The competitor is another application that tries to help their users run through their design sprints, called Duco[^8]. MOBGEN thinks they can have an advantage over Duco if Enso gets the new configuration function, and can become way bigger than the competition with an additional reporting system that is also being build simultaneously with this project. Enso could become a much better tool than Duco in our opinion, and we think Enso has a lot of potential to grow into a big tool.

#### Threats
The biggest threat we face is that the design sprints lose popularity over time. The research company Gartner developed a diagram that can be used to determine if a method is at the top of it’s hype or not. They use the Gartner Hype Cycle Diagram for this, showed in the image below. Gartner believes that ‘Post-Scrum methodologies’ are already over their peak[^9]. ‘Post-Scrum’ includes all agile/scrum methodologies in their diagram.

&nbsp;
![Gartner Hype Cycle]({{ book.img }}/gartner-hype-cycle.png)

Design sprints are not necessary in an agile/scrum project, but can be really useful. Design sprints can also be used outside of a agile/scrum system, and were introduced way after agile/scrum was introduced. I don’t think agile/scrum will be going away anytime soon, as most of the big companies are working with it[^3]. Still, we have to be aware that design sprints can lose their value and the industry will move to another method where Enso cannot be used anymore.

___
### Design Challenge
##### _“How could the current Enso application give facilitators of design sprints the possibility to create their own design sprint agendas and give participants of those design sprints better information about the agenda during the design sprint?”_
___

### Research questions
##### Concept
1. What is a design sprint and how do you facilitate one?
  * What is the goal of a design sprint?
  * What is the normal procedure for a design sprint?
  * Which people take part of a design sprint?
2. Who is the target audience?
  * What are their needs and wants of the Enso application?
  * What do we have that the competitors don’t have?
3. What are the problems a facilitator has with the current Enso application?
  * Why do these problems exist, and in what way are they problems?
  * When do these problems occur and how often?
  * Is there a way these problems can be prevented?
4. What would a facilitator want to do with a design sprint tool?
  * Why does a facilitator wants to do this?
  * Is the application the best solution for the goals a facilitator has, or can a different solution give better results?
5. What does a participant want to know and get from the application during a design sprint?
  * What information is important for the participant of a design sprint?
  * Why does the participant want to know this information?

##### Design
1. What is the preferred way of creating content in a mobile application?
  * What are best practices around user input in a mobile application?
  * What information is needed to create a sprint and how do you visually request this from the user?
2. What are the best practices around agendas and events for mobile applications?
  * How do you display an agenda clearly in a mobile application?
  * How do you give the user the ability to edit an existing agenda?
3. How does the participant view differ from the facilitator view?
  * How do you give a participant access to a facilitators design sprint?
  * What are best practices around requesting access in a mobile application?

##### Technical
1. What are the restrictions of React Native?
  * How can you solve those restrictions?
  * What other alternatives are there instead of React Native?
  * What are advantages of React Native?
2. What are the best practices is designing a mobile application codebase?
  * What different ways are there to set up a project?
  * How do you deal with the differences between iOS and Android technically?
  * How do you deal with all the side effects that happen on mobile?
3. How can you write scalable, reusable and maintainable code in React Native?
  * What packages can you use to make the code more clean and efficient?
  * How can you work with a version control system, and why is it considered indispensable in a project?
  * How can you make sure the code you write will work as expected?

### Focus
I want to do what I love, which for me is building a technical solution for a problem. **The main focus for me in this project is how to deal with user specific data inside a React Native application, and how to give the user the best experience when editing content inside this application.**

The focus is mostly on the technical part of the project, but also on the UX part. I want to create the best flow for the user, but also high quality code where every decision is backed by research. I can be proud when at the end of the project I have made the target audience happy with a smooth experience and code that is reusable, scalable and maintainable by other developers.

### Product vision
The current app is already a great tool for facilitators based on the feedback we have gotten back from them at MOBGEN. I think this tool can not only be used at design sprints, but also with any other workshop one might want to give. This tool can become something really big, and fill in a gap in the current market. There is currently one similar app worth mentioning in this market, called Duco, but it doesn’t have the features the facilitators really need, as we already found out during some interviews.[^1]

In the future Enso could become the workshop tool everybody wants to use, we have the opportunity to add the features the facilitators really need and want.

### Possible impact of the product
Enso could become the market leader in workshop facilitator tools, because this market is relatively empty. There are not a lot of tools that help someone facilitate a workshop. You can find a lot of lists on the internet about how to facilitate a workshop, but none of them actually help the facilitator with custom solutions.

### Roadmap & Planning
##### Concept
| # | Research question | Activities | Deliverables |
| --- | --- | --- | --- |
| 1 | What is a design sprint and how do you facilitate one? | <ul><li>Interviews with some facilitators</li><li>Interviews with participants</li><li>Research on the web</li></ul> | <ul><li>Design brief</li><li>Roadmap</li><li>Expert interview notes</li></ul> |
| 2 | Who is the target audience? | <ul><li>Making personas based on the interviews done earlier</li><li>Making empathy maps based on the interviews done earlier</li></ul> | <ul><li>Personas target audience</li><li>Empathy maps target audience</li></ul> |
| 3 | What are the problems a facilitator has with the current Enso application? | <ul><li>Observation during a design sprint</li><li>Interview with the facilitator of the design sprint about what does not work in Enso</li></ul> | <ul><li>Observation notes</li><li>Interview notes</li><li>Customer Journey</li></ul> |
| 4 | What would a facilitator want to do with a design sprint tool? | <ul><li>Sketching possible solutions based on previous research</li><li>Testing those solutions with end-users</li></ul> | <ul><li>Requirements list facilitator</li><li>User stories facilitator</li></ul> |
| 5 | What does a participant want to know and get from the application during a design sprint? | <ul><li>Interviews with participants about what they want from Enso during a design sprint</li></ul> | <ul><li>Requirements list participant</li><li>User stories participant</li></ul> |

After answering these questions I will have a clear idea what the problem is and what the concept of the project is. The result of answering these questions will be mostly documents with text, but also personas, empathy maps and customer journey. At the end I will have the requirements lists and the user stories to work from and make the UX designs.

##### Design
| # | Research question | Activities | Deliverables |
| --- | --- | --- | --- |
| 6 | What is the preferred way of creating content in a mobile application? | <ul><li>Desk research to best practices around content creation in mobile applications</li><li>UX sketches that can be used to test the possible solutions</li></ul> | <ul><li>Best practices research document</li><li>UX sketches</li></ul> |
| 7 | What are the best practices around agendas and events for mobile applications? | <ul><li>Desk research to best practices around agendas and showing events in mobile applications</li><li>UX sketches that can be used to test the possible solutions</li></ul> | <ul><li>Addition to best practices research document</li><li>UX sketches</li></ul> |
| 8 | How does the participant view differ from the facilitator view? | <ul><li>UX sketches for a possible flow to invite participants to a facilitators sprint</li></ul> | <ul><li>User test notes and outcomes to iterate on</li></ul> |

By answering these questions I will have the UX sketches that I can use to start the prototype. The UX sketches will be tested with the target audience and their feedback will be used to improve the UX sketches. The end result of these questions will be a document where I describe the design choices that were made, and an invision prototype of all the UX screens.

##### Technical
| # | Research question | Activities | Deliverables |
| --- | --- | --- | --- |
| 9 | What are the restrictions of React Native? | <ul><li>Desk research to restrictions of a React Native project</li></ul> | <ul><li>Technical document that describes the restrictions of React Native that we have to deal with</li></ul> |
| 10 | What are the best practices is designing a mobile application codebase? | <ul><li>Desk research on React Native project setup</li></ul> | <ul><li>Code framework to develop on based on the first prototype of Enso</li></ul> |
| 11 | How can you write scalable, reusable and maintainable code in React Native? | <ul><li>Desk research around scalable, reusable and maintainable code</li><li>Interview with senior developer</li></ul> | <ul><li>Principles of scalable, reusable and maintainable in the codebase</li><li>A documentation for the written code</li></ul> |

The decisions made on the technical part will be done based on the research of the above questions. These questions will help me make the right decisions in the code base to create a product that can be picked up by another developer, but also can be used to add new features to the application.

### Planning
![Project planning]({{ book.img }}/planning.png)

##### Planning description
I made a planning for the weeks that are still to come. In every week you can see which research question I will tackle, what activities I will take place to do so, and what documents or files will be delivered.

The planning starts with the concept phase. It will take me only two weeks, which seems a bit short at first sight, but I have done quite some research in week 1 till 6, so I can reuse most of that to do the concept phase.

After the concept phase I will start with the design phase. In this phase I will translate the concept to a design that can solve the found problems. I will do some iterations on the designs based on user tests with real end-users.

When the designs are finished I will start with the development of the feature. The end product will be a React Native prototype that allows a participant to create their own sprints in the application. All design or technical decisions will be backed by research that is done during the project.

The full planning is available via this [link](https://docs.google.com/spreadsheets/d/1fe8AlPRZcAEi3cYq_WSzRiAzKV5D9_j00ZQsqEQb1PU/edit?usp=sharing).

### References
[^1]: Ouddeken, J. (2017, November 20th). Enso User Test Notes. Consulted on 15-02-2018 from: https://docs.google.com/document/d/1AVcM-3lrpWvb_lH7vqqXENN8cACiGlwWyVQ5GcncXpo/edit?usp=sharing
[^2]: Conversation was held in January 2018 with the Chief Executive Officer and the Chief Creative Officer of MOBGEN.
[^3]: de Vreede, E. (18-10-2016). Design Sprint: van vraagstuk naar concreet product in 5 dagen. Consulted on 12-03-2018 from: https://www.frankwatching.com/archive/2016/10/18/design-sprint-van-vraagstuk-naar-concreet-product-in-5-dagen/
[^4]: AJ&Smart. (06-03-2018). The design sprint a trend? Consulted on 15-03-2018 from: https://www.youtube.com/watch?v=0RhwwYaipZ8
[^5]: Wodehouse, C. (24-11-2017). 7 reasons why React Native is the future of Hybrid Mobile Apps. Consulted on 15-02-2018 from: https://www.upwork.com/hiring/mobile/react-native-hybrid-app-development/
[^6]: Apple. (06-02-108). What’s new in Safari. Consulted on 15-02-2018 from: https://developer.apple.com/library/content/releasenotes/General/WhatsNewInSafari/Articles/Safari_11_1.html
[^7]: Shilova, M. (14-09-2017). Progressive web apps: key benefits, statistics, use cases. Consulted on 15-02-2018 from: https://apiumhub.com/tech-blog-barcelona/progressive-web-apps/
[^8]: Duco. (Date unknown). Duco App. Consulted on 15-02-2018 from: http://duco.newhaircut.com/
[^9]: West, M. Wilson, N. James Mann, K. Hype Cycle for Application Development. Consulted on 17-02-2018 from: https://www.gartner.com/document/3779164
