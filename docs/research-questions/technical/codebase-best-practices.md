# Codebase Best Practices
###### Technical research question
---

To develop a good application you need to know how to structure you code, write consistent code and also how to make it easy to add new features to the project. Following best practices in development prevents dirty code that is not understandable anymore.

### 2.1 What different ways are there to set up a project?
There are almost unlimited ways to setup a project in development, but some are more convenient than others. I did research to project structures in the [project structure](../../technical/project-structure.md) section of the technical phase. I describe the smart and dumb components setup with the help of an article of Dan Abramov, who is one of the creators of React and Redux.

This way of setting up a project is used in many of the beginner tuturials, but also in some of the biggest projects MOBGEN did. The Shell Oasis project I worked on also used this setup, and the KPN project MOBGEN is using it. Dennis Korff, senior frontend developer at MOBGEN also told me this is currently the preferred way of setting up React project in a conversation we had about this topic [^1].

In the end there are certainly many ways to set up a project, but the setup I used is the most common. The use of containers and components is also explained in the official React tutorial by Facebook [^2]

Putting this in practice, my project was setup following two guidelines, the smart and dumb components one, and a Redux structure aimed at medium to large scale projects. The setup is explained in detail on the [project structure](../../technical/project-structure.md) page.

### 2.2 How do you deal with all the side effects that happen on mobile?
On a mobile phone a lot of side effects happen. Side effects are actions that interrupt a process. For example fetching data from a server when suddenly the user quits the application. To handle these side effects I made use of a very powerful package: Redux Saga.

Redux saga is a library that aims to make application side effects (i.e. asynchronous things like data fetching and impure things like accessing the browser cache) easier to manage, more efficient to execute, simple to test, and better at handling failures. [^3]

Redux Saga is a middleware that lives between the actions and the reducers. You can call a saga function with an action, the saga listener will listen for a specific action to be fired, and then call the corresponding saga function. This saga function is an ES7 generator function [^4]. You can recognize them by the `*` behind the `function` keyword. A saga function looks like this: `function* generatorFunction() { ... }`.

An example saga looks like this:

```javascript
// importing the Redux Saga functions I used
import { cancel, put, select, take, takeLatest } from 'redux-saga/effects';
import { exampleSagaSuccessAction, exampleSagaErrorAction } from './actions';
import { EXAMPLE_ACTION_REQUEST } from './constants';
import { LOCATION_CHANGE } from '../Navigator/constants';
import { makeSelectObjectFromStore } from './selectors';

// The generator function
function* exampleSaga() {
  try {
    // When this function is fired it is going to select an object from the Store
    const payload = yield select(makeSelectObjectFromStore());
    // The generator function waits until the yield above returns a value
    // And will continue the function.
    // It would 'put' (call) on of the imported actions.
    yield put(exampleSagaSuccessAction(payload));
  } catch (error) {
    // When the function catches an error it would 'put' (call) the error action
    // I imported above.
    yield put(exampleSagaErrorAction(error));
  }
}

// This function is a so called 'watcher' that watches for the EXAMPLE_ACTION_REQUEST
// to be fired in the application. When that happens it runs the exampleSaga.
// When LOCATION_CHANGE occurs this function will cancel the 'watcher' and cancel the
// running saga.
// This function is exported and imported and used in the Redux store where it is added
// as a middleware.
export function* watchexampleSaga() {
  const watcher = yield takeLatest(EXAMPLE_ACTION_REQUEST, exampleSaga);
  yield take(LOCATION_CHANGE);
  yield cancel(watcher);
}
```

What this does is give you way more control over which fetch calls or selectors are running in your application. When the user starts a fetch and decides to navigate away from the screen, you can very easily cancel this request with the saga.

### References
[^1]: Korff, D. (02-06-2018). Interview with a senior developer at MOBGEN about best practices.
[^2]: Facebook. (Date unknown). React tutorial. Consulted on 08-06-2018 from: https://reactjs.org/tutorial/tutorial.html
[^3]: Redux Saga. (Date unknown). Redux saga documentation. Consulted on 08-06-2018 from: https://redux-saga.js.org/
[^4]: Multiple authors (23-05-2018). MDN web docs: function*. Consulted on 08-06-2018 from: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function*

<!-- - https://medium.com/skyshidigital/5-best-practices-for-react-native-development-you-probably-doesnt-know-474df87d74e6
- https://medium.com/dailyjs/11-mistakes-ive-made-during-react-native-redux-app-development-8544e2be9a9
- https://americanexpress.io/clean-code-dirty-code/ -->