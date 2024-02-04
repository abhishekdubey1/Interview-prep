<div align="center">
   <h1>Mixed Concepts in JavaScript</h1>
</div>

<ol>

   <li>

   **What will be the output?**

   ```JS
   // Mixed Concepts - Question 1
   // Concepts: Variable scoping, Closures
   var x = 10;
   function outer() {
     var x = 20;
     function inner() {
       console.log(x);
     }
     return inner;
   }
   var closureFn = outer();
   closureFn();
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: 20
   #### Explanation: The inner function has access to the variable `x` from its closure, which is the `x` from the outer function.

   </p>
   </details>
   </li>

   <!-- Repeat the pattern for the remaining questions -->

   <li>

   **What will be the output?**

   ```JS
   // Mixed Concepts - Question 2
   // Concepts: this keyword
   function example() {
     console.log(this);
     function inner() {
       console.log(this);
     }
     inner();
   }
   example();
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: Window (or global object), Window
   #### Explanation: The first 'this' refers to the global object (Window in a browser environment), and the second 'this' inside `inner()` also refers to the global object.

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // Mixed Concepts - Question 3
   // Concepts: Asynchronous execution, Event loop
   function asyncExample() {
     console.log("Start");
     setTimeout(function () {
       console.log("Timeout");
     }, 0);
     console.log("End");
   }
   asyncExample();
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: Start, End, Timeout
   #### Explanation: The `setTimeout` function is non-blocking, and its callback is placed in the event queue, allowing the "End" to be logged before the "Timeout".

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // Mixed Concepts - Question 4
   // Concepts: Variable hoisting, Block scope
   var a = 5;
   function example() {
     console.log(a);
     if (true) {
       let a = 10;
     }
     console.log(a);
   }
   example();
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: 5, 5
   #### Explanation: The first `console.log(a)` refers to the global variable 'a', and the second `console.log(a)` within the block refers to the local variable 'a'.

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // Mixed Concepts - Question 5
   // Concepts: Closures, IIFE (Immediately Invoked Function Expression)
   var counter = (function () {
     var count = 0;
     return function () {
       return ++count;
     };
   })();
   console.log(counter());
   console.log(counter());
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: 1, 2
   #### Explanation: The `counter` function utilizes closures to create a private variable 'count' that persists across multiple invocations.

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // Mixed Concepts - Question 6
   // Concepts: Closures, Variable binding in a loop
   for (var i = 0; i < 3; i++) {
     setTimeout(function () {
       console.log(i);
     }, 0);
   }
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: 3, 3, 3
   #### Explanation: Due to the asynchronous nature of `setTimeout`, all three callbacks reference the final value of 'i' after the loop completes.

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // Mixed Concepts - Question 7
   // Concepts: Variable scope, Global vs. Local variables
   var x = 10;
   function example() {
     console.log(x);
     x = 20;
   }
   example();
   console.log(x);
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: 10, 20
   #### Explanation: The first `console.log(x)` refers to the global variable 'x', and the second `console.log(x)` within the function refers to the local variable 'x'.

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // Mixed Concepts - Question 8
   // Concepts: Closures, Lexical scoping
   function outer() {
     var x = 30;
     function inner() {
       console.log(x);
     }
     return inner;
   }
   var closureFn = outer();
   closureFn();
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: 30
   #### Explanation: The inner function retains access to the variable 'x' from its lexical scope even after the outer function has finished executing.

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // Mixed Concepts - Question 9
   // Concepts: Variable scoping
   var x = 5;
   function example() {
     var x = 10;
     function inner() {
       console.log(x);
     }
     inner();
   }
   example();
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: 10
   #### Explanation: The inner function has access to the variable 'x' from its lexical scope, which is the 'x' from the function `example()`.

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // Mixed Concepts - Question 10
   // Concepts: let declarations, Block scope
   console.log(a);
   let a = 15;
   console.log(a);
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: ReferenceError: Cannot access 'a' before initialization
   #### Explanation: Variables declared with 'let' are not hoisted to the top, and attempting to access them before declaration results in a ReferenceError.

   </p>
   </details>
   </li>

</ol>
