### <div align="center"><h1>Async vs. Defer</h1></div>

<ol>

<li>

**What is the purpose of the `async` attribute in HTML script tags?**

- A: To execute the script asynchronously.
- B: To defer the script until the HTML document is fully parsed.
- C: To block rendering of the HTML page.
- D: To specify the script source.

<details>
<summary><b>Answer</b></summary>
<p>

#### Option: A

</p>
</details>
</li>

<li>

**How does the `defer` attribute differ from `async` in script tags?**

- A: `async` ensures scripts are executed in order, while `defer` allows immediate execution.
- B: `async` blocks HTML parsing, while `defer` waits for HTML parsing to complete.
- C: `async` and `defer` are interchangeable and can be used together.
- D: `async` requires a specific order for script execution, whereas `defer` allows any order.

<details>
<summary><b>Answer</b></summary>
<p>

#### Option: B

</p>
</details>
</li>

<li>

**When might you choose to use the `defer` attribute over `async` in script tags?**

- A: When the script should be executed asynchronously.
- B: When the script relies on DOM being fully parsed before execution.
- C: When the script must block HTML parsing for optimal performance.
- D: When there is no specific preference between `async` and `defer`.

<details>
<summary><b>Answer</b></summary>
<p>

#### Option: B

</p>
</details>
</li>

<li>

**Which scenario is suitable for using the `async` attribute in a script tag?**

- A: When the script should be executed after the HTML document is fully parsed.
- B: When the script relies on the DOM being fully parsed before execution.
- C: When the script can be executed independently and doesn't depend on HTML parsing.
- D: When the script needs to block the rendering of the HTML page.

<details>
<summary><b>Answer</b></summary>
<p>

#### Option: C

</p>
</details>
</li>

<li>

**Provide an example of combining both `async` and `defer` attributes in a script tag.**

- A: `<script src="example.js" async></script>`
- B: `<script src="example.js" defer></script>`
- C: `<script src="example.js" async defer></script>`
- D: `<script src="example.js"></script>`

<details>
<summary><b>Answer</b></summary>
<p>

#### Option: C

</p>
</details>
</li>

<li>

**What happens if you use both `async` and `defer` attributes in the same script tag?**

- A: The `async` attribute takes precedence.
- B: The `defer` attribute takes precedence.
- C: Both attributes cancel each other out.
- D: It depends on the browser.

<details>
<summary><b>Answer</b></summary>
<p>

#### Option: A

</p>
</details>
</li>

<li>

**Explain the impact of using the `async` attribute on script execution order.**

- A: Scripts with `async` are executed in order, regardless of their position in the HTML.
- B: Scripts with `async` are executed immediately, and their order may not be guaranteed.
- C: The `async` attribute has no effect on the script execution order.
- D: Using `async` always ensures sequential execution.

<details>
<summary><b>Answer</b></summary>
<p>

#### Option: B

</p>
</details>
</li>

<li>

**In what scenarios might you prefer using a combination of `async` and `defer` for different scripts on a web page?**

- A: When scripts are independent and can execute in any order.
- B: When scripts have dependencies and must be executed in a specific order.
- C: When scripts should block HTML parsing.
- D: When scripts are short and can be executed inline.

<details>
<summary><b>Answer</b></summary>
<p>

#### Option: A

</p>
</details>
</li>

<li>

**Can the `async` and `defer` attributes be used in inline script tags?**

- A: Yes, for both `async` and `defer`.
- B: Only `async` can be used in inline scripts.
- C: Only `defer` can be used in inline scripts.
- D: No, neither `async` nor `defer` can be used in inline scripts.

<details>
<summary><b>Answer</b></summary>
<p>

#### Option: A

</p>
</details>
</li>

<li>

**How does the `async` attribute impact the rendering of the HTML page?**

- A: It blocks rendering until the script is executed.
- B: It doesn't affect rendering, allowing the HTML to render in parallel.
- C: It significantly slows down the rendering process.
- D: It prioritizes rendering over script execution.

<details>
<summary><b>Answer</b></summary>
<p>

#### Option: B

</p>
</details>
</li>

</ol>
