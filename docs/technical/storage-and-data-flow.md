## Data flow and storage
###### How is the data handled and stored in the application
---

Every application has to deal with data. This can be a lot of data, or a small bit of data, depending on the size of the application. Data is often created and modified in an application, and sometimes stored on the users device itself, or even on a remote server. For storing data, it is nice to have a certain pattern to follow. For the Enso project I worked with the Redux way of working to handle data.

##### What is it?
Redux is a way of storing your data in your app. It does that by putting all your data in a global 'store'. The store is the place where all the data of your app lives, and if anything changes, that store will also change.

Redux has three core principles:
1. **Single source of truth**
2. **State is read-only**
3. **Changes are made with pure functions**

Redux is initially hard to grasp, but it is best explained using a flow chart.

![Redux flow](https://camo.githubusercontent.com/9de527b9432cc9244dc600875b46b43311918b59/68747470733a2f2f73332e616d617a6f6e6177732e636f6d2f6d656469612d702e736c69642e65732f75706c6f6164732f3336343831322f696d616765732f323438343739302f415243482d5265647578322d657874656e6465642d7265616c2d6465636c657261746976652e676966)

1. In the flow an event is dispatched from the view, this is our starting point. This event is clicking a button, for example.
```javascript
// When the user presses this button, the onPress function is fired!
<Button title="Action dispatcher" onPress={() => action()} />
```
2. This click event fires an action that describes what happened.
```javascript
const action = () => ({
     type: 'BUTTON_CLICK', // notice the type: 'BUTTON_CLICK', the type is used later as well and should describe the action.
});
```
This is a so called pure function. It returns the same object every time it is called.

3. This action goes through some middleware. Middleware is where data fetching calls, and normalization of the data take place.

4. It the goes into a so called 'reducer' that takes the current state of the 'store', applies the action changes to that 'store' and returns a new copy of the 'store' that is an updated version of the 'store'
```javascript
const reducer = (state = {}, action) => {
     switch (action.type) {
       case 'BUTTON_CLICK': // This is our action!
         return {
           ...state, // this is where we take a copy of the state
           isButtonClicked: true, // and apply the new value to that copy
         }
       default:
         return state;
     }
}
```
5. The new state is then returned to the view, and triggers a re-render of the view.
For example: if we used to have a state that looked like this:
```javascript
const state = {
     name: 'example name',
     isButtonClicked: false,
     isConnected: true,
};
```
We would have a state that looks like this after the button click:
```javascript
const state = {
     name: 'example name',
     isButtonClicked: true, // This changed with our action!
     isConnected: true,
};
```
The important thing to notice is that Redux makes a copy of the state, it does not overwrite values. This means the state is immutable.

Redux is a very nice way to implement a very scalable way of working with data in your app. You can use Redux for small apps, but it's overkill for most of the applications. Only when the user can do multiple things in the application and adjust values, it might be a good idea to implement Redux.

The downside of Redux is that you have to edit three files to create one action. The view itself, the action and the reducer.

##### Alternatives
- [MobX](https://mobx.js.org/)
- [RxJs](https://github.com/ReactiveX/rxjs/tree/stable)
- [Realm](https://realm.io/)

##### Why Redux?
Redux is more manual than MobX, and for the Enso project that is what I needed. This means you need to write more code yourself, which can be seen as a downside. The code you write is however easily testable and extremely predictable, which is considered a good practice. I wanted to have full control over what my data structure looked like. Redux gave me this functionality.

Realm is only usable by React Native and node.js applications, and because there were some vague plans of making a web port of the React Native application I wanted to use as much packages as possible that could be used on Native and web.

The reason I chose for Redux is because of the many packages I can integrate into the Redux environment. Examples of those packages are Redux Saga, Reselect and Redux Persist. These packages are also being used in web apps, so that is a big bonus in the reusable aspect of the code. Redux is also very well supported by a massive community, and has a great documentation. Besides that, a lot of developers at MOBGEN are working with Redux, so it is easier to find help when I have questions or problems.
