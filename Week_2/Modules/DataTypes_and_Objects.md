# Notes on Week 2 Module 1 - DataTypes and Objects


## Data Types 

- In JS all values that are not objects are primitive

They are:
- undefined
- null
- Boolean
- string
- number
- symbol



## Objects
- Objects are not primitives. Anything not in the list above is an object
- arrays and functions are subcategories of objects
- Objects have properties
- six primitive types and objects make the seven fundamental types of JavaScript
- contain key-value pairs
- contain keys which are always strings or symbols
- have unique keys
- have their keys point to value which can be of any type
- Objects have literal syntax using braces
- object values can be of any type
- you can nest objects in objects


To define - can do either of the ways below. Preference for no quotes around the key.

``` JavaScript
const tinyObject = { "size": "Tiny" };
const tinyObject = { size: "Tiny" };
```

### REMEMBER 
that object keys are strings. When using bracket notation you need to put the quotes on. 

``` JavaScript
person[‘foo’];
```


### Object RULES
- keys are always strings – always interpreted as a literal string even if unquoted but it is necessary to quote if using spaces,  hyphens or periods
- each key is unique
- each key is associated with exactly one value

### Iterating over an object
- use a for in statement
``` JavaScript 

for (const key in object){
};
```


### Primitives and Properties
- primitive types don’t have properties
- but you can use things like string.length on them
- this is because primitive types have corresponding objects
- all primitives except symbol have a corresponding object constructor
- object constructors can be invoked with the word new.
- each object has methods associated with them based on what constructor was used
- in the case of using string.length – the string is being coerced to a string object in order to access the property length however, the string itself is still a primitive data type.
- so when you call a string object property on a primitive string it invokes properties of the equivalent object type.
- JavaScript performs type coercion on strings, numbers, and other primitive types, turning them into objects in order to make them act like objects.