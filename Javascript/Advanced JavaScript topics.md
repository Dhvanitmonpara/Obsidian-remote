---
sticker: lucide//chevron-up
---
# Date() function

- **Purpose:** 
  - Creates a new Date object that represents a specific point in time.
  - Used to work with dates and times in JavaScript.

- **Syntax:** 
  ```javascript
  let currentDate = new Date();
  ```
  - The `Date()` function can also take parameters to specify a particular date and time:
    ```javascript
    let specificDate = new Date(year, monthIndex, day, hour, minute, second, millisecond);
    ```

- **Return Value:**
  - A `Date` object representing the current date and time when no parameters are passed.
  - A `Date` object representing the specified date and time when parameters are provided.

- **Parameters:** 
  - `year` (optional): The year (e.g., 2022).
  - `monthIndex` (optional): The month, specified as a number from 0 (January) to 11 (December).
  - `day` (optional): The day of the month, from 1 to 31.
  - `hour` (optional): The hour, from 0 to 23.
  - `minute` (optional): The minute, from 0 to 59.
  - `second` (optional): The second, from 0 to 59.
  - `millisecond` (optional): The millisecond, from 0 to 999.

- **Methods:**
  - `getDate()`: Returns the day of the month (from 1 to 31).
  - `getDay()`: Returns the day of the week (from 0 for Sunday to 6 for Saturday).
  - `getMonth()`: Returns the month (from 0 for January to 11 for December).
  - `getFullYear()`: Returns the year (four digits).
  - `getHours()`: Returns the hour (from 0 to 23).
  - `getMinutes()`: Returns the minutes (from 0 to 59).
  - `getSeconds()`: Returns the seconds (from 0 to 59).
  - `getMilliseconds()`: Returns the milliseconds (from 0 to 999).
  - `toString()`: Returns a string representation of the date and time.
  - Many more methods for manipulating and formatting dates.

- **Examples:**
  ```javascript
  let currentDate = new Date();
  console.log(currentDate);
  // Output: Current date and time

  let specificDate = new Date(2022, 0, 1);
  console.log(specificDate);
  // Output: January 1, 2022

  console.log(specificDate.getMonth()); 
  // Output: 0 (January)

  console.log(specificDate.getDay()); 
  // Output: 6 (Saturday)
  ```

- **Note:**
  - Month indices are zero-based (0 for January, 11 for December).
  - Timezone considerations should be taken into account when working with dates.

```js
let currentDate = new Date();

let currentMonth = currentDate.getMonth();
console.log(currentMonth);
```

# Behaviour of `this` keyword

The `this` keyword in JavaScript behaves differently depending on how and where it is used. Here's an overview of its behavior:

1. **In Global Scope:**
   - In the global scope (outside of any function), `this` refers to the global object. In a web browser, the global object is `window`.

2. **In Function Scope:**
   - In a regular function (not in strict mode), `this` refers to the global object (`window` in a browser) when the function is called without an explicit context.
   - In strict mode, if a function is called without an explicit context, `this` remains `undefined`.

3. **In Object Methods:**
   - In an object method, `this` refers to the object that the method is called on. It allows the method to access and modify properties of the object.

4. **In Constructor Functions:**
   - In a constructor function (a function used with the `new` keyword to create objects), `this` refers to the newly created instance of the object.
   - When a constructor function is invoked with `new`, `this` inside the function points to the newly created object.

5. **In Event Handlers:**
   - In event handlers or callback functions attached to DOM elements, `this` typically refers to the element that triggered the event.
   - However, in modern JavaScript, using arrow functions in event handlers changes the behavior of `this`, making it lexically scoped (not bound to the element).

6. **Using Call, Apply, or Bind:**
   - The `call()`, `apply()`, and `bind()` methods allow you to specify the value of `this` explicitly when invoking a function.
   - `call()` and `apply()` immediately invoke the function, while `bind()` returns a new function with the specified `this` value bound, without invoking the function immediately.

7. **Arrow Functions:**
   - Arrow functions do not have their own `this` context. Instead, they inherit `this` from the enclosing lexical context (the context in which they are defined).

Understanding the behavior of `this` is crucial for writing correct and maintainable JavaScript code, especially in object-oriented and event-driven programming paradigms. It's important to pay attention to how `this` is used in different contexts to avoid unexpected behavior and bugs.

# IIFE

**Immediately Invoked Function Expressions (IIFE)**

- **Definition:**
  - An Immediately Invoked Function Expression (IIFE) is a JavaScript design pattern that executes a function immediately after it's created.

- **Syntax:**
  ```javascript
  (function() {
    // code to be executed immediately
  })();
  ```
  - Alternatively, you can wrap the entire function expression in parentheses to make it more readable: `(() => { /* code */ })();`

- **Purpose:**
  - Encapsulates code to avoid polluting the global scope.
  - Creates a new scope for variables, preventing them from conflicting with variables in other parts of the program.
  - Useful for initializing variables, defining utility functions, or executing setup code.

- **Benefits:**
  - Avoids naming collisions: Variables and functions declared within an IIFE are local to the function and do not pollute the global namespace.
  - Encapsulation: Helps maintain clean and modular code by encapsulating functionality within a private scope.
  - Self-contained: Allows the creation of modules that can be easily included in other scripts without causing conflicts.

- **Usage:**
  - Initializing variables:
    ```javascript
    (function() {
      var x = 10;
      console.log(x); // Output: 10
    })();
    ```
  - Avoiding global namespace pollution:
    ```javascript
    (function() {
      var utility = {
        // utility functions
      };
      // use utility functions internally
    })();
    ```

- **Parameter Passing:**
  - You can pass parameters to an IIFE:
    ```javascript
    (function(msg) {
      console.log(msg);
    })("Hello, World!"); // Output: Hello, World!
    ```

- **Common Mistake:**
  - Forgetting the parentheses around the function expression can lead to syntax errors:
    ```javascript
    // SyntaxError: Unexpected token (
    function() {
      // code
    }();
    ```

- **Use Cases:**
  - Modularizing code.
  - Creating isolated scopes.
  - Defining private variables and functions.
  - Bootstrapping applications.

- **Conclusion:**
  - IIFEs provide a convenient way to execute code immediately while maintaining a clean and encapsulated scope.
  - They are commonly used in JavaScript development to avoid global namespace pollution and create modular and maintainable code.

IIFEs are a powerful tool in JavaScript for creating self-contained and modular code, particularly in situations where you want to avoid polluting the global namespace or need to create isolated scopes.

# 