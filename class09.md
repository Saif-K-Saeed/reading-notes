# HTML - Forms

HTML Forms are required, when you want to collect some data from the site visitor. For example, during user registration you would like to collect information such as name, email address, credit card, etc.

A form will take input from the site visitor and then will post it to a back-end application such as CGI, ASP Script or PHP script etc. The back-end application will perform required processing on the passed data based on defined business logic inside the application.

There are various form elements available like text fields, textarea fields, drop-down menus, radio buttons, checkboxes, etc.

The HTML `<form>` tag is used to create an HTML form and it has following syntax −

``<form action = "Script URL" method = "GET|POST">``
  ``form elements like input, textarea etc.``
``</form>``

## Form Attributes

- **action**
Backend script ready to process your passed data.

- **method**
Method to be used to upload data. The most frequently used are GET and POST methods.

- **target**
Specify the target window or frame where the result of the script will be displayed. It takes values like _blank,_self, _parent etc.

- **enctype**
You can use the enctype attribute to specify how the browser encodes the data before it sends it to the server. Possible values are −

## HTML Form Controls

There are different types of form controls that you can use to collect data using HTML form −

- Text Input Controls
- Checkboxes Controls
- Radio Box Controls
- Select Box Controls
- File Select boxes
- Hidden Controls
- Clickable Buttons
- Submit and Reset Button

## HTML - Lists

HTML offers web authors three ways for specifying lists of information. All lists must contain one or more list elements. Lists may contain −

`<ul>` − An unordered list. This will list items using plain bullets.

`<ol>` − An ordered list. This will use different schemes of numbers to list your items.

`<dl>` − A definition list. This arranges your items in the same way as they are arranged in a dictionary.

## HTML - Tables

The HTML tables allow web authors to arrange data like text, images, links, other tables, etc. into rows and columns of cells.

The HTML tables are created using the `<table>` tag in which the `<tr>` tag is used to create table rows and `<td>` tag is used to create data cells. The elements under `<td>` are regular and left aligned by default

## JavaScript - Events

avaScript's interaction with HTML is handled through events that occur when the user or the browser manipulates a page.

When the page loads, it is called an event. When the user clicks a button, that click too is an event. Other examples include events like pressing any key, closing a window, resizing a window, etc.

Developers can use these events to execute JavaScript coded responses, which cause buttons to close windows, messages to be displayed to users, data to be validated, and virtually any other type of response imaginable.

---

### Mouse events

 |*Event* | *Performed* | *Event Handler* | *Description|
 |-----|---------|-------|-------|------|
|click| onclick |When mouse click on an element.|

|mouseover |onmouseover| When the cursor of the mouse comes over |the element
|mouseout| onmouseout| When the cursor of the mouse leaves an element|
|mousedown| onmousedown| When the mouse button is pressed over the element|
|mouseup |onmouseup| When the mouse button is released over the element|
|mousemove| onmousemove| When the mouse movement takes place.|
