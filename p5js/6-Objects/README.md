# 6. Objects

  - [Object Literals](#object-literals)
  - [Dot Notation](#dot-notation)
  - [Object Methods](#object-methods)
  - [this Keyword](#this-keyword)
  - [Arrays of Objects](#arrays-of-objects)
  - [JSON & APIs](#json--apis)

---
## Object Literals

Object literals- "a comma-separated list of name-value pairs wrapped in curly braces. Object literals encapsulate data, enclosing it in a tidy package" ([citation](http://www.dyn-web.com/tutorials/object-literal/)). Like an array, an object is used to store a variety of information. But unlike arrays, the data in the object does not have to be _ordered_ in a list. Instead, objects have fields with values.Let's consider an example. To initialize an object, we use curly brackets:

```javascript
let yoda = {};
```

We can also define properties—including arrays and other objects—when we create objects:

```javascript
let yoda = {
   name: "Yoda",
   age: 657,
   planet: "Dagobah",
   quotes: ["Me so silly!", "Me Jedi!"],
   friend: {
      name: "Luke",
      relationship: "padawan"
   }
};
```

## Dot Notation

It's possible to add or change properties of an object using _dot notation_ once the object has been created:

```javascript
yoda.lightSaberColor = "green"; // added new property
yoda.age = 748;                 // updated property
```

You also use _dot notation_ to access properties, even nested objects, in the object:

```javascript
console.log(yoda.age);        // prints 748
console.log(yoda.friend.name) // prints "Luke"
```

Or to access items inside of nested arrays:

```javascript
console.log(yoda.quotes[0]);  // prints "Me so silly!"
```


## Object Methods

Methods are functions inside of objects. It's useful sometimes to have functions specific to an object:

```javascript
let yoda = {
   /* fields and values */
   useTheForce: function(){
      console.log("Using the force, I AM!");
   }
};
```

To use a method associated with an object, we employ dot notation with the function:

```javascript
yoda.useTheForce();   // "Using the force, I AM!"
```

It's also possible to add methods to existing objects:

```javascript
yoda.callItLikeItIs() = function() {
  console.log("The fear of loss is a path to the dark side.");
}

yoda.callItLikeItIs();  // prints "The fear of loss is a path to the dark side."
```

And finally, it's possible to _pass arguments_ to methods:

```javascript
let yoda = {
   /* fields and values */
   fly: function(distance){
     if (distance > 100) {
       console.log("uh, this is the force, not a magic carpet.")
     }
      else {
        console.log("Zooming " + distance + " feet!");
      }
   }
};

function setup() {
  yoda.fly(50);
  yoda.fly(500);
}
```

## this Keyword

If you'd like your method to operate on the object's own properties (for example, if you'd like to write a method to change Yoda's planet when he travels), you have to use the _this_ keyword:

```javascript
let yoda = {
   name: "Yoda",
   age: 957,
   planet: "Dagobah",
   travelingTo: function(destination) {
      this.planet = destination;
   }
};

function setup() {
  console.log(yoda.planet);         // prints "Dagobah"
  yoda.travelingTo("Death Star");
  console.log(yoda.planet);         // prints "Death Star"
}

```

## Arrays of Objects
As we've seen, objects can contain arrays as a property, but the reverse is also true! We can store an array of objects:

```javascript
let cars = [
    { make: "Toyota", model: "Prius" },
    { make: "Ford", model: "Focus" },
    { make: "Tesla", model: "Model 3" }
]
```

## JSON & APIs
**JSON** (JavaScript Object Notation) is a format of representing data in a manner that can be easily exchanged between different programming languages (C++, Java, Python, ...). JSON is effectively a set of name value pairs that looks just like an array of objects. Notice the quotation marks around field names.

```javascript
{
    "students":[  
        { "name":"Ashi", "faveSnack": "Cheetos" },  
        { "name":"Alekha", "faveSnack": "Starburst" },  
        { "name":"Zhengli", "faveSnack": "oatmeal cookies" }  
    ]
} 
```

Many **APIs** (Application Programming Interface) return data in JSON format. An API is a set of protocols that makes it possible for programmers to ask a server for data (e.g. what is the weather this week?) and get back the reqested information. 


* [Here's a Pokemon API](https://pokeapi.co/)
* [Here's a p5.js example of using a weather API](https://p5js.org/examples/hello-p5-weather.html)