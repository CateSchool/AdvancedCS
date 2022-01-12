# Big 0

  - [Orders](#orders)
    - [Constant O(1)](#constant-o1)
    - [Linear O(n)](#linear-on)
    - [Quadratic O(n<sup>2</sup>)](#quadratic-onsup2sup)
  - [Rules](#rules)
  - [Visualization](#visualization)

---

[Slides](https://docs.google.com/presentation/d/1hofPvMHXBBipxNjF7rr6q-qxJclXTXygcL6YIRNEEsY/edit?usp=sharing)  
[Video](https://www.youtube.com/watch?v=__vX2sjlpXU)

**Big O** is a method for analyzing the efficiency of an algorithms, including both **space** (amount of memory) and **time** (how long to execute). We use Big O to describe an algorithm's **complexity**, the amount of resources (time and memory) it takes to run. Big O is used to classify algorithms when the input (referred to as `N`) approaches infinity.

Considerations of Big O:    
1. we examine algorithms as a function of `N` when `N` **approaches infinity**
2. we analyze an algorithm's **worst-case** running time / memory use

## Orders 

### Constant O(1)
A constant time algorithm will take the same amount of time no matter what size `N` (the input) is. We use the notation `O(1)` for constant time algorithms.

```javascript
function getConstant(n) {
  return n*100 + 20;
}
```

Consider the following example where the `getConstant()` function is called 3 times:

```javascript
function get3Constants(n) {
  return getConstant(n) + getConstant(n-1) + getConstant(n-2);
}
```

You might think to describe the Big O as `3*O(1)` since this equation calls the constant function 3 times; however, we don't consider constant multipliers. [Here's an explanation from Stack Overflow](https://stackoverflow.com/questions/22188851/why-is-the-constant-always-dropped-from-big-o-analysis):

> Big-O notation doesn't care about constants because big-O notation only describes the long-term growth rate of functions, rather than their absolute magnitudes. Multiplying a function by a constant only influences its growth rate by a constant amount, so linear functions still grow linearly, logarithmic functions still grow logarithmically, exponential functions still grow exponentially, etc. Since these categories aren't affected by constants, it doesn't matter that we drop the constants."

In short, we consider this algorithm to have a time complexity of `O(1)` and drop the 3.

### Linear O(n)
The following function effectively has `N` operations (we use a for loop to repeat an operation n times):

```javascript
function getLinear(n) {
  let x = 0;
  for (let i = 0; i < n; i++) {
    x += n;
  }
  return x;
}
```

### Quadratic O(n<sup>2</sup>)

```javascript
function getQuadratic(n) {
  let x = 0;
  for (let i = 0; i < n; i++) {
     for (let j = 0; j < n; j++) {
        x += n;
      }
  }
  return x;
}
```

## Rules

When calculating Big O:   
1. We **ignore constants** (more on this below)
2. only take **highest order term** (more on this below)

For example:  
 
```javascript
function getCombo(n) {
  return getConstant(n) + getLinear(n) + getQuadratic(n);
}
```

At first glance, we might describe the Big O of `getCombo()` as the sum of the orders of its other function calls, in other words:

```
O(1) + O(n) + O(n^2)
```

**HOWEVER**, for functions that involve a variety of terms such as `O(1)` and `O(n)`, we only consider the **highester order term**. This is because for very large values of `N`, constants and low-order terms don't have a significant impact on the time / space complexity relative to higher order terms. For this reason, we would describe `getCombo()` as having a time complexity of O(n<sup>2</sup>), the highest order term.


## Visualization
![big o](big0.jpeg)


