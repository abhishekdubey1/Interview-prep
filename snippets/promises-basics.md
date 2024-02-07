<div align="center">
   <h1>Promise Basics in JavaScript</h1>
</div>

<ol>

   <li>

   **Question 1: What is the output of the following code snippet?**

   ```javascript
   const myPromise = new Promise((resolve, reject) => {
     setTimeout(() => {
       resolve('Resolved!');
     }, 1000);
   });

   myPromise.then((data) => {
     console.log(data);
   });
   ```

   <details>
   <summary><b>Answer</b></summary>
   <p>
   Output: "Resolved!"
   Explanation: The promise resolves after 1 second, and the then() method logs the resolved value.
   </p>
   </details>
   </li>
   
   <li>

   **Question 2: What is the output of the following code snippet?**

   ```javascript
   const myPromise = new Promise((resolve, reject) => {
     setTimeout(() => {
       reject('Rejected!');
     }, 1000);
   });

   myPromise.catch((error) => {
     console.log(error);
   });
   ```

   <details>
   <summary><b>Answer</b></summary>
   <p>
   Output: "Rejected!"
   Explanation: The promise rejects after 1 second, and the catch() method logs the rejection reason.
   </p>
   </details>
   </li>
   
   <li>

   **Question 3: What will be the output of the following code snippet?**

   ```javascript
   const myPromise = new Promise((resolve, reject) => {
     setTimeout(() => {
       resolve('Resolved!');
     }, 1000);
   });

   myPromise.then((data) => {
     console.log(data);
   }).catch((error) => {
     console.error(error);
   });
   ```

   <details>
   <summary><b>Answer</b></summary>
   <p>
   Output: "Resolved!"
   Explanation: The promise resolves after 1 second, and the then() method logs the resolved value. Since there is no rejection, catch() is not executed.
   </p>
   </details>
   </li>
   
   <li>

   **Question 4: What is the output of the following code snippet?**

   ```javascript
   const myPromise = new Promise((resolve, reject) => {
     setTimeout(() => {
       reject('Rejected!');
     }, 1000);
   });

   myPromise.then((data) => {
     console.log(data);
   }).catch((error) => {
     console.error(error);
   });
   ```

   <details>
   <summary><b>Answer</b></summary>
   <p>
   Output: "Rejected!"
   Explanation: The promise rejects after 1 second, and the catch() method logs the rejection reason.
   </p>
   </details>
   </li>
   
   <li>

   **Question 5: What will be the output of the following code snippet?**

   ```javascript
   const myPromise = new Promise((resolve, reject) => {
     reject('Rejected!');
   });

   myPromise.then((data) => {
     console.log(data);
   }).catch((error) => {
     console.error(error);
   });
   ```

   <details>
   <summary><b>Answer</b></summary>
   <p>
   Output: "Rejected!"
   Explanation: The promise is immediately rejected, and the catch() method logs the rejection reason.
   </p>
   </details>
   </li>
   
   <li>

   **Question 6: What is the output of the following code snippet?**

   ```javascript
   const myPromise = new Promise((resolve, reject) => {
     resolve('Resolved!');
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

   **Question 7: What will be the output of the following code snippet?**

   ```javascript
   const myPromise = new Promise((resolve, reject) => {
     resolve('Resolved!');
   });

   myPromise.then((data) => {
     throw new Error('Custom Error');
   }).catch((error) => {
     console.error(error.message);
   });
   ```

   <details>
   <summary><b>Answer</b></summary>
   <p>
   Output: "Custom Error"
   Explanation: The then() method throws a custom error, and the catch() method logs the error message.
   </p>
   </details>
   </li>
   
   <li>

   **Question 8: What is the output of the following code snippet?**

   ```javascript
   const myPromise = new Promise((resolve, reject) => {
     setTimeout(() => {
       resolve('Resolved!');
     }, 1000);
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

   **Question 9: What is the output of the following code snippet?**

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

   **Question 10: What will be the output of the following code snippet?**

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
         reject('Additional data');
       }, 1000);
     });
   }).catch((error) => {
     console.error(error);


   });
   ```

   <details>
   <summary><b>Answer</b></summary>
   <p>
   Output: "Resolved!" (followed by "Additional data")
   Explanation: The first then() method logs the resolved data and returns a new promise, which rejects with "Additional data" after 1 second. The catch() method logs this rejection reason.
   </p>
   </details>
   </li>

</ol>
