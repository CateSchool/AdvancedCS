As a perhaps more exciting example, let's say we want to write a function, `getTempColor()` that converts temperature in Celsius (in a range from 0 to 40 degrees C) to a color on a gradient scale from blue to red. Examine all of the functions in the example below that return values: 


```javascript
function setup() {
    createCanvas(400, 400);

    let celsiusString = prompt("Please enter temperature in celsius");
    let celsius = parseFloat(celsiusString); // turn the string to a float
    background(getColorFromTemp(celsius));
}

function getColorFromTemp(celsius) {
    // constrain the temperature to the range 0-40
    celsius = constrain(celsius, 0, 40);
    // map the temperature range to a number from 0-1
    let percent = map(celsius, 0, 40, 0, 1);
    // define red and blue colors
    let r = color(255, 0, 0);
    let b = color(0, 0, 255);
    // use lerpColor() to return a color interpolated between red and blue
    return lerpColor(b, r, percent);
}
```