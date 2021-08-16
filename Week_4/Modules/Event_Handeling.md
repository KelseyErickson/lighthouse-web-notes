# Module 1 Week 4 - Event Handling and User Input

## User Events
- user events can occure at any time when the app is running so they need to be handled asychronously
- user evens can be clicking a ling, submitting a form, dragging and dropping, so on

## CallBacks 
- callbacks are a major way that JS handles dealing with code that needs to run later

## Event Handling and User Input
- instead of using setTimeOut we can have code run any time the user provides input to the program. 
- 'on' method is a common method name for registering callback to handle events. 
- not all even handling is due to direct user input

``` JavaScript
const stdin = process.stdin;
// don't worry about these next two lines of setup work.
stdin.setRawMode(true);
stdin.setEncoding('utf8');

////////////
// Event Handling for User Input
////////////

// on any input from stdin (standard input), output a "." to stdout
stdin.on('data', (key) => {
  process.stdout.write('.');
});

console.log('after callback');

```