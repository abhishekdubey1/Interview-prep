**Question 1: Output Based**

```javascript
function example() {
  let a = 10;

  if (true) {
    let b = 20;

    if (true) {
      let a = 30;
      console.log(a + b);
    }
  }
}

example();
```

<details>
<summary><b>Answer</b></summary>
<p>

#### Output: 50

</p>
</details>

---

**Question 2: Output Based**

```javascript
function outer() {
  const x = 5;

  if (true) {
    const x = 10;

    if (true) {
      console.log(x);
    }
  }
}

outer();
```

<details>
<summary><b>Answer</b></summary>
<p>

#### Output: 10

</p>
</details>

---

**Question 3: Output Based**

```javascript
function example() {
  let a = 20;

  if (true) {
    let b = 30;

    if (true) {
      a = 10;
    }
  }

  console.log(a);
}

example();
```

<details>
<summary><b>Answer</b></summary>
<p>

#### Output: 10

</p>
</details>

---

**Question 4: Output Based**

```javascript
function example() {
  let a = 10;

  if (true) {
    let b = 20;

    if (true) {
      const a = 30;

      function inner() {
        let b = 40;
        console.log(a + b);
      }

      inner();
    }
  }
}

example();
```

<details>
<summary><b>Answer</b></summary>
<p>

#### Output: 70

</p>
</details>

---

**Question 5: Output Based**

```javascript
function outer() {
  let a = 5;

  if (true) {
    let a = 10;

    if (true) {
      console.log(a);
    }
  }
}

outer();
```

<details>
<summary><b>Answer</b></summary>
<p>

#### Output: 10

</p>
</details>

---

**Question 6: Theory Based**

Which of the following statements about block scope and shadowing is true?

a) Variables declared with `let` inside a block are hoisted to the top of the block.

b) Variables declared with `let` inside a block can be accessed outside the block.

<details>
<summary><b>Answer</b></summary>
<p>

#### Answer: a)

</p>
</details>

---

**Question 7: Theory Based**

What is the concept of shadowing in JavaScript?

a) It refers to the process of creating a shadow effect in the UI.

b) It occurs when a variable declared inside a local scope has the same name as a variable in the outer scope, causing the inner variable to "shadow" the outer one.

<details>
<summary><b>Answer</b></summary>
<p>

#### Answer: b)

</p>
</details>
