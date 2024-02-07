<div align="center">
   <h1>Understanding Promises in JavaScript</h1>
</div>

<ol starts='1'>
   <li>

   **What will be the output of the following code snippet?**

   ```javascript
   const myPromise = new Promise((resolve, reject) => {
     resolve('Resolved!');
   });

   myPromise.then((data) => {
     console.log(data);
   }).catch((error) => {
     console.error(error);
   }).finally(() => {
     console.log('Finally!');
   });
   ```

   <details>
   <summary><b>Answer</b></summary>
   <p>
   Output: "Resolved!" (followed by "Finally!")
   Explanation: The promise resolves successfully, logs the resolved value, and then executes the finally() method.
   </p>
   </details>
   </li>
   
   <li>

   **What is the purpose of the catch() method in promises?**

   - To handle rejected promises and execute error-handling logic.

   </li>
   
   <li>

   **What is the purpose of the finally() method in promises?**

   - To execute code after either the promise is resolved or rejected, regardless of the outcome.

   </li>
   
   <li>

   **What happens if both then() and catch() methods are chained after a promise?**

   - If the promise resolves, then() executes. If the promise rejects, catch() executes.

   </li>
   
   <li>

   **What will be the output of the following code snippet?**

   ```javascript
   const myPromise = new Promise((resolve, reject) => {
     reject('Rejected!');
   });

   myPromise.then((data) => {
     console.log(data);
   }).catch((error) => {
     console.error(error);
   }).finally(() => {
     console.log('Finally!');
   });
   ```

   <details>
   <summary><b>Answer</b></summary>
   <p>
   Output: "Rejected!" (followed by "Finally!")
   Explanation: The promise rejects, logs the rejection reason, and then executes the finally() method.
   </p>
   </details>
   </li>
   
   <li>

   **What will be the output of the following code snippet?**

   ```javascript
   const myPromise = new Promise((resolve, reject) => {
     throw new Error('Custom Error');
   });

   myPromise.then((data) => {
     console.log(data);
   }).catch((error) => {
     console.error(error.message);
   }).finally(() => {
     console.log('Finally!');
   });
   ```

   <details>
   <summary><b>Answer</b></summary>
   <p>
   Output: "Custom Error" (followed by "Finally!")
   Explanation: The promise throws a custom error, catches it, logs the error message, and then executes the finally() method.
   </p>
   </details>
   </li>
   
   <li>

   **What will be the output of the following code snippet?**

   ```javascript
   const myPromise = new Promise((resolve, reject) => {
     setTimeout(() => {
       resolve('Resolved!');
     }, 1000);
   });

   myPromise.then((data) => {
     console.log(data);
     throw new Error('Custom Error');
   }).catch((error) => {
     console.error(error.message);
   }).finally(() => {
     console.log('Finally!');
   });
   ```

   <details>
   <summary><b>Answer</b></summary>
   <p>
   Output: "Resolved!" (followed by "Custom Error" and "Finally!")
   Explanation: The promise resolves after 1 second, logs the resolved value, then throws a custom error, catches it, logs the error message, and finally executes the finally() method.
   </p>
   </details>
   </li>
   
   <li>

   **What is the purpose of chaining promises using then() method?**

   - To handle asynchronous operations sequentially and avoid callback hell.

   </li>
   
   <li>

   **What will be the output of the following code snippet?**

   ```javascript
   const myPromise = new Promise((resolve, reject) => {
     resolve('Resolved!');
   });

   myPromise.then((data) => {
     console.log(data);
     return 'Additional data';
   }).then((additionalData) => {
     console.log(additionalData);
   });
   ```

   <details>
   <summary><b>Answer</b></summary>
   <p>
   Output: "Resolved!" (followed by "Additional data")
   Explanation: The first then() method logs the resolved data and returns "Additional data", which is then logged by the second then() method.
   </p>
   </details>
   </li>
   
   <li>

   **What is the purpose of the reject() method in promises?**

   - To explicitly reject a promise with a specified reason.

   </li>
   
   <li>

   **What is the purpose of the resolve() method in promises?**

   - To explicitly resolve a promise with a specified value.

   </li>
   
   <li>

   **What will be the output of the following code snippet?**

   ```javascript
   const myPromise = new Promise((resolve, reject) => {
     setTimeout(() => {
       resolve('Resolved!');
     }, 1000);
   });

   myPromise.then((data) => {
     console.log(data.toUpperCase());
   }).catch((error) => {
     console.error(error);
   });
   ```

   <details>
   <summary><b>Answer</b></summary>
   <p>
   Output: "RESOLVED!"
   Explanation: The promise resolves with the string "Resolved!", and the then() method converts it to uppercase and logs it.
   </p>
   </details>
   </li>
   
   <li>

   **What is promise chaining in JavaScript?**

   - It is a technique where multiple then() methods are chained to handle asynchronous operations sequentially.

   </li>
   
   <li>

   **What will be the output of the following code snippet?**

   ```javascript
   const myPromise = new Promise((resolve, reject) => {
     setTimeout(() => {
       resolve('Resolved!');
     }, 1000);
   });

   myPromise.then((data) => {
     console.log(data);
     return new Promise((resolve, reject) => {
       setTimeout(() => {
         resolve('Additional data');
       }, 1000);
     });
   }).then((additionalData) => {
     console.log(additionalData);
   });
   ```

   <details>
   <summary><b>Answer</b></summary>
   <p>
   Output: "Resolved!" (followed by "Additional data")
   Explanation: The first then() method logs the resolved data and returns a new promise, which resolves with "Additional data" after 1 second. The second then() method logs this additional data.
   </p>
   </details>
   </li>
   
   <li>

   **What is the purpose of the then() method in promises?**

   - To handle the resolved state of a promise and execute success-handling logic.

   </li>
   
   <li>

   **What is the purpose of the finally() method in promises?**

   - To execute code after either the promise is resolved or rejected, regardless of the outcome.

   </li>
   
</ol>
