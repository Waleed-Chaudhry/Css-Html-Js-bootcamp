# Intermediate CSS

### Fonts
* Set any font from https://www.cssfontstack.com/
* Changed font size (absolute: px, and relative: em)
* Changed font weight (bold), vertical spacing, alignment and decoration (underline, line-through) 
* Can also pick fronts from https://fonts.google.com/
  * Need to link the font in the html
  * And then use the font in the css

### Box Model
* Positioning of elements 
* Every element has a box around it (that's the highlight you see when you try in inspect in Chrome)
* Added border
  * border, width and height (absolute and relative)
  * ```border-bottom: 2px solid #f1f1f1;``` to only get the bottom border
* Added padding
  * Between element and border
  * All sides by default, or a given side only
* Margin 
  * Space between elements (space between images)
  * top, right, bottom, left

### Tic Tac Toe
* Board is a table element with 3 <tr> and 3 <td> within each row to create the 9 boxes
* Need to give td a height, width and background via css to get it to show up
* Create a vertical and horizontal class for the boxes
  * Can give vertical and horizontal class for the same box (the middle box in the middle row)
* Can center align the table using ```	table {margin: auto;}```
* Add a hover to each box

### Gallery Application
* Add all the image sources to the html
* Use float: left to make all the images be continuous
* Calculate width of an image (need 3 images per row, so 30%)
* Use the remainder to calculate the margins
  * Need 6 margins in total per row. 10% left after the images. So 10/6 = 1.66% 

### CSS Blog
* Keep the width at 700px and then start shrinking down ```max-width: 700px;``` 
* Vertical line around the quote is simply just a left border
* Adding horizontal spaces between letters: ```letter-spacing: 0.2rem;```
  * rem is set by the root element, without regards to parent element like em
* ```<hr>``` to add a horizontal line between the two blog posts
