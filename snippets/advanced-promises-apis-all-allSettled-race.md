<div align="center">
   <h1>Understanding Advanced Promise APIs in JavaScript</h1>
</div>

<ol starts='1'>
   <li>

   **What is the purpose of the Promise.all() method?**

   <details>
   <summary><b>Answer</b></summary>
   <p>
   The Promise.all() method is used to handle multiple promises simultaneously. It takes an iterable of promises as input and returns a single Promise that resolves when all of the input promises have resolved, or rejects if any of the promises reject.
   </p>
   </details>
   </li>
   
   <li>

   **What is the purpose of the Promise.allSettled() method?**

   <details>
   <summary><b>Answer</b></summary>
   <p>
   The Promise.allSettled() method returns a promise that resolves after all of the provided promises have settled, i.e., after each promise has either been fulfilled or rejected. It does not short-circuit if any promise rejects and instead waits for all promises to complete.
   </p>
   </details>
   </li>
   
   <li>

   **What is the purpose of the Promise.race() method?**

   <details>
   <summary><b>Answer</b></summary>
   <p>
   The Promise.race() method returns a promise that resolves or rejects as soon as one of the promises in the iterable resolves or rejects, with the value or reason from that promise. It is useful for scenarios where you want to race multiple promises and handle the result of the first resolved promise.
   </p>
   </details>
   </li>
   
   <li>

   **What will be the output of the following code snippet using Promise.all()?**

   ```javascript
   const promise1 = Promise.resolve(1);
   const promise2 = Promise.resolve(2);
   const promise3 = Promise.resolve(3);

   Promise.all([promise1, promise2, promise3]).then((values) => {
     console.log(values);
   });
   ```

   <details>
   <summary><b>Answer</b></summary>
   <p>
   Output: [1, 2, 3]
   Explanation: All promises resolve successfully, and the then() method receives an array containing the resolved values.
   </p>
   </details>
   </li>
   
   <li>

   **What will be the output of the following code snippet using Promise.allSettled()?**

   ```javascript
   const promise1 = new Promise((resolve, reject) => setTimeout(resolve, 1000, 'one'));
   const promise2 = new Promise((resolve, reject) => setTimeout(reject, 2000, 'two'));
   const promises = [promise1, promise2];

   Promise.allSettled(promises).then((results) => {
     results.forEach((result) => {
       console.log(result.status);
     });
   });
   ```

   <details>
   <summary><b>Answer</b></summary>
   <p>
   Output: "fulfilled" (for promise1), "rejected" (for promise2)
   Explanation: The Promise.allSettled() method waits for all promises to settle and returns an array of objects representing the fulfillment statuses of the promises.
   </p>
   </details>
   </li>
   
   <li>

   **What will be the output of the following code snippet using Promise.race()?**

   ```javascript
   const promise1 = new Promise((resolve, reject) => setTimeout(resolve, 1000, 'one'));
   const promise2 = new Promise((resolve, reject) => setTimeout(reject, 2000, 'two'));

   Promise.race([promise1, promise2]).then((value) => {
     console.log(value);
   }).catch((reason) => {
     console.error(reason);
   });
   ```

   <details>
   <summary><b>Answer</b></summary>
   <p>
   Output: "one"
   Explanation: Promise.race() returns the result of the first resolved or rejected promise. In this case, promise1 resolves first with the value "one".
   </p>
   </details>
   </li>
   
   <li>

   **What happens if a promise within a Promise.all() rejects, but Promise.allSettled() is used instead?**

   <details>
   <summary><b>Answer</b></summary>
   <p>
   With Promise.all(), if any promise within the iterable rejects, the entire Promise.all() call immediately rejects with the reason of the first rejected promise. However, with Promise.allSettled(), all promises in the iterable are waited for, and the returned promise resolves only after all of the input promises have either resolved or rejected. Therefore, even if a promise within the iterable rejects, Promise.allSettled() will still wait for all promises to settle before resolving, and the result will include the statuses of all promises.
   </p>
   </details>
   </li>
   
   <li>

   **Explain a scenario where using Promise.race() is beneficial.**

   <details>
   <summary><b>Answer</b></summary>
   <p>
   Promise.race() is beneficial in scenarios where you have multiple asynchronous operations and you want to handle the result of the first completed operation, regardless of whether it resolves or rejects. For example, in a real-time application where you're fetching data from multiple sources, you might use Promise.race() to race the requests and respond to the user with the data from the fastest source, providing a more responsive user experience.
   </p>
   </details>
   </li>
   
   <li>

   **How can you mimic the behavior of Promise.all() using Promise.race()?**

   <details>
   <summary><b>Answer</b></summary>
   <p>
   To mimic the behavior of Promise.all() using Promise.race(), you can create a wrapper function that takes an array of promises as input, creates a new promise, and returns it. Within the wrapper function, you use Promise.race() to race the input promises. If any of the input promises reject, you reject the new promise with the reason of the first rejected promise. Otherwise, if all input promises resolve, you resolve the new promise with an array containing the resolved values of all input promises.
   </p>
   </details>
   </li>
   
   <li>

   **Discuss the differences between Promise.all() and Promise.allSettled().**

   <details>
   <summary><b>Answer</b></summary>
   <p>
   - Promise.all() rejects immediately if any promise within the iterable rejects, while Promise.allSettled() waits for all promises to settle before resolving.
   - Promise.all() returns a rejected promise if any input promise rejects, with the reason of the first rejected promise, while Promise.allSettled() always returns a fulfilled promise with an array of objects representing the fulfillment statuses of the input promises.
   - Promise.all() short-circuits if any promise rejects, while Promise.allSettled() waits for all promises to settle regardless of their outcome.
   </p>
   </details>
   </li>
   
   <li>

   **Explain the potential risks of using Promise.race().**

   <details>
   <summary><b>Answer</b></summary>
   <p>
   One potential risk of using Promise.race() is that it doesn't guarantee resource cleanup for promises that lose the race. If multiple promises are racing, and the loser promises involve operations that need cleanup (e.g., closing network connections, releasing locks), those operations might not be performed, leading to resource leaks or incorrect behavior. Additionally, in some scenarios, using Promise.race() might introduce non-deterministic behavior, making it harder to reason about the code.
   </p>
   </details>
   </li>
   
</ol>
