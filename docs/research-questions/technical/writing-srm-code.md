# Writing Scalable, Reusable and Maintainable Code
###### Technical research question
---

### 3.1 What packages or patterns can you use to make the code more clean and efficient?
Good code is consistent code. To enforce consistency in  a project, a developer can use a couple of tools. Using a modern editor (VSCode, WebStorm or something similar) it is possible to add a linter to the code editor. This linter is a program that checks the code as it is being written down. It will give the developer warnings when the code is not consistent or when the code that is written down is outdated or not adviced. There are a couple of linters available, but in the Enso project I used ESLint [^1]. When I make a mistake in the code it shows you the following:

![eslint error]({{ book.img }}/eslint-error.png)

The ESLint plugin is checking against a lot of rules. At MOBGEN the developers use the Airbnb setup with some additional rules added to the setup. This enforces the developers to write the same type of code. The ESLint also checks against the indentation of the code and returns an error when the indentation is not correct.

Another package that I used in the project that was adviced by Dennis Korff, senior developer at MOBGEN [^2], was the Prettier package [^3]. Prettier is an an autoformatter for your code. When you hit save it automatically reformats the code following the ESLint rules that are set up for the Prettier plugin.

A good pattern that should be followed and is considered a best practice as well is the smart and dumb components pattern I explain in the [project structure](../../technical/project-structure.md) section. With this pattern logic is separated from visual components.

To keep the code consistent and clean we did code reviews as well. This is explained in the next section a bit more, as it is part of the Git workflow.

### 3.2 How can you work with a version control system, and why is it considered indispensable in a project?
When working on a development project, there is nothing worse than code loss. To prevent this, Git was used. Git is a version control system made by Linus Thorvalds [^4]. Git works with branches that basically have a copy of the project on them. For example you have the `master` branch that contains the latest release of an application, a `development` branch that contains features that are done for a next release, and most of the time multiple `feature/branch-name` branches where developers work on their own separate features [^5].

Without Git or another version control system you are constantly copying files between developers, which is very error sensitive. You want to prevent that. Another benefit of using a version control system is the possibility to go back in history and run an older version of the app. This could be useful when, for some reason, the current branch has errors on them and the developer wants to check where these errors slipped into the project. Git serves as a history tool for those situations.

Besides that you can do very structured code reviews when using a branching model like the one Vincent Driessen describes on his blog [^6]. When a feature branch is being merged into the development branch, the developer that requests this merge assigns a couple of developers as reviewers to this request. The assigned developers will then check the code for any inconsistencies or errors before it gets merged into the development branch. This way you ensure that everything that is on the development branch is actually working. [^7]

Below is an example of how such pull request looks like:
![enso-bitbucket-pull-request.png]({{ book.img}}/enso-bitbucket-pull-request.png)

### 3.3 How can you make sure the code you write will work as expected?
Doing code reviews is a big part of making sure that the code works as expected. A second set of eyes and brains that scan the code can already prevent many bugs or help you with improving your code. Another good practice is to do unit tests on the code. Unit testing is breaking your application into smaller pieces and subjecting these pieces to a number of tests you have written for them [^8].

Imagine the following function:

```javascript
export function sum(a, b) {
  return a + b;
}
```

To unit test this function you can:

```javascript
// call the function
sum(2, 4) // should return 6
```

Functions in real world applications are most of the time a bit more complex, but it is still important to test these functions. For testing in React, Facebook made a package named Jest. With Jest you can run the tests in your command line. An example of a unit test with jest would be as follows:

Imagine we have the following function again:

```javascript
export function sum(a, b) {
  return a + b;
}
```

With jest we can test this function as follows:

```javascript
import { sum } from './sum';

test('adds 1 + 2 to equal 3', () => {
  expect(sum(1, 2)).toBe(3);
});
```

Jest will run this test and add the `passed` flag when the test returns true. With the smart and dumb components setup that was described earlier it is easier to do the unit tests as well. Your dumb components only render the data, so they are easy to test.

The unit tests are a good way to keep track of which properties every component receives. When another developer changes some things in a component, runs the tests and they suddenly fail, he or she knows something is not correct and has to change. This way you will prevent unexpected errors. [^9]

---

### References
[^1]: Author unknown. (Date unknown). ESLint documentation. Consulted on 08-06-2018 from: https://eslint.org/
[^2]: Korff, D. (02-06-2018). Interview with a senior developer at MOBGEN about best practices.
[^3]: Author unknown. (Date unknown). Prettier GitHub. Consulted on 08-06-2018 from: https://github.com/prettier/prettier
[^4]: Author unkown. (31-10-2017). Linus Thorvalds wikipedia. Consulted on 08-06-2018 from: https://nl.wikipedia.org/wiki/Linus_Torvalds
[^5]: Strumpflohner, J. (30-04-2013) Git Explained: For Beginners. Consulted on 08-06-2018 from: https://juristr.com/blog/2013/04/git-explained/
[^6]: Vincent Driessen. (01-05-2010). A successful Git branching model. Consulted on 08-06-2018 from: https://nvie.com/posts/a-successful-git-branching-model/
[^7]: Radigan, D. (Date unknown). Code reviews. Consulted on 08-06-2018 from: https://www.atlassian.com/agile/software-development/code-reviews
[^8]: Mattj. (16-03-2009). What is unit testing answer. Consulted on 06-08-2018 from: https://stackoverflow.com/a/652309/8301587
[^9]: Facebook. (Date unkown). Jest documentation. Consulted on 06-08-2018 from: https://facebook.github.io/jest/docs/en/getting-started.html
