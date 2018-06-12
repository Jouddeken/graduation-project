#### ENS-105: create-sprint-participants
**As a** user of the Enso application <br />
**I want** to set a number of participants in my sprint <br />
**So that I** can adjust my planning/durations and equipment based on that

###### Summary
A user of the Enso application should be able to set the number of participants in a sprint they want to create. This step (along with all the steps in the create sprint flow) should be possible to do offline. The default value of the number of participants should be 7, the user can add or subtract participants from that number. A description underneath the number should give the user an explanation why the number defaults to 7: it is the preferred number of participants in a sprint. Screens should follow the new art direction of the Enso application.

###### Acceptance criteria
- User can navigate to the create-sprint-participants screen from the create-sprint-start-date screen
- Default participants value should be 7
- User can add (+1) a participant
- User can subtract (-1) a participant
- User can see the current progress in steps of the sprint creation flow
- User should be able to skip this step by clicking on 'skip'
- By clicking the enter button at the bottom of the screen, the user should be taken to their newly created sprint, as this is the last step in the process.
- The keyboard should automatically be activated when entering this screen
