Here are all **19 JavaScript Map Questions with Answers**:

---

### **1. Create a new Map and add key-value pairs to it.**

```js
const myMap = new Map();
myMap.set("name", "Manoj");
myMap.set("age", 24);
myMap.set("city", "Madurai");
```

---

### **2. Get the value of a specific key in a Map.**

```js
console.log(myMap.get("name")); // Output: "Manoj"
```

---

### **3. Check if a key exists in a Map.**

```js
console.log(myMap.has("age")); // Output: true
```

---

### **4. Iterate over the keys of a Map using a for...of loop.**

```js
for (let key of myMap.keys()) {
  console.log(key);
}
```

---

### **5. Iterate over the values of a Map using a for...of loop.**

```js
for (let value of myMap.values()) {
  console.log(value);
}
```

---

### **6. Iterate over the key-value pairs of a Map using a for...of loop.**

```js
for (let [key, value] of myMap) {
  console.log(`${key}: ${value}`);
}
```

---

### **7. Convert a Map to an array of key-value pairs.**

```js
const mapArray = Array.from(myMap);
console.log(mapArray);
// Output: [["name", "Manoj"], ["age", 24], ["city", "Madurai"]]
```

---

### **8. Convert an array of key-value pairs to a Map.**

```js
const arr = [["lang", "JavaScript"], ["type", "Dynamic"]];
const newMap = new Map(arr);
console.log(newMap.get("lang")); // Output: "JavaScript"
```

---

### **9. Use the forEach() method to iterate over the key-value pairs of a Map.**

```js
myMap.forEach((value, key) => {
  console.log(`${key} => ${value}`);
});
```

---

### **10. Use the Map keys() method to get an iterator for the keys of a Map.**

```js
const keys = myMap.keys();
for (let key of keys) {
  console.log(key);
}
```

---

### **11. Use the Map values() method to get an iterator for the values of a Map.**

```js
const values = myMap.values();
for (let val of values) {
  console.log(val);
}
```

---

### **12. Use the Map entries() method to get an iterator for the key-value pairs of a Map.**

```js
const entries = myMap.entries();
for (let [key, value] of entries) {
  console.log(`${key}: ${value}`);
}
```

---

### **13. Use the Map has() method to check if a Map contains a key.**

```js
console.log(myMap.has("city")); // Output: true
```

---

### **14. Use the Map get() method to get the value associated with a key in a Map.**

```js
console.log(myMap.get("age")); // Output: 24
```

---

### **15. Use the Map set() method to add a new key-value pair to a Map.**

```js
myMap.set("country", "India");
console.log(myMap.get("country")); // Output: "India"
```

---

### **16. Use the Map delete() method to remove a key-value pair from a Map.**

```js
myMap.delete("age");
console.log(myMap.has("age")); // Output: false
```

---

### **17. Use the Map clear() method to remove all key-value pairs from a Map.**

```js
myMap.clear();
console.log(myMap.size); // Output: 0
```

---

### **18. Use the Object.fromEntries() method to create a new object from a Map.**

```js
const mapToObject = new Map([
  ["name", "Manoj"],
  ["role", "Developer"]
]);
const obj = Object.fromEntries(mapToObject);
console.log(obj); // Output: { name: "Manoj", role: "Developer" }
```

---

### **19. Use the Map constructor to create a new Map from an array of key-value pairs.**

```js
const entriesArray = [["fruit", "apple"], ["color", "red"]];
const fruitMap = new Map(entriesArray);
console.log(fruitMap.get("fruit")); // Output: "apple"
```

---

Would you like **Set & WeakMap questions next** or go for **JavaScript Classes & Prototypes**?
