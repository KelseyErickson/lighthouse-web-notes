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


Additional example from mentor using objects

``` Javascript
const groups = {

  groupOne: {
    members: ['Adam', 'Andy', 'Sam', 'Andrea'],
    groups: {
      subGroupOne: {
        members: ['Adam', 'Andrea']
      },
      subGroupTwo: {
        members: ['Andy', 'Sam'],

        groups: {
          subGroupOne: {
            members: ['Adam', 'Andrea'],

            groups: {
              subGroupOne: {
                members: ['Adam', 'Andrea']
              },
              subGroupTwo: {
                members: ['Andy', 'Sam'],
                groups: {
                  subGroupOne: {
                    members: ['Adam', 'Andrea']
                  },
                  subGroupTwo: {
                    members: ['Andy', 'Sam']
                  }
                }
              }
            }
          },
          subGroupTwo: {
            members: ['Andy', 'Sam']
          }
        }
      }
    }
  },

  groupTwo: {
    members: ['Adam', 'Joe', 'Sam', 'Andrea'],
    groups: {
      subGroupThree: {
        members: ['Adam', 'Andrea']
      },
      subGroupFour: {
        members: ['Joe', 'Sam']
      }
    }
  }
}

const numberOfNamesInGroups = (memberName, groups) => { // to find the number of times the name appears in members
  let count = 0;
  for (const mainGroupKey in groups) {
    const group = groups[mainGroupKey]; // here we are accessing the keys in groupOne and groupTwo
    for (const member of group.members) { // for every array of members we find we loop through and check if the names match
      if (member === memberName) {
        count++; // if they do we will add to the count. 
      }
    }

    if(group.groups){ // for every group(remember this is groupOne and groupTwo from above) .groups - so everytime you run into a groups key under the other groups
      count += numberOfNamesInGroups('Adam', group.groups); // we call the function again to go through all of this again until the count is done and there are no more nested objects. 

      // the stopping condition is if we have another nested object, if we don't the counter just updates it all and we are done. 
    }
  
  }


  return count;
}



console.log(numberOfNamesInGroups('Adam', groups)); 

```