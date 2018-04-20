## [Reselect](https://github.com/reactjs/reselect)
##### What is it?
Reselect is a package that gives you a good way of selecting certain values from the Redux store. The package was developed specifically to work together with Redux. You can write a selector to select multiple values from multiple selectors from the store. Imagine a simple Redux store, this simple store could look like this:

<!-- Gist: Redux example store object -->
{% gist id="f4b51dfffc63d228a0168e7da719ca9d" %}{% endgist %}

An example of a selector can be:

<!-- Gist: Reselect example function -->
{% gist id="89c11e99b77635bfbd0346c152e98ef9" %}{% endgist %}

##### Alternatives
Because Reselect is specifically made for Redux (or Flux, the old version of Redux), there are no other packages made that do the same as Reselect. It is not mandatory to work with Reselect, but it does make your life easier when creating a complicated application. It makes an application faster with the memoization of selectors (selectors are saved in the cache memory, so they can be reused easily and quick).

##### Why Reselect?
Reselect was used because it was the only option there was, and because it is so well integrated in the Redux ecosystem. With the Reselect package you can write more functions you can reuse easier, which is one of the concepts of good code. Without the Reselect package the code is less testable and harder to read.

---

##### References
- Open source (Reselect). (Date unknown). Reselect GitHub. Consulted on 29-03-2018 from: https://github.com/reactjs/reselect
- Research done during internship from 01-11-2017 till 19-02-2018
