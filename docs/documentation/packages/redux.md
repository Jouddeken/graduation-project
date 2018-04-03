## [Redux](https://redux.js.org/)

##### What is it?
Redux is a predictable state container for JavaScript apps. Redux creates a object tree in a so called store for your application. Redux can be described in three fundamental principles:

<span style="opacity: 0.75;">**1. Single source of truth**</span><br />
The state of the entire application is stored in a single object tree in a single store. A Redux store example can look like this:

![Example of a Redux Store]({{ book.img }}/redux-store-debug.png)

<span style="opacity: 0.75;">**2. State is read-only**</span><br />
The only way to change the state is to emit an action, an object describing what happened.

<span style="opacity: 0.75;">**3. Changes are made with pure functions**</span><br />
To specify how the state tree is transformed by actions, you write pure reducers.

Redux creates a object tree for the application in a so called store. The above is an example of a so called Redux Store. Only with actions you can adjust the store. An action is a pure function and can look like this:

<!-- Gist: Redux action function -->
{% gist id="8f423c9307b84476e9875651eeb29ac0" %}{% endgist %}

The only way the store can be transformed is via reducers. Reducer functions take the current state of the store and the fired action as arguments and returns the updated state. A reducer can look like this:

<!-- Gist: Redux reducer function -->
{% gist id="ad33aeefa5df7723ec98a3ab715fb6f9" %}{% endgist %}

##### Alternatives
- [MobX](https://mobx.js.org/)
- [Realm](https://realm.io/)

##### Why Redux?
Redux is more manual than MobX, and for the Enso project that is what I needed. This means you need to write more code yourself, which can be seen as a downside. The code you write is however easily testable and extremely predictable, which is considered a good practice.

Realm is only usable by React Native and node.js applications, and because there were some vague plans of making a web port of the React Native application I wanted to use as much packages as possible that could be used on Native and web.

The reason I chose for Redux is because of the many packages I can integrate into the Redux environment. Examples of those packages are Redux Saga, Reselect and Redux Persist. These packages are also being used in web apps, so that is a big bonus in the reusable aspect of the code. Redux is also very well supported by a massive community.
