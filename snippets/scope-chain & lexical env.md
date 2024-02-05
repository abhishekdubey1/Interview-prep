### <div align="center"><h1>Scope Chain & Lexical Environment</h1></div>

<ol start="1">

<li>

**What will be the result of invoking the counter function?**

```javascript
var counter = (function () {
  var count = 0;

  return function () {
    return ++count;
  };
})();

console.log(counter());
console.log(counter());
```

<details>
<summary><b>Answer</b></summary>
<p>

#### Output: 1, 1

</p>
</details>
</li>

<li>

**What will be logged to the console in the following code?**

```javascript
for (var i = 0; i < 3; i++) {
  setTimeout(function () {
    console.log(i);
  }, 0);
}
```

<details>
<summary><b>Answer</b></summary>
<p>

#### Output: 3, 3, 3

</p>
</details>
</li>

<li>

**What will be the logged result of the closure function?**

```javascript
function outer() {
  var x = 30;

  function inner() {
    console.log(x);
  }

  return inner;
}

var closureFn = outer();
closureFn();
```

<details>
<summary><b>Answer</b></summary>
<p>

#### Output: 30

</p>
</details>
</li>

<li>
**Explain the term "Closure" in the context of the scope chain.**

<details>
<summary><b>Answer</b></summary>
<p>

#### Answer:

A closure is formed when a function is defined inside another function, creating a closure over the outer function's scope. This allows the inner function to access and "close over" variables from its outer function, even after the outer function has finished executing.

</p>
</details>
</li>

<li>
**How does the JavaScript engine resolve variable references in the scope chain?**

<details>
<summary><b>Answer</b></summary>
<p>

#### Answer:

When a variable is referenced, the engine looks for it in the current function's Environment Record. If not found, it follows the `[[Scope]]` chain, moving up through the outer lexical environments until it finds the variable or reaches the global scope. If the variable is not found, a ReferenceError is thrown.

</p>
</details>
</li>
<li>
**How does the `let` keyword affect the scope chain in comparison to `var`?**

<details>
<summary><b>Answer</b></summary>
<p>

#### Answer:

Variables declared with `let` have block scope, meaning they are only accessible within the block where they are declared. This is in contrast to `var`, which has function scope. `let` variables are not hoisted to the top of the block like `var`, and they are part of the Temporal Dead Zone until they are declared.

</p>
</details>
</li>

<li>

**What is the Temporal Dead Zone (TDZ) in JavaScript?**

<details>
<summary><b>Answer</b></summary>
<p>

#### Answer:

The Temporal Dead Zone is the period between the start of the block and the actual declaration of a `let` or `const` variable. During this time, accessing the variable results in a `ReferenceError`. It emphasizes the block-scoping behavior of `let` and `const` variables.

</p>
</details>
</li>

<li>

**How does the scope chain behave in arrow functions compared to regular functions?**

<details>
<summary><b>Answer</b></summary>
<p>

#### Answer:

Arrow functions do not have their own `this`, `arguments`, and `super`, and they do not have their own scope. Instead, they inherit these values from the enclosing lexical scope. This behavior is different from regular functions, which have their own `this` and `arguments` binding.

</p>
</details>
</li>

<li>

**Explain the concept of a "Scope Leak."**

<details>
<summary><b>Answer</b></summary>
<p>

#### Answer:

A scope leak occurs when a variable is unintentionally exposed outside its intended scope. This can happen when a variable is declared without `var`, `let`, or `const`, making it global or part of an outer function's scope. Scope leaks can lead to unexpected behavior and bugs.

</p>
</details>
</li>
<li>
**What will be the output of the following code?**

```javascript
function outer() {
  var a = 10;

  if (true) {
    let b = 20;

    if (true) {
      const c = 30;

      function inner() {
        var d = 40;
        console.log(a + b + c + d);
      }

      inner();
    }
  }
}

outer();
```

<details>
<summary><b>Answer</b></summary>
<p>

#### Output: 100

</p>
</details>
</li></ol>
