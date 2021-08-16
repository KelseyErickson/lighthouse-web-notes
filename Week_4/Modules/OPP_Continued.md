# Module 1 Week 4

## Super

- you may want your subclass to have almost the same but slightly different code than the superclass. 

- when a subclass implements a method that already exists in the superclass it is called method overriding. 


- you can reference the parent class with the word 'super'. Super allows us to access the super class. 

- use 'super' to avoid repeating code that is already in the super class 

## Getters and Setters

- Getters and setters are special methods that are used to get value of or set the value of a property
- these are helpful fo validating data before assigning it to a property and computing a value on the fly instead of pulling it out of a property

``` JavaScript
 get price() {
    const basePrice = 10;
    const toppingPrice = 2;
    return basePrice + this.toppings.length * toppingPrice;
  }

  set size(size) {
    if (size === 's' || size === 'm' || size === 'l') {
      this._size = size;
    }
  }


  let pizza = new Pizza();

pizza.price;      // instead of getPrice()
pizza.size = 's'; // instead of setSize(size)

```

- by using the get and set keywords these can be accessed as if they were value properties instead of methods. (this is in an object called Pizza)

- this makes these both functions and values 
- get and set bind an object's property to a function that will be called when the value is looked up. 
- though not always necessary the get an set keywords help make the interface more simple

## Best Practices 
- primary goals of OOP is to reduce duplicate code and to break up code into sensibly-divded units. 
- it allows for abstraction - leaving the more complex details below the current level and allowing the interface to be simple and easy to use. 
- use inheritance to reduce duplicate code

## Public vs Private
- in JS there is no way of making something private. if you add an _ to the start of a property name other deveopers will know that they shouldn't access it directly

## Single Responsibiliy Principle 

- a class should be responsible for a single part of the app's functionality. 
- that way changing one aspect of our app no other parts should be affected

## Review
- OOP is a programming paradigm where we use objects to encapsulate (group) data and behaviour. 
- data and behaviour become properties of those objects
- OPP itself does not require classes. 
- classes have data in the form of value properties and behaviour in the form of methods