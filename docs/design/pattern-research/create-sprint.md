# create-sprint
###### Design pattern

### Introduction
For the creation of the sprint, we need data from the user. This data needs to be in a specific format. Beforehand we sat down with the Enso team, and thought about which data we needed from the user. We ended up with the following list:

| Value | Required |
| :-- | :-- |
| Name | Yes |
| Challenge | No |
| Template | Yes |
| Dates | Yes |
| Participants | No |

The challenge and participants are values that are not required, but the facilitators mentioned that they would like to see this feature in the concept phase. They wanted to use the challenge as a description for the sprint, or maybe just put the name of the client there. Participants would default to a value of 7, which is the preferred number of participants in a design sprint according to Tim Höfer, product designer at AJ&Smart, who has done over 100 of design sprints.[^1]

### Option 1 &mdash; [Good defaults](http://ui-patterns.com/patterns/GoodDefaults) [^2]
The first option I thought of was a good default option. In this case the application would guess what values you want to fill in for the screen.

![Skyscanner good defaults](https://cdn-images-1.medium.com/max/1600/1*1MQ_ludtPo5spcjVbO6hnw.png)

The above image comes from the skyscanner website. The site automatically selects a return ticket, requests your location to put the nearest airport as your 'from' location, sets the return and depart dates on today and tomorrow and selects a ticket for 1 adult. This helps the user to minimize the values he or she has to fill in.

### Option 2 &mdash; [Wizard](http://ui-patterns.com/patterns/Wizard) [^3]
Lastly I thought about creating a wizard for the flow. According to wikipedia a wizard is: "A software wizard or setup assistant is a user interface type that presents a user with a sequence of dialog boxes that lead the user through a series of well-defined steps." [^4]

The most well known example of a wizard are the installation wizards you get when installing new programs on your computer.

![Install wizard](http://kb.mozillazine.org/images/Fx3SetupWizard_SetupType.png)

These wizard guide the user through the process by asking questions to the user. Most of the times the wizards have default values the user can use to install or setup the program.

### Option 3 &mdash; [Structured format](http://ui-patterns.com/patterns/StructuredFormat) [^5]
The second option was a structured format option, that is also frequently used in payment applications and webshops. This pattern is most of the times really similar to the wizard pattern. The difference between the wizard and this pattern is that in this pattern the user is given a structure where he or she can fill in the data. For example a calendar date picker, or dropdowns. The example below comes from the zalando iOS application.

<div class="images-row group">
  <div class="image-item image-item--1-2 image-item--border">
    <img src="{{ book.img }}/patterns/zalando-1.png">
  </div>
  <div class="image-item image-item--1-2 image-item--border">
    <img src="{{ book.img }}/patterns/zalando-2.png">
  </div>
  <div class="image-item image-item--1-2 image-item--border">
    <img src="{{ book.img }}/patterns/zalando-4.png">
  </div>
  <div class="image-item image-item--1-2 image-item--border">
    <img src="{{ book.img }}/patterns/zalando-5.png">
  </div>
</div>

The structured format gives the user a clear view of how many steps there are still to be taken, and what these steps are. It also gives the user a 'structure' to use when filling in the data.

### Conclusion
The smart defaults option sounds like a good solution for getting the data we need, but after talking with the facilitators and designers at MOBGEN they explained that this might not be the best decision. The name, challenge and dates of the design sprints are so specific for each sprint, that the application cannot guess them correctly.

The wizard might be a better solution because it forces the user to focus on a specific part of the process. Combined with the structured data pattern, that is also a sort of wizard, it might be a good solution to get the data we need.

In the end the structured data pattern is the preferred option for our problem, and would give the user the best guidance when entering the information. Downside of this pattern is that there are a lot of navigational changes when filling in the information.

### References
[^1]: Höfer, T. (2018, March 15th). All You Need to Run a Design Sprint. Consulted on 28-04-2018 from: https://blog.ajsmart.com/all-you-need-to-run-a-design-sprint-6bfe7ff68963
[^2]: Author unknown. (Date unknown). Good Defaults Design Pattern. Consulted on 28-04-2018 from: http://ui-patterns.com/patterns/GoodDefaults
[^3]: Author unknown. (Date unknown). Wizard Design Pattern. Consulted on 28-04-2018 from: http://ui-patterns.com/patterns/Wizard
[^4]: Author unknown. (2018, March 17th). Wizard (software). Consulted on 28-04-2018 from: https://en.wikipedia.org/wiki/Wizard_(software)
[^5]: Author unknown. (Date unknown). Structured Format Design Pattern. Consulted on 28-04-2018 from: http://ui-patterns.com/patterns/StructuredFormat
