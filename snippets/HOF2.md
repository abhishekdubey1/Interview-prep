<div align="center">
   <h1>JavaScript Array Manipulation</h1>
</div>

<ol>

   <li>

   **Print Full Names**

   ```javascript
   const users = [
     {firstName: "john", lastName: "Biden", age: 26},
     {firstName: "jimmy", lastName: "cob", age: 75},
     {firstName: "sam", lastName: "lewis", age: 50},
     {firstName: "Ronald", lastName: "Mathew", age: 26},  
   ];

   const output = users.map((x) => {
       return x.firstName + " " + x.lastName;
   });

   console.log(output);
   ```
   <br/>
   <details>
   <summary><b>Explanation</b></summary>
   <p>
   This code snippet iterates over the array of objects `users` and uses the `map` function to create a new array containing full names by concatenating the `firstName` and `lastName` properties of each object.
   </p>
   </details>
   </li>
   
   <li>

   **Print Users of a Particular Age along with their Frequency**

   ```javascript
   const users = [
     {firstName: "john", lastName: "Biden", age: 26},
     {firstName: "jimmy", lastName: "cob", age: 75},
     {firstName: "sam", lastName: "lewis", age: 50},
     {firstName: "Ronald", lastName: "Mathew", age: 26},  
   ];

   const output = users.reduce(function(acc, curr) {
       if (acc[curr.age]) {
           acc[curr.age]++;
       } else {
           acc[curr.age] = 1;      
       }
       return acc;
   }, {});

   console.log(output);
   ```
   <br/>
   <details>
   <summary><b>Explanation</b></summary>
   <p>
   This code snippet uses the `reduce` function to iterate over the `users` array and count the frequency of each age. It creates an object where the keys are the ages and the values are the frequencies of those ages.
   </p>
   </details>
   </li>
   
   <li>

   **Print Objects with Marks > 60 and Roll Number > 15**

   ```javascript
   let student = [
     {name: "Smith", rollNumber: 31, marks: 80},
     {name: "Jenny", rollNumber: 15, marks: 69},
     {name: "John", rollNumber: 16, marks: 35},
     {name: "Tiger", rollNumber: 7, marks: 55}
   ];

   const details = student.filter((x) => x.marks > 60 && x.rollNumber > 15);
   console.log(details); 
   ```
   <br/>
   <details>
   <summary><b>Explanation</b></summary>
   <p>
   This code snippet uses the `filter` function to create a new array containing objects with marks greater than 60 and roll numbers greater than 15.
   </p>
   </details>
   </li>
   
   <li>

   **Print Sum of Marks of All Students**

   ```javascript
   let student = [
     {name: "Smith", rollNumber: 31, marks: 80},
     {name: "Jenny", rollNumber: 15, marks: 69},
     {name: "John", rollNumber: 16, marks: 35},
     {name: "Tiger", rollNumber: 7, marks: 55}
   ];

   const details = student.reduce((acc, curr) => {
       return acc += curr.marks;
   }, 0);

   console.log(details);
   ```
   <br/>
   <details>
   <summary><b>Explanation</b></summary>
   <p>
   This code snippet uses the `reduce` function to calculate the sum of marks of all students in the `student` array.
   </p>
   </details>
   </li>
   
   <li>

   **List of First Names from Users with Age > 30**

   ```javascript
   const users = [
     {firstName: "john", lastName: "Biden", age: 26},
     {firstName: "jimmy", lastName: "Cob", age: 75},
     {firstName: "Sam", lastName: "Lewis", age: 50},
     {firstName: "Ronald", lastName: "Mathew", age: 26},  
   ];

   const output = users.filter((x) => x.age > 30).map((x) => x.firstName);
   console.log(output);
   ```
   <br/>
   <details>
   <summary><b>Explanation</b></summary>
   <p>
   This code snippet uses the `filter` function to create a new array containing objects with age greater than 30, and then uses the `map` function to extract the first names from those objects.
   </p>
   </details>
   </li>
   
   <li>

   **Print Names of Students Who Scored More Than 60**

   ```javascript
   let student = [
     {name: "Smith", rollNumber: 31

, marks: 80},
     {name: "Jenny", rollNumber: 15, marks: 69},
     {name: "John", rollNumber: 16, marks: 35},
     {name: "Tiger", rollNumber: 7, marks: 55}
   ];

   const ans = student.filter((x) => x.marks > 60).map((x) => x.name);
   console.log(ans);
   ```
   <br/>
   <details>
   <summary><b>Explanation</b></summary>
   <p>
   This code snippet uses the `filter` function to create a new array containing objects with marks greater than 60, and then uses the `map` function to extract the names from those objects.
   </p>
   </details>
   </li>
   
   <li>

   **Print Total Marks for Students with Marks > 60 after Adding 20 Marks to Those Scoring Less Than 60**

   ```javascript
   let student = [
     {name: "Smith", rollNumber: 31, marks: 80},
     {name: "Jenny", rollNumber: 15, marks: 69},
     {name: "John", rollNumber: 16, marks: 35},
     {name: "Tiger", rollNumber: 7, marks: 55}
   ];

   const totalMarks = student.map((stu) => {
       if (stu.marks < 60) {
           stu.marks += 20;
       }
       return stu;
   }).filter((stu) => stu.marks > 60).reduce((acc, curr) => acc + curr.marks, 0);

   console.log(totalMarks);
   ```
   <br/>
   <details>
   <summary><b>Explanation</b></summary>
   <p>
   This code snippet first modifies the marks of students scoring less than 60 by adding 20 to their marks. Then, it filters out students with marks greater than 60 and calculates the total marks for those students using the `reduce` function.
   </p>
   </details>
   </li>

</ol>
