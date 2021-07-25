# JavaScript Functions
In JavaScript, a function allows you to define a block of code, give it a name and then execute it as many times as you want.

//defining a function

`function `<function-name>`()`
`{`

    // code to be executed
};

//calling a function

`<function-name>`();

Example

`function Message() {
    alert("Hello World!");
}`

`Message();`

- ## Function Parameters
`function` Message`(`firstName, lastName`)` `{`
    `alert``(``"`Hello `"` `+` firstName `+` " "` +` lastName`);`
`}`

Message`("`Saif`","`saeed`");`

Message`(100, 200);`

`function` Message`(`firstName`,`lastName`) {`

   ` alert`("`Hello `" +` firstName `+ " " +` lastName`);`
`}

Message`("`Saif`","`Saeed`", "`Mr.`"); `// display Hello Saif Saeed

ShowMessage`();` // display Hello undefined undefined
- ## The Arguments Object
`function` Message`(`firstName`,` lastName`) {`
    `alert``("`Hello `" +`arguments[0] `+ " " +` arguments[1]`);`
}

Message`("`Saif`","`Saeed`");` 

Message`(`100, 200`);`

- ## Return Value
`function` Sum(val1, val2) {

    return val1 + val2;
};

`var` result `=`` Sum(10,20); // returns 30

`function` Multiply(val1, val2) {

   ` console.log`( val1 * val2);
};

result = Multiply(10,20); // undefined

- ## Function Expression
`var` add `=` `function` sum(val1, val2) {
    `return` val1 + val2;
};

`var` result1`=` add(10,20);

`var` result2` =` sum(10,20); // not valid

- ## Anonymous Function
`var` Message `=` `function (){`

    `alert`("Hello World!");
};
`
Message();

`va`r sayHello `=` `function` (firstName) {

    `alert`("Hello " + firstName);
};

Message();

sayHello("Saif");

- ## Nested Functions
`function` Message(firstName)
{
    `function`SayHello`()` {

        `alert`("Hello " + firstName);

    }

    `return` SayHello();
}

 Message("Saif");
 

  #### Points to Remember :
- JavaScript a function allows you to define a block of code, give it a name and then execute it as many times as you want.
- A function can be defined using function keyword and can be executed using () operator.
- A function can include one or more parameters. It is optional to specify function parameter values while executing it.
- JavaScript is a loosely-typed language. A function parameter can hold value of any data type.
- You can specify less or more arguments while calling function.
- All the functions can access arguments object by default instead of parameter names.
- A function can return a literal value or another function.
- A function can be assigned to a variable with different name.
- JavaScript allows you to create anonymous functions that must be assigned to a variable.