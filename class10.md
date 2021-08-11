# Error Handling & Debugging

## Code Debugging

Often, when programming code contains errors, nothing will happen. There are no error messages, and you will get no indications where to search for errors.

Searching for (and fixing) errors in programming code is called code debugging.

## Why is Debugging Important

Debugging is done mostly to avoid the incorrect operation of an application by fishing out bugs and incorrect code. Let’s look at some of the importance of debugging and why developers should meticulously and efficiently debug their applications.
Bugs can make your application crash. With proper debugging, you can spot bugs from your code and avert unexpected behavior.

## How to Debug JavaScript

- Identifying a Bug
- Isolate the Bug

 1. Forward Analysis
 2. Backward Analysis

- Determine the Cause of the Bug
- Fixing the Bug
- Test the Application

## Debugging Methods in JavaScript

- Web Console
Most web browsers have a web console that allows developers to log information associated with a web page. Since JavaScript can run on a web page, developers can debug their applications from the web console. One advantage of debugging with the web console is the ability to interact with a web page by executing JavaScript expressions relating to a page. You can open Firefox’s web console by pressing the `CTRL + SHIFT + K` buttons.

 1. Log
 To quickly debug code, developers log outputs in some portions of their code using the `console.log()` function. This function takes a parameter that can be an array, an object, Strings, or numbers. It is very useful for debugging because it returns the value of the parameter given as a log so that the developer can easily see what’s going on in their application.

 2. Warn
  Sometimes, there are lots of logs in the console and it becomes difficult for the developer to spot a bug quickly. To make messages of interest distinct from other logs, the developer can make use of the `console.warn()` function. This function is very similar to the `console.log()` function, as it takes in parameters and returns the value of the parameters. However, it prints out logs as warnings.
 3. Error
 Sometimes, logs of errors get more attention and are easier to spot out. This is what the console.error() function does. It’s just like the console.log() and console.warn() function.
 4. Assert
 The `console.assert()` function will write an error in your console if the assertion is false. It accepts parameters like the assertion and error message
 5. Debugger Statement
 In JavaScript, the debugger statement is used for invoking a debugger or stopping the execution of the code if there’s no debugger. This is used for setting breakpoints in your application. Setting breakpoints when debugging is a good practice since it allows the developer to inspect the program during its execution

by ***Saif Saeed***  [GitHup](https://github.com/Saif-K-Saeed)
