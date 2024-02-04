<div align="center">
   <h1>Understanding setTimeout and setInterval in JavaScript</h1>
</div>

<ol start="1">

   <li>

   **What will be the output?**

   ```JS
   // setTimeout - Question 16
   console.log("Start");
   setTimeout(function() {
     console.log("Timeout");
   }, 2000);
   console.log("End");
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: "Start", "End", "Timeout"
   #### Explanation: The `setTimeout` function is non-blocking, and the callback is executed after the specified time interval (2 seconds).

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // setInterval - Question 17
   var count = 0;
   var intervalId = setInterval(function() {
     console.log("Interval", count++);
     if (count > 2) {
       clearInterval(intervalId);
     }
   }, 1000);
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: "Interval 0", "Interval 1", "Interval 2"
   #### Explanation: The `setInterval` function repeatedly executes the callback at a specified interval (1 second) until `clearInterval` is called.

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // setTimeout - Question 18
   console.log("Start");
   setTimeout(function() {
     console.log("Timeout");
   }, 0);
   console.log("End");
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: "Start", "End", "Timeout"
   #### Explanation: The `setTimeout` function with a delay of 0 still executes asynchronously after the main thread finishes.

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // setInterval - Question 19
   var count = 0;
   setTimeout(function() {
     var intervalId = setInterval(function() {
       console.log("Interval", count++);
       if (count > 2) {
         clearInterval(intervalId);
       }
     }, 1000);
   }, 2000);
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: "Interval 0", "Interval 1", "Interval 2"
   #### Explanation: The initial `setTimeout` delays the start of the `setInterval`, resulting in the first log after 2 seconds.

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // setTimeout - Question 20
   var count = 0;
   setInterval(function() {
     console.log("Interval", count++);
     if (count > 2) {
       clearInterval(this);
     }
   }, 1000);
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: "Interval 0", "Interval 1", "Interval 2"
   #### Explanation: `this` inside the `setInterval` callback refers to the global object, and `clearInterval(this)` stops the interval.

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // setTimeout - Question 21
   var count = 0;
   setTimeout(function() {
     console.log("Timeout", count++);
   }, 1000);
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: "Timeout 0"
   #### Explanation: The callback is executed once after the specified delay (1 second).

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // setInterval - Question 22
   var count = 0;
   var intervalId = setInterval(function() {
     console.log("Interval", count++);
     if (count > 2) {
       clearInterval(intervalId);
     }
   }, 0);
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: "Interval 0", "Interval 1", "Interval 2"
   #### Explanation: The interval is still asynchronous, and the callback is executed after the main thread finishes.

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // setTimeout - Question 23
   var count = 0;
   setTimeout(function() {
     console.log("Timeout", count++);
   }, 0);
   console.log("End");
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: "End", "Timeout 0"
   #### Explanation: The `setTimeout` callback is still asynchronous, and "End" is logged before the callback.

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // setInterval - Question 24
   var count = 0;
   setInterval(function() {
     console.log("Interval", count++);
   }, 1000);
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: "Interval 0" (repeated every second)
   #### Explanation: The interval continues indefinitely, logging "Interval" with an incrementing count.

   </p>
   </details>
   </li>

   <li>

   **What will be the output?**

   ```JS
   // setInterval - Question 25
   var count = 0;
   setTimeout(function() {
     var intervalId = setInterval(function() {
       console.log("Interval", count++);
       if (count > 2) {
         clearInterval(intervalId);
       }
     }, 1000);
   }, 2000);
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: "Interval 0", "Interval 1", "Interval 2"
   #### Explanation: The initial `setTimeout` delays the start of the `setInterval`, resulting in the first log after 2 seconds.

   </p>
   </details>
   </li>

</ol>
