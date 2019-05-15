### Introduction

* Cascading Style Sheets
* http://www.mezzoblue.com/zengarden/alldesigns/
* General Rule: We use a selector for an html element, and change its property
  ```
  selector {
    property: value;
    otherpropert: othervalue:
  }
  ```
* Create a seperate .css file, link it to an HTML and use it to style the HTML
 
 ### Using Colors
 
* Can use color names like red, do a HEX value of the color, and or a rgb value
  * Can use a color picker online and grab the HEX value from there
  * There is also an rgba -> alpha (transparency which ranges from 0.0 to 1.0)

### Background and border
* Added background color to a tag or the whole body
* Added background images
* Added Borders
* Added text decorations
* Can add font size ```font-size: 25px;``` and left margins ```margin-left: 50px;```

### CSS Selectors
* How we've been selecting html elements from .css file
* Element Selector: All instances of a given element
* ID Selector: Just the given element
* Class Selector: Assign the same formatting to multiple elements

### Chrome Inspector
* Right click -> Inspect
* Elements shows an interactive html view
* Styles shows the CSS
  * Can unchcked styles to remove them
  * Can click the color to open up the color picker

### Advanced CSS Selectors
* Star -> selects every element on the page
* Descendent Selectors -> all elements with a given selector within a parent selector
  * Can do something like ul p or ul .class
  * Can have more than two elements in the chain
* Adjacent Selectors -> All elements that immediately follow the parent selector
* All elements with a given attribute 
  * e.g. all anchors with a given url
  * all checkboxes ```input[type="checkbox"]```
  * all inputs with type text ```input[type="text"]```
* nth of type 
  * e.g. select all 3rd li element inside each group of li elements
  * Can also select all even elements inside each group ```li:nth-of-type(even)```

### Specificity and Cascade
* Child inherits parent's style e.g. styling body changes the entire file
* Child can override the style set up parent by simply setting it again
* Styles in Chrome Inspector shows you Inherited from
* Specificity: How CSS decides which style to apply to an element if it is being targeted by multiple styles
  * e.g. child styling is more specific than the parent one
  * an li is more specific than ui, which in turn is more specific than body
* Specificity hierarchy: (lowest to highest)
  * Type selectors: Adjacent and Descendant (Spec: 2) followed by Element (Spec: 1)
  * Class, Attribute and Pseudo selectors (Spec: 10)
  * ID Selector (Spec: 100)

### Other selectors and styles:
  * Select all "checked" checkboxes ```input:checked```
  * Make upper case: ```text-transform: uppercase```
  * Select first letter of a given id ```#id:first-letter```
  * Change properties upon hovering over h1 ```h1:hover {color: blue;}```
  * Make all visited links blue ```a:visited {color:gray;}```
