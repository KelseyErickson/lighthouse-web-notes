# Module 1 Week 3 - Testing

## File exporting

We learned that in Node:
- modules are its way of organizing code into individual files 
- every js file in node is implicitly a module 
- we can console.log(module) and see its details 
- module.exports tells node what to export from a file 
    - it defaults to {} 
- we can use require with relative paths (like ./myModule) 
- it doesn't need the .js extension, as that is implied 


## Terms
packages – self-contained code libraries that we can install and use in our projects. Packages refer to packages libraries 

Automated testing - write code to test the code we want to write

Unit testing – the practice of testing small pieces of code – typically individual functions alone and isolated. If your test uses some external resource like a network or database it is not a unit test. Unit tests help you design your code. 

Integration testing – tests how parts of the system work together – the integration of parts. Integrations tests would talk to a real database. It is helpful to verfify if two different systems like a database and your app work together.They are slower. Focus on unit tests unless you absolutely needs an integration test.

Functional testing – aka E2E testing or browser testing. Testing of complete fucntionality of some application. This means using a tool to automate a browser, which is then used to click around on the pages to test the application. It is diffcult to write a miantin because they are complex. Should be used for common user interactions

BDD – behaviour driven development – is a process that emerged from test-driven development. Specify the behaviour of the app in terms of user stories which are broken down into scenarios that can be built and tested

## Notes on Testing
- unit testing should be the main focus when testing js code.
- you have to test a lot of possibilities not just the ‘Happy” or easiest path
- you have to try to break it in as many ways possible
- Happy path" tests are very useful, because they catch the most critical bugs, but are definitely not sufficient


