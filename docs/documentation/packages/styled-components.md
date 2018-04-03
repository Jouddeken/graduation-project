## [Styled Components](https://github.com/styled-components/styled-components)
##### What is it?
Styled Components is a styling library that originally was made for the React web package. In version 3 it was possible to use the package with React Native, but there were some performance issues with it. Now that version 4 is released and those problems are gone, developers can use the package to make styling components in React Native easy. Without Styled Components a component with some styling may look like the following:

<!-- Gist: React Native styling -->
{% gist id="230ceab078623837d0253fa799e7b666" %}{% endgist %}

With Styled Components the same component looks like this:

<!-- Gist: Styled Component -->
{% gist id="f52d052280243def442dce4c68b1c14c" %}{% endgist %}

##### Alternatives
- [React Native's `StyleSheet.create();`](https://facebook.github.io/react-native/docs/style.html)
- [Glamorous Native](https://github.com/robinpowered/glamorous-native)
- [React Native Tachyons](https://github.com/tachyons-css/react-native-style-tachyons)

##### Why Styled Components?
As you can see the Styled Components way adds one more file to the amount of files needed, but will make it much easier to reuse components that have been made. The syntax to create a new Styled Component is also shorter than using the default React Native `StyleSheet.create();` function. The Glamorous package is a great competitor to Styled Components, but since MOBGEN was already using Styled Components in web projects and I already knew the package I chose for Styled Components. The last package in the alternatives list is the React Native Tachyons package. This package gives you shortcuts like `flx-i` and `asfs` to use on your components. The `flx-i` stands for `flex: 1` and `asfs` stands for `align-self: flex-start`. I don't think this method is very readable, as a developer you have to know the Tachyons package to make use of this. It makes the code less readable for another developer.