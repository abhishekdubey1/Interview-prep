1. **For...in Loops**:
   - Iterate over the properties of the object `person` using a `for...in` loop and log each property name and value.

<details>
<summary><b>Answer</b></summary>
<p>

```javascript
const person = {
  name: 'John',
  age: 30,
  gender: 'male'
};

for (let prop in person) {
  console.log(prop + ':', person[prop]);
}
```

This loop iterates over each property in the `person` object and logs both the property name and its corresponding value.

</p>
</details>

2. **Using Object.keys(), Object.values(), and Object.entries()**:
   - Use `Object.keys()` to extract the keys of the object `car` and log them.
   - Use `Object.values()` to extract the values of the object `car` and log them.
   - Use `Object.entries()` to extract both keys and values of the object `car` and log them.

<details>
<summary><b>Answer</b></summary>
<p>

```javascript
const car = {
  make: 'Toyota',
  model: 'Camry',
  year: 2020
};

console.log('Keys:', Object.keys(car));
console.log('Values:', Object.values(car));
console.log('Entries:', Object.entries(car));
```

- `Object.keys(car)` returns an array of keys: `['make', 'model', 'year']`.
- `Object.values(car)` returns an array of values: `['Toyota', 'Camry', 2020]`.
- `Object.entries(car)` returns an array of key-value pairs: `[['make', 'Toyota'], ['model', 'Camry'], ['year', 2020]]`.

</p>
</details>

3. **Shallow and Deep Cloning**:
   - Create a shallow clone of the object `originalObject` and log the clone.
   - Create a deep clone of the object `originalObject` and log the clone.

<details>
<summary><b>Answer</b></summary>
<p>

```javascript
const originalObject = { a: 1, b: { c: 2 } };

// Shallow clone
const shallowClone = { ...originalObject };
console.log('Shallow Clone:', shallowClone);

// Deep clone
const deepClone = JSON.parse(JSON.stringify(originalObject));
console.log('Deep Clone:', deepClone);
```

- The shallow clone creates a new object with the same top-level properties as `originalObject`. However, nested objects are still referenced.
- The deep clone creates a completely new object with no shared references, including nested objects.

</p>
</details>

4. **Merging Objects using Object.assign()**:
   - Merge the objects `object1` and `object2` using `Object.assign()` and log the merged object.

<details>
<summary><b>Answer</b></summary>
<p>

```javascript
const object1 = { a: 1, b: 2 };
const object2 = { b: 3, c: 4 };

const mergedObject = Object.assign({}, object1, object2);
console.log('Merged Object:', mergedObject);
```

- `Object.assign()` merges the properties of `object1` and `object2` into a new object. If there are conflicting property names, the last one wins.

</p>
</details>

5. **Merging Objects using Spread Syntax**:
   - Merge the objects `object1` and `object2` using the spread syntax (`...`) and log the merged object.

<details>
<summary><b>Answer</b></summary>
<p>

```javascript
const object1 = { a: 1, b: 2 };
const object2 = { b: 3, c: 4 };

const mergedObject = { ...object1, ...object2 };
console.log('Merged Object:', mergedObject);
```

- The spread syntax spreads the properties of `object1` and `object2` into a new object, effectively merging them.

</p>
</details>

6. **Merging Objects using Object Destructuring**:
   - Merge the objects `object1` and `object2` using object destructuring and log the merged object.

<details>
<summary><b>Answer</b></summary>
<p>

```javascript
const object1 = { a: 1, b: 2 };
const object2 = { b: 3, c: 4 };

const mergedObject = { ...object1, ...object2 };
console.log('Merged Object:', mergedObject);
```

- Object destructuring with spread syntax works similarly to the spread syntax alone, creating a new object with merged properties.

</p>
</details>
