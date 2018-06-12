# Codebase Best Practices
###### Technical research question
---

### 2.1 What different ways are there to set up a project?
There are almost unlimited ways to setup a project in development, but some are more convenient than others. I did research to project structures in the [project structure](../../technical/project-structure.md) section of the technical phase. I describe the smart and dumb components setup with the help of an article of Dan Abramov, who is one of the creators of React and Redux.

This way of setting up a project is used in many of the beginner tuturials, but also in some of the biggest projects MOBGEN did. The Shell Oasis project I worked on also used this setup, and the KPN project MOBGEN is using it. Dennis Korff, senior frontend developer at MOBGEN also told me this is currently the preferred way of setting up React project in a conversation we had about this topic [^2].

In the end there are certainly many ways to set up a project, but the setup I used is the most common. The use of containers and components is also explained in the official React tutorial by Facebook [^1]

Putting this in practice, my project was setup following two guidelines, the smart and dumb components one, and a Redux structure aimed at medium to large scale projects. The setup is explained in detail on the [project structure](../../technical/project-structure.md) page.

### 2.2 How do you deal with all the side effects that happen on mobile?
On a mobile phone a lot of side effects happen. Side effects are actions that interrupt a process. For example fetching data from a server when suddenly the user quits the application.

### References
- https://medium.com/skyshidigital/5-best-practices-for-react-native-development-you-probably-doesnt-know-474df87d74e6
- https://medium.com/dailyjs/11-mistakes-ive-made-during-react-native-redux-app-development-8544e2be9a9
- https://americanexpress.io/clean-code-dirty-code/
[^1]: Facebook. (Date unknown). React tutorial. Consulted on 08-06-2018 from: https://reactjs.org/tutorial/tutorial.html
[^2]: Korff, D. (02-06-2018). Interview with a senior developer at MOBGEN about best practices.
