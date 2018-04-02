## [Redux Saga](https://github.com/redux-saga/redux-saga)
##### What is it?
Redux Saga is a library that helps you handle side effects in your application. Examples of side effects are asynchronous things like data fetching and impure things like browser cache. Redux Saga is a Redux middleware, which means it can be started, paused and cancelled from the main application with Redux actions. The Saga has access to the whole Redux store and can dispatch actions as well. It uses ES6 generator function to make the sagas easy to read, write and test. With these generator functions, a Saga looks like a regular javascript function.

An example of a Redux Saga is:

<!-- Gist: Redux saga function -->
<script src="{{ book.gist }}/737dd3d5b79a7840ea7e1fcc8959be3b.js"></script>

The saga above is watching for the `FETCH_ALL_DATA` action to be fired. When that happens the watcher function fires the `getDataFromApi` function. The `getDataFromApi` function fires an action at the moment it is initiated. This can be used to display a loader for example. It then selects a token that is stored in the Redux store with a selector (more on selectors later). When it has received the token it calls the `fetchApiData` function that fires a fetch function to get some data from an API. The last step in this saga is to put an action with the data coming from the API call as payload.

The generator function simply takes one step at a time. When the previous step is done it continues to the next. It is easy to start, stop and pause these generator functions for this reason.

##### Alternatives
- Callbacks
- Promises
- [Redux-thunk](https://github.com/gaearon/redux-thunk)

##### Why Redux Saga?
Redux Saga was preferred over callbacks because with the callback method you end up in what developers have named: callback hell. You write so many callbacks that the functions are not easily readable anymore. A key factor in writing good code is to make sure it is readable by all developers.

Promises were also not the correct solutions because they can not be cancelled. Once a promise is made there is no possibility to stop it. It will finish or end up as an error. If a uses requests data via a promise, but then navigates away from the screen, you want to cancel the request. This is not possible with promises.

The third option, Redux-thunk, uses the ES2017 async/await functionalities. This is a good competitor and is used by a lot of people (8.355 stars on GitHub). The downside of Redux-thunk is that it is not as easy to test as Redux Saga. Another key factor in writing good code is to test your code with unit-tests and other tests. For the above reasons Redux Saga was used in the project.

In short: Redux Saga was used to prevent callback hell, be able to cancel functions/requests and to be able to test the code as good as possible.
