## [Smart & dumb components](https://medium.com/@dan_abramov/smart-and-dumb-components-7ca2f9a7c7d0)
##### What is it?
Smart and Dumb components is a way of organizing your React application. There are many other names for this concept. Some people call them _Container and Presentational_ components, _Fat and Skinny_ components, _Smart and Dumb_ components or _Stateful and Pure_ components. The core concept of it is that one of the two is taking care of all the business logic, and the other one of displaying the data.

In my case this would mean that Smart components are the place where fetching data from an external source takes place and any other functions like navigating. Inside this Smart component live some dumb components. They do not have any functionality and only take care of displaying the data in a way the designer wants.

**This means that Smart components:**
- Are concerned with how things _work_
- May contain both Smart and Dumb components inside them, but never set any styles
- Provide the data and behavior to other components inside of them
- Are made with `class [...] extends React.Component {...}`
- Connect with the Redux store via the `connect()` function
- Are stateful (have state)
- Examples of Smart Components: TabBar, HomeScreen, HeaderBar

**This means that Dumb components:**
- Are concerned with how things _look_
- Are completely separated from the rest of the app
- Do not specify how the data is loaded/fetched/mutated
- Receive data and callbacks exclusively via props
- Rarely have their own state (only UI state like if something is folded out or not)
- Are written as functional components using a `function [...] ({ ...props }) {...}`
- Examples: H1, OrderedList, Image

  ##### Alternatives
_Soon to come, stay tuned_ 🎶

##### Why smart & dumb components?
_Soon to come, stay tuned_ 🎶
