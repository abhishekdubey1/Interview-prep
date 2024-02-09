<div align="center">
   <h1>Understanding Objects in JavaScript</h1>
</div>

<ol>

   <li>

   **Object Creation**:

   - Explain the various methods for creating objects in JavaScript.

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Answer:
   - Objects can be created using object literals `{}`, `new Object()` syntax, constructor functions, and ES6 classes.
   - Object literals are the simplest way to create objects, where key-value pairs are enclosed in curly braces.
   - The `new Object()` syntax creates an empty object.
   - Constructor functions are traditional functions used with the `new` keyword to create multiple instances of an object.
   - ES6 classes provide a more structured way to create objects using the `class` keyword.

   </p>
   </details>
   </li>

   <li>

   **Properties**:

   - How do you access properties of an object in JavaScript?

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Answer:
   - Properties of an object can be accessed using dot notation (`object.property`) or bracket notation (`object['property']`).
   - Dot notation is more concise and easier to read but cannot be used if the property name contains special characters or starts with a number.
   - Bracket notation is versatile and allows accessing properties with dynamic keys or special characters.

   </p>
   </details>
   </li>

   <li>

   **Methods**:

   - How do you define and invoke methods within objects?

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Answer:
   - Methods are defined as functions within objects.
   - They can be invoked using the object's name followed by dot notation and the method name, e.g., `object.method()`.
   - Methods can access and modify object properties using the `this` keyword to refer to the current object.

   </p>
   </details>
   </li>

   <li>

   **Object Creation**:

   - What will be the output of the following code snippet?

   ```javascript
   const obj1 = {};
   const obj2 = new Object();
   function Obj3() {}
   const obj3 = new Obj3();
   class Obj4 {}
   const obj4 = new Obj4();
   console.log(obj1, obj2, obj3, obj4);
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: `{}`, `{}`, `{}`, `Obj4 {}`
   #### Explanation: `obj1` and `obj2` are created using object literals and `new Object()` syntax, resulting in empty objects. `obj3` is created using a constructor function, and `obj4` is created using an ES6 class.

   </p>
   </details>
   </li>

   <li>

   **Properties**:

   - What will be the output of the following code snippet?

   ```javascript
   const person = { name: 'John', age: 30 };
   console.log(person.name, person['age']);
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: `John 30`
   #### Explanation: Dot notation (`person.name`) and bracket notation (`person['age']`) are used to access properties of the `person` object.

   </p>
   </details>
   </li>

   <li>

   **Methods**:

   - What will be the output of the following code snippet?

   ```javascript
   const calculator = {
     add: function(a, b) { return a + b; },
     subtract: function(a, b) { return a - b; }
   };
   console.log(calculator.add(5, 3), calculator.subtract(7, 2));
   ```

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: `8 5`
   #### Explanation: The `add` and `subtract` methods of the `calculator` object are invoked with arguments `(5, 3)` and `(7, 2)` respectively, resulting in the addition and subtraction of numbers.

   </p>
   </details>
   </li>

   <li>

   **Object Creation**:

   - Create an object named `car` with properties `make`, `model`, and `year` using object literal notation. Output the object.

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: `{ make: 'Toyota', model: 'Corolla', year: 2020 }`
   #### Explanation: 
   ```javascript
   const car = {
     make: 'Toyota',
     model: 'Corolla',
     year: 2020
   };
   console.log(car);
   ```

   </p>
   </details>
   </li>

   <li>

   **Properties**:

   - Add a new property `color` to the `car` object created earlier with the value `'blue'`. Output the updated object.

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: `{ make: 'Toyota', model: 'Corolla', year: 2020, color: 'blue' }`
   #### Explanation: 
   ```javascript
   car.color = 'blue';
   console.log(car);
   ```

   </p>
   </details>
   </li>

   <li>

   **Methods**:

   - Define a method `start` within the `car` object that logs `'Engine started'` when invoked. Output the result of invoking the `start` method.

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: `Engine started`
   #### Explanation: 
   ```javascript
   car.start = function() {
     console.log('Engine started');
   };
   car.start();
   ```

   </p>
   </details>
   </li>

   <li>

   **Object Prototypes and Inheritance**:

   - Create a new object `truck` that inherits properties from the `car` object. Add a new property `capacity` to the `truck` object with the value `5000kg`. Output the `truck` object.

   <br/>
   <details>
   <summary><b>Answer</b></summary>
   <p>

   #### Output: `{ make: 'Toyota', model: 'Corolla', year: 2020, color: 'blue', capacity: '5000kg' }`
   #### Explanation: 
   ```javascript
   const truck = Object.create(car);
   truck.capacity = '5000kg';
   console.log(truck);
   ```

   </p>
   </details>
   </li>

</ol>

