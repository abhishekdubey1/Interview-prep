<div align="center">
   <h1>Interview Questions on CSS Fundamentals</h1>
</div>

<ol starts='1'>
   <li>

   **Explain the concept of the CSS Box Model and its components.**

   <details>
   <summary><b>Answer</b></summary>
   <p>
   The CSS Box Model describes the layout of elements on a webpage as a series of rectangular boxes. It consists of four main components:
   - Content: The actual content of the element, such as text, images, or other media.
   - Padding: The space between the content and the element's border.
   - Border: A line that surrounds the padding and content of the element.
   - Margin: The space outside the border, which separates the element from neighboring elements.
   </p>
   </details>
   </li>
   
   <li>

   **Differentiate between the display property values: block, inline, and inline-block.**

   <details>
   <summary><b>Answer</b></summary>
   <p>
   - Block: Elements with display: block; take up the full width available and start on a new line. They stack vertically, one after another.
   - Inline: Elements with display: inline; only take up as much width as necessary and do not force new lines. They flow within the content, alongside other inline elements.
   - Inline-Block: Elements with display: inline-block; behave like inline elements in terms of flow but can have block-level properties like width and height. They allow for elements to have block properties while remaining in the flow of the document.
   </p>
   </details>
   </li>
   
   <li>

   **Describe the positioning values in CSS: static, relative, absolute, and fixed.**

   <details>
   <summary><b>Answer</b></summary>
   <p>
   - Static: Elements with position: static; are positioned according to the normal flow of the document. This is the default value.
   - Relative: Elements with position: relative; are positioned relative to their normal position in the document flow. They can be moved using top, right, bottom, and left properties without affecting the layout of other elements.
   - Absolute: Elements with position: absolute; are positioned relative to their closest positioned ancestor (or the initial containing block if no ancestor is positioned). They are removed from the normal flow of the document.
   - Fixed: Elements with position: fixed; are positioned relative to the viewport and do not move when the page is scrolled. They are also removed from the normal flow of the document.
   </p>
   </details>
   </li>
   
   <li>

   **How does the margin collapsing phenomenon occur in CSS? Provide an example.**

   <details>
   <summary><b>Answer</b></summary>
   <p>
   Margin collapsing occurs when the top and bottom margins of adjacent elements collapse into a single margin. This happens in certain situations, such as when two adjacent elements are siblings or when an element contains only text and has a top and bottom margin. For example:
   ```css
   .element1 {
     margin-bottom: 20px;
   }

   .element2 {
     margin-top: 30px;
   }
   ```
   In this case, if element1 and element2 are adjacent, the margin between them collapses to 30px, not the sum of both margins (20px + 30px = 50px).
   </p>
   </details>
   </li>
   
   <li>

   **How can you remove the default margin and padding from all elements in CSS?**

   <details>
   <summary><b>Answer</b></summary>
   <p>
   To remove the default margin and padding from all elements, you can use the following CSS reset:
   ```css
   * {
     margin: 0;
     padding: 0;
     box-sizing: border-box; /* Optional: Ensures that padding and border are included in the element's total width and height */
   }
   ```
   This selector targets all elements (*) and sets their margin and padding to zero. The box-sizing property with a value of border-box ensures that padding and border are included in the element's total width and height.
   </p>
   </details>
   </li>
   
   <li>

   **Explain the difference between the position: relative; and position: absolute; properties.**

   <details>
   <summary><b>Answer</b></summary>
   <p>
   - Relative Positioning: Elements with position: relative; are positioned relative to their normal position in the document flow. They can be moved using the top, right, bottom, and left properties without affecting the layout of other elements. The original space occupied by the element is preserved in the document flow.
   - Absolute Positioning: Elements with position: absolute; are positioned relative to their closest positioned ancestor (or the initial containing block if no ancestor is positioned). They are removed from the normal flow of the document and do not affect the position of other elements. Absolute positioned elements are placed based on their containing block, which can be different from the document or viewport.
   </p>
   </details>
   </li>
   
   <li>

   **How can you horizontally center a block-level element using CSS?**

   <details>
   <summary><b>Answer</b></summary>
   <p>
   To horizontally center a block-level element using CSS, you can use the following combination of properties:
   ```css
   .centered {
     width: 200px; /* Set the desired width */
     margin: 0 auto; /* Set the top and bottom margin to 0 and horizontally center using auto */
   }
   ```
   This sets the left and right margin to auto, which evenly distributes the available space on both sides of the element, effectively centering it horizontally within its containing block.
   </p>
   </details>
   </li>
   
   <li>

   **Explain the purpose of the display: none; property and its impact on layout and accessibility.**

   <details>
   <summary><b>Answer</b></summary>
   <p>
   The display: none; property is used to hide an element from the page layout entirely. It removes the element from the normal flow of the document, making it invisible and taking up no space. While display: none; can be useful for hiding content temporarily or conditionally, it can also impact accessibility, as screen readers and other assistive technologies will not detect hidden elements. It's essential to use display: none; judiciously and consider alternative methods, such as visibility: hidden; or off-screen positioning, when accessibility concerns are present.
   </p>
   </details>
   </li>
   
   <li>

   **Explain the differences between the visibility: hidden; and display: none; properties in CSS.**

   <details>
   <summary><b>Answer</b></summary>
   <p>
   - visibility: hidden;: The visibility property hides an element while still occupying space in the layout. The element is not visible, but its space is preserved, affecting the layout flow and potentially causing elements to collapse around it.
   - display: none;: The display property removes an element entirely from the layout, making it invisible and not occupying any space. The element is removed from the document flow, and other elements behave as if it doesn't exist, potentially affecting layout and positioning.
   </p>
   </details>
   </li>
   
   <li>

   **How can you create equal-height columns using CSS without using flexbox or grid?**

   <details>
   <summary><b>Answer</b></summary>
   <p>
   One approach to creating equal-height columns without flexbox or grid is by using the background-color and padding properties to create the illusion of equal height. This technique involves applying a background color to a parent container and setting padding-bottom with a percentage value to create a visually consistent height. For example:
   ```css
   .container {
     overflow: hidden;
   }

   .column {
     float: left;
     width: 33.33%;
     padding-bottom: 9999px; /* Large padding to create equal height */
     margin-bottom: -9999px; /* Offset negative margin to prevent extra space */
     background-color: lightgray; /* Background color to fill the column */
   }
   ```
   This method relies on the fact that padding percentages are calculated based on the width of the containing block, allowing columns to appear visually equal in height regardless of content.
   </p>
   </details>
   </li>
   
   <li>

   **Explain the purpose of the z-index property in CSS and how it affects the stacking order of elements.**

   <details>
   <summary><b>Answer</b></summary>
   <p>
   The z-index property in CSS controls the stacking order of elements along the z-axis (depth) within the document's stacking context. Elements with a higher z-index value appear visually above elements with lower z-index values within the same stacking context. The z-index property only applies to positioned elements (i.e., those with a position value other than static). When multiple elements overlap in the same stacking context, the element with the highest z-index value will be displayed on top. Elements with a negative z-index value are positioned behind the default stacking order.
   </p>
   </details>
   </li>
   
   <li>

   **How can you vertically center an element within its parent using CSS?**

   <details>
   <summary><b>Answer</b></summary>
   <p>
   To vertically center an element within its parent using CSS, you can use the following combination of properties:
   ```css
   .parent {
     position: relative; /* Ensure relative positioning for absolute positioning of child */
   }

   .child {
     position: absolute; /* Position the child element absolutely */
     top: 50%; /* Move the top edge to the vertical center of the parent */
     transform: translateY(-50%); /* Adjust vertically by half of its own height */
   }
   ```
   This technique positions the child element absolutely within its parent and uses the top and transform properties to center it vertically.
   </p>
   </details>
   </li>
   
   <li>

   **What is the purpose of the overflow property in CSS, and how can it be used to handle content overflow?**

   <details>
   <summary><b>Answer</b></summary>
   <p>
   The overflow property in CSS specifies how content that overflows the bounds of its containing element should be handled. It can take several values, including:
   - visible: Content overflows the element's box without clipping.
   - hidden: Content that overflows the element's box is clipped and not visible.
   - scroll: Content that overflows the element's box is clipped, and a scrollbar is added to navigate the overflowed content.
   - auto: Similar to scroll, but only adds a scrollbar when necessary.
   The overflow property can be used to control the behavior of elements with fixed dimensions or to prevent layout issues caused by overflowing content.
   </p>
   </details>
   </li>
   
</ol>
