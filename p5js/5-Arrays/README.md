# 6. Arrays

## Accessing Arrays
Arrays are used to store multiple values in a single variable. Arrays can store any type of data:

```javascript
let emptyArray = [];
let names = ["Jenna", "Jessica", "James"];
let years = [2019, 2017, 2015, 2000];
let rando = [ "woot!", -19.4, false];
```

We can use an index (beginning with 0) to access the values in an array:

```javascript
let  arr = [10, "Jenna", true];

console.log(arr[0]);        // 10
console.log(arr[1]);        // "Jenna"
console.log(arr[2]);        // true
```

Or we can use an index to set values of an array:

```javascript
let  arr = [10, "Jenna", true];

arr[0] = -17;
console.log(arr[0]);        // -17
console.log(arr[1]);        // "Jenna"
```

## Arrays & Loops
Arrays are most powerful when leveraged with loops to automate tasks. 