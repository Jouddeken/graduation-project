#### set-sprint-navigation
**As a** user of the Enso application <br />
**I want** to navigate in the create sprint flow <br />
**So that I** can create my sprints but also go back to adjust a value

###### Summary
The user should be able to navigate smoothly between the pages of the create-sprint flow. It should be possible to edit a value halfway through the flow, by going back to that screen using a back button in the header. The flow should be possible to start from anywhere in the app by using the center button in the tab bar, except when a user is in a sprint because then there is no tab bar. When the flow is finished, that is when the user clicks on the create sprint button in the bottom of the create-sprint-participants screen, the user should be taken to the newly created sprint.

###### Acceptance criteria
- On iOS and Android the navigator should be identical
- On Android the back button should navigate a screen back
- On iOS swiping from left to right should navigate a screen back
- The user should be able to go back one screen at any point of the flow
- The user should be able to skip the create-sprint-challenge and the create-sprint-participants steps

---
