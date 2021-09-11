# Component Based Architecture

## What is a Component?

A component is a modular, portable, replaceable, and reusable set of well-defined functions that encapsulates its implementation and exports it as a top-level interface.

 A component is a software object that is intended to interact with other components, encapsulates a certain functionality or a set of functionalities, has a clearly defined interface and corresponds to a recommended behavior that is common to all components within an architecture.

 A software component can only be defined as a unit of composition with a contractually defined interface and explicit context dependencies. That is, a software component can be implemented independently and is subject to composition by third parties.

### *Characteristics of Components*

- **Reusability** − Components are usually designed to be reused in different situations in different applications. However, some components may be designed for a specific task.

- **Replaceable** − Components may be freely substituted with other similar components.

- **Not context specific** − Components are designed to operate in different environments and contexts.

- **Extensible** − A component can be extended from existing components to provide new behavior.

- **Encapsulated** − A A component depicts the interfaces, which allow the caller to use its functionality, and do not expose details of the internal processes or any internal variables or state.

- **Independent** − Components are designed to have minimal dependencies on other components.

### *Advantages*

- **Ease of deployment** − As new compatible versions become available, it is easier to replace existing versions with no impact on the other components or the system as a whole.

- Reduced cost − The use of third-party components allows you to spread the cost of development and maintenance.

- **Ease of development** − Components implement well-known interfaces to provide defined functionality, allowing development without impacting other parts of the system.

- **Reusable** − The use of reusable components means that they can be used to spread the development and maintenance cost across several applications or systems.

- **Modification of technical complexity** − A component modifies the complexity through the use of a component container and its services.

- **Reliability** − The overall system reliability increases since the reliability of each individual component enhances the reliability of the whole system via reuse.

- **System maintenance and evolution** − Easy to change and update the implementation without affecting the rest of the system.

- **Independent** − Independency and flexible connectivity of components. Independent development of components by different group in parallel. Productivity for the software development and future software development.

---

## What is Props and How to Use it in React

### What are props?

“Props” stands for properties. It is a special keyword in React which is used for passing data from one component to another.

Logically, components are just like JavaScript functions. They accept random inputs (called “props”) and return React elements which tell what should be displayed on the screen.

Props can be used to pass any kind of data such as:  

- String
- Array
- Integer
- Boolean
- Objects or
- Functions

### How are props used in React?

Props are mainly used for passing data from the parent component to child component. It motivates us to reuse the components and reduce redundancy as well. But as a growing app, you might see a lot of bugs with typechecking.  

### What is the flow of props?

Flow is a static type checker for your JavaScript code. It is developed at Facebook and is often used with React. It lets you annotate the variables, functions, and React components with a special type syntax, and catch mistakes early

- Add Flow to your project as a dependency.
- Ensure that Flow syntax is stripped from the compiled code.
- Add type annotations and run Flow to check them.