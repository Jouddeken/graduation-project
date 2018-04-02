## [Redux Persist](https://github.com/rt2zz/redux-persist)
##### What is it?
Redux Persist is another package that can only be used with Redux. As explained before, the Redux store is a big object that contains the state of your application. What Redux Persist does is saving the Redux store in the local storage of the users device. When the user closes the application and comes back after some time, it takes the values that were stored in the local storage, and 'persists' them into the Redux store. This gives the user an application that is in the same state as the moment it was left.

##### Alternatives
- Local SQL Database

##### Why Redux Persist?
Redux Persist was chosen over a local SQL database because creating a local SQL database would take much more time for every new feature. You would have to decide which values you want to store and write function to store those values in the database. Redux Persist is widely used in the React (Native) community (5000+ stars on GitHub), and is a very mature package. The package itself is really easy to use, and does most of the work out of the box.