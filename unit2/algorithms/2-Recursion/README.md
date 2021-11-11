# Recursion

A **recursive** function is a function that calls itself. Every recursive function has two parts:

1. a base case or termination condition
2. a non-base case that calls the function and moves it towards termination


```javascript
function recursiveFun(...) {
    if (/* base case */) {
        // stop calling
    }
    else {
        recursiveFun(...)
    }
}
```

**NOTE**: If your code never reaches the base case, you will end up with infinite recursion, causing your program to run out of memory!


## Writing Recursive Functions
Write a function that calculates the factorial of a number.

| Iteratively | Recursively |
| ----------- | ----------- |
| 0! = 1      | 0! = 1       |
| 1! = 1      | 1! = 1 \* 0!     |
| 2! = 2\*1    | 2! = 2 \* 1!     |
| 3! = 3\*2\*1  | 3! = 3 \* 2!        |
| n! = n\*..3\*2\*1  | n! = n \* (n-1)!       |


Here is the recursive function in action:

```javascript
function factorial(n) {
    if (n === 0)
        return 1;
    else
        return n * factorial(n-1);
}
```

Compare this to the iterative solution:

```javascript
function factorial(n) {
    let fac = 1;
    for (let i = 1; i <= n; i++) {
        fac *= n;
    }
    return fac;
}
```

## Use cases
Fib iterative vs. 
function is asymptotically O(2<sup>n</sup>). 
iterative runs in O(n)

When to avoid recursion:
1. algorithms with large arrays (too many recursive calls can lead to memory overloads)

When to use recursion:
1. number of operations is small and recursion simplifies readability of code 
2. branching processes with trees
3. divide-and-conquer algorithms (mergesort and binary search)

beginning
// sum of digits
// raise to a power

more advanced
// traversal with recursion: https://javascript.info/recursion
// ispalindrome
* 1, 0 return true;
* remove first and last letters
* those same, remaining string is the same, it's a palindrome
* otherwise, not
