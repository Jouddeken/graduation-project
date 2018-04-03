## [React Native](https://facebook.github.io/react-native/)
##### What is it?
React Native is the native version of the [React.js](https://reactjs.org) language used for the web. It allows a developer to create an iOS and Android application with a single codebase. The React Native code compiles to Objective-C and Java, which can be run on iOS and Android respectively. By that way you create native apps with Javascript code. The framework was developed by Facebook, who also made the [React.js](https://reactjs.org) library for the web. React Native is being used by Facebook itself, Airbnb, Skype, Tesla and Wallmart.

##### Alternatives
There are some alternatives for React Native:
- [Ionic](https://ionicframework.com/)
- [PhoneGap/Cordova](https://cordova.apache.org/)
- [Xamarin](https://www.xamarin.com/)
- [Progressive Web Apps](https://developers.google.com/web/progressive-web-apps/)
- [Flutter](https://flutter.io/)
- Native iOS and native Android

##### Why React Native?
The top two options, Ionic and PhoneGap/Cordova, simply wrap a web-view in a native component. This results in a webpage in an app. The applications are slow and cannot make use of some of the native functionalities like push notifications. Xamarin does give the user the experience of a native app, but it is written in C#. It compiles the C# code to an iOS and an Android application, which would mean for me to learn a whole new language.

Progressive Web Apps are also a good option, you can still write javascript code and run it on an Android or iOS device. The application runs in the browser on the users device. At the beginning of the Enso project PWA's were not fully supported on iOS, and MOBGEN preferred a native app that you can download from the AppStore and PlayStore.

The next big think in cross-platform area is possibly Flutter, the React Native of Google. The framework is written in the Dart language, which also means that I had to learn a new language to work on the project. It also was not officially released as a beta when the Enso project was started, so it was not advised to use in real world projects.

The main reason I decided to use React Native was of the fact that one developer was able to create both the iOS and the Android app from one codebase. The Enso project is on a tight budget (no budget), it can only make use of intern developers, and most of the time there is only one intern assigned to the project. That is also the reason I did not go for a native iOS and Android application. Another reason is that I was assigned to the Enso project and did not know how to make native iOS and Android apps.

Another reason was that MOBGEN is working a lot with React, and in the case of a web version of the application, a lot of the code from the React Native project could be used in a React for web project. It is also easy for another developer to continue the work on the project as React Native does not differ much from React.

Lastly, React Native has a very big community behind it. There are a lot of packages from the React community that can also be used in React Native, but there are also a lot of packages made specifically for React Native by the community.

---

##### References
- Facebook. (Date unknown). React Native. Consulted on 23-03-2018 from: https://facebook.github.io/react-native/
- Kukic, Ado. (10-01-2017). Alternatives to Native Mobile App Development. Consulted on 23-03-2018 from: https://auth0.com/blog/alternatives-to-native-mobile-app-development/
- Google. (Date unknown). Flutter. Consulted on 223-03-2018 from: https://flutter.io/
- Research done during internship from 01-11-2017 till 19-02-2018
