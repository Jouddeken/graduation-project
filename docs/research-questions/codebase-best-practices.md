# Codebase Best Practices
###### Technical research question
---

### Codebase best practices
- Comments to describe the code
- ESlint to catch errors
- Prettier to format code for everybody

### What different ways are there to set up a project?
- Project folder structure (containers/components/global/services etc.), see [project structure](../technical/project-structure.md).
- Smart & dumb components to make reusable parts
- Redux store to handle all data

### How do you deal with all the side effects that happen on mobile?
Explaining the closing of the app and other side effects that can happen and how you can handle them with sagas. This has to be a sort of child friendly explanation of redux-saga and how it can be used in React Native to, for example cancel a fetch call when the user navigates away, or closes the app, or get's a phone call.

### References
- https://medium.com/skyshidigital/5-best-practices-for-react-native-development-you-probably-doesnt-know-474df87d74e6
- https://medium.com/dailyjs/11-mistakes-ive-made-during-react-native-redux-app-development-8544e2be9a9
- https://americanexpress.io/clean-code-dirty-code/
