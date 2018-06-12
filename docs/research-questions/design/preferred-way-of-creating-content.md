# What is the preferred way of creating a new sprint on a mobile application?
###### Design research question
---

The new feature I had to wireframe was one where the user could configure their own sprints. I needed to know some values from the user to create a new sprint. I also needed the user to be focussed on a single task, and make the flow as quickly as possible while still remaining being focussed on a single task.

I had to find out what these values were and what the best practices were around requesting these values from the user.

### 2.1 What information is needed to create a sprint and how do you visually request this from the user?
Together with the facilitators at MOBGEN, the designers, Lan and Alejandro and the Product owner of Enso, Yoav, we made a list of the information that was needed to create a sprint. The list of values we needed was:

| Value | Required |
| :-- | :-- |
| Name | Yes |
| Challenge | No |
| Template | Yes |
| Dates | Yes |
| Participants | No |

We needed the name to quickly show the difference between two sprints for the user of the application. The name would also be displayed big on the overview screen where the user can select a sprint, this value is required in the create sprint flow.

The challenge is something for the user, to further specify what the sprint is about. What is the goal of the sprint.

We had to know which template the user wants to use for this sprint, so that one is required as well.

We also ask the user to select the dates the design sprint will be ran, to order the design sprints chronologically, this value is also required.

Lastly we ask the user the number of participants, which could be used to display equipment values for an event and specific tips. For example how big the room should be for an exercise.

To visually request this information from the user I used a wizard. With the wizard we could request this information screen by screen, as described in the [create sprint pattern](../../design/pattern-research/create-sprint.md) research section. I also used the structured format pattern to make it easier for the user to understand what values had to be filled in. For example: showing a calendar when requesting a date value. This solution forced the user to focus on one task at the time when creating a sprint.

See the [UX prototype](../../design/ux-prototype.md) to see how the designs ended up being.

### 2.2 What are best practices around requesting values from a user in a mobile application?
I looked at the following patterns for the creation of a new sprint on a mobile application. To see the detailed pattern description go to the [ create sprint pattern](../../design/pattern-research/create-sprint.md) research section.

I looked at three patterns that could be applied when creating a sprint in the application:

- Good defaults
- Wizard
- Structured format

In the end I combined the wizard with the structured format to make a create-sprint flow where the user focusses on one input at the time, with the least amount of steps needed to be taken. This solution was [tested](../../design/ux-user-tests.md) with multiple people at MOBGEN, and overall they were enthusiastic about it and how it worked. Most of them thought it was very intuitive and clear what was expected from them.

After the user tests I had some feedback on the designs. I tried to apply the feedback to the designs during development, to speed up the process, and to spend more time on development. This means that the UX prototype can differ a bit from the actual iOS or Android prototype.

I also ran into some restrictions with React Native during the development, or had to solve things a bit differently due to time pressure. You can download the prototype via the [Prototype](../../technical/prototype.md) page.

See the [UX prototype](../../design/ux-prototype.md) to see how the designs ended up being.
