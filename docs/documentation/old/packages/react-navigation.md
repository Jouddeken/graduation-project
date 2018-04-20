## [React Navigation](https://github.com/react-navigation/react-navigation)
##### What is it?
React Navigation is a package developed by the react-community. It helps you to set up navigation in React Native apps, which can be a really hard thing to do in React Native. This package helps you to match you navigation for iOS and Android. You write the same code for both platforms and the package takes care of the difference between the two platforms, for example the animations between routes.

##### Alternatives
- [React Router](https://github.com/ReactTraining/react-router/tree/master/packages/react-router-native)
- [React Native Navigation](https://github.com/wix/react-native-navigation)
- [Native Navigation](https://github.com/airbnb/native-navigation/)
- [React Native's solutions](https://facebook.github.io/react-native/docs/navigation.html#navigatorios)

##### Why React Navigation?
Navigation is a difficult part of the React Native ecosystem. There is no best go-to solution. All packages have some downsides and setting up a good navigator is difficult and time consuming.

Before going for the React Navigation package I tried out the Wix router package (React Native Navigation), but found out that it was not possible to customize the tab bar in the bottom of the screen. I also tried the React Router package because that is the package that is being used for web projects at MOBGEN most of the times, but it was not as performant and easy to use as the React Navigation package. The solutions given by the React Native package itself are not sufficient enough anymore. The creators of the React Native package are not giving navigational solutions to developers, and suggest you to use React Navigation or Native Navigation (created by Airbnb). Native Navigation is a package that is still in beta, and it is not advised to use beta packages in production apps.

From the navigational packages React Navigation was the easiest to set up and the most enjoyable to work with. The package was still hard to use and making new navigational components can sometimes be challenging.

---

##### References
- Open Source (React Community). (Date unknown). React Navigation GitHub. Consulted on 28-03-2018 from: https://github.com/react-navigation/react-navigation
- Open Source (React Training). (Date unknown). React Router Native. Consulted on 28-03-2018 from: https://github.com/ReactTraining/react-router/tree/master/packages/react-router-native
- Open Source (Wix). (Date unknown). React Native Navigation. Consulted on 28-03-2018 from: https://github.com/wix/react-native-navigation
- Open Source (Airbnb). (Date unknown). Native Navigation. Consulted on 28-03-2018 from: https://github.com/airbnb/native-navigation/
- Open Source (Facebook). (Date unknown). Navigating between screens. Consulted on 28-03-2018 from: https://facebook.github.io/react-native/docs/navigation.html#navigatorios
- Research done during internship from 01-11-2017 till 19-02-2018
