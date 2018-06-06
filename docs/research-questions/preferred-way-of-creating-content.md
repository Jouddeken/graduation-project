# Preferred way of creating content on mobile applications
###### Design research question
---
The creation of content in the Enso application is creating new design sprints. I did research to this with the pattern research and found a nice way of letting the users create new content in the application. I went for the wizard option where the user has structured format inputs that help the user to understand what values should be filled in.

### What are best practices around requesting values from a user in a mobile application?
I looked at the following patterns for the creation of a new sprint on a mobile application. To see the detailed pattern description go to the [ create sprint pattern research section](../design/pattern-research/create-sprint.md).

I looked at three patterns that could be applied when creating a sprint in the application:

- Good defaults
- Wizard
- Structured format

In the end I combined the wizard with the structured format to make a create-sprint flow where the user focusses on one input at the time, with the least amount of steps needed to be taken.

### What information is needed to create a sprint and how do you visually request this from the user?
Together with the facilitators at MOBGEN and the Product owner of Enso, Yoav, we made a list of the information that was needed to create a sprint. The list of values we needed was:

| Value | Required |
| :-- | :-- |
| Name | Yes |
| Challenge | No |
| Template | Yes |
| Dates | Yes |
| Participants | No |

We needed the name to quickly show the difference between two sprints for the user of the application. The name would also be displayed big on the overview screen where the user can select a sprint, this value is required in the create sprint flow. The challenge is something for the user, to further specify what the sprint is about. What is the goal of the sprint. We had to know which template the user wants to use for this sprint, so that one is required as well. We also ask the user to select the dates the design sprint will be ran, to order the design sprints chronologically, this value is also required. Lastly we ask the user the number of participants, which we will use to display equipment values for an event and specific tips. For example how big the room should be for an exercise.

With the wizard we could request this information screen by screen from the user, as described in the [create sprint pattern research section](../design/pattern-research/create-sprint.md).
