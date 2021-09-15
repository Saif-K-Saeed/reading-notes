
# Thinking in React

React community has provided a direction on how to think in React way and build big, fast, and scalable applications. React has reached multiple platforms and is widely used as a popular JavaScript UI interface library.

**Step 1** − Creating a simple mock service

If we need to make a server call and fetch data. We can create a mock service to start with and build a component to fetch and display data.

Here we can include the processing of JSON in components and evaluating the expected result.

**Step 2** − Break the functionality into smaller components
 The first Thing React suggests is to create a smaller understandable design of boxes. These boxes will represent the association between the different components and the passing of data flow.

The making of components should be based on the principle of single responsibility. That means a single component should handle a single task.

Creating a component hierarchy will make developers' tasks easier.

**Step 3** − If possible start by making a simple static version

With the use of mock service and smaller components, we can create a static version and build the app thereon.

Creating a static version should not use state modifications. It should play with the passage of props and rendering Ui only. Keeping one-way data flow in React makes it simple and modular

To make it more clear the difference and use case of props and state should be understood very well.

**Step 4** − Identifying the Minimal representation of UI state

For making the app interactive the state should be able to trigger from the relevant component.

Identifying the required mutable state is necessary to build the correct app.

Step 5 − Identify where the state should live −

The state can be shared between the multiple child components. Lifting the state up can be used to make communication between the multiple components. Using state management libraries like Redux solves a lot of issues arising from the state.

React strongly recommends the one-way downflow of data to components.

**Step 6**− Add two-way data flow if required −

The controlled component in form handling is the example of two-way data binding.

---

## Higher-Order Functions

A higher-order function is a function that takes another function as parameter and/or returns a function.

### Taking Functions as Parameters

```
fun calculate(x: Int, y: Int, operation: (Int, Int) -> Int): Int {  // 1
    return operation(x, y)                                          // 2
}
​
fun sum(x: Int, y: Int) = x + y                                     // 3
​
fun main() {
    val sumResult = calculate(4, 5, ::sum)                          // 4
    val mulResult = calculate(4, 5) { a, b -> a * b }               // 5
    println("sumResult $sumResult, mulResult $mulResult")
}
```

1. Declares a higher-order function. It takes two integer parameters, `x` and `y`. Additionally, it takes another function `operation` as a parameter. The `operation` parameters and return type are also defined in the declaration.
2. The higher order function returns the result of `operation` invocation with the supplied arguments.
3. Declares a function that matches the `operation` signature.
4. Invokes the higher-order function passing in two integer values and the function argument `::sum`. `::` is the notation that references a function by name in Kotlin.
5. Invokes the higher-order function passing in a lambda as a function argument. Looks clearer, doesn't it?
  
### Returning Functions

```
fun operation(): (Int) -> Int {                                     // 1
    return ::square
}
​
fun square(x: Int) = x * x                                          // 2
​
fun main() {
    val func = operation()                                          // 3
    println(func(2))                                                // 4
}
```

1. Declares a higher-order function that returns a function. `(Int) -> Int` represents the parameters and return type of the `square` function.
2. Declares a function matching the signature.
3. Invokes `operation` to get the result assigned to a variable. Here `func` becomes `square` which is returned by operation.
4. Invokes `func`. The `square` function is actually executed.
