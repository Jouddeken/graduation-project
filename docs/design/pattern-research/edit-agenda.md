# edit-agenda
###### Design pattern

### Introduction
A sprint agenda is a collection of events that are going to be done during the selected day of the design sprint. The events are in a list in the current version of the Enso application, and that list worked good. With the next release we are adding some features to this list, most of them are edit features.

The features we were going to add to the existing agenda events list are:
- Mark event as done
- Remove event
- Reorder event
- Add event

### Option 1 &mdash; Edit mode
The first pattern I looked at was the pattern that is used in the iOS clock application. In this application they have a list of clocks that display the time around the world. These clocks could be the events in the case of the Enso application. The user has an edit and add button. In the case of the clock application they are placed in the top of the screen. With the edit button the user 'activates' the edit-mode. The red delete icon and the three horizontal lines appear on every item, to indicate a delete and reorder action.

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

After clicking on the red delete button the item moves to the left to reveal the actual delete button. This forces the user to do at least two actions, and prevents accidental deletion of items (clocks). When clicking on the three horizontal drag lines the item turns slightly transparant and the user can drag the item around the screen. When clicking the plus, the user is taken to another screen where he or she can select a new clock to add to the list.

### Option 2 &mdash; Single item edit
Another option I looked at was single edit mode. In this mode the user can edit a single item at any given point in time, without having to enable an edit mode. This pattern is found in the messages application on iOS devices. The user sees a list of messages and can swipe from right to left to reveal options. There is an 'edit' button that activates a similar edit mode as described in the pattern above.

<div class="images-row group">
  <div class="image-item image-item--1-2 image-item--border">
    <img src="{{ book.img }}/patterns/single-edit-1.jpeg">
  </div>
  <div class="image-item image-item--1-2 image-item--border">
    <img src="{{ book.img }}/patterns/single-edit-2.jpeg">
  </div>
</div>

This option is probably faster compared to the first option when the user wants to edit a single item, but when there are more than two option for the user, the menu that slides out might get cluttered with too many options.

### Option 3 &mdash; Mass edit
The third option I looked at was mass edit mode, where the user can edit many items at once. This pattern also has an edit mode, that activates the checkboxes on the left side of the items. The user can select the items he or she wants to do something with, and with the bar in the bottom of the screen perform an action on them. With this option the user can delete or move multiple items at once, which is faster than doing it one by one for every item.

<div class="images-row group">
  <div class="image-item image-item--1-3 image-item--border">
    <img src="{{ book.img }}/patterns/mass-edit-1.jpeg">
  </div>
  <div class="image-item image-item--1-3 image-item--border">
    <img src="{{ book.img }}/patterns/mass-edit-2.jpeg">
  </div>
  <div class="image-item image-item--1-3 image-item--border">
    <img src="{{ book.img }}/patterns/mass-edit-3.jpeg">
  </div>
</div>

### Conclusion
After reviewing the options above I chose the first option to be added to the UX prototype to be tested. This was because it offered the possibility to add events with an add button, and enabling the edit mode with a button. When the user was in the edit mode he or she could drag the events around with the drag handles on the right, and remove the item with the delete button on the left. I also had to add a function where the user could mark an event as done, that could be done by swiping from left to right on an item.

The single item edit would be too cluttered with options with three functionalities in the swipeout menu: mark as done, delete and drag. And the mass edit option would be a nice feature to add later in the project. For the first version it was enough to delete events one at the time. This decision would also speed up the development phase.
