# ENS-400: edit-event
###### Epic
---
### Description
Make users able to edit certain info of events in the templates. This means the user can change the following:

- Edit the event's duration (edit-event-duration)
- Edit the event's tips (edit-event-tips)
- Edit the event's equipment (edit-event-equipment)
- Edit the event's visual (edit-event-visual)

### Problem
In the current version of the Enso application it is not possible to edit anything in the application, so editing events is also not possible. In the new version the user can create sprints and agendas that contain events. Some of this data should be editable.

### High level proposal
The new feature should be implemented using the new Enso art direction.

### Value to users
Users are able to edit some details of the events to make them suit their needs.

### Value to MOBGEN
Making users able to edit the events is essential for a good user experience. We want to give the user the possibility to create their own sprints and also edit the events in those sprints. This will make the app look professional and well thought through.

### User stories
{% include "./edit-event-duration.md" %}
{% include "./edit-event-tips.md" %}
{% include "./edit-event-equipment.md" %}
{% include "./edit-event-visual.md" %}