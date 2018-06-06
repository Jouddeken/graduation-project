## Styling
###### Styling
---

With every application comes a design. This design has to be translated to code. There are always many ways to translate these visual styles to code, as well in React Native. We have three options we can chose from when styling the application

1. React Native's StyleSheet
2. Styled components
3. Glamorous Native

### React Native's StyleSheet [^1]
I have used the React Native's StyleSheet in the first version of the Enso application. This solution works pretty well for small to semi-large applications, but when the application scales up to a bigger application it is nicer to have something with more functionalities build into it. Besides that it does not feel like you are writing actual css, as you are writing css in javascript. This means that `border-radius` has to be written down as: `borderRadius`. For a frontend developer this does not feels natural.

### Styled components [^2]
I tried this package with the first release of the Enso application as well, but it had some major performance issues when used on the phones. Currently they released a new major version of the package (version 3.0.0 is now released), and this version fixes the performance issues. I have used the styled components library on web project before, and a lot of other developers at MOBGEN as well. This means they could easily understand how things were styled when they would join the Enso project. The styled components package has a lot of functionalities that make the development easier, and can also be used on the web.

### Glamorous Native [^3]
Glamorous Native is pretty similar to Styled components but was specifically made for native projects as the name would suggest. The project is based on the Glamorous package that is used on web which is now being migrated to emotion. Glamorous is also heavily influenced on Styled components.

### Conclusion
In the end I chose to use the styled component library because of the following reasons:
- You can use the actual css syntax
- Myself and MOBGEN were familiar with the package from the web projects
- It's more scalable compared to React Native's StyleSheet
- You can do conditional styling based on the props of a component

Eventhough with Glamorous you can strip out the parser and have a smaller bundle size, I prefer the styled components. This is because I am familiar with the package and don't have to think about how to use it.

### References
[^1]: Facebook. (Date unknown). StyleSheet. Consulted on 06-06-2018 from: https://facebook.github.io/react-native/docs/stylesheet.html
[^2]: Styled components. (Date unknown). Styled components GitHub. Consulted on 06-06-2018 from: https://github.com/styled-components/styled-components
[^3]: Glamorous Native. (Date unknown). Glamorous Native Github. Consulted on 06-06-2018 from: https://github.com/robinpowered/glamorous-native
[^4]: third774. (09-09-2017). Styled Components vs. Glamorous - pros/cons. Consulted on 06-06-2018 from: https://www.reddit.com/r/reactjs/comments/6uz3aa/styled_components_vs_glamorous_proscons_of_each/
