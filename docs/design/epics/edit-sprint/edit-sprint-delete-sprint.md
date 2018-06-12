#### ENS-208: edit-sprint-delete-sprint
**As a** user of the Enso application <br />
**I want** to delete a created sprint <br />
**So that I** can clean up my sprints or delete an incorrect one

###### Summary
A user should be able to remove sprints that are created in the application. The user should see this option when navigating from sprint-overview to edit sprint via the 'edit' button. The user should see a popup to confirm their action on delete. After deletion the user should be taken to the home screen. This functionality should be available offline. Screens should follow the new art direction of the Enso application.

###### Acceptance criteria
- User can navigate to edit-sprint screen from sprint-overview.
- User can click the 'delete sprint' button
- User gets shown a popup on clicking the button to confirm their action <br />
&nbsp;&nbsp;--**A**. User can click 'delete' <br />
&nbsp;&nbsp;--**B**. User can click 'cancel'
- **A**: The sprint is deleted and the user is taken to the home screen
- **B**: Popup closes, nothing happens
