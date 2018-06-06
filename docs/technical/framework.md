## Framework
###### What framework was used in the application and why
---

To explain which framework was used in this application and the reasons behind it, you first have to understand the explanation of a framework. Neha Choudhary gave a great explanation on a [StackOverflow page](https://stackoverflow.com/a/12733126/8301587) that describes a framework very well:

> If I told you to cut a piece of paper with dimensions 5m by 5m, then surely you would do that. But suppose I ask you to cut 1000 pieces of paper of the same dimensions. In this case, you won't do the measuring 1000 times; obviously, you would make a frame of 5m by 5m, and then with the help of it you would be able to cut 1000 pieces of paper in less time. So, what you did was make a framework which would do a specific type of task. Instead of performing the same type of task again and again for the same type of applications, you create a framework having all those facilities together in one nice packet, hence providing the abstraction for your application and more importantly many applications.
>
> <cite style="float: right">-- Nahe Choudhary</cite>
> <br />

In summary, a framework is a tool that you can use to create or do something. This works very well for developing applications, where developers often do the same tasks multiple times and maybe a minor detail changes. A framework can help developers create new projects quicker. It is good to note that you don't necessarily need to use a framework for a lot of projects, but for bigger projects it can be very nice to have a set of pre-made functions and a structure you can already use.

The framework used in the Enso application is **React Native**.

##### What is it?
React Native is the native version of the [React.js](https://reactjs.org) library used for the web. Native means that this library is for Android and iOS devices. It allows a developer to create a cross-platform application with a single codebase. The React Native code compiles to Objective-C and Java, which can be run on iOS and Android respectively. By that way you create native apps with Javascript code. The framework was developed by Facebook, who also made the [React.js](https://reactjs.org) library for the web. React Native is being used by Facebook itself but also by Airbnb, Skype, Tesla and Wallmart. [^1]

##### Alternatives [^2]
There are some alternatives for React Native:
- [Ionic](https://ionicframework.com/)
- [PhoneGap/Cordova](https://cordova.apache.org/)
- [Xamarin](https://www.xamarin.com/)
- [Progressive Web Apps](https://developers.google.com/web/progressive-web-apps/)
- [Flutter](https://flutter.io/)
- Native iOS and native Android

##### Why React Native?
The top two options, Ionic and PhoneGap/Cordova, simply wrap a web-view in a native component. This results in a webpage in an app. The applications are slow and cannot make use of some of the native functionalities like Touch ID. Xamarin does give the user the experience of a native app, but it is written in C#. It compiles the C# code to an iOS and an Android application, which would mean for me to learn a whole new language.

Progressive Web Apps are also a good option, you can still write javascript code and run it on an Android or iOS device. The application runs in the browser on the users device. At the beginning of the Enso project PWA's were not fully supported on iOS, and MOBGEN preferred a native app that you can download from the AppStore and PlayStore.

The next big think in cross-platform area is possibly Flutter, the React Native of Google. The framework is written in the Dart language, which also means that I had to learn a new language to work on the project. It also was not officially released as a beta when the Enso project was started, so it was not advised to use in real world projects. [^3]

The main reason I decided to use React Native was of the fact that one developer was able to create both the iOS and the Android app from one codebase. The Enso project is on a tight budget (no budget), it can only make use of intern developers, and most of the time there is only one intern assigned to the project. That is also the reason I did not go for a native iOS and Android application. Another reason is that I was assigned to the Enso project and did not know how to make native iOS and Android apps.

Another reason was that MOBGEN is working a lot with React, and in the case of a web version of the application, a lot of the code from the React Native project could be used in a React for web project. It is also easy for another developer to continue the work on the project as React Native does not differ much from React.

Lastly, React Native has a very big community behind it. There are a lot of packages from the React community that can also be used in React Native, but there are also a lot of packages made specifically for React Native by the community.

The other options are not necessarily bad options, but React Native was for this project and for MOBGEN the best solution as it had most of the things that were needed. A downside of React Native is that it is not as performant as a native app, and that some functionalities where you want to make use of native components such as Touch ID are hard to do and sometimes impossible, although more and more packages that support these kind of features are being released every day. [^4]

##### Pro's of React Native [^5] [^6]
- Written in a known language (Javascript)
- Big community with a lot of packages
- Well known (React) by the MOBGEN developers, so easily
- Faster/cheaper development with a smaller team

##### Con's of React Native [^5] [^6]
- Native developer still needed for usage of native functionalities
- It's difficult to make the navigation work correctly and easily on both platforms
- Facebook rules, massively relying on one company
- Just not as fast/smooth as real native apps

---

##### References
[^1]: Facebook. (Date unknown). React Native. Consulted on 23-03-2018 from: https://facebook.github.io/react-native/
[^2]: Kukic, Ado. (10-01-2017). Alternatives to Native Mobile App Development. Consulted on 23-03-2018 from: https://auth0.com/blog/alternatives-to-native-mobile-app-development/
[^3]: Google. (Date unknown). Flutter. Consulted on 23-03-2018 from: https://flutter.io/
[^4]: Research done during internship from 01-11-2017 till 19-02-2018
[^5]: Chrzanowska, Natalia. (22-10-2017). React Native - Pros and Cons Of Facebook’s Framework. Consulted on 06-06-2018 from: https://www.netguru.co/blog/react-native-pros-and-cons
[^6]: Kiewning, Dennis. (04-01-2018). React Native - The Good, the Bad and the Ugly. Consulted on 06-06-2018 from: https://medium.com/widgetlabs/react-native-and-the-good-the-bad-and-the-ugly-f10b5baf703e
