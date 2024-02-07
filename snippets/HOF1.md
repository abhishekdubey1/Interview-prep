**Question 1: Output Based (Map)**

```javascript
const numbers = [1, 2, 3, 4, 5];

const doubledNumbers = numbers.map(num => num * 2);

console.log(doubledNumbers);
```

<details>
<summary><b>Answer</b></summary>
<p>

#### Output: [2, 4, 6, 8, 10]

</p>
</details>

---

**Question 2: Output Based (Filter)**

```javascript
const numbers = [1, 2, 3, 4, 5];

const evenNumbers = numbers.filter(num => num % 2 === 0);

console.log(evenNumbers);
```

<details>
<summary><b>Answer</b></summary>
<p>

#### Output: [2, 4]

</p>
</details>

---

**Question 3: Output Based (Reduce)**

```javascript
const numbers = [1, 2, 3, 4, 5];

const sum = numbers.reduce((acc, curr) => acc + curr, 0);

console.log(sum);
```

<details>
<summary><b>Answer</b></summary>
<p>

#### Output: 15

</p>
</details>

---

**Question 4: Output Based (Map)**

```javascript
const words = ["hello", "world", "how", "are", "you"];

const upperCaseWords = words.map(word => word.toUpperCase());

console.log(upperCaseWords);
```

<details>
<summary><b>Answer</b></summary>
<p>

#### Output: ["HELLO", "WORLD", "HOW", "ARE", "YOU"]

</p>
</details>

---

**Question 5: Output Based (Filter)**

```javascript
const numbers = [1, 2, 3, 4, 5];

const oddNumbers = numbers.filter(num => num % 2 !== 0);

console.log(oddNumbers);
```

<details>
<summary><b>Answer</b></summary>
<p>

#### Output: [1, 3, 5]

</p>
</details>

---

**Question 6: Output Based (Reduce)**

```javascript
const numbers = [1, 2, 3, 4, 5];

const product = numbers.reduce((acc, curr) => acc * curr, 1);

console.log(product);
```

<details>
<summary><b>Answer</b></summary>
<p>

#### Output: 120

</p>
</details>

---

**Question 7: Theory Based (Map)**

What does the `map` method do in JavaScript?

a) Removes elements from an array based on a condition.

b) Creates a new array by applying a function to each element in the original array.

c) Sorts the elements of an array in ascending order.

<details>
<summary><b>Answer</b></summary>
<p>

#### Answer: b) Creates a new array by applying a function to each element in the original array.

</p>
</details>

---

**Question 8: Theory Based (Filter)**

What does the `filter` method do in JavaScript?

a) Modifies each element of an array based on a condition.

b) Creates a new array with only the elements that pass a test specified by a given function.

c) Finds the first occurrence of a specified value in an array and returns its index.

<details>
<summary><b>Answer</b></summary>
<p>

#### Answer: b) Creates a new array with only the elements that pass a test specified by a given function.

</p>
</details>

---

**Question 9: Theory Based (Reduce)**

What does the `reduce` method do in JavaScript?

a) Returns the first element in an array that satisfies a provided testing function.

b) Applies a function against an accumulator and each element in the array to reduce it to a single value.

c) Reverses the order of the elements in an array.

<details>
<summary><b>Answer</b></summary>
<p>

#### Answer: b) Applies a function against an accumulator and each element in the array to reduce it to a single value.

</p>
</details>

---

**Question 10: Higher Order Functions**

Which of the following functions is a higher order function?

a) `forEach`

b) `map`

c) `reduce`

<details>
<summary><b>Answer</b></summary>
<p>

#### Answer: All of the above (forEach, map, and reduce) are higher order functions.

</p>
</details>

Sure, here are additional questions:

---

**Question 11: Output Based (Map)**

```javascript
const names = ["Alice", "Bob", "Charlie"];

const nameLengths = names.map(name => name.length);

console.log(nameLengths);
```

<details>
<summary><b>Answer</b></summary>
<p>

#### Output: [5, 3, 7]

</p>
</details>

---

**Question 12: Output Based (Filter)**

```javascript
const numbers = [10, 20, 30, 40, 50];

const filteredNumbers = numbers.filter(num => num > 25);

console.log(filteredNumbers);
```

<details>
<summary><b>Answer</b></summary>
<p>

#### Output: [30, 40, 50]

</p>
</details>

---

**Question 13: Output Based (Reduce)**

```javascript
const words = ["apple", "banana", "orange"];

const concatenatedWords = words.reduce((acc, curr) => acc + curr, "");

console.log(concatenatedWords);
```

<details>
<summary><b>Answer</b></summary>
<p>

#### Output: "applebananaorange"

</p>
</details>

---

**Question 14: Higher Order Functions**

Which of the following functions returns a new array with the elements that satisfy a provided condition?

a) `forEach`

b) `map`

c) `filter`

<details>
<summary><b>Answer</b></summary>
<p>

#### Answer: c) `filter`

</p>
</details>

---

**Question 15: Theory Based**

What is the purpose of a callback function in JavaScript?

a) To perform an asynchronous operation.

b) To modify each element of an array.

c) To be passed as an argument to another function, which is then invoked later in the program execution.

<details>
<summary><b>Answer</b></summary>
<p>

#### Answer: c) To be passed as an argument to another function, which is then invoked later in the program execution.

</p>
</details>
