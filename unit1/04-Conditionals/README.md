# 4. Conditionals

  - [if / else](#if--else)
  - [if / else if / else](#if--else-if--else)
  - [Comparison Operators](#comparison-operators)
  - [Logical Operators](#logical-operators)
  - [Booleans](#booleans)
    - [mouseIsPressed](#mouseispressed)
  - [keyPressed()](#keypressed)
  - [Resources](#resources)
---

## if / else

Conditional statements are used to give our programs logical flow. 

```javascript
if ( /* some condition */ ) {
    // execute if true
}
else {
    // execute if condition isn't true
}
```

As an example, we can use conditionals to make an ellipse blue if the mouse is on the left half of the canvas, and red if it's on the right side of the canvas:

```JavaScript
function setup() {
    createCanvas(400, 400);
}

function draw() {

   if (mouseX < width/2) {
      fill(0, 0, 255);
   }
   else {
      fill (255, 0, 0);
   }

   ellipse(width/2, height/2, 100, 100);
}
```

## if / else if / else

The if / else if / else structure can be used to test multiple conditions. The format is:

```javascript
if ( /* condition */ ) {
   // code to execute
}
else if ( /* condition */ ) {
   // code to execute
}
// infinite number of else ifs ...
else {
   // code to execute
}
```

For example, we might print different statements based on a person's age: 

```javascript
let age = 10;
if (age < 3) {
  console.log("baby");
}
else if (age < 18) {
  console.log("youth");
}
else if (age < 65) {
  console.log("adult");
}
else {
  console.log("senior");
}
```

## Comparison Operators

When determing whether an expression inside a conditional is true or false, we can use a variety of comparison operators:

* `<` (less than)
* `>` (greater than)
* `<=` (less than or equal to)
* `>=` (greater than or equal to)

To determine if quantities are equal or not:
* `===` returns true if values and data types are the same
* `==`  returns true if values are the same
* `!=`  returns true if values are not equal
* `!==` returns true if values are not equal or if data types are not the same

```javascript
'5' == 5    // true
'5' === 5   // false
'5' != 4    // true
'5' !== 5   // true
5 !== 5     // false
```

## Logical Operators
We can use logical operators to make compound conditional statements.
* &&    (and)
* ||    (or)
* !     (not)

For example, we can use the logical "&&" operator to test if x is between -5 **AND** 5:

```JavaScript
// from JavaScript Basics (see link above)
let x = 1;
if (x > -5 && x < 5) {
  // execute some code!
}
```

To check if x equals 5 **OR** 3:

```javascript
let x = 3;
if (x === 3 || x === 5) {
  // execute some code!
}
```

## Booleans
So far we've primarily looked at two data types- numbers and strings ("hello!"). As we move into exploring conditional logic, a new type of variable is going to become important: booleans. Booleans store if values are *true* or *false*.

```javascript
let a = true;
let b = false;
let c = 5 === '5';  // false
let d = 4 > 1;      // true
```

### mouseIsPressed
We can use a built-in boolean variable, **mouseIsPressed**, to show text when the mouse is pressed:

```javascript
if (mouseIsPressed) {
  text("CLICKED", 100, 100);
}
```

Be careful not to confuse the boolean, `mouseIsPressed`, with the function, `mousePressed()`, which is called automatically when the mouse is pressed.

```javascript
function mousePressed() {
   console.log(mouseX, mouseY);
}
```

## keyPressed()
p5.js has other functions (besides the `draw()`, `setup()`, and `mousePressed()`) that are called automatically. 

`keyPressed()` is runs automatically when a key is pressed. We can use this function with conditional statements to add interactivity to our sketches:

```javascript
function keyPressed() {
    // for arrow keys
    if (keyCode === LEFT_ARROW) {
        console.log("left arrow pressed");
    } else if (keyCode === RIGHT_ARROW) {
        console.log("right arrow pressed");
    }
    else if (key === 'a') {
        console.log("a key pressed");
    }
}
```

## Resources
* [3.1: Introduction to Conditional Statements ](https://www.youtube.com/watch?v=1Osb_iGDdjk&list=PLRqwX-V7Uu6Zy51Q-x9tMWIv9cueOFTFA&index=14) (Daniel Shiffman)
* [3.3: Else and Else if, AND and OR](https://www.youtube.com/watch?v=r2S7j54I68c&list=PLRqwX-V7Uu6Zy51Q-x9tMWIv9cueOFTFA&index=16)
* [3.4: Boolean Variables](https://www.youtube.com/watch?v=Rk-_syQluvc&list=PLRqwX-V7Uu6Zy51Q-x9tMWIv9cueOFTFA&index=17)