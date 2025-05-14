Here are **easy array exercise questions with answers** — great for JavaScript interviews and beginner practice:

---
### Array Exercise Questions

### Easy:

### ✅ Question 1: How do you add a new element `5` to the end of the array `numbers`?

```js
numbers.push(5);
```

---

### ✅ Question 2: How can you check if an array `fruits` contains the value `"apple"`?

```js
fruits.includes("apple");
```

---

### ✅ Question 3: What method can you use to remove the last element from an array `colors`?

```js
colors.pop();
```

---

### ✅ Question 4: How do you find the number of elements in an array `grades`?

```js
grades.length;
```

---

### ✅ Question 5: Given an array `words`, how can you join all its elements into a single string separated by commas?

```js
words.join(",");
```

---

### ✅ Question 6: Given an array `fruits`, how do you add a new element `"banana"` to the beginning of the array?

```js
fruits.unshift("banana");
```

---

### ✅ Question 7: How can you check if an array `numbers` is empty (contains no elements)?

```js
numbers.length === 0;
```

---

### ✅ Question 8: What method can you use to remove the first element from an array `animals`?

```js
animals.shift();
```

---

### ✅ Question 9: How do you find the largest number in an array `scores`?

```js
Math.max(...scores);
```

---

### ✅ Question 10: Given an array `names`, how can you add multiple names, `"Alice"` and `"Bob"`, to the end of the array in one step?

```js
names.push("Alice", "Bob");
```

---

Would you like the next level (medium difficulty) array questions with logic practice?


Here are **medium-level JavaScript array questions** with **clear solutions** — perfect for interviews like Capgemini:

---

### Medium Level:

### ✅ 1. **Sum of all positive numbers**

```js
function sumPositive(numbers) {
  return numbers.filter(n => n > 0).reduce((sum, n) => sum + n, 0);
}

console.log(sumPositive([1, -2, 3, 4, -5])); // Output: 8
```

---

### ✅ 2. **Filter names starting with "A"**

```js
const filtered = names.filter(name => name.startsWith("A"));
```

---

### ✅ 3. **Reverse array `characters`**

```js
characters.reverse();
```

---

### ✅ 4. **Sort strings alphabetically**

```js
function sortStrings(arr) {
  return arr.slice().sort();
}

console.log(sortStrings(["banana", "apple", "cherry"])); // ["apple", "banana", "cherry"]
```

---

### ✅ 5. **Find index of first `7`**

```js
const index = numbers.indexOf(7);
```

---

### ✅ 6. **Longest string in an array**

```js
function longestString(arr) {
  return arr.reduce((longest, str) => str.length > longest.length ? str : longest, "");
}

console.log(longestString(["hi", "hello", "world", "javascript"])); // "javascript"
```

---

### ✅ 7. **Combine two arrays**

```js
const combinedArray = [...arr1, ...arr2];
```

---

### ✅ 8. **Remove duplicates from `values`**

```js
const uniqueValues = [...new Set(values)];
```

---

### ✅ 9. **Extract names from people array**

```js
function extractNames(people) {
  return people.map(person => person.name);
}

const people = [
  { name: "Manoj", age: 24, city: "Madurai" },
  { name: "Alice", age: 22, city: "Delhi" }
];

console.log(extractNames(people)); // ["Manoj", "Alice"]
```

---

### ✅ 10. **Sum of even numbers**

```js
function sumEven(numbers) {
  return numbers.filter(n => n % 2 === 0).reduce((sum, n) => sum + n, 0);
}

console.log(sumEven([1, 2, 3, 4, 5, 6])); // Output: 12
```

---

Here are the **Hard-level JavaScript Array Exercise Questions** with **interview-ready answers** – perfect for a Capgemini or any advanced technical interview:

---

### Hard Level:

### ✅ 1. **Return Unique Values (No Duplicates)**

```js
function getUnique(arr) {
  return [...new Set(arr)];
}

console.log(getUnique([1, 2, 2, 3, 4, 4, 5])); // [1, 2, 3, 4, 5]
```

---

### ✅ 2. **Custom `map()` Implementation**

```js
function customMap(arr, callback) {
  const result = [];
  for(let i = 0; i < arr.length; i++) {
    result.push(callback(arr[i], i, arr));
  }
  return result;
}

const nums = [1, 2, 3];
const squared = customMap(nums, n => n * n);
console.log(squared); // [1, 4, 9]
```

---

### ✅ 3. **Find Intersection of Two Arrays**

```js
function getIntersection(arr1, arr2) {
  return arr1.filter(value => arr2.includes(value));
}

console.log(getIntersection([1, 2, 3], [2, 3, 4])); // [2, 3]
```

---

### ✅ 4. **Find Person with Highest Age**

```js
function getOldestPerson(people) {
  return people.reduce((oldest, person) => 
    person.age > oldest.age ? person : oldest
  );
}

const people = [
  { name: "Manoj", age: 24 },
  { name: "Priya", age: 30 },
  { name: "Ravi", age: 27 }
];

console.log(getOldestPerson(people)); // { name: "Priya", age: 30 }
```

---

### ✅ 5. **Find Median of Numbers**

```js
function getMedian(numbers) {
  const sorted = [...numbers].sort((a, b) => a - b);
  const mid = Math.floor(sorted.length / 2);
  return sorted.length % 2 !== 0
    ? sorted[mid]
    : (sorted[mid - 1] + sorted[mid]) / 2;
}

console.log(getMedian([5, 3, 8, 1, 6])); // 5
```

---

### ✅ 6. **Filter Books Published Before 2000**

```js
function oldBooks(books) {
  return books.filter(book => book.publicationYear < 2000);
}

const books = [
  { title: "Old Book", author: "A", publicationYear: 1995 },
  { title: "New Book", author: "B", publicationYear: 2010 }
];

console.log(oldBooks(books)); // [{ title: "Old Book", ... }]
```

---

### ✅ 7. **Custom `filter()` Implementation**

```js
function customFilter(arr, callback) {
  const result = [];
  for(let i = 0; i < arr.length; i++) {
    if (callback(arr[i], i, arr)) {
      result.push(arr[i]);
    }
  }
  return result;
}

console.log(customFilter([1, 2, 3, 4], n => n % 2 === 0)); // [2, 4]
```

---

### ✅ 8. **Square Each Number**

```js
function squareArray(numbers) {
  return numbers.map(n => n * n);
}

console.log(squareArray([2, 3, 4])); // [4, 9, 16]
```

---

### ✅ 9. **Merge Two Sorted Arrays**

```js
function mergeSorted(arr1, arr2) {
  let merged = [], i = 0, j = 0;
  
  while (i < arr1.length && j < arr2.length) {
    merged.push(arr1[i] < arr2[j] ? arr1[i++] : arr2[j++]);
  }
  
  return [...merged, ...arr1.slice(i), ...arr2.slice(j)];
}

console.log(mergeSorted([1, 3, 5], [2, 4, 6])); // [1, 2, 3, 4, 5, 6]
```

---

### ✅ 10. **Count Word Occurrences**

```js
function wordCount(words) {
  return words.reduce((count, word) => {
    count[word] = (count[word] || 0) + 1;
    return count;
  }, {});
}

console.log(wordCount(["apple", "banana", "apple", "orange", "banana", "apple"]));
// { apple: 3, banana: 2, orange: 1 }
```

---

Here are **20 JavaScript Array Questions with Answers**:

---

### **1. Create an array with three elements and print out the second element.**

```js
const arr = [10, 20, 30];
console.log(arr[1]); // Output: 20
```

---

### **2. Create an array with five elements and print out the length of the array.**

```js
const arr = [1, 2, 3, 4, 5];
console.log(arr.length); // Output: 5
```

---

### **3. Create an array with four elements and print out each element using a for loop.**

```js
const arr = [5, 10, 15, 20];
for (let i = 0; i < arr.length; i++) {
  console.log(arr[i]);
}
```

---

### **4. Create an array with six elements and print out each element using a forEach loop.**

```js
const arr = [2, 4, 6, 8, 10, 12];
arr.forEach(el => console.log(el));
```

---

### **5. Create an array with three elements and add a fourth element to the end of the array.**

```js
const arr = [1, 2, 3];
arr.push(4);
console.log(arr); // Output: [1, 2, 3, 4]
```

---

### **6. Create an array with four elements and remove the second element.**

```js
const arr = [10, 20, 30, 40];
arr.splice(1, 1);
console.log(arr); // Output: [10, 30, 40]
```

---

### **7. Create an array with five elements and remove the last element.**

```js
const arr = [1, 2, 3, 4, 5];
arr.pop();
console.log(arr); // Output: [1, 2, 3, 4]
```

---

### **8. Create an array with three elements and check if the array includes a specific value.**

```js
const arr = [100, 200, 300];
console.log(arr.includes(200)); // Output: true
```

---

### **9. Create an array with five elements and sort the array in ascending order.**

```js
const arr = [5, 1, 3, 4, 2];
arr.sort((a, b) => a - b);
console.log(arr); // Output: [1, 2, 3, 4, 5]
```

---

### **10. Create an array with five elements and sort the array in descending order.**

```js
const arr = [5, 1, 3, 4, 2];
arr.sort((a, b) => b - a);
console.log(arr); // Output: [5, 4, 3, 2, 1]
```

---

### **11. Create two arrays, concatenate them and print out the resulting array.**

```js
const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];
const result = arr1.concat(arr2);
console.log(result); // Output: [1, 2, 3, 4, 5, 6]
```

---

### **12. Create an array with three elements and convert it to a string.**

```js
const arr = [10, 20, 30];
console.log(arr.toString()); // Output: "10,20,30"
```

---

### **13. Create an array with four elements and reverse the order of the elements.**

```js
const arr = [1, 2, 3, 4];
arr.reverse();
console.log(arr); // Output: [4, 3, 2, 1]
```

---

### **14. Create an array with five elements and find the index of a specific value.**

```js
const arr = [10, 20, 30, 40, 50];
console.log(arr.indexOf(30)); // Output: 2
```

---

### **15. Create an array with six elements and slice the array to create a new array with the first three elements.**

```js
const arr = [5, 10, 15, 20, 25, 30];
const sliced = arr.slice(0, 3);
console.log(sliced); // Output: [5, 10, 15]
```

---

### **16. Create an array with six elements and use the map method to double each element.**

```js
const arr = [1, 2, 3, 4, 5, 6];
const doubled = arr.map(num => num * 2);
console.log(doubled); // Output: [2, 4, 6, 8, 10, 12]
```

---

### **17. Create an array with four elements and use the while loop to calculate the sum of all elements.**

```js
const arr = [10, 20, 30, 40];
let sum = 0, i = 0;
while (i < arr.length) {
  sum += arr[i];
  i++;
}
console.log(sum); // Output: 100
```

---

### **18. Create an array with five elements and use the filter method to return only the even numbers.**

```js
const arr = [1, 2, 3, 4, 5];
const even = arr.filter(num => num % 2 === 0);
console.log(even); // Output: [2, 4]
```

---

### **19. Create an array with three elements and use the join method to concatenate the elements with a dash (-) separator.**

```js
const arr = ["HTML", "CSS", "JavaScript"];
console.log(arr.join("-")); // Output: "HTML-CSS-JavaScript"
```

---

### **20. Create two arrays with three elements each and use the concat method to combine them into a new array.**

```js
const a = [1, 2, 3];
const b = [4, 5, 6];
const combined = a.concat(b);
console.log(combined); // Output: [1, 2, 3, 4, 5, 6]
```

---

Great! Since you said **yes**, I’ll give you **both** — starting with **Set & WeakSet questions with answers**, followed by **Function & Closure interview tasks**.

---

## ✅ **Set & WeakSet Questions (with Answers)**

---

### **1. Create a new Set and add values to it.**

```js
const mySet = new Set();
mySet.add(1);
mySet.add(2);
mySet.add(3);
console.log(mySet); // Set { 1, 2, 3 }
```

---

### **2. Check if a value exists in a Set.**

```js
console.log(mySet.has(2)); // true
```

---

### **3. Remove an element from a Set.**

```js
mySet.delete(2);
console.log(mySet); // Set { 1, 3 }
```

---

### **4. Iterate over a Set using for...of loop.**

```js
for (const value of mySet) {
  console.log(value); // 1, then 3
}
```

---

### **5. Get the size of a Set.**

```js
console.log(mySet.size); // 2
```

---

### **6. Clear all elements in a Set.**

```js
mySet.clear();
console.log(mySet); // Set {}
```

---

### **7. Create a Set from an array (with duplicates).**

```js
const arr = [1, 2, 2, 3, 3, 4];
const uniqueSet = new Set(arr);
console.log([...uniqueSet]); // [1, 2, 3, 4]
```

---

### **8. What is a WeakSet in JavaScript?**

A `WeakSet` only stores **objects**, and those objects are held **weakly** (non-preventing garbage collection).

---

### **9. Create a WeakSet and add objects.**

```js
const ws = new WeakSet();
const obj = { name: "Manoj" };
ws.add(obj);
console.log(ws.has(obj)); // true
```

---

### **10. Why can’t you iterate over a WeakSet?**

Because WeakSets are **not enumerable**, and don’t support iteration (`forEach`, `for...of`) — for security and GC (Garbage Collection) reasons.

---

## ✅ **Function + Closure Interview Tasks (with Answers)**

---

### **1. Write a function that returns another function (Closure Example).**

```js
function outer(x) {
  return function inner(y) {
    return x + y;
  }
}
const add5 = outer(5);
console.log(add5(3)); // Output: 8
```

---

### **2. Create a function that remembers how many times it has been called.**

```js
function counter() {
  let count = 0;
  return function () {
    count++;
    return count;
  };
}
const countCalls = counter();
console.log(countCalls()); // 1
console.log(countCalls()); // 2
```

---

### **3. Create a private variable using closure.**

```js
function secretHolder() {
  let secret = "I am private";
  return {
    getSecret: () => secret,
    setSecret: (newSecret) => secret = newSecret,
  };
}
const sh = secretHolder();
console.log(sh.getSecret()); // "I am private"
sh.setSecret("Updated!");
console.log(sh.getSecret()); // "Updated!"
```

---

### **4. Implement a custom `once` function (only runs once).**

```js
function once(fn) {
  let called = false;
  let result;
  return function (...args) {
    if (!called) {
      result = fn(...args);
      called = true;
    }
    return result;
  };
}
const runOnce = once(() => "Running!");
console.log(runOnce()); // "Running!"
console.log(runOnce()); // "Running!" (cached)
```

---

### **5. Make a debounce function using closure.**

```js
function debounce(fn, delay) {
  let timer;
  return function (...args) {
    clearTimeout(timer);
    timer = setTimeout(() => fn(...args), delay);
  };
}
```

Usage:

```js
const log = () => console.log("Typing stopped");
const debouncedLog = debounce(log, 300);
debouncedLog(); debouncedLog(); // logs only once after pause
```

---

**Promise + Async-Await Questions**, **DOM Interview Tasks**, or **Real-Time System Design Questions (e.g. infinite scroll, modal manager)**

Perfect! Since you said **yes**, I’ll give you **all three** categories one by one — with **interview-ready JavaScript questions and answers**.

---

## ✅ **1. Promise + Async/Await Questions with Answers**

---

### **1. What is a Promise in JavaScript?**

A Promise is an object that represents the **eventual completion (or failure)** of an asynchronous operation and its resulting value.

---

### **2. Create a Promise that resolves after 2 seconds.**

```js
const myPromise = new Promise((resolve, reject) => {
  setTimeout(() => resolve("Done!"), 2000);
});
myPromise.then(console.log); // "Done!" after 2 seconds
```

---

### **3. What is async/await in JavaScript?**

`async` makes a function return a Promise.
`await` pauses the execution of an `async` function until the Promise is resolved.

---

### **4. Rewrite above Promise code using async/await.**

```js
async function run() {
  const result = await new Promise(resolve => {
    setTimeout(() => resolve("Done!"), 2000);
  });
  console.log(result); // "Done!"
}
run();
```

---

### **5. What happens if a Promise is rejected inside async function?**

Use `try/catch` to handle it:

```js
async function fetchData() {
  try {
    let data = await fetch("wrong_url");
  } catch (err) {
    console.error("Error:", err.message);
  }
}
```

---

### **6. How do you run multiple Promises in parallel?**

```js
Promise.all([
  Promise.resolve(1),
  Promise.resolve(2)
]).then(console.log); // [1, 2]
```

---

## ✅ **2. DOM Interview Tasks (with Examples)**

---

### **1. Add a class to a DOM element.**

```js
document.querySelector("div").classList.add("highlight");
```

---

### **2. Toggle visibility of an element on button click.**

```js
document.querySelector("button").addEventListener("click", () => {
  const box = document.querySelector("#box");
  box.style.display = box.style.display === "none" ? "block" : "none";
});
```

---

### **3. Change text content of an element.**

```js
document.getElementById("title").textContent = "New Title";
```

---

### **4. Append a new list item.**

```js
const li = document.createElement("li");
li.textContent = "New Item";
document.querySelector("ul").appendChild(li);
```

---

### **5. Add event delegation to list.**

```js
document.querySelector("ul").addEventListener("click", function(e) {
  if (e.target.tagName === "LI") {
    alert("Clicked: " + e.target.textContent);
  }
});
```

---

## ✅ **3. Real-Time System Design: JS Tasks**

---

### **1. Infinite Scroll Skeleton (basic idea)**

```js
window.addEventListener("scroll", () => {
  if (window.innerHeight + window.scrollY >= document.body.offsetHeight - 10) {
    loadMoreItems(); // Fetch and append more items
  }
});
```

---

### **2. Modal Manager in JavaScript**

```js
function openModal() {
  document.getElementById("modal").style.display = "block";
}
function closeModal() {
  document.getElementById("modal").style.display = "none";
}
document.getElementById("openBtn").onclick = openModal;
document.getElementById("closeBtn").onclick = closeModal;
```

---

### **3. Debounced Search Box**

```js
function debounce(fn, delay) {
  let timer;
  return function (...args) {
    clearTimeout(timer);
    timer = setTimeout(() => fn(...args), delay);
  };
}
const search = debounce((query) => {
  console.log("Searching for:", query);
}, 300);

document.getElementById("searchInput").addEventListener("input", (e) => {
  search(e.target.value);
});
```

---

Great! Let's continue with **all three** sections — these are **must-know topics** for frontend interviews.

---

## ✅ **1. JavaScript Event Loop & Microtask Queue – Questions with Answers**

---

### **1. What is the Event Loop in JavaScript?**

The Event Loop is a mechanism that allows JavaScript to **perform non-blocking operations** by handling **callbacks, Promises, events, etc.** asynchronously using **queues**.

---

### **2. What is the Call Stack?**

It’s where function calls are added and removed in **LIFO** order. JS runs one function at a time from this stack.

---

### **3. What is the Microtask Queue?**

It stores callbacks from resolved **Promises** or `queueMicrotask()`. It's **processed before** the macrotask queue.

---

### **4. What is the Macrotask Queue?**

It stores tasks like `setTimeout`, `setInterval`, or DOM events. These are processed **after** the microtask queue.

---

### **5. What is the output of this code? Why?**

```js
console.log("Start");

setTimeout(() => console.log("setTimeout"), 0);

Promise.resolve().then(() => console.log("Promise"));

console.log("End");
```

**Output:**

```
Start
End
Promise
setTimeout
```

**Explanation:**

* Sync: "Start" → "End"
* Microtask (Promise): after sync
* Macrotask (setTimeout): after microtask

---

## ✅ **2. Browser Rendering & Performance Interview Q\&A**

---

### **1. What is the Critical Rendering Path?**

It's the steps the browser takes to **convert HTML, CSS, and JS into pixels** on the screen.

---

### **2. What blocks browser rendering?**

* **Synchronous JavaScript**
* **Large CSS files**
* **Blocking external fonts**
* **Too many DOM manipulations**

---

### **3. How can you improve page performance?**

* Minify CSS/JS
* Use `async`/`defer` with scripts
* Lazy-load images
* Use caching/CDNs
* Reduce DOM depth

---

### **4. Difference: repaint vs reflow**

* **Repaint**: visual change without layout (e.g., color).
* **Reflow**: layout recalculation (e.g., size, position). Reflows are **more expensive**.

---

### **5. What is layout thrashing and how to avoid it?**

**Layout thrashing** happens when JS reads & writes to the DOM **repeatedly**, triggering multiple reflows. Avoid by **batching DOM reads/writes**.

---

## ✅ **3. HTML/CSS Rapid Revision + 10 Tricky Interview Scenarios**

---

### **1. What are semantic HTML tags?**

Tags that convey meaning: `<article>`, `<section>`, `<main>`, `<aside>`, `<header>`, `<footer>`, etc.

---

### **2. How do you make a div a circle in CSS?**

```css
.circle {
  width: 100px;
  height: 100px;
  border-radius: 50%;
}
```

---

### **3. What is the difference between `visibility: hidden` and `display: none`?**

* `visibility: hidden`: Hides element but occupies space.
* `display: none`: Hides and removes from layout.

---

### **4. How to center a div using Flexbox?**

```css
.parent {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

---

### **5. How does z-index work?**

Used to control stacking of elements. Works only on positioned elements (relative, absolute, fixed).

---

### **6. How to make a responsive grid using CSS Grid?**

```css
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
}
```

---

### **7. What is the difference between absolute and fixed positioning?**

* **absolute**: positioned relative to nearest positioned ancestor.
* **fixed**: positioned relative to viewport.

---

### **8. How do you hide elements only on mobile screens?**

```css
@media (max-width: 768px) {
  .hide-on-mobile {
    display: none;
  }
}
```

---

### **9. What is specificity in CSS?**

It determines **which rule wins** when multiple CSS rules apply. Inline > ID > Class > Tag.

---

### **10. How to make a sticky header?**

```css
header {
  position: sticky;
  top: 0;
  background: white;
}
```

---


