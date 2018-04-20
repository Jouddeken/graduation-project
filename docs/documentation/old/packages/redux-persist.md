## [Redux Persist](https://github.com/rt2zz/redux-persist)
##### What is it?
Redux Persist is another package that can only be used with Redux. As explained before, the Redux store is a big object that contains the state of your application. What Redux Persist does is saving the Redux store in the local storage of the users device. When the user closes the application and comes back after some time, it takes the values that were stored in the local storage, and 'persists' them into the Redux store. This gives the user an application that is in the same state as the moment it was left.

##### Alternatives
- Local SQL Database
- Firebase
- Realm

##### Why Redux Persist?
Redux Persist was chosen over a local SQL database because creating a local SQL database would take much more time for every new feature. You would have to decide which values you want to store and write function to store those values in the database. Firebase could be used but is more work than the Redux Persist way. Realm is not an option because I want to code to possibly be reused on web.

Redux Persist is widely used in the React (Native) community (5000+ stars on GitHub), and is a very mature package. The package itself is really easy to use, and does most of the work out of the box.

---

##### References
- Open source (Redux Persist). (Date unknown). Redux Persist GitHub. Consulted on 30-03-2018 from: https://github.com/rt2zz/redux-persist
- Filipe Borges. 14-06-2017. Stackoverflow answer. Consulted on 30-03-2018 from: https://stackoverflow.com/questions/44376002/what-are-my-options-for-storing-data-when-using-react-native-ios-and-android#answer-44549668
- Research done during internship from 01-11-2017 till 19-02-2018
