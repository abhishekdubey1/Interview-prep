<div align="center">
   <h1>JavaScript Window and This Keyword</h1>
</div>

<ol>

   <li>

   **What will be the output?**

   ```JS
   // Window and This Keyword - Question 1
   function example1() {
     console.log(this);
   }
   example1();
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: Window (or global object)
   #### Explanation: In a global context, `this` refers to the global object (Window in a browser environment).

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // Window and This Keyword - Question 2
   function example2() {
     function inner() {
       console.log(this);
     }
     inner();
   }
   example2();
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: Window (or global object)
   #### Explanation: The `this` inside `inner()` also refers to the global object in a global context.

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // Window and This Keyword - Question 3
   var obj = {
     prop: "I am an object property",
     example3: function() {
       console.log(this.prop);
     }
   };
   obj.example3();
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: "I am an object property"
   #### Explanation: In a method, `this` refers to the object that the method is called on (`obj` in this case).

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // Window and This Keyword - Question 4
   var obj = {
     prop: "I am an object property",
     example4: function() {
       function inner() {
         console.log(this);
       }
       inner();
     }
   };
   obj.example4();
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: Window (or global object)
   #### Explanation: The `this` inside `inner()` refers to the global object because `inner()` is a regular function, not a method.

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // Window and This Keyword - Question 5
   var obj = {
     prop: "I am an object property",
     example5: function() {
       var self = this;
       function inner() {
         console.log(self.prop);
       }
       inner();
     }
   };
   obj.example5();
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: "I am an object property"
   #### Explanation: Using a variable (`self`) to store the reference to `this` allows access to the object property inside `inner()`.

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // Window and This Keyword - Question 6
   function example6() {
     console.log(this);
   }
   var boundFunction = example6.bind("Bound Context");
   boundFunction();
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: "Bound Context"
   #### Explanation: The `bind` method creates a new function with a specified `this` value, and calling that function logs the specified context.

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // Window and This Keyword - Question 7
   var obj = {
     prop: "I am an object property",
     example7: function() {
       setTimeout(function() {
         console.log(this.prop);
       }, 0);
     }
   };
   obj.example7();
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: undefined
   #### Explanation: Inside the `setTimeout` callback, `this` does not refer to the object (`obj`), resulting in `undefined`.

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // Window and This Keyword - Question 8
   var obj = {
     prop: "I am an object property",
     example8: function() {
       setTimeout(() => {
         console.log(this.prop);
       }, 0);
     }
   };
   obj.example8();
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: "I am an object property"
   #### Explanation: Arrow functions do not have their own `this` context, so they inherit it from the enclosing scope (`example8`), which is the object (`obj`).

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // Window and This Keyword - Question 9
   function example9() {
     this.prop = "I am a global object property";
   }
   example9();
   console.log(prop);
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: "I am a global object property"
   #### Explanation: When `example9` is called, it sets the `prop` property on the global object (Window in a browser environment).

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // Window and This Keyword - Question 10
   function example10() {
     this.prop = "I am a global object property";
     setTimeout(function() {
       console.log(this.prop);
     }, 0);
   }
   example10();
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: undefined
   #### Explanation: Inside the `setTimeout` callback, `this` does not refer to the global object, resulting in `undefined`.

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // Understanding "this" - Question 11
   var obj = {
     prop: "I am an object property",
     example11: function() {
       console.log(this.prop);
     }
   };
   var globalFunc = obj.example11;
   globalFunc();
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: undefined
   #### Explanation: When calling `globalFunc`, `this` is not bound to the object (`obj`), resulting in `undefined`.

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // Understanding "this" - Question 12
   var obj = {
     prop: "I am an object property",
     example12: function() {
       setTimeout(function() {
         console.log(this.prop);
       }, 0);
     }
   };
   obj.example12();
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: undefined
   #### Explanation: Inside the `setTimeout` callback, `this` is not bound to the object (`obj`), resulting in `undefined`.

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // Understanding "this" - Question 13
   var obj = {
     prop: "I am an object property",
     example13: function() {
       setTimeout(() => {
         console.log(this.prop);
       }, 0);
     }
   };
   obj.example13();
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: "I am an object property"
   #### Explanation: Arrow functions inherit `this` from the enclosing scope (`example13`), which is the object (`obj`).

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // Understanding "this" - Question 14
   function example14() {
     console.log(this);
   }
   var boundFunc = example14.bind("Bound Context");
   boundFunc.call("Call Context");
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: "Bound Context"
   #### Explanation: The `bind` method takes precedence over the `call` method, so `this` is determined by the `bind` context.

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // Understanding "this" - Question 15
   var obj = {
     prop: "I am an object property",
     example15: function() {
       setTimeout(function() {
         console.log(this.prop);
       }.bind(obj), 0);
     }
   };
   obj.example15();
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: "I am an object property"
   #### Explanation: The `bind` method explicitly binds `this` to the object (`obj`) inside the `setTimeout` callback.

   </p>
   </details>
   </li>

</ol>
