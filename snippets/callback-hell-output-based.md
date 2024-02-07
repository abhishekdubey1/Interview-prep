<div align="center">
   <h1>Callback Hell in JavaScript</h1>
</div>

<ol>

   <li>

   **What will be the output of the following code snippet?**

   ```javascript
   function fetchData(callback) {
     setTimeout(() => {
       callback('Data fetched');
     }, 1000);
   }

   fetchData((data) => {
     console.log(data);
   });
   ```

   <details>
   <summary><b>Answer</b></summary>
   <p>
   Output: "Data fetched"
   Explanation: The fetchData function asynchronously fetches data and invokes the callback function with the fetched data after 1 second.
   </p>
   </details>
   </li>
   
   <li>

   **What is the output of the following code snippet?**

   ```javascript
   function fetchData(callback) {
     setTimeout(() => {
       callback('First data');
       setTimeout(() => {
         callback('Second data');
       }, 1000);
     }, 1000);
   }

   fetchData((data) => {
     console.log(data);
   });
   ```

   <details>
   <summary><b>Answer</b></summary>
   <p>
   Output: "First data" (followed by "Second data" after 1 second)
   Explanation: The fetchData function invokes the callback with "First data" after 1 second, then schedules another callback invocation with "Second data" after another second.
   </p>
   </details>
   </li>
   
   <li>

   **What will be the output of the following code snippet?**

   ```javascript
   function fetchData(callback) {
     setTimeout(() => {
       callback('First data');
       setTimeout(() => {
         callback('Second data');
         setTimeout(() => {
           callback('Third data');
         }, 1000);
       }, 1000);
     }, 1000);
   }

   fetchData((data) => {
     console.log(data);
   });
   ```

   <details>
   <summary><b>Answer</b></summary>
   <p>
   Output: "First data" (followed by "Second data" after 1 second, then "Third data" after another second)
   Explanation: The fetchData function invokes the callback with "First data" after 1 second, then schedules callbacks for "Second data" and "Third data" with additional delays.
   </p>
   </details>
   </li>
   
   <li>

   **What is the output of the following code snippet?**

   ```javascript
   function fetchData(callback) {
     setTimeout(() => {
       callback('First data');
       setTimeout(() => {
         callback('Second data');
         setTimeout(() => {
           callback('Third data');
           setTimeout(() => {
             callback('Fourth data');
           }, 1000);
         }, 1000);
       }, 1000);
     }, 1000);
   }

   fetchData((data) => {
     console.log(data);
   });
   ```

   <details>
   <summary><b>Answer</b></summary>
   <p>
   Output: "First data" (followed by "Second data", "Third data", and "Fourth data" with 1-second intervals)
   Explanation: The fetchData function schedules multiple callbacks with increasing delays, resulting in sequential output of the fetched data.
   </p>
   </details>
   </li>
   
   <li>

   **What will be the output of the following code snippet?**

   ```javascript
   function fetchData(callback) {
     setTimeout(() => {
       callback('First data');
       setTimeout(() => {
         callback('Second data');
         setTimeout(() => {
           callback('Third data');
           setTimeout(() => {
             callback('Fourth data');
             setTimeout(() => {
               callback('Fifth data');
             }, 1000);
           }, 1000);
         }, 1000);
       }, 1000);
     }, 1000);
   }

   fetchData((data) => {
     console.log(data);
   });
   ```

   <details>
   <summary><b>Answer</b></summary>
   <p>
   Output: "First data" (followed by "Second data", "Third data", "Fourth data", and "Fifth data" with 1-second intervals)
   Explanation: The fetchData function schedules multiple callbacks with increasing delays, resulting in sequential output of the fetched data.
   </p>
   </details>
   </li>
   
   <li>

   **What is the output of the following code snippet?**

   ```javascript
   function fetchData(callback) {
     setTimeout(() => {
       callback('First data');
       setTimeout(() => {
         callback('Second data');
         setTimeout(() => {
           callback('Third data');
           setTimeout(() => {
             callback('Fourth data');
             setTimeout(() => {
               callback('Fifth data');
               setTimeout(() => {
                 callback('Sixth data');
               }, 1000);
             }, 1000);
           }, 1000);
         }, 1000);
       }, 1000);
     }, 1000);
   }

   fetchData((data) => {
     console.log(data);
   });
   ```

   <details>
   <summary><b>Answer</b></summary>
   <p>
   Output: "First data" (followed by "Second data", "Third data", "Fourth data", "Fifth data", and "Sixth data" with 1-second intervals)
   Explanation: The fetchData function schedules multiple callbacks with increasing delays, resulting in sequential output of the fetched data.
   </p>
   </details>
   </li>
   
   <li>

   **What will be the output of the following code snippet?**

   ```javascript
   function fetchData(callback) {
     setTimeout(() => {
       callback('First data');
       setTimeout(() => {
         callback('Second data');
         setTimeout(() => {
           callback('Third data');
           setTimeout(() => {
             callback('Fourth data');
             setTimeout(() => {
               callback('Fifth data');
               setTimeout(() => {
                 callback('Sixth data');
                 setTimeout(() => {
                   callback('Seventh data');
                 }, 1000);
               }, 1000);
             }, 1000);
           }, 1000);
         }, 1000);
       }, 1000);
     }, 1000);
   }

   fetchData((data) => {
     console.log(data);
   });
   ```

   <details>
   <summary><b>Answer</b></summary
