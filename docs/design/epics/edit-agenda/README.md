# edit-agenda
###### Epic
---
### Description
Make users able to edit the sprint agenda of the sprint they created. This means the user can do the following:

1. Edit the order of events in the agenda (edit-agenda-change-order)
2. Mark events as complete (edit-agenda-mark-completed)
3. Remove an agenda event (edit-agenda-remove-event)
4. Add an event or energiser (edit-agenda-add-event)

### Problem
In the current version of the Enso application you can not make your own sprints, and thus it is also not possible to edit the agenda. In the new version the user can create their own agendas, the user should be able to edit those.

### High level proposal
The new feature should be implemented using the new Enso art direction.

### Value to users
Users are able to edit their agendas.

### Value to MOBGEN
Making users able to edit the agenda is essential for a good user experience. We want to give the user the possibility to create their own sprints and also edit their agendas. This will make the app look professional and well thought through.

### User stories
{% include "./edit-agenda-change-order.md" %}
{% include "./edit-agenda-mark-completed.md" %}
{% include "./edit-agenda-remove-event.md" %}
{% include "./edit-agenda-add-event.md" %}
