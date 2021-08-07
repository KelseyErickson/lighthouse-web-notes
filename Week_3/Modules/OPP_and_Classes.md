# Module 1 Week 3 - OPP and Classes


## OOP -  Object Oriented Programming

- object orientation – use of objects to keep code modular and reduce repetition

OO (object orientation) is a software development paradigm 
- JavaScript is not strictly OO in the way that Java or Ruby are 
- Functional Programming is an alternative paradigm, and one that JavaScript also uses
- OO bundles together related state and logic into an object that can be passed around as a single entity.

## Terms
Object - is a bundle of info also known as a state. Each property that an object has, can represent the state of that object

Method - when a property’s value is a function it is called a method. Can make Objects have behaviour.

'this' – is a keyword. The value is determined at the time of the call and depends on how and where it is called. This refers to the object that the method was called on.


## Classes 

- JS mimics the behaviour of class based OOP languages. Classes were introduced in ES6
- before this prototypes were what were used in JS and still are.
- since Es6 using classes has slowly bcome the preferred way 
- but still importatn to understand prototypes

## Classes are blueprints 
- in OOP classes are blueprints or templates that we use to create instances of objects
- use class keyword.

``` JavaScript
class Thing {

}
```

## Naming Rules
- class names should be nouns and the first letter should be capitalized
- to create a new object from a class we use the new keyword

``` JavaScript
let thing1 = new Thing();
```

## Instances
- when you create an object using a class it is an instance of that class
- there can be many instances of the same class but they are all considered separate objects

## Methods and Properties
- you can add a methods to a class

``` JavaScript
class SomeClass {
  methodName(parameters) {
    // this is a method
  }
}
class SomeClass {
  someMethod() {
    this.hello = "hi"; // Created a property called hello
  }
}

```

### Note
- you can call methods on the instances but not on the class itself since it is just a blueprints

## Constructor
constructor – a special kind of methos that gets exectured when an object instance in sreated from a class. Eveything inside the constructor methos will get run for the new isntance of the class. Helps set up default state for new instances. It is for setting default values. 