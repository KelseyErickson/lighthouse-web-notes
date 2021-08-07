# Module 1 Week 3

## Recursion

-  is an alternative to traditional looping that allows you to do the same thing, just in a slightly different way
- recursion isn’t necessarily better it is different
- any problem you can solve with a for loop you can solved with recursion and vice versa 
- recursion is a function that calls itself until in doesn’t – function will continue to call itself until the condition is met
- every recursive function must stop calling itself at some point

## Terms
recursive case – as long as it is true the function will continue to call itself

base case – if this is true the function will not call itself


- in a proper recusive function with each recursive call the input must gradually resolve towards the base case
- in order to be recursive a function must have at lease one recursive case and at lease one base case.

``` JavaScript
function countEvenToTwelve(number) {
2.|   if (number <= 12) { // Recursive Case
3.|     console.log(number);
4.|     // The function will call itself again and get closer to the base case
5.|     countEvenToTwelve(number+2);
6.|   }
7.|   // Base case, do nothing when number > 12
8.| }
9.| countEvenToTwelve(0);

```

- Being able to identify when the problem you are solving is just a smaller instance of the problem you have already solved will allow you to determine when to use recursion instead of iteration.
