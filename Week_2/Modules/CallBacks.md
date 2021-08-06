# Notes on Week 2 Module 1 - Fucntions and Call Backs

## Functions

### Functions are first class objects 
- can be stored in variables and passed around
- can do everything that other objects can do (like have properties assigned to them)

### Call Back Functions
- is a function passed by reference into another function
- the receiver function is therefore accepting behaviour to perform by calling the callback function that it now has access to
- the receiver function can decide to call the callback function at any time, as many times as it wants

### High order functions
- functions that take in callbacks are referred to as high order functions
- high order functions are any functions which operate on other functions
- this means built-in functions such as forEach, Filter and others can be called ‘High-Order-Functions’
- functions are values in JS and can pass them around. These can pass into a higher order functions
- allows us to put a lot of smaller functions into bigger functions
- Map is also a higher order function. It transforms each element of an array. Map can be used to return a specific property of an object
