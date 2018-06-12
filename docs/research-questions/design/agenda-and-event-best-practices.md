# Agenda and event best practices
###### Design research question
---

### 1.1 How do you give the user the ability to edit an existing agenda?
To find out how users of the application could edit the agenda in a user friendly way, I first started to think about which values should be editable for the users.

I came up with the following list:
- Mark event as done
- Remove event
- Reorder event
- Add event

After I made this list of values that should be editable, I looked into some [design patterns](../design/pattern-research/edit-agenda.md) that showed how other applications managed to do this. I reviewed these patterns, together with two designers that were already involved with the Enso application, Alejandro and Lan. They are both UX/UI designers at MOBGEN and mostly work on the Shell Drive application. Together with them I selected the best option to add to the UX prototype.

The patterns I looked into were:
- Edit mode
- Single item edit
- Mass edit

Together with the two experts, Alejandro and Lan, we decided to go for an edit mode that had to be activated by the user. I then made a couple of [iterations](../../design/design-process.md) of the preferred pattern that could work for the Enso application, and finally made a version of the pattern that I tested during the [UX user testing](../../design/ux-user-tests.md). After the user tests I had some feedback on the designs, that I implemented during the development.

During the development I also ran into some technical obstacles, that forced me to create something that might not always look 100% similar to the designs. This was because of time pressure and restrictions of React Native and my React Native knowledge.

See the [UX prototype](../../design/ux-prototype.md) to see how the designs ended up being.

### 1.2 How do you give the user the ability to edit an existing sprint or event?
Editing sprint values and event values are quite similar to each other. For consistency I wanted to use the same pattern for these two functionalities. I used the iOS pattern that Apple uses to give their users the ability to edit values. In the UX tests the participants could easily find this edit button, and were fermilliar with it.

The user should be able to edit the following sprint values:
- Name
- Challenge
- Template
- Dates
- Participants
- Sprint day title
- Sprint day start time

For event I the user should be able to edit the following values
- Equipment
- Tips
- Duration

For this release I decided not to give the users the ability to edit the events title or description. This was to speed up the development process a bit. In a future release the user should be able to edit these values and configure the sprint even more.

I looked at how other applications enabled their users to edit values, for example user name or email values. This can be found in the [edit-sprint](../../design/pattern-research/edit-sprint) section, and selected three patterns:

- WYSIWYG editor
- Single screen form
- Inplace editor

I asked the help of the two experts again, and thought about the situation this feature will be used in, which is before or during a design sprint. The editting had to be fast, but it was also important that no accidental edit happened. We decided to add the single screen form to the UX prototype so we could test that.

With this solution it is very clear to the users which values can be editted and it is hard to make accidental edits. The user has to actively go to a different page and click on a save button to change values. While it is hard to accidentally change a value, participants of the [UX user tests](../../design/ux-user-tests.md) could still quickly edit a value if they wanted to.

See the [UX prototype](../../design/ux-prototype.md) to see how the designs ended up being.
