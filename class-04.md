# Forms

No matter what kind of app you’re writing, there’s a good chance you need at least one form.

Forms in React are often a pain, filled with verbose and boilerplate-y code.

Let’s look at how to make forms in React with less pain.

In this article we’ll be focusing on using plain React, with no libraries. You’ll learn how forms really work, so you can confidently build them yourself. And if later you choose to add a form library, you’ll know how they work under the hood.

We’re going to cover:

- How to create React forms without installing any libraries
- The two styles of inputs in React forms
- When to use Controlled vs. Uncontrolled inputs
- An easy way to get values out of uncontrolled inputs
  
## How to Create Forms with Plain React

Let’s dive right in. We’re going to build a simple contact form. Here’s the first iteration, a standalone component called `ContactForm` that renders a form:

```
function ContactForm() {
  return (
    <form>
      <div>
        <label htmlFor="name">Name</label>
        <input id="name" type="text" />
      </div>
      <div>
        <label htmlFor="email">Email</label>
        <input id="email" type="email" />
      </div>
      <div>
        <label htmlFor="message">Message</label>
        <textarea id="message" />
      </div>
      <button type="submit">Submit</button>
    </form>
  );
}
```
You don’t need to install a library to do any of this. React has built-in support for forms, because HTML and the DOM have built-in support for forms. At the end of the day, React is rendering DOM nodes.

In fact, for small forms, you probably don’t need a form library at all. Something like Formik or react-hook-form is overkill if all you need is a simple form.

There’s no `state` in here yet, and we’re not responding to form submission, but this component will already render a form you can interact with. (If you submit it, the page will reload, because submission is still being handled in the default way by the browser)

## React Forms vs. HTML Forms

If you’ve worked with forms in plain HTML, a lot of this will probably seem familiar.

There’s a `form` tag, and `labels` for the `input`s, same as you’d write in HTML.

Each label has an `htmlFor` prop that matches the `id` on its corresponding input. (That’s one difference: in HTML, the label attribute would be `for`. React uses `htmlFor` instead.)

If you haven’t done much with plain HTML, just know that React didn’t make this stuff up! The things React does are pretty limited, and the way forms work is borrowed from HTML and the DOM.

## Two Kinds of Inputs: Controlled vs. Uncontrolled

Inputs in React can be one of two types: controlled or uncontrolled.

An **uncontrolled** input is the simpler of the two. It’s the closest to a plain HTML input. React puts it on the page, and the browser keeps track of the rest. When you need to access the input’s value, React provides a way to do that. Uncontrolled inputs require less code, but make it harder to do certain things.

With a **controlled** input, YOU explicitly control the value that the input displays. You have to write code to respond to keypresses, store the current value somewhere, and pass that value back to the input to be displayed. It’s a feedback loop with your code in the middle. It’s more manual work to wire these up, but they offer the most control.



## How Ternary Operator Works in React?

Before understanding the working of the ternary operator we need to understand why we need the ternary operators. You have seen conditional statements in the JavaScript where we execute either of the statement on the basis of the success or failure of the conditions, in the same we may face a situation where we wanted to display one html or any component on the conditional basis. To explain the working of it we can take some points.

- We can put a conditional expression inside the curly braces.
- The expression written inside the curly braces can be a combination of multiple expressions but they will always return a single boolean value.
- If the expression of the condition written inside curly braces is true then we will display the output written in the fir