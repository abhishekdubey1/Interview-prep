
<div align="center">
   <h1>JS Execution questions</h1>
</div>

<ol>

   <li>

   **What will be the output?**

   ```JS
   // Question 1: Variable Hoisting
   console.log(a);
   var a = 5;
   console.log(a);
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: undefined, 5
   #### Explanation: Variable declarations are hoisted to the top, but only the declaration is hoisted, not the assignment.

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // Question 2: Function Hoisting
   greet();
   function greet() {
      console.log("Hello!");
   }
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: Hello!
   #### Explanation: Function declarations are hoisted entirely, so the function can be called before its declaration.

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // Question 3: Scope and Execution Context
   var x = 10;
   function example() {
      console.log(x);
      var x = 20;
   }
   example();
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: undefined
   #### Explanation: Variable `x` is hoisted, but the `console.log(x)` is executed before `x` is assigned the value 20.

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // Question 4: Global vs. Local Variables
   var x = 30;
   function printX() {
      console.log(x);
   }
   function updateX() {
      var x = 50;
      printX();
   }
   updateX();
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: 30
   #### Explanation: The `printX` function uses the global variable `x`, not the local variable `x` inside the `updateX` function.

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // Question 5: Closures
   function outer() {
      var outerVar = "I am outside!";
      function inner() {
         console.log(outerVar);
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

   #### Output: I am outside!
   #### Explanation: The inner function retains access to the `outerVar` even after the outer function has finished executing.

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // Question 6: This Keyword
   function showThis() {
      console.log(this);
   }
   showThis();
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: Window (or global object in a browser environment)
   #### Explanation: In a global context, 'this' refers to the global object.

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // Question 7: Lexical Scoping
   function outer() {
      var x = 10;
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

   #### Output: 10
   #### Explanation: The inner function retains access to the variable `x` from its lexical scope, even after the outer function has finished executing.

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // Question 8: Asynchronous Execution
   console.log("Start");
   setTimeout(function () {
      console.log("Timeout");
   }, 0);
   console.log("End");
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>


   <p>

   #### Output: Start, End, Timeout
   #### Explanation: The setTimeout function is non-blocking, so "Timeout" is logged after the main thread finishes executing "End".

   </p>
   </details>
   </li>

</ol>
