# 5. Arrays


  - [Accessing 2D Arrays](#--accessing-2d-arrays)
  - [Initializing Arrays](#initializing-arrays)
    - [push()](#push)
    - [other array methods](#other-array-methods)
  - [Accessing Array Values](#accessing-array-values)
  - [Setting Array Values](#setting-array-values)
  - [Arrays & Loops](#arrays--loops)
  - [2D arrays](#2d-arrays)
    - [Accessing 2D Arrays](#accessing-2d-arrays)
    - [Initializing 2D Arrays](#initializing-2d-arrays)
    - [Looping through 2D Arrays](#looping-through-2d-arrays)
---

## Initializing Arrays
Arrays allow us to store multiple values at once.
```javascript
const cars = ["Yukon", "Toyota", "Honda"];
```
Arrays are used to store multiple values in a single variable. Arrays can store any type of data:

```javascript
const emptyArray = [];
const names = ["Jenna", "Jessica", "James"];
const years = [2019, 2017, 2015, 2000];
const rando = [ "woot!", -19.4, false];
```

[Extra reading: using const with arrays](https://www.w3schools.com/js/js_array_const.asp).

If an array is empty, we can set the values in a variety of ways. To create an array of random numbers:
```javascript
let arr = [];
for (let i = 0; i < 10; i++) {
    arr[i] = random();
}
```
### push()
The method `push()` appends elements to the end of an array:
```javascript
let arr = [];
for (let i = 0; i < 10; i++) {
    arr.push(random());
}
```

### other array methods
* `pop()` (removes last item)
* `shift()` (removes first item)
* `unshift(element)` (adds **element** to the beginning of the array)
* `splice(startIndex, n)` (removes **n** elements begining at **startIndex**)
  
```javascript
let fruits = ["apple", "kiwi", "banana", "strawberry"];
fruits.pop();           // ["apple", "kiwi", "banana"]
fruits.shift();         // ["kiwi", "banana"]
fruits.unshift("pear"); // ["pear", "kiwi", "banana"]
fruits.splice(1, 1);    // ["pear", "banana"]
```

## Accessing Array Values
We can use an **index** (the position of an *element* in an array beginning with 0) to access the values in an array:

```javascript
const arr = [10, "Jenna", true];

console.log(arr[0]);        // 10
console.log(arr[1]);        // "Jenna"
console.log(arr[2]);        // true
```

## Setting Array Values
Assuming we have initialized a variable as an array, e.g. `let arr = []`, we can use an index to **set** values of an array:

```javascript
let  arr = [10, "Jenna", true];

arr[0] = -17;
console.log(arr[0]);        // -17
console.log(arr[1]);        // "Jenna"
```

## Arrays & Loops
Arrays are most powerful when leveraged with loops to automate tasks. Let's use a for loop to calculate the average ages of a group of people.

```javascript
let ages = [11, 23, 2, 48, 90, 88, 70];

let sum = 0;
for (let i = 0; i < ages.length; i++) {
    sum += ages[i];
}

let average = sum/ages.length;
```

Note that to get the **length** of an array, we can use the `.length` property.

## 2D arrays

### Accessing 2D Arrays
We can use the following (row, column) notation to access items in 2D arrays:
```javascript
let arr = [
    [3, 2, 6, 10],
    [9, 8, 13, 1],
    [15, 5, 0, 4]
]
console.log(arr[0][1]); // 2
console.log(arr[2][1]); // 5
```

### Initializing 2D Arrays
We can use a for loop to initialize an array.
```javascript
let arr = [];
for (let r = 0; r < 10; r++) {
    // make sure to initialize empty sub arrays first
    arr[r] = [];
    for (let c = 0; c < 10; c++) {
        arr[r][c] = random();
    }
} 
```

### Looping through 2D Arrays
Notice how `arr.length` and `arr[0].length` are used in the for loop:
```javascript
let arr = [[2,5,3], [3, 5, 8], [9, 9, 10]];
for (let r = 0; r < arr.length; r++) {
    for (let c = 0; c < arr[0].length; c++) {
       console.log(arr[r][c]);
    }
} 
```
