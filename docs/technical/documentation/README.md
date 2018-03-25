# Application Documentation 📚
###### What software or patterns were used and why?
---

## [React Native](https://facebook.github.io/react-native/)
##### What is it?
React Native is the native version of the [React.js](https://reactjs.org) language used for the web. It allows a developer to create an iOS and Android application with a single codebase. The React Native code compiles to Objective-C and Java, which can be run on iOS and Android respectively. By that way you create native apps with Javascript code. The framework was developed by Facebook, who also made the [React.js](https://reactjs.org) library for the web. React Native is being used by Facebook itself, Airbnb, Skype, Tesla and Wallmart.[^1]

##### Alternatives
There are some alternatives for React Native:
- [Ionic](https://ionicframework.com/) [^2]
- [PhoneGap/Cordova](https://cordova.apache.org/) [^2]
- [Xamarin](https://www.xamarin.com/) [^2]
- [Progressive Web Apps](https://developers.google.com/web/progressive-web-apps/) [^2]
- [Flutter](https://flutter.io/) [^3]

All the alternatives did not give the app the native like feeling like React Native is doing, except Flutter. Flutter is however written in the Dart language [^3], which required to much learning of a new language to be effective in this project.

##### Why React Native?
The main reason we decided to use React Native was of the fact that one developer was able to create both the iOS and the Android app from one codebase. The Enso project is on a tight budget (no budget) so we can only have intern developers, and most of the time there is only one intern assigned to the project.

Another reason was that MOBGEN is working a lot with React, and in the case of a web version of the application we could reuse a lot of the code from the React Native part to render te website. It is also easy for another developer to continue the work on the project as React Native does not differ much from React.

Lastly, React Native has a very big community behind it. There are a lot of packages from the React community that can also be used in React Native, but there are also a lot of packages made specifically for React Native by the community.

## [Redux](https://redux.js.org/)

##### What is it?
Redux is a predictable state container for Javascript apps. Redux creates a read-only object of data, that only can be updated with pure functions (actions) or reducers. Pure functions are functions that always return the same result, and a reducers is an updater that takes the current state, applies the changes and returns that next state.

![Example of a Redux Store]({{ book.img }}/redux-store-debug.png)
The above is an example of a so called Redux Store. The store is the place where all the data is stored and, as stated before, is read-only. With `actions` you can adjust the store. An action looks like this:

```javascript
const exampleAction = (id) => ({
  type: EXAMPLE_CONST,
  payload: id,
});
```

##### Why was it used?

##### Alternatives

## [Redux Saga](https://github.com/redux-saga/redux-saga)
##### What is it?

##### Why was it used?

##### Alternatives

## [Reselect](https://github.com/reactjs/reselect)
##### What is it?

##### Why was it used?

##### Alternatives

## [Recompose](https://github.com/acdlite/recompose)
##### What is it?

##### Why was it used?

##### Alternatives

## [Redux Persist](https://github.com/rt2zz/redux-persist)
##### What is it?

##### Why was it used?

##### Alternatives

## [Styled Components](https://github.com/styled-components/styled-components)
##### What is it?

##### Why was it used?

##### Alternatives

---

### References
[^1]: Facebook. (Date unknown). React Native. Consulted on 23-03-2018 from: https://facebook.github.io/react-native/
[^2]: Kukic, Ado. (10-01-2017). Alternatives to Native Mobile App Development. Consulted on 23-03-2018 from: https://auth0.com/blog/alternatives-to-native-mobile-app-development/
[^3]: Google. (Date unknown). Flutter. Consulted on 223-03-2018 from: https://flutter.io/
