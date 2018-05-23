# Pattern research 🎛
###### Common solutions to solve problems
---

### Create sprint
To create a sprint the application needs some simple information from the user. Before creating a sprint the user has to fill in three required fields, and two optional. The application needs:

- A name for the sprint
- A challenge for the sprint
- A template that is going to be used in the sprint
- Dates the sprint is going to take place
- The number of participants in the sprint

The challenge and number of people are not required to fill in. Challenge can be skipped in this flow and the number of participants defaults to 7, as that is the preferred number of participants in a sprint.

I looked at how Zalando guides a user through the order process:

<div class="images-row group">
  <div class="image-item image-item--1-2 image-item--border">
    <img src="{{ book.img }}/patterns/zalando-1.png">
  </div>
  <div class="image-item image-item--1-2 image-item--border">
    <img src="{{ book.img }}/patterns/zalando-2.png">
  </div>
  <div class="image-item image-item--1-2 image-item--border">
    <img src="{{ book.img }}/patterns/zalando-4.png">
  </div>
  <div class="image-item image-item--1-2 image-item--border">
    <img src="{{ book.img }}/patterns/zalando-5.png">
  </div>
</div>

Zalando guides the user through the process of ordering clothes online by splitting the tasks a user has to do in easy steps. This methods makes it easier for the user to focus on a specific task, and you can keep all important information above the fold. With the steps at the top of the screen it is also very clear for the user how far in the process he is, and how long it approximately is going to take.

For creating a sprint I am going to do the same, give the user a number of steps to make clear how long the process is, and give every step a dedicated screen.

### Edit sprint
The user should have the ability to change some values of a sprint. The things a user can do are:

- Change the name of the sprint
- Change the challenge of the sprint
- Change the template of a sprint
- Change the date of a sprint
- Change the number of participants in the sprint
- Change the titles of every day in the sprint
- Change the start times of every day in the sprint

I looked at other applications where you can edit multiple values, for example details of a users profile. I found two main ways in which the bigger, market leading, application give their users the ability to change values. You can divide those application in two groups, one group where they have one screen that acts as an overview, with multiple items on the screen the user can click on. After a click the user goes to a new screen where this single value can be adjusted.

<div class="images-row group">
  <div class="image-item image-item--1-2 image-item--border">
    <img src="{{ book.img }}/patterns/facebook-1.png">
  </div>
  <div class="image-item image-item--1-2 image-item--border">
    <img src="{{ book.img }}/patterns/twitter-1.png">
  </div>
  <div class="image-item image-item--1-2 image-item--border">
    <img src="{{ book.img }}/patterns/uber-1.png">
  </div>
  <div class="image-item image-item--1-2 image-item--border">
    <img src="{{ book.img }}/patterns/snapchat-1.png">
  </div>
</div>

The other group are application where the user can edit all the values on one screen. The user can click on an input and the keyboard shows up.

<div class="images-row group">
  <div class="image-item image-item--1-2 image-item--border">
    <img src="{{ book.img }}/patterns/marktplaats-1.png">
  </div>
  <div class="image-item image-item--1-2 image-item--border">
    <img src="{{ book.img }}/patterns/instagram-1.png">
  </div>
</div>

### Edit agenda

When a user is in an agenda view, where all the events of that day are listed, he can do multiple things:

- Reorder the events
- Mark an event as done
- Delete an event
- Add a new event

These features are all available in the iOS clock application:

<div class="images-row group">
  <div class="image-item image-item--1-2">
    <img src="{{ book.img }}/patterns/iOS-timer-1.jpeg">
  </div>
  <div class="image-item image-item--1-2">
    <img src="{{ book.img }}/patterns/iOS-timer-2.jpeg">
  </div>
  <div class="image-item image-item--1-2">
    <img src="{{ book.img }}/patterns/iOS-timer-3.jpeg">
  </div>
  <div class="image-item image-item--1-2">
    <img src="{{ book.img }}/patterns/iOS-timer-4.jpeg">
  </div>
</div>

The good thing about this is that to delete an event the user has to click 3 times. This means it can never happen accidentally during the design sprint. Also, both iOS and Android users are familiar with the three stripes that are being used to indicate a reorder function [^1]. The most difficult feature in this screen is probably the mark as complete function. This is because on the left side will be the remove button, and on the right the reorder button.

### Home
The homepage in the application has two states. One where the user has created sprints, and one where the user does not have any sprints at all. I looked at how other apps fix this problem.

<div class="images-row group">
  <div class="image-item image-item--1-3 image-item--border">
    <img src="{{ book.img }}/patterns/empty-state-1.png">
  </div>
  <div class="image-item image-item--1-3 image-item--border">
    <img src="{{ book.img }}/patterns/empty-state-2.png">
  </div>
  <div class="image-item image-item--1-3 image-item--border">
    <img src="{{ book.img }}/patterns/empty-state-3.png">
  </div>
</div>

Some applications do this better than others. For example the first application gives the user a description on what to do in the application. However, the user can not click on an additional button that does the same as the + in the text. That is what the Facebook example does have. It gives the user two options: 1. install the application and 2. read more about it. The last example is something you want to prevent. It does not give the user any idea on how to get invites.

---

###### References
[^1]: Apple Inc. (Date unknown). Human Interface Guidelines. Consulted on 24-04-2018 from: https://developer.apple.com/ios/human-interface-guidelines/user-interaction/gestures/#standard-gestures
[^1]: Google. (Date unknown). Material Design Guidelines. Consulted on 24-04-2018 from: https://material.io/guidelines/components/lists-controls.html
