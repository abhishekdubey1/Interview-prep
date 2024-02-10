<h1>`this` keyword in JavaScript:</h1>

---

1. **Output-based**:
   - What will be the output of the following code snippet?

   ```javascript
   const person = {
     firstName: 'John',
     lastName: 'Doe',
     fullName: function() {
       return this.firstName + ' ' + this.lastName;
     }
   };

   console.log(person.fullName());
   ```

<details>
<summary><b>Answer</b></summary>
<p>

#### Output: "John Doe"
#### Explanation: Inside the `fullName` method, `this` refers to the `person` object, so `this.firstName` and `this.lastName` access the properties of the `person` object.

</p>
</details>

2. **Output-based**:
   - What will be the output of the following code snippet?

   ```javascript
   function greet() {
     console.log('Hello, ' + this.name);
   }

   const obj = { name: 'World', greet: greet };
   greet();
   obj.greet();
   ```

<details>
<summary><b>Answer</b></summary>
<p>

#### Output:
```
Hello, undefined
Hello, World
```
#### Explanation: In the first call to `greet()`, `this` inside the function refers to the global object (in non-strict mode), where `name` is not defined. In the second call (`obj.greet()`), `this` refers to the `obj` object, so it prints `"Hello, World"`.

</p>
</details>

3. **Output-based**:
   - What will be the output of the following code snippet?

   ```javascript
   const obj1 = {
     prop: 'I am obj1',
     method: function() {
       console.log(this.prop);
     }
   };

   const obj2 = { prop: 'I am obj2' };

   obj1.method(); // Output 1
   obj1.method.call(obj2); // Output 2
   ```

<details>
<summary><b>Answer</b></summary>
<p>

#### Output 1: "I am obj1"
#### Output 2: "I am obj2"
#### Explanation: In the first call to `obj1.method()`, `this` refers to `obj1`, so it prints `"I am obj1"`. In the second call using `call()`, `this` is explicitly set to `obj2`, so it prints `"I am obj2"`.

</p>
</details>

4. **Output-based**:
   - What will be the output of the following code snippet?

   ```javascript
   const obj = {
     prop: 'I am obj',
     method: function() {
       setTimeout(function() {
         console.log(this.prop);
       }, 1000);
     }
   };

   obj.method();
   ```

<details>
<summary><b>Answer</b></summary>
<p>

#### Output: undefined
#### Explanation: Inside the `setTimeout` callback function, `this` no longer refers to the `obj` object but to the global object (in non-strict mode) or `undefined` (in strict mode). Therefore, `this.prop` results in `undefined`.

</p>
</details>

5. **Output-based**:
   - What will be the output of the following code snippet?

   ```javascript
   const obj = {
     prop: 'I am obj',
     method: function() {
       setTimeout(() => {
         console.log(this.prop);
       }, 1000);
     }
   };

   obj.method();
   ```

<details>
<summary><b>Answer</b></summary>
<p>

#### Output: "I am obj"
#### Explanation: Arrow functions don't bind their own `this` value but inherit it from the enclosing lexical context. So, inside the arrow function passed to `setTimeout`, `this` refers to the `obj` object.

</p>
</details>

6. **Multiple Choice**:
   - What is the value of `this` inside a regular function declared in strict mode?
     - a) The global object
     - b) The `undefined` value
     - c) The function's context
     - d) It depends on how the function is called

<details>
<summary><b>Answer</b></summary>
<p>

#### Correct Answer: b) The `undefined` value
#### Explanation: In strict mode, `this` inside a regular function is `undefined` if the function is not called as a method of an object or explicitly bound to a context.

</p>
</details>

7. **Output-based**:
   - What will be the output of the following code snippet?

   ```javascript
   const obj = {
     prop: 'I am obj',
     method: () => {
       console.log(this.prop);
     }
   };

   obj.method();
   ```

<details>
<

summary><b>Answer</b></summary>
<p>

#### Output: undefined
#### Explanation: Arrow functions do not have their own `this`. Instead, they inherit `this` from the enclosing lexical context (the global scope in this case), where `this` is `undefined`.

</p>
</details>

8. **Output-based**:
   - What will be the output of the following code snippet?

   ```javascript
   const obj = {
     prop: 'I am obj',
     method: function() {
       return () => {
         console.log(this.prop);
       };
     }
   };

   const innerFunc = obj.method();
   innerFunc();
   ```

<details>
<summary><b>Answer</b></summary>
<p>

#### Output: "I am obj"
#### Explanation: The `method` function returns an arrow function, which captures the `this` value from the lexical context of its surrounding function (`method`), where `this` refers to the `obj` object.

</p>
</details>

9. **Multiple Choice**:
   - Which of the following statements about the `this` keyword is true?
     - a) It always refers to the object where the function was defined
     - b) It always refers to the object where the function is called
     - c) It depends on how the function is called and the function's context
     - d) It is determined by the JavaScript runtime environment

<details>
<summary><b>Answer</b></summary>
<p>

#### Correct Answer: c) It depends on how the function is called and the function's context
#### Explanation: The value of `this` depends on the execution context and how the function is invoked, not just where it was defined.

</p>
</details>

10. **Theory-based**:
    - Explain in your own words what the `this` keyword refers to in JavaScript and how its value is determined.

<details>
<summary><b>Answer</b></summary>
<p>

#### Explanation:
The `this` keyword in JavaScript refers to the context in which a function is executed. Its value is determined dynamically based on how a function is invoked, rather than where it is defined. In non-arrow functions, `this` is determined by the function's execution context, which can be the global object, the object the function is a method of, or any object the function is bound to using methods like `call()`, `apply()`, or `bind()`. Arrow functions, on the other hand, lexically capture `this` from the surrounding code at the time of their definition, so they inherit the value of `this` from their enclosing scope.

</p>
</details>
