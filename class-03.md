# Lists And Keys In React

## How to display lists of elements in React?

You can use map method to loop through an array of items and then use curly braces to insert it into your JSX code:

```
const todos = ["buy milk", "learn react", "walk the dog"];
const ToDoList = () => (
  <ul>
    {todos.map(todo => (
     <li>{todo}</li>
    ))}
  </ul>;
};
```

Here we mapped through the array of `string`s array using the array `map()` method. We return `li` element for each item. If you run this code - you’ll get a warning that you need to provide keys for your list items.

### Providing Keys

React keeps track of the identity of each list item by it’s `key` attribute. Using this prop it determines what items were added, changed or removed.

It’s important that this key should be uniquely associated with each list item, ideally it should be some unique id:

```
const todos = [
    {text: "buy milk", id: 0},
    {text: "learn react", id: 1},
    {text: "walk the dog", id: 2}
];

const ToDoList = () => (
  <ul>
    {todos.map(todo => (
      <li key={todo.id}>
        {todo.text}
      </li>
    ))}
  </ul>;
};
```

If your items don’t have unique identifiers you can use `map` with `index` as last resort. It’s not optimal solution because this `index` won’t be bound to specific element and if the order of your element changes - the index will also change.

```
const todos = ["buy milk", "learn react", "walk the dog"];

const ToDoList = () => (
  <ul>
    {todos.map((todo, index) => (
      <li key={index}>{todo}</li>
    ))}
  </ul>;
};
```

It is important that `keys` would be unique among siblings, so in our example we can’t use `todos` values as keys. We can’t guarantee that our todos won’t have duplicates.

### Using Lists With Components

In previous examples we were using li items, but in real React applications you’ll often use custom components inside your lists.

```
const todos = [
    {text: "buy milk", id: 0},
    {text: "learn react", id: 1},
    {text: "walk the dog", id: 2}
];

const ToDoList = () => (
  <ul>
    {todos.map((todo) => (
      <ToDoItem key={todo.id} text={todo.text} />
    ))}
  </ul>;
};
```

Keys are provided for elements inside of the loop, so you need to provide it inside of the component, or to component children:

```
const todos = [] // your todos

const ToDoItem = ({ text }) => <li key={text}>text</li>;
// THIS IS WRONG

const ToDoList = () => (
  <ul>
    {todos.map((todo) => (
      <ToDoItem key={todo.id} text={todo.text} />
    ))}
  </ul>;
};
```

Here is the correct example:

```
const todos = [] // your todos

const ToDoItem = ({ text }) => <li>text</li>;
// THIS IS WRONG

const ToDoList = () => (
  <ul>
    {todos.map((todo) => (
      <ToDoItem key={todo.id} text={todo.text} />
    ))}
  </ul>;
};
```

### Recap

When you render lists in React you have to specify a special `key` prop for your items. It is required for React to effectively track changes in the list.

You should provide keys only to the outermost items inside your list, not their children. If you use custom components, like `ToDoItem` in our example - you should keep the `key` on the `<ToDoItem />` elements, and not inside the component.

Keys should be unique across siblings in your list. In case if you can’t provide unique id’s you can use `map()`with `index`, but that’s not optimal and should be used only as last resort.

## Pass Action or Function to Child Component

You can pass state values to a child component as a prop, but you can also pass functions directly to the child component like this:
```
<ChildComponent
    // The child component will access using actionName
    actionName={this.actual_action_name}
/>
```
`actionName` is the name of the props that can be accessed by the child component. Once you trigger an action or pass the data from the child component, the same action's name will be accessed using `this.props.action_name.`

Let’s look at a simple example of passing an action to the child component.

```
<MyChildComponent
    onSubmitData={this.onSubmitData}
/>
```
From the child component, you can trigger an action using `this.props.onSubmitData()` so that the action into the parent component will be triggered.
