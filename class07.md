#

## HTML Table

HTML table tag is used to display data in tabular form (row * column). There can be many columns in a row.

We can create a table to display data in tabular form, using `<table>` element, with the help of `<tr>`, `<td>`, and `<th>`elements.

In Each table, table row is defined by `<tr>` tag, table header is defined by `<th>`, and table data is defined by`<td>` tags.

HTML tables are used to manage the layout of the page e.g. header section, navigation bar, body content, footer section etc. But it is recommended to use div tag over table to manage the layout of the page .

-------

Tag |Description
-----|---------
`<table>`| It defines a table.
`<tr>`| It defines a row in a table.
`<th>`| It defines a header cell in a table.
`<td>`| It defines a cell in a table.
`<caption>`| It defines the table caption.
`<colgroup>`| It specifies a group of one or more columns in a table for formatting.
`<col>`| It is used with `<colgroup>` element to specify column properties for each column.
`<tbody>` |It is used to group the body content in a table.
`<thead>` |It is used to group the header content in a table.
`<tfooter>` |It is used to group the footer content in a table.

---------

## Object Literal

Object Literals
An object literal is “flat”. You create it, you add properties and methods to it, and all of those properties and methods are public. You can mutate any members of that object at any time. A JavaScript object literal does not, by nature, provide private scope. But any of the members of an object literal can certainly be a function that is capable of private scope. Object literals are useful because they allow you to create clean name-spaced code that is easy to pass around and consume.

## Instance Objects

An instance object is what is returned when instantiating a JavaScript constructor function, using the JavaScript “new” keyword. When you say “`var bar = new Foo()`”, “`bar`” becomes an “instance” of the function “`Foo()`”. Any expressions within `Foo()` are executed, any local variables in `Foo()` are copied and provided in “`bar`”, and the value of “`this`” inside of “`bar`”, refers to “`bar`”. The function “`Foo`” is never changed in any way; it simply acts as a “blueprint” for “`bar`”, and “`bar`” is an “instance” of “Foo”. Any local variables inside of “`bar`” are completely private and can only be muted by privileged members of that object.

-----

- Objects
- Arrays
- Functions

name  | Example
----- |--------
Objects|`var` car = `{type:"Fiat", model:"500", color:"white"}`;
Arrays|`var` cars = `["Saab", "Volvo", "BMW"]`;
Functions |function myFunction(p1, p2) { `return p1 * p2;`   `of p1 and p2`}

by ***Saif Saeed***  [GitHup](https://github.com/Saif-K-Saeed)
