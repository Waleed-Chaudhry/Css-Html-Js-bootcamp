# JavaScript


### Introduction
* Can write JavaScript code on the Chrome Inspector
* Primitives: Numbers, String, booleans, null/undefined
  * Undefined: Delcared but never initialized
  * null: Explicity nothing, assign null to a variable, not undefined
* Methods: 
  * alert("hello world") to display a popup box
  * clear() to clear the console
  * console.log()
  * var name = prompt("What is your name?) to get an input from the user in a popup and store it to the var name
    * Chrome doesn't display the HTML on the page until after the popup has been closed
* To run a js script through an html:
  ```
  <head>
    <title>JS Stalker</title>
    <script type="text/javascript" src="script.js"></script>
  </head>
  ```
    * The script should come after the body so that it runs after the html executes
 
### Control Flow
* Logical operators
  * Use === for comparison
  ```javascript
  var x = 99
  console.log(x == "99") // true == performs type coercion
  console.log(x === "99") // false
  ```
  * && -> And, || -> Or, ! -> Not (All 3 are logical operators)
* Comparison
  ```javascript
  if (a > b) {
    // code here
  } else if {
    // more code
  } else {
    // else condition code
  }
  ```
* Loops
  ```javascript
  // While loop
  while (a>b) {
    // code here
  }
  
  // For loop
  for (var i = 0; i < cars.length; i++)
    // code here
  }
  ```
 
 ### Functions
 * Variables aren't type checked
   ```javascript
   function square (num) {
     console.log(num * num)
   }
   ```
* If you assign var square = 5 later in the code, the function will be overwritten
* Variable Scoping
  * var num defined outside a function in available on the whole file
  * var num defined inside a function is only available within that function
* Functions can be passed as arguments to a function as well
  ```javascript
  function sing (num) { console.log('twinkle') }
  setInterval(sing, 1000)
  
  // Can replace sing in setInterval with the function definition aka an anonymous function
  setInterval(function sing (num) { console.log('twinkle') }, 1000)
  ```

### Arrays
```javascript
var array1 = [] // can be initialized as empty
var array2 = [1, 'sample', true, 'text'] // same array can have any type of data
console.log(array1.length) // 0 .length is available for strings too
console.log(array2.pop()) // last item, text
array2.push('new data') // appends to the append of the array
console.log(array2) // [ 1, true, 'new data' ]
array2.unshift('start') // append at head
console.log(array2.shift()) // remove the head (start)
var array3 = array2.splice(1, 3)
console.log(array2) // [1] original array is left with the non spliced range
// slice doesn't modify the original array, and end in non inclusive
console.log(array3) // ['sample', true, 'new data' ], both indices inclusive
console.log(array3.indexOf('sample')) // 0, -1 if not present
array3.forEach(function (item) {
  console.log(item)
})
```

### Objects
```javascript
var person = {
  firstName: 'John',
  lastName: 'Doe',
  age: 50,
  eyeColor: 'blue',
  add: function (x, y) { // function within an object
    // Can use this to define multuple functions named speak within the same class
    // While avoiding namespace collisions
    return x + y
  }
}

console.log(person['lastName']) // to retrive key
// person.lastName also works as long as key doesn't start with a number
person.lastName = 'Nash' // to update the key
console.log(person.add(10, 5)) // 15
```
