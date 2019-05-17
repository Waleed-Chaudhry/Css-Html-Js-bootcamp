# Bootstrap

### Introduction
* Just a single css and html file you can plug in 
* You get a bunch of stuff for free like buttons, forms and navbars which are mobile friendly
* App using bootstrap: https://expo.getbootstrap.com/

### Installation 
* Download the zip from: https://blog.getbootstrap.com/2015/06/15/bootstrap-3-3-5-released/
* Grab bootstrap.css from dist/css and put it into your project folder
* Link the css file to your html like you would link any other css file
* Can also link the .css file without downloading using:  
  ```<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css">```
* Dcoumentation at: https://getbootstrap.com/docs/3.3/css/

### Buttons, Forms and Inputs
* Added buttons with different options, sizes and active state, and disabled state
  * Added button with link attached
  * Can override bootstrap button style
* Added a jumbotron
  * It's a component
  * https://getbootstrap.com/docs/3.3/components/#jumbotron
* Added regular forms and inline forms
* Added a container around the whole thing to get better left and right margins

### Navigation Bar
* They scale upon resizing, and on tablet/mobile view
* Added headers and buttons
* Place the container inside the navbar to make content inside the navbar aligned
* Need to add js and jQuery to make the default nav bar button work
```
<script src="https://code.jquery.com/jquery-2.1.4.js"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/js/bootstrap.min.js"></script>
```
* Select which content to hide and be accessible from the hamburger button when you resize horizontally

### Grid System
* Have elements size by side, and then stack on tablet and mobile view
* https://getbootstrap.com/docs/3.3/css/#grid
* Every container can be divided into 12 columns
  * Using the grid system we can pick how many of those 12 units can a given element take
  * To show 4 items in a row, you have each item take up 3 units
* Grid should always be inside a container
* Can specifiy how many units to use for each of the 4 views - large(monitor), medium (laptop), small (tablet), xs (mobile)
* Can nest columns within columns
  * Remember to add a row inside a column and then split that child row to add more columns

### Image Gallery
* Copied over Nav bar from the grid system
* Images are inside class thumbnail to scale them down and give them a border
  * Don't have to create columns inside rows since thumbnails automatically wrap
* Gliphicons to add icons
  * https://getbootstrap.com/docs/3.3/components/#glyphicons
  * Grab the name of the icon you want
  * ```<span class="glyphicon glyphicon-search" aria-hidden="true"></span>```
  * Can add a space after the span closes to add padding after the icon
  * Also added the icon to the nav bar
* Made the nav bar fixed to the top when scrolling vertically
* Add the 70px padding to the top of the body to restore the space above the jumpbotron
* Used fontawsome icon/font library
  * Grab the html link from https://fontawesome.com/start
* Customized the colors and backgrounds on the jumbotron
  * The icon within the jumbotron is treated as text when it comes to coloring
  * .navbar-inverse a tag is needed to change the color of the links on the nav bar
    * Simply using a tag isn't specific enough and gets overriden by specificity
    * Grab the more specific tag from the chrome inspector
 * Add the custom file/font awesome style after the bootstrap in the HTML to override bootstrap styles
