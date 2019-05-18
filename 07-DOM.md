# DOM

### Introduction
* Interface between JS and HTML + CSS
* Interactivity, Games, Scroll effects, Form validations, animations
* Browser models each HTML tag into an a javascript object inside the document parent object

### Select Elements
* We select HTML tags using JavaScipt code, and then manipulate
* Open the Chrome inspector and type document to access the document
```javascript
// All methods are called on the document object
document.getElementById("id") // html tag id
document.getElementsByClass("class) //list because you can have multiple elements with the same class
document.getElementsByTagName("li") //list of all elements that have the tag name "li"
document.querySelector("#highlight") //Takes a CSS-style selector to return the object
// Always returns just the first element that matches
document.querySelectorAll("#highlight") //list of elements containing all the matches
```
  
### Manipulating Style
* Define a new class on the css file
``` 
.big {
  font-size: 100px
}
```
* Paragraph is: ```<p>Corgi mixes are <strong>super</strong> adorable</p>```
* Select paragraph in the Inspector console: 
  * ```javascript var p = document.querySelector("p")```
  * Will show up as undefined in the console, but you can type p in the next line to check its contents
* Manipulate its style by adding the style class to its stylelist
  * ```javascript p.classList.add("big") ```
  * ```javascript p.classList.remove("big") ```
  * ```javascript p.classList.toggle("big") ```

### Manipulating Text Content
```javascript
javascript var p = document.querySelector("p")
p.textContent // Corgi mixes are super adorable
p.textContent = "dummy text" // will throw away the inner strong tag
p.innerHTML = "dummy text" // will also throw away inner HTML tags
// Can use either of the two if there are no inner html tags
document.body.innerHTML = "<h1>GoodBye<h1>" // Will set the html
// innerText will just treat h1 tag as text
```

### Manipulating Attributes
```	<img src="https://barrelhorseworld.com/dogs/images/1145556d.jpg">```
```javascript
var img = document.getElementsByTagName("img")[0]
img.getAttribute("src") //"https://barrelhorseworld.com/dogs/images/1145556d.jpg"
img.setAttribute("src", "https://www.google.com/images/branding/googlelogo/2x/googlelogo_color_272x92dp.png")
// can also setAttribute on href
```

### Playing with Google Code Along
```javascript
// Manipulating multiple elements at the same time inside Chrome Inspector Console
var links = document.getElementsByTagName("a")
for (var i = 0; i < links.length; i++) {
  links[i].style.background = "pink";
  links[i].style.border = "1px dashed purple";
  links[i].setAttribute("href", "http://www.bing.com");
}
```

### Events
* Clicking, pressing a key, hovering, dragging and dropping
* Select an element and then add an event listener it
  * The type of event e.g. a click, change of a text value (scorekeeper)
  * The function to run when the event occurs - can be a named function or an anonymous function
* Can have more than one listener on a given element
* Generally a good idea to give all your html elements an id
* Event listners covered in TODO: 
  * mouse over
  * mouse out
