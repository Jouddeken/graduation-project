# edit-sprint
###### Design pattern

### Introduction
A created sprint has the following values:

| Value | Editable |
| :-- | :-- |
| Name | Yes |
| Challenge | Yes |
| Template | No |
| Dates | Yes |
| Participants | Yes |

As stated in the table all the values except the template are editable for the user of the application. The user should be able to edit these values when clicking on an 'edit' button when on the sprint overview screen.

### Option 1 &mdash; [WYSIWYG editor](http://ui-patterns.com/patterns/WYSIWYG) [^1]
An option for editing the sprint values could be a **W**hat **Y**ou **S**ee **I**s **W**hat **Y**ou **G**et editor. The WYSIWYG pattern is most of the time used for desktop applications, where there is more space on the screen and you don't have to display a keyboard on the screen.

![WYSIWYG editor]({{ book.img }}/patterns/wysiwyg.png)

This pattern is really nice for writing documents, or getting long text data input from a user. But the task we are trying to complete in the Enso application is getting short values from the user. The patterns in mainly focussed on desktop as well.

### Option 2 &mdash; Single screen form
Another option is to put every value the user can change on one screen. This would give the user a good overview of which values can be changed, and you can categorize some values as well. This pattern is often seen in account settings, as seen in the two examples below.

<div class="images-row group">
  <div class="image-item image-item--1-2 image-item--border">
    <img src="{{ book.img }}/patterns/marktplaats-1.png">
  </div>
  <div class="image-item image-item--1-2 image-item--border">
    <img src="{{ book.img }}/patterns/instagram-1.png">
  </div>
</div>

What would happen when a user clicks on any of the values, the keyboard show up, and the user can edit the value.

### Option 3 &mdash; [Inplace editor](http://ui-patterns.com/patterns/InplaceEditor) [^2]
The third option I thought of was the inplace editor. This means that a user can click on a value when it is displayed in the application. We could use this pattern on mobile when the user long presses on the title of the sprint, a keyboard shows up and he or she can edit the sprint title. Yet, with the lack of space on mobile screens, this might not be the best solution.

<div class="images-row group">
  <div class="image-item image-item--border">
    <img src="http://ui-patterns.com/uploads/image/file/225/best_old_17.jpg">
  </div>
</div>

Above is an example of an inplace editor. The user can click on a value and that value becomes editable on the spot. We could use this option with a long press on mobile. When the user long-presses on an editable value the keyboard shows up and the user can edit the value. Downside of this pattern is that it might not be totally clear what is editable and what is not.

### Conclusion
Comparing these three options I chose to add the second one, single screen form,  to the UX prototype that I was going to test. I went for that option because in the application we do not have long texts that have to be editted, and we only have a couple of values that need to be edittable. This option also gives the user a nice overview of all the values that can be editted, and the user can scroll through the options without having to guess if they can edit it or not.

### References
[^1]: Author unknown. (Date unknown). WYSIWYG Design Pattern. Consulted on 28-04-2018 from: http://ui-patterns.com/patterns/WYSIWYG
[^2]: Author unknown. (Date unknown). Inplace Editor Design Pattern. Consulted on 28-04-2018 from: http://ui-patterns.com/patterns/InplaceEditor
