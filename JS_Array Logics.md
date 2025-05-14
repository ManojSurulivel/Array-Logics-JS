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

Would you like **Set & WeakSet Questions next** or **Function + Closure Interview Tasks**?
