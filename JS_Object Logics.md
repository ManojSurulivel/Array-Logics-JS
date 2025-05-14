Here are all 10 Object-based JavaScript questions with **answers**:

---

### **Question 1: What is an object in JavaScript?**

**Answer:**
An object in JavaScript is a collection of key-value pairs where each key (property) is a string (or Symbol) and each value can be any data type.

```js
const person = {
  name: "Manoj",
  age: 24,
  isDeveloper: true
};
```

---

### **Question 2: What is the difference between dot notation and bracket notation for accessing object properties?**

**Answer:**

* **Dot notation**: `obj.key` — used when the property name is a valid identifier (no spaces, no starting with a number).
* **Bracket notation**: `obj["key"]` — used when the property name is dynamic or contains special characters or spaces.

```js
const obj = { name: "Manoj", "full name": "Manoj Surulivel" };
console.log(obj.name);           // Dot
console.log(obj["full name"]);   // Bracket
```

---

### **Question 3: How do you loop through the properties of an object in JavaScript?**

**Answer:**
Using `for...in` loop:

```js
const person = { name: "Manoj", age: 24, job: "Developer" };
for (let key in person) {
  console.log(`${key}: ${person[key]}`);
}
```

---

### **Question 4: What is the difference between an object and an array in JavaScript?**

**Answer:**

* Objects store unordered key-value pairs.
* Arrays store ordered elements and are indexed by numbers.

```js
const obj = { name: "Manoj" };          // Object
const arr = ["Manoj", 24, "Developer"]; // Array
```

---

### **Question 5: Write a JavaScript function to convert an object into a list of `[key, value]` pairs.**

**Answer:**

```js
function objectToPairs(obj) {
  return Object.entries(obj);
}

console.log(objectToPairs({ name: "Manoj", age: 24 }));
// Output: [ ["name", "Manoj"], ["age", 24] ]
```

---

### **Question 6: Write a function that takes an object representing a person and returns their full name.**

**Answer:**

```js
function getFullName(person) {
  return `${person.firstName} ${person.lastName}`;
}

const user = { firstName: "Manoj", lastName: "Surulivel" };
console.log(getFullName(user)); // Output: "Manoj Surulivel"
```

---

### **Question 7: Create an object with your personal details. Now print all the keys in ascending order.**

**Answer:**

```js
const me = {
  name: "Manoj",
  age: 24,
  location: "Madurai",
  profession: "Developer"
};

const sortedKeys = Object.keys(me).sort();
console.log("Sorted Keys:", sortedKeys);
```

---

### **Question 8: Create an object with your personal details. Now filter out all the values and show them in descending order.**

**Answer:**

```js
const me = {
  name: "Manoj",
  age: 24,
  city: "Madurai",
  profession: "Developer"
};

const sortedValues = Object.values(me).sort().reverse();
console.log("Descending Values:", sortedValues);
```

---

### **Question 9: Create an object to hold information on your favorite recipe and print it in a structured way.**

**Answer:**

```js
const recipe = {
  title: "Mole",
  servings: 2,
  ingredients: ["cinnamon", "cumin", "cocoa"]
};

console.log(recipe.title);
console.log("Serves:", recipe.servings);
console.log("Ingredients:");
recipe.ingredients.forEach(ingredient => console.log(ingredient));
```

---

### **Question 10: Create a JavaScript function inside an object which finds max of 3 numbers. Call the function and print the result.**

**Answer:**

```js
const mathUtils = {
  maxOfThree: function (a, b, c) {
    return Math.max(a, b, c);
  }
};

console.log("Max is:", mathUtils.maxOfThree(10, 25, 7)); // Output: 25
```

---

Would you like **Array-based questions** next or go for **Map, Set & WeakMap** exercises?
