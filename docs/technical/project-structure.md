## Project structure

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
Smart and dumb components are the default way to setup a project at MOBGEN, and was the way it was learned to me during my first internship at MOBGEN. It is also an industry standard used by a lot of developers. A lot of articles are written on this subject on, for example, Medium, but also on the React website itself. I chose to use the smart and dumb component setup because:

- It's scalable
- Clear what does what
- Easy to understand
- Fast and structured

### References
[^1]: Mangin, Alexis. (28-04-2016). How to better organize your React applications?. Consulted on 06-06-2018 from: https://medium.com/@alexmngn/how-to-better-organize-your-react-applications-2fd3ea1920f1
[^2]: Facebook. (Date unknown). File structure. Consulted on 06-06-2018 from: https://reactjs.org/docs/faq-structure.html
[^3]: Abramov, Dan. (23-02-2015). Presentational and Container components. Consulted on 06-06-2018 from: https://medium.com/@dan_abramov/smart-and-dumb-components-7ca2f9a7c7d0.