# Design iterations 🔄
###### The design process I went through
---

### Introduction
I followed the same pattern to create a new UX design for all the screens in the application. I would look at design patterns that proofed to work in other applications, and applied them to my screens, sometimes changing some things a bit or combining two patterns on one screen.

I would make 2 or 3 options for each screen, and discuss with Alejandro Cruz Moreno, designer for Enso and Shell and has worked for many clients as a UX or UI designer. I would also show my designs to Lan Belic, who is a senior UX designer at MOBGEN. Lan has also worked at the Enso project and for the Shell apps and websites. They would give me feedback on my designs and helped me to come to a final solution that we could test. I chose not to test all the options I had to save some time in the design process, and to be able to spend more time on development, as development is my specialization.

### Create sprint flow
For these screens I created 3 options that might work. I looked at payment flow patterns of Zalando and other webshops, where the user has to be guided through a couple of steps. Option 1 was a long screen where all the necessary information could be filled in. Option 2 was a flow where the application itself tried to choose the correct values for the information itself, and the user could edit them later. The last option, option 3, was a wizard like flow, where the user was presented one input on every screen and had to actively press next to go to the next input.

#### Option 1
<div class="images-row group">
  <div class="image-item image-item--1-2 image-item--border">
    <img src="{{ book.img }}/design/create-sprint-single-screen.jpg" />
  </div>
</div>

#### Option 2
<div class="images-row group">
  <div class="image-item image-item--1-2 image-item--border">
    <img src="{{ book.img }}/design/create-sprint-default-add.jpg" />
  </div>
  <div class="image-item image-item--1-2 image-item--border">
    <img src="{{ book.img }}/design/create-sprint-default-edit.jpg" />
  </div>
</div>

#### Option 3
<div class="images-row group">
  <div class="image-item image-item--1-3 image-item--border">
    <img src="{{ book.img }}/design/create-sprint-wizard-v1-1.jpg" />
  </div>
  <div class="image-item image-item--1-3 image-item--border">
    <img src="{{ book.img }}/design/create-sprint-wizard-v1-2.jpg" />
  </div>
  <div class="image-item image-item--1-3 image-item--border">
    <img src="{{ book.img }}/design/create-sprint-wizard-v1-3.jpg" />
  </div>
  <div class="image-item image-item--1-3 image-item--border">
    <img src="{{ book.img }}/design/create-sprint-wizard-v1-4.jpg" />
  </div>
  <div class="image-item image-item--1-3 image-item--border">
    <img src="{{ book.img }}/design/create-sprint-wizard-v1-5.jpg" />
  </div>
</div>

After showing these screens to Alejandro and Lan we decided that the first or the third option were the best ones. The second option was not realistic because every design sprint is so specific in it's name, challenge and date that you could not expect the application to guess those values correctly. The first option was a good one, but compared to the third option we all preferred the wizard like flow. It forces the user to focus on a single input and prevents the mobile phone's keyboard to be over any of the inputs.

After we chose the wizard option, I got some feedback from the two designers. I made a new version where I changed the step indicator a bit, and the order of inputs. The template is now the third step in the flow, so we know the number of days the sprint is going to take, and we can display that on the datepicker screen.

Besides that I added a short description for every template option, so the user can read something about the template. Lastly I changed the number of participants to be 7 by default, as that is the suggested amount of participants in a design sprint.

#### Option 3 - iteration
<div class="images-row group">
  <div class="image-item image-item--1-3 image-item--border">
    <img src="{{ book.img }}/design/create-sprint-wizard-v2-1.png" />
  </div>
  <div class="image-item image-item--1-3 image-item--border">
    <img src="{{ book.img }}/design/create-sprint-wizard-v2-2.png" />
  </div>
  <div class="image-item image-item--1-3 image-item--border">
    <img src="{{ book.img }}/design/create-sprint-wizard-v2-3.png" />
  </div>
  <div class="image-item image-item--1-3 image-item--border">
    <img src="{{ book.img }}/design/create-sprint-wizard-v2-4.png" />
  </div>
  <div class="image-item image-item--1-3 image-item--border">
    <img src="{{ book.img }}/design/create-sprint-wizard-v2-5.png" />
  </div>
</div>


### Edit sprint flow
For these screens I looked at applications where the user can edit values. Examples for this are user accounts where you can edit your name, email or other information. Examples of this are Facebook, Twitter, Uber, Snapchat, Marktplaats and Instagram. I chose to follow the design pattern of Marktplaats and Instagram, where the user can edit a value by clicking on the input. After the click the keyboard will appear on the screen the user currently is at. The other examples had an extra navigational step, where the user is taken to the next screen after clicking on a value.

<div class="images-row group">
  <div class="image-item image-item--1-2 image-item--border">
    <img src="{{ book.img }}/design/edit-sprint.png" />
  </div>
  <div class="image-item image-item--1-2 image-item--border">
    <img src="{{ book.img }}/design/edit-sprint-day.png" />
  </div>
</div>

Lan and Alex found my option a good one, and agreed to put this flow in the UX prototype we were going to test. I did not make any other options beside a couple of iterations on this version, to speed up the design phase and make more time for development.

### Edit agenda flow
For the edit agenda flow, my screens are highly influenced by the iOS clock application. This application has a list of all the clock the user has on his or her phone. We have a similar list, but our list has all the events in it. The clock application gives the user a couple of functionalities. A user can add, remove, drag and edit clocks. We have those actions as well on this screen, as stated in the user story. On our screen we have one extra action, which is the mark as done.

This resulted in the following UX sketches:

<div class="images-row group">
  <div class="image-item image-item--1-3 image-item--border">
    <img src="{{ book.img }}/design/edit-agenda-default.png" />
  </div>
  <div class="image-item image-item--1-3 image-item--border">
    <img src="{{ book.img }}/design/edit-agenda-complete.png" />
  </div>
  <div class="image-item image-item--1-3 image-item--border">
    <img src="{{ book.img }}/design/edit-agenda-completed.png" />
  </div>
</div>
<div class="images-row group">
  <div class="image-item image-item--1-3 image-item--border">
    <img src="{{ book.img }}/design/edit-agenda-edit.png" />
  </div>
  <div class="image-item image-item--1-3 image-item--border">
    <img src="{{ book.img }}/design/edit-agenda-delete.png" />
  </div>
  <div class="image-item image-item--1-3 image-item--border">
    <img src="{{ book.img }}/design/edit-agenda-snackbar.png" />
  </div>
</div>
<div class="images-row group">
  <div class="image-item image-item--1-3 image-item--border">
    <img src="{{ book.img }}/design/edit-agenda-drag.png" />
  </div>
</div>

After clicking on add event the user is taken to a screen where he can select events, energisers or other events to add to the agenda. The user can click on any of the events, and the event will be added to the bottom of the agenda.

<div class="images-row group">
  <div class="image-item image-item--1-3 image-item--border">
    <img src="{{ book.img }}/design/edit-agenda-add-event.png" />
  </div>
  <div class="image-item image-item--1-3 image-item--border">
    <img src="{{ book.img }}/design/edit-agenda-add-energiser.png" />
  </div>
  <div class="image-item image-item--1-3 image-item--border">
    <img src="{{ book.img }}/design/edit-agenda-add-other.png" />
  </div>
</div>

As said I made a couple of options of the screens that had to get a UX design. When I had some things done I would discuss them with the two experts, Alejandro and Lan, and we would select a version of the screen we were going to put in the UX prototype we were going to test. Below is an example of how my sketch file looked like.

![Sketch file]({{ book.img }}/design/sketch-create-sprint-overview.png)
