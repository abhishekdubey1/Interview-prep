**Question 1: Output Based**

```javascript
function greet(name) {
  console.log(`Hello, ${name}!`);
}

function introduce(callback) {
  callback("Alice");
}

introduce(greet);
```

<details>
<summary><b>Answer</b></summary>
<p>

#### Output: Hello, Alice!

</p>
</details>

---

**Question 2: Output Based**

```javascript
document.addEventListener("click", function () {
  console.log("Page Clicked!");
});
```

<details>
<summary><b>Answer</b></summary>
<p>

#### Output: (Will log "Page Clicked!" when the document is clicked)

</p>
</details>

---

**Question 3: Output Based**

```javascript
const numbers = [1, 2, 3, 4];

numbers.forEach(function (num) {
  console.log(num * 2);
});
```

<details>
<summary><b>Answer</b></summary>
<p>

#### Output: 
```
2
4
6
8
```

</p>
</details>

---

**Question 4: Output Based**

```javascript
function eventHandler() {
  console.log("Button Clicked!");
}

document.getElementById("myButton").addEventListener("click", eventHandler);
```

<details>
<summary><b>Answer</b></summary>
<p>

#### Output: (Assuming an HTML button with the id "myButton" exists, it will log "Button Clicked!" when clicked)

</p>
</details>

---

**Question 5: Output Based**

```javascript
const saySomething = function (message) {
  console.log(message);
};

saySomething("Hello World!");
```

<details>
<summary><b>Answer</b></summary>
<p>

#### Output: Hello World!

</p>
</details>

---

**Question 6: Theory Based**

What is a first-class function in JavaScript?

a) It refers to functions that are defined at the top of the script.

b) It means functions can be treated like any other variable, allowing them to be assigned to variables, passed as arguments, and returned from other functions.

<details>
<summary><b>Answer</b></summary>
<p>

#### Answer: b)

</p>
</details>

---

**Question 7: Theory Based**

What is an anonymous function in JavaScript?

a) A function without a name.

b) A function that can only be used within a specific scope.

<details>
<summary><b>Answer</b></summary>
<p>

#### Answer: a)

</p>
</details>

---

**Question 8: Theory Based**

What is a callback function in JavaScript?

a) A function that calls another function.

b) A function passed as an argument to another function, which will be invoked later.

<details>
<summary><b>Answer</b></summary>
<p>

#### Answer: b)

</p>
</details>

---

**Question 9: Theory Based**

What is the purpose of an event listener in JavaScript?

a) To listen for music events in a web page.

b) To respond to specific events (e.g., user actions) by executing a function.

<details>
<summary><b>Answer</b></summary>
<p>

#### Answer: b)

</p>
</details>

---

**Question 10: Theory Based**

How are first-class functions beneficial in JavaScript?

a) They allow functions to be executed only once.

b) They enable functions to be treated as values, facilitating features like higher-order functions.

<details>
<summary><b>Answer</b></summary>
<p>

#### Answer: b)

</p>
</details>
