# Qualities of Effective Code

## Descriptive names
- variables / functions / object names should be descriptive (e.g. `getCelsius()` is better than `calcTemp()`)
- use camelCase

## Variables
- Avoid global variables

## Indentation
- properly indented
- be consistent

## Readability
- Easy to understand, straightforward code is better than “clever” code
- Another programmer should be able to easily absorb the flow and logic of your code

## Comments
- Explain your code for someone else
- Don't need a comment for every line

## Always use semicolons
- Technically, most browsers will allow you to get away with omitting semicolons, but it’s good practice to use them

## Functions
- A function should only do one thing (“separation of concerns”)
- Generally speaking, the smaller the function, the better
    - Shoot for less than 20 lines (but probably more than 2) 
    - Functions that perform multiple tasks should call different functions to perform each subtask.  
- Less arguments are better (shoot for <= 4)
- Don’t repeat yourself
    - Separate out repeated code into separate functions

## Line length
- Try to shoot for 80 characters or less
- If a JavaScript statement does not fit on one line, the best place to break it is after an operator or a comma.

## File Organization
- When applicable, separate classes into individual files

## Error handling & prevention
- Well-written code handles errors
- Well-written code anticipates and prevents bugs by creating tests & checking boundary conditions  


