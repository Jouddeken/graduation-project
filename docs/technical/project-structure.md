## Project structure
###### How was the project folder structure setup and why?
---

The project is set up following a set of simple rules that work well with the React framework and specially with the Redux way of working.

##### What is it?
Smart and Dumb components is a way of organizing your React application. There are many other names for this concept. Some people call them _Container and Presentational_ components, _Smart and Dumb_ components or _Stateful and Pure_ components. The core concept of it is that one of the two is taking care of all the business logic, and the other one of displaying the data.

In my case this would mean that Smart components are the place where fetching data from an external source takes place and any other functions like navigating. Inside this Smart component live some dumb components. They do not have any functionality and only take care of displaying the data in a way the designer wants.

**This means that Smart components:**
- Are concerned with how things _work_
- May contain both Smart and Dumb components inside them, but never set any styles
- Provide the data and behavior to other components inside of them
- Are made with `class [name] extends React.Component { class }`
- Connect with the Redux store via the `connect()` function
- Are stateful (have state)
- Examples of Smart Components: TabBar, HomeScreen, HeaderBar

**This means that Dumb components:**
- Are concerned with how things _look_
- Are completely separated from the rest of the app
- Do not specify how the data is loaded/fetched/mutated
- Receive data and callbacks exclusively via props
- Rarely have their own state (only UI state like if something is folded out or not)
- Are written as functional components using a `function [name] ({ ...props }) { function }`
- Examples: H1, OrderedList, Image

In short, this means Smart components do all the data handling and pass the correct data to the dumb components. The dumb components simply render the given data, and can be easily reused in other Smart components.

---

The codebase should have the following structure when following this pattern:
```text
 - src
   - components
     - Component1
       - index.js
     - Component2
       - index.js
     - etc...
   - containers
     - Container1
       - actions.js
       - constants.js
       - index.js
       - reducer.js
       - sagas.js
       - selectors.js
     - Container2
       - actions.js
       - constants.js
       - index.js
       - reducer.js
       - sagas.js
       - selectors.js
     - etc...
```

##### Alternative
Some people prefer to keep all actions, constants, reducers, sagas and selectors in one file. This is a nice approach when the application is smaller, and does not have a lot of actions, constants, reducers, sagas and selectors. The folder structure would be as follows:

```text
  - src
    - actions
      - actionFile1.js
      - actionFile2.js
    - components
      - Component1
        - index.js
      - Component2
        - index.js
    - constants
      - constantsFile1.js
      - constantsFile2.js
    - reducers
      - reducersFile1.js
      - reducersFile2.js
    - sagas
      - sagasFile1.js
      - sagasFile2.js
    - selectors
      - selectorsFile1.js
      - selectorsFile2.js
    - container1.js
    - container2.js
```

The difference here is that the actions, constants, reducers, sagas and selectors are now grouped together instead of in a separate container folder.

##### Why smart & dumb components?
Smart and dumb components are the default way to setup a project at MOBGEN, and was the way it was learned to me during my first internship at MOBGEN. It is also an industry standard used by a lot of developers. A lot of articles are written on this subject on, for example, Medium, but also on the React website itself. I decided to use the smart and dumb component setup because:

- It's scalable
- Clear what does what
- Easy to understand
- Fast and structured
- Industry standard

### How did I set up my project?
To explain the project structure, it is the easiest to show and describe what the most important files do.
<div class="images-row group">
  <div class="image-item image-item--1-3 image-item--border">
    <img src="{{ book.img }}/enso-folder-setup.png">
  </div>
  <div class="image-item image-item--2-3 image-item--border">
    <p>You would enter the application in the App.js file at the bottom of the image. Underneath this App.js is a file called reducers.js, this file takes all reducers from the containers, and puts them in the Redux store. The file sagas.js underneath the reducers.js file does the same, but then for the sagas of all the containers. In store.js we initialize the Redux store, this is the single source of truth all our data will be in.</p>
    <p>In the folder 'containers' are all the screens of the application. Besides that there is a container call App. In app we render the navigator, which we initialize in the Navigator folder. We use the navigator to show the correct screens and to navigate through the application. Every time we navigate in the application the navigator requests a new screen/container to show.</p>
    <p>Most of the containers have a set of files in them, these files are:</p>
    <ul>
      <li>actions.js</li>
      <li>constants.js</li>
      <li>index.js</li>
      <li>reducer.js</li>
      <li>sagas.js</li>
      <li>selectors.js</li>
    </ul>
  </div>
</div>

**actions.js**<br />
Inside the actions.js files are the actions the container can perform. The actions are part of Redux, and as explained are pure functions (function that return the same things every time they are being called). Example of an action file:

```javascript
// importing the constants from the constants.js file in the same folder
import {
  EXAMPLE_TYPE_REQUEST,
  EXAMPLE_TYPE_SUCCESS,
  EXAMPLE_TYPE_ERROR,
} from './constants';

export const exampleActionRequest = id => ({
  type: EXAMPLE_TYPE_REQUEST,
  payload: id,
});
export const exampleActionSuccess = id => ({
  type: EXAMPLE_TYPE_SUCCESS,
  payload: id,
});
export const exampleActionError = error => ({
  type: EXAMPLE_TYPE_ERROR,
  error,
});
```

**constants.js**<br />
Inside the constants file are the constants that are used for this container. Most of the time there are three types of the same constant. One request, one success and one error. These constants are used in the actions, sagas, and reducer. Example of a constants file:

```javascript
export const EXAMPLE_TYPE_REQUEST = 'ContainerName/EXAMPLE_TYPE_REQUEST'
export const EXAMPLE_TYPE_SUCCESS = 'ContainerName/EXAMPLE_TYPE_SUCCESS'
export const EXAMPLE_TYPE_ERROR = 'ContainerName/EXAMPLE_TYPE_ERROR'
```

**index.js**<br />
This file contains the actual container. Most of the time it has a React in it. This file is what connects the container to the Redux store, and what is rendered on the users screen. Example of an index file:

```javascript
// importing the React library from the node_modules
import React from 'react';
// importing the function that connects the container to the Redux store
import { connect } from 'react-redux';
// importing the function that helps with creating selectors to select values from the Redux store
import { createStructuredSelector } from 'reselect';
// Higher Order Component function that takes in a component, applies functions and returns a component
// Used to add the mapStateToProps and mapDispatchToProps to the container
import compose from 'recompose/compose';
// importing an example action from the actions file in this folder
import { exampleAction } from './actions';
// importing the selectors that select the home title and an id from the Redux store
import { selectHomeTitle, selectHomeId } from './selectors';
// importing a Title component from the components folder (this is a dumb component)
import Title from '../../components/Text/Title';
// importing a Wrapper from the Wrapper.js file in this folder
import Wrapper from './Wrapper';

class ExampleContainer extends React.Component {
  // When clicking on the Button, it will fire the exampleAction from the ./actions.js file
  render() {
    <Wrapper>
      <Title>{this.props.title}</Title>
      <Button
        title="Click me!"
        onPress={() => this.props.action(this.props.id)}
      />
    </Wrapper>
  }
}

// Mapping selectors that return values to the props of this container
const mapStateToProps = createStructuredSelector({
  title: selectHomeTitle(),
  id: selectHomeId(),
});

// mapping actions to the props of this container
function mapDispatchToProps(dispatch) {
  return {
    action: id => dispatch(exampleAction(id)),
  };
}

// This part connects the container to the Redux store
export default compose(
  connect(
    mapStateToProps,
    mapDispatchToProps
  )
)(ExampleContainer);
```

**reducer.js**<br />
The reducer is a pure function that takes the current state of the reducer in the Redux store, makes a copy of that state and applies the changed values to that copy. Note that the state of the Redux store is never directly changed because of this way. An example of a reducer.js file is as follows:

```javascript
// importing the constant from './constants'
import { EXAMPLE_TYPE_SUCCESS } from './constants';

// the initial state of this reducer, when the app loads this is applied
const initialState = {
  title: null,
  id: null,
}

// the reducer, it is listening for action.type (the constant) and when that is true,
// it spreads the state (creating a new object) and applies the changed values to
// this new object
export const exampleReducer = (state = initialState, action) => {
  switch (action.type) {
    case EXAMPLE_TYPE_SUCCESS:
      return {
        ...state,
        id: action.payload,
      };
    default:
      return {
        ...state,
      };
  }
};
```

**sagas.js**<br />
In the sagas file we run a function when a certain value is true. These functions are middleware, which means they happen between the action and the reducer. When an action is fired you can lead it through a saga and after the saga pass it to the reducer. Sagas are ES6 generator functions, which means the functions wait for the current step to finish until they go to the next step. An example of a sagas file is as follows:

```javascript
// importing functions from the Redux Saga package from the node_modules
import { all, put, select, take, takeLatest } from 'redux-saga/effects';
// importing the actions from the actions.js file in this folder
import {
  exampleActionSuccess,
  exampleActionError,
} from './actions';
// importing the constant the saga should listen for
import { EXAMPLE_TYPE_REQUEST } from './constants';
// importing selectors
import {
  makeSelectHomeTitleWithId,
} from './selectors';

// The ES6 generator function, notice the '*' after the function keyword
function* exampleSaga(action) {
  try {
    // Since we are using yield, the function will stop and select the values
    // from the store with the selector. When it is done selecting the values
    // it will come back and continue.
    const payload = yield select(makeSelectHomeTitleWithId(action.payload));
    // After selecting a new payload from the store we yield put() a success action
    yield put(exampleActionSuccess(payload))
  } catch (error) {
    // When things go wrong we yield put() the error action and fire an error
    yield put(exampleActionError(error));
  }
}

// This is the watcher that is listening for the EXAMPLE_TYPE_REQUEST to be fired
// this constant is fired upon clicking on the button in the index.js file in this
// folder. When is sees this EXAMPLE_TYPE_REQUEST it will fire the exampleSaga.
function* exampleWatcher() {
  yield all([
    yield takeLatest(EXAMPLE_TYPE_REQUEST, exampleSaga),
  ]);
}
```

**selectors.js**<br />
Last, but certainly not least, we have the selectors.js file. In this file are functions that are being used to select values from the Redux store. An example of a selectors.js file is as follows:

```javascript
// importing the createSelector function from reselect. This function creates memoized
// selectors which means it is kept in the cache of the users memory, and faster when
// called again
import { createSelector } from 'reselect';

// selects the home reducer from the redux store (state)
const selectHomeDomain = state => state.home;

// selects the title from an object with key id from the home reducer
const makeSelectHomeTitleWithId = id => createSelector(
  [selectHomeDomain()],
  (home) => {
    const title = home.data[id].title;
    return title;
  }
);

// selects the title from the home reducer
const selectHomeTitle = () => createSelector(
  [selectHomeDomain()],
  (home) => home.title,
);

// Selects the id from the home reducer
const selectHomeId = () => createSelector(
  [selectHomeDomain()],
  (home) => home.id,
);

// exporting the selectors
export {
  selectHomeDomain,
  makeSelectHomeTitleWithId,
  selectHomeTitle,
  selectHomeId,
};
```

All these files together make one functioning container, and one container is one screen in the application. Containers are smart, and they import dumb components that render the data the smart container passed to them.

### References
[^1]: Mangin, Alexis. (28-04-2016). How to better organize your React applications?. Consulted on 06-06-2018 from: https://medium.com/@alexmngn/how-to-better-organize-your-react-applications-2fd3ea1920f1
[^2]: Facebook. (Date unknown). File structure. Consulted on 06-06-2018 from: https://reactjs.org/docs/faq-structure.html
[^3]: Abramov, Dan. (23-02-2015). Presentational and Container components. Consulted on 06-06-2018 from: https://medium.com/@dan_abramov/smart-and-dumb-components-7ca2f9a7c7d0.