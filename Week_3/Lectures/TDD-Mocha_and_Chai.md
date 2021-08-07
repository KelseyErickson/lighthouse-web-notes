# Week 3 Lecture 1  - NPM and Test Driven development 

## Terms

- manual testing – console.log is the most common way..  
- unit test – testing of a unit – it is easiest to do with functions that returns something
- testing externally – makes it easier because then we do not have tests built into the functions
- automated testing - tests are separate from our actual code
- deprecated – it is no longer recommended that you use this
- test driven developmentt – you write the tests first and then write your code to pass the tests

## Console.assert
- console.assert – will tell you if it passes of failed
- console.assert takes a logical expression and a message if the assertion fails
- will sprinkled them throughout the code. You should never see it if the program with working properly
- will not use it much in the program but it is used sometimes
- we are going to use an assertion library instead

## Nodejs
- Node – is js but not quite. It was developed by google as a command-line version of JS that allows you to run node on a terminal rather than just on a browser
- Node is an extension of JS – get some extra built in things
- one of those extra things is the assert packages – to make it work you have to use the require keyword
- you need to use require to use node modules
- now you can use any functions that exist in the assert module in node

### Note
- have a look at node documentation to see what is available

## How to use Modules
- need to export the function from the functions file
- then add it to the test file with require 
- module wrapper – when you run a nodejs program – nodejs wraps it and you do not see it
- when you require from a file you get back the exports object from the module
- when you require you get whatever module.exports is.
- module.exports = function; - do not put the brackets after the function because we do not intend to run it

``` JavaScript
module.exports.sayhello = sayhello;
module.exports = {sayHello};
module.exports = function;

```

- if you export as a object then you have to use it as an object

## NPM
- like the amazon of node packages - it is huge
- NPM is three randoms letters they put together – not really node package manager
- millions of packages for free

## Installing Mocha
- mocha is one of those packages offered by NPM
- mocha is a test framwork and one of the biggest
- can install globally – attached to the nodejs in the computer – anything I run will have access to mocha
- install locally – install only to the project – this will allow you to use differetn version of node for different projects. Also sends mocha with the project so if someone doesn’t have it, it will still work

## .json
- need a package.json file – file that controls the projects
- before we can install a package you need to initialize the node project
- npm init – creates a new project with a package.json
- fill out the information
- now you can install mocha for the projects
- npm installs mocha in the project and added files.
- made changes to the package.json file – adds the info. It is a dev dependency – meaning only used for development

### Note
- do not edit the json.lock file
- do not add node modules files to github – it is horrible

## .gitignore
- to not add node modules files we use a gitignore file
- .gitignore – tell it what files we do not want tracked it github or belong to git at all
- put in there node_modules

## Mocha
- use 'describe' and 'it' in the test file
- mocha tests only care about erros that are thrown
- mocha is a test runner and that is all – it does automated testing

## Chai 
- chai – assertion library - independant of mocha
- chai is a sophisticated assertion library – not required to do mocha tests with but is helpful
- similar to assert module but has extra features 