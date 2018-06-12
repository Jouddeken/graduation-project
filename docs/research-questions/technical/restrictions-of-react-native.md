# Restrictions of React Native
###### Technical research question
---

React Native is a library that enables a developer to write a cross-platform application using a single codebase. React Native comes from the React package that was made for the web. React Native runs the javascript code the developers write and runs this on the users device. In contrast to PhoneGap or Cordova it is not a webview layer in a native wrapper, but actual javascript code that runs on the phone.

This means with React Native you can use some of the native functionalities that a phone offers. Examples of these native functionalities are: a fingerprint scanner, notifications, vibrations, location or the phones local storage. With this also comes the first restriction. At the time of writing this, most of the native modules are supported in React Native. But when it was just released you could not use some of those native modules the phone has. Facebook (the creator of React and React Native) had to add this to the React Native project first, or some developer had to make this feature and make a pull request in the React Native repository on GitHub to get it into the project.

This takes time, so when a new native module is introduced, React Native apps cannot immediately use it, or you would still need native Java (Android) and Swift (iOS) developers to make use of this new native module.

Another issue I had with React Native was navigation. React Native only supports iOS navigation out of the box, and suggest to use the react-navigation package when developing an application. This react-navigation package is wildly complicated at first sight, when you never did any mobile development, and only did web development. You will drown in Stack, Tab and Drawer Navigators, and soon you have no idea how to setup you navigator.

It is more complex than navigating on the web. I tried to use other navigation packages, such as react-native-navigation (made by Wix, the website-builder-website), and react-router (react-router is the router you use in React for web). Performance and navigational speaking react-navigation was the best package. In React Native: navigating is hard.

Lastly there are some performance issues when doing heavy hardware actions in a React Native application. Take Pinterest for example, they looked into React Native and asked themselves if they could write their application with it. The short answer was: 'no'. Their native applications were optimized to handle the unlimited scrolling feature they have. It was not possible to match the same performance with React Native. [^1] [^2] [^3]

### 1.1 How can you solve those restrictions?
The lack of support of native modules is already getting less and less. A lot of the native modules are already supported or can be supported using community made packages. If the native module you need is not yet supported by React Native itself, and there was no developer from the community that decided to make a package that enables support of this native module, you end up needing iOS and Android developers to help you out. They would have to write an implementation for the native module and forward those functions to React Native.

Navigation is still a problem. It is not really a restriction as it will work, but customizing the navigation is very limited. During the project I had a lot of problems figuring out how to set up the navigator and to control the way containers would enter the screen. Maybe for a native developer this would be easier, but for someone coming from the web development area, it did not always make sense.

Lastly the performance is also still a problem, and I don't see this being fixed in the near future. The main issue with this is that the code that is executed is not native code. It is Javascript that is running in the JavascriptCore engine (the engine that runs in Safari as well). Native code will always be faster and perform better than non-native code. However, for building user interfaces in a way where you can reuse them on the web as well React Native is a very good solution.

### 1.2 What other alternatives are there instead of React Native?
There are multiple alternatives to React Native or alternatives to develop iOS and Android applications.

| Alternative | Description |
| :-- | :-- |
| [Ionic](https://ionicframework.com/) | Ionic is very similar to React Native. You could say Ionic the the Angular Native of Angular. |
| [PhoneGap/Cordova](https://cordova.apache.org/) | Phonegap/Cordova is wrapping a webview in a native container. You can make an application out of an existing website very easily. |
| [Xamarin](https://www.xamarin.com/) | Xamarin is a way of creating cross-platform applications which makes use of the C# language to create the code |
| [Progressive&nbsp;Web&nbsp;Apps](https://developers.google.com/web/progressive-web-apps/) | A fairly new option in the list of competitors. With progressive web apps a user can 'download' a website to their phone, and this website has access to some native modules like notifications. |
| [Flutter](https://flutter.io/) | Flutter is the React Native competitor from Google. It uses the Dart language. With Flutter the user can  |
| Native&nbsp;iOS&nbsp;and&nbsp;native&nbsp;Android | These are well known options most applications are build in. |

### 1.3 What are advantages of React Native?
The advantages of React Native are the fact that you can quickly develop an iOS and Android application with a single codebase. However, most of the competitors can do this as well, so this is only an advantage over native development. For native development you will still need to create two codebases, one for each platform.

The community behind React and React Native is massive. It has a solid number 4 in the most used frameworks in the 2017 Stackoverflow survey [^4], and is the most loved framework [^5] according to the over 64.000 developers who filled in the survey [^6]. React Native itself has close to 65.000 stars on GitHub and has 1.676 contributors working on it [^7].

Besides the above React Native has some advantages for developers that come from web development, especially those who have worked with React for web. React Native is written in the Javascript language, which is well known by almost all web developers and is the most popular programming language [^8]. This makes it easy for them to switch to native development because they don't have to learn a new language.

React is already well known by the MOBGEN developers, so for me this was an advantage React Native had as well. If I had questions I could easily ask them to other developers working at MOBGEN.

For the Enso team it was an advantage that with React Native we could have only one developer working on both the iOS and Android application. This was an advantage because there is no budget for this project, and only interns or unassigned employees can work on this project.

### References
[^1]: Shah, H. (23-11-2017). React native limitations that every developer should know about. Consulted on 08-06-2018 from: https://www.simform.com/react-native-limitations-app-development/
[^2]: Girish, R. (30-10-2017). What are the current limitations and features of React Native?. Consulted on 08-06-2018 from: https://www.quora.com/What-are-the-current-limitations-and-features-of-React-Native/
[^3]: Senkovska, Z. (27-07-2017). React Native Limitations and Best Practices to Deal With Them. Consulted on 08-06-2018 from: https://apiko.com/blog/react-native-limitations-and-best-practices-to-deal-with-them/
[^4]: Stack OverFlow. (Januari 2018). Stack Overflow Developer Survey Results. Consulted on 06-08-2018 from: Stackohttps://insights.stackoverflow.com/survey/2017#technology-frameworks-libraries-and-other-technologies
[^5]: Stack OverFlow. (Januari 2018). Stack Overflow Developer Survey Results. Consulted on 06-08-2018 from: Stackohttps://insights.stackoverflow.com/survey/2017#technology-most-loved-dreaded-and-wanted-frameworks-libraries-and-other-technologies
[^6]: Stack OverFlow. (Januari 2018). Stack Overflow Developer Survey Results. Consulted on 06-08-2018 from: Stackohttps://insights.stackoverflow.com/survey/2017
[^7]: Facebook. (Date unknown). React Native GitHub. Consulted on 06-08-2018 from: https://github.com/facebook/react-native/
[^8]: Stack OverFlow. (Januari 2018). Stack Overflow Developer Survey Results. Consulted on 06-08-2018 from: Stackohttps://insights.stackoverflow.com/survey/2017#technology-programming-languages