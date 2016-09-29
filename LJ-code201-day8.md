# LJ Code 201 - Day 8
**How to Structure Code**
- Set up data
    - Types of Data:
        - var
- Define our actions
    - Types of actions:
        - functions
- Execute our actions
    - Types of execution;
        - functions calls (i.e. `function();` )

**Why to structure code this way**
- for readability
- This is widely considered best convention

**Function Declarations vs Function Expressions**
- Function Declarations
    -  Example
        - `function createFunction() {}`
    - Can be executed/called (i.e. `createFunction();` ) higher in the code than they are declared.
    - Function declarations are available as soon as the the JS interpreter starts executing the code because they are saved in memory when the JS interpreter makes it’s initial read pass.
- Function Expressions
    - Example
        - `var varName = function() {}`
    - Cannot be executed/called (i.e. `varName();` ) until after the function has been declared.
    - Function expressions are not available until after the the JS interpreter has it’s second (executing) read through of the code. On the first pass through the code the JS interpreter only looks at the varName and stores that in memory but does not store any of the actions the function does inside of the memory.
        - this is the opposite of function declarations which stores all of the actions of a function declaration on the initial read pass through of the code so that the function can then be called higher in the code because the browser memory already holds all of the actions of all of the declared functions.
- Why you might want to use function expressions instead of function declarations
    - to save browser memory (i.e. speed)
    - it’s more elegant to use function declarations for things that are always executed where as it is more elegant to use function expressions for functions we won’t always use.

**JavaScript Events**

- Async is one of the primary values that events provide.
- Creating events (very general)
    - identify in the DOM where the event listener should be listening
        - `var listener = document.getElementById(‘ID used in HTML’);`
    - create the event listener
        - `listener.addEventListener(‘event’, functionName, eventFlow);`
        - for our purposes we don’t need the eventFlow at this time.
    - Attach event handler to event listener that executes code.

    ```
        function functionName (event) {
        // code to run after event listener fires
}
```

    - For event functions we need to use the parameter of “event” or “e”

**HTML Forms**

- with a form you want to attach event listeners to the form (not the submit button)
    - need to set an ID to the form tag so that it can be accessed via the event listener.
- Fieldset isn’t needed but it does provide some structure as well as the border to the form
- Legend tag adds a title to the form and should be added directly after the fieldset
- Label sits just above it’s corresponding input.
    - uses an attribute of “for” that matches the “name” attribute on the corresponding input
- Input
    - uses an attribute of “name” (see above) and “type”
    - “size" attribute will set the width of the input box
    - there are other attributes that can be added
