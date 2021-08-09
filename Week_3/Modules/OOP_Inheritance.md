# Week 3 Module 1 - OPP and Inheritance
## Inheritance
- we can use this to build a new class based on an existing class. 
- you can use the keyword 'extends' to share code from an existing class.
``` JavaScript
class Person {
  constructor(name, quirkyFact) {
    this.name = name;
    this.quirkyFact = quirkyFact;
  }


class Student extends Person {
  enroll(cohort) {
    this.cohort = cohort;
  }
}

```
- so the student class inherits behavious from the person class
- student in this calse is a subclass for the person class 
- person is the superclass


