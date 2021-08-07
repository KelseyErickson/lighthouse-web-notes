# Module 1 Week 3

## Object methods and this

It is common to have objects with properties that reference data (string, numbers, arrays, other objects, etc)

``` JavaScript
const person = {
  firstName: 'Bob',  // <= property containing data
  lastName:  'Smith' // <= ditto
}

```

You can also assign functions to object properties.

``` JavaScript

const person = {
  firstName: 'Bob',
  lastName:  'Smith',
  fullName: function() {
    return this.firstName + ' ' + this.lastName;
  }
}

```
- Functions like this that are attached to objects are often referred to as a method
- ‘this’ is often used when working with methods in js
- we need the method to be able to refer to the object that it is within – this is the most common use of ‘this’
- ‘this’ – for now we will use it inside an object’s method . ‘this’ points to the object where its function resides. It referes to the objects method(function) it was called on
