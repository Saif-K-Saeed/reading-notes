# State and Props

### State

The state is an updatable structure that is used to contain data or information about the component and can change over time. The change in state can happen as a response to user action or system event. It is the heart of the react component which determines the behavior of the component and how it will render. A state must be kept as simple as possible. It represents the component's local state or information. It can only be accessed or modified inside the component or by the component directly.

### Props

Props are read-only components. It is an object which stores the value of attributes of a tag and work similar to the HTML attributes. It allows passing data from one component to other components. It is similar to function arguments and can be passed to the component the same way as arguments passed in a function. Props are immutable so we cannot modify the props from inside the component.

### Difference between State and Props

Props| State
----------------|-------------------
Props are read-only.| State changes can be asynchronous.
Props are immutable.| State is mutable.
Props allow you to pass data from one component to other components as an argument.|State holds information about the components.
Props can be accessed by the child component.| State cannot be accessed by child components.
Props are used to communicate between components.| States can be used for rendering dynamic changes with the component.
Stateless component can have Props. |Stateless components cannot have State.
Props make components reusable. |State cannot make components
 Props are external and controlled by whatever renders the component. |The State is internal and controlled by the React Component itself.




