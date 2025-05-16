// REJEX:


To extract numbers like `200` and `23` from the given string in JavaScript, you can use a **regular expression** to match all the numbers.

### Code:

```javascript
const str = "@#₹ I have a 200 apples and 23 mangoes $%=";
const numbers = str.match(/\d+/g);
console.log(numbers); // Output: ['200', '23']
```

### Explanation:

* `\d+` matches one or more digits.
* `g` flag ensures it finds **all** matches in the string.
* The result is an array of number **strings** — you can convert them to actual numbers if needed:

```javascript
const numValues = numbers.map(Number); // [200, 23]
```

ANOTHER METHODS:
If you want to **print only the numbers**, not as an array, but one by one like:

```
200  
23
```

### Here's the code:

```javascript
const str = "@#₹ I have a 200 apples and 23 mangoes $%=";
const numbers = str.match(/\d+/g);
numbers.forEach(num => console.log(num));
```

### Output:

```
200  
23
```

Got it, Manoj! Here's a set of **realistic JavaScript interview-style questions** just like the one you were asked today, where you extract or manipulate specific types of data:

---

### **Question 1: Extract Numbers from a String**

```js
let str = "@#₹ I have a 200 apples and 23 mangoes $%=";
let result = str.match(/\d+/g);
console.log(result.join('\n'));
```

**Output:**

```
200
23
```

**Explanation:**
`\d+` matches one or more digits. `match(/\d+/g)` finds all such matches in the string. `join('\n')` prints each number on a new line.

---

### **Question 2: Extract Only Words (No Symbols or Numbers)**

```js
let str = "@#₹ I have a 200 apples and 23 mangoes $%=";
let result = str.match(/[a-zA-Z]+/g);
console.log(result);
```

**Output:**
`[ 'I', 'have', 'a', 'apples', 'and', 'mangoes' ]`

---

### **Question 3: Count the Numbers in a Sentence**

```js
let sentence = "There are 2 apples, 10 bananas, and 1 mango.";
let count = sentence.match(/\d+/g).length;
console.log(count); // Output: 3
```

---

### **Question 4: Extract Decimal or Floating Numbers**

```js
let text = "Prices: 199.99, 45.50 and 100.";
let numbers = text.match(/\d+(\.\d+)?/g);
console.log(numbers); // Output: ['199.99', '45.50', '100']
```

---

### **Question 5: Extract All Special Characters**

```js
let messy = "@#₹ I have a 200 apples and 23 mangoes $%=";
let specials = messy.match(/[^a-zA-Z0-9\s]/g);
console.log(specials); 
```

**Output:**
`[ '@', '#', '₹', '$', '%', '=' ]`

---

Yes, exactly — these are **regex-based JavaScript questions**, often asked in interviews to test your skills in:

* **String parsing**
* **Pattern matching**
* **Data extraction (like numbers, words, symbols)**
* **Practical use of `.match()`, `.replace()`, `.split()`, etc.**

These types of questions are **common in real-time interviews** because they test:

* Your understanding of JavaScript string methods
* How well you handle dynamic data
* Your ability to work with real-world, messy strings

Let me know if you want:

* More regex challenges,
* A cheat sheet for commonly used regex patterns,
* Or to practice **non-regex string logic tasks** too.


Great! Here are **10 real-time regex-based string parsing interview questions** with **answers and explanations** — all practical and commonly asked:

---

### **1. Extract all numbers from a sentence**

```js
const str = "He bought 3 apples, 25 bananas, and 7 mangoes.";
const numbers = str.match(/\d+/g).map(Number);
console.log(numbers); // [3, 25, 7]
```

**Explanation:** `\d+` matches one or more digits. `g` flag finds all matches. `map(Number)` converts strings to numbers.

---

### **2. Extract only words (exclude numbers/symbols)**

```js
const str = "Price is $200, not 100!";
const words = str.match(/\b[a-zA-Z]+\b/g);
console.log(words); // ["Price", "is", "not"]
```

**Explanation:** `\b` ensures word boundaries; `[a-zA-Z]+` matches word characters only.

---

### **3. Count number of digits in a string**

```js
const str = "I have 2 cats, 3 dogs, and 1 parrot";
const count = (str.match(/\d/g) || []).length;
console.log(count); // 3
```

---

### **4. Remove all special characters**

```js
const str = "Hello @#World$%^&*";
const clean = str.replace(/[^a-zA-Z0-9 ]/g, "");
console.log(clean); // "Hello World"
```

---

### **5. Extract all capitalized words**

```js
const str = "Today I Met John And Sarah At The Park.";
const caps = str.match(/\b[A-Z][a-z]*\b/g);
console.log(caps); // ["Today", "I", "Met", "John", "And", "Sarah", "At", "The", "Park"]
```

---

### **6. Find all email addresses in a string**

```js
const str = "Contact us at test@example.com or info@mail.com";
const emails = str.match(/\b[\w.-]+@[\w.-]+\.\w{2,}\b/g);
console.log(emails); // ["test@example.com", "info@mail.com"]
```

---

### **7. Extract decimal numbers from string**

```js
const str = "Bill: 23.75, Tax: 3.50, Tip: 4.25";
const decimals = str.match(/\d+\.\d+/g).map(Number);
console.log(decimals); // [23.75, 3.5, 4.25]
```

---

### **8. Extract words longer than 5 characters**

```js
const str = "JavaScript regex questions are very powerful";
const longWords = str.match(/\b\w{6,}\b/g);
console.log(longWords); // ["JavaScript", "regex", "questions", "powerful"]
```

---

### **9. Find how many times a word appears**

```js
const str = "apple banana apple orange apple";
const matches = str.match(/\bapple\b/g) || [];
console.log(matches.length); // 3
```

---

### **10. Replace all numbers with asterisks**

```js
const str = "Credit card: 1234 5678 9012 3456";
const masked = str.replace(/\d/g, "*");
console.log(masked); // "Credit card: **** **** **** ****"
```

---

Would you like:

* **More regex-based real interview challenges**?
* Or **interactive practice tasks** to solve on your own and then check answers?



Perfect! Here's what you asked for — categorized and structured to help you **master real interview-level string/regex challenges** quickly:

---

## **1. More Regex Challenges (with answers)**

### **Q1. Extract all words that start with a capital letter**

```js
const str = "Meet John, Alice, and Bob at the Cafe.";
const result = str.match(/\b[A-Z][a-z]*\b/g);
console.log(result); // ["Meet", "John", "Alice", "Bob", "Cafe"]
```

---

### **Q2. Remove duplicate spaces**

```js
const str = "This    is     a   test";
const result = str.replace(/\s+/g, " ");
console.log(result); // "This is a test"
```

---

### **Q3. Extract all hashtags from a string**

```js
const str = "Loving the #sunset and #beach vibes!";
const result = str.match(/#\w+/g);
console.log(result); // ["#sunset", "#beach"]
```

---

### **Q4. Validate if a string is a valid 10-digit phone number**

```js
const phone = "9876543210";
const isValid = /^\d{10}$/.test(phone);
console.log(isValid); // true
```

---

### **Q5. Remove HTML tags from a string**

```js
const html = "<h1>Hello</h1><p>World</p>";
const clean = html.replace(/<[^>]*>/g, "");
console.log(clean); // "HelloWorld"
```

---

## **2. Regex Cheat Sheet**

| Pattern  | Description                        | Example                                    |
| -------- | ---------------------------------- | ------------------------------------------ |
| `\d`     | digit (0–9)                        | `/\d+/g` finds numbers                     |
| `\w`     | word character (a–z, A–Z, 0–9, \_) | `/\w+/g` finds words                       |
| `\s`     | whitespace (space, tab, newline)   | `/\s+/g` removes extra spaces              |
| `\b`     | word boundary                      | `/\bword\b/` finds exact word              |
| `[^abc]` | not a, b, or c                     | `/[^0-9]/g` removes digits                 |
| `.`      | any character except newline       | `/./g` matches every char                  |
| `*`      | zero or more times                 | `/a*/g` matches "", "a", "aa"              |
| `+`      | one or more times                  | `/a+/g` matches "a", "aa"                  |
| `{n,m}`  | between n and m times              | `/\d{2,4}/` matches 2 to 4 digits          |
| `^`      | start of string                    | `/^Hi/` matches strings starting with "Hi" |
| `$`      | end of string                      | `/end$/` matches strings ending with "end" |

---

## **3. Non-Regex String Logic Interview Tasks**

### **Q1. Count the number of vowels in a string**

```js
const countVowels = (str) => str.match(/[aeiou]/gi)?.length || 0;
console.log(countVowels("Hello World")); // 3
```

---

### **Q2. Reverse a string**

```js
const reverse = (str) => str.split('').reverse().join('');
console.log(reverse("frontend")); // "dnetnorf"
```

---

### **Q3. Check if a string is a palindrome**

```js
const isPalindrome = (str) => {
  str = str.toLowerCase().replace(/[^a-z]/g, "");
  return str === str.split('').reverse().join('');
};
console.log(isPalindrome("Madam")); // true
```

---

### **Q4. Capitalize the first letter of every word**

```js
const capitalize = (str) =>
  str.replace(/\b\w/g, char => char.toUpperCase());
console.log(capitalize("hello world")); // "Hello World"
```

---

### **Q5. Find the most frequent character in a string**

```js
const mostFrequentChar = (str) => {
  const freq = {};
  for (let char of str.replace(/\s/g, '')) {
    freq[char] = (freq[char] || 0) + 1;
  }
  return Object.entries(freq).sort((a, b) => b[1] - a[1])[0][0];
};
console.log(mostFrequentChar("javascript interview")); // "i"
```

---

Would you like:

* **Regex Quizzes & Mini Challenges (timed practice)?**
* **String logic without regex (pure loops & conditions)?**
* Or **Mini Projects involving real-world string parsing (form validation, search filter, etc.)?**



Great! Here's **all three** — so you get maximum hands-on practice, real-world context, and interview-level prep:

---

## **1. Regex Quizzes & Mini Challenges (Timed Practice Style)**

Try solving each in under 60 seconds:

### **Q1. Extract all numbers from the string**

```js
let str = "Order 123, shipped on 25th, ID#9823";
console.log(str.match(/\d+/g)); // ["123", "25", "9823"]
```

---

### **Q2. Validate an email address**

```js
let email = "test@example.com";
console.log(/^[\w.-]+@[a-z]+\.[a-z]{2,3}$/.test(email)); // true
```

---

### **Q3. Find all words ending in "ing"**

```js
let sentence = "I am singing, dancing, and coding";
console.log(sentence.match(/\b\w+ing\b/g)); // ["singing", "dancing", "coding"]
```

---

### **Q4. Mask all digits in a string**

```js
let phone = "My number is 9876543210";
console.log(phone.replace(/\d/g, "*")); // "My number is **********"
```

---

## **2. String Logic Without Regex (Pure Loop/Condition)**

### **Q1. Count vowels without using regex**

```js
function countVowels(str) {
  let count = 0;
  let vowels = ['a', 'e', 'i', 'o', 'u'];
  for (let char of str.toLowerCase()) {
    if (vowels.includes(char)) count++;
  }
  return count;
}
console.log(countVowels("Frontend Engineer")); // 6
```

---

### **Q2. Remove duplicate characters from a string**

```js
function removeDuplicates(str) {
  let result = '';
  for (let char of str) {
    if (!result.includes(char)) result += char;
  }
  return result;
}
console.log(removeDuplicates("aabbccdde")); // "abcde"
```

---

### **Q3. Find the longest word in a sentence**

```js
function longestWord(sentence) {
  let words = sentence.split(' ');
  let max = "";
  for (let word of words) {
    if (word.length > max.length) max = word;
  }
  return max;
}
console.log(longestWord("JavaScript is extremely powerful")); // "extremely"
```

---

## **3. Mini Projects (Real-World String Parsing)**

### **A. Form Validator Mini Task**

```js
function validateForm(name, email, password) {
  if (name.length < 3) return "Name too short";
  if (!email.includes("@") || !email.endsWith(".com")) return "Invalid email";
  if (password.length < 6) return "Password too short";
  return "Form valid";
}
console.log(validateForm("Manoj", "manoj@gmail.com", "123456")); // "Form valid"
```

---

### **B. Search Filter Functionality**

```js
function search(items, query) {
  return items.filter(item => item.toLowerCase().includes(query.toLowerCase()));
}
console.log(search(["Apple", "Banana", "Grapes"], "ap")); // ["Apple", "Grapes"]
```

---

### **C. Flatten Hashtags from Tweets**

```js
function extractHashtags(tweets) {
  return tweets.flatMap(tweet => tweet.split(" ").filter(word => word.startsWith("#")));
}
console.log(extractHashtags(["Loving the #sunset", "Chill with #friends at #beach"])); 
// ["#sunset", "#friends", "#beach"]
```

---

Perfect! Here's a **power combo** of both:

---

## **1. Real Interview-Style Regex Challenges (With Answers)**

### **Challenge 1: Extract only the numbers from a messy string**

```js
let str = "My ID is 42, I earned ₹5000.50 in April.";
console.log(str.match(/\d+(\.\d+)?/g)); 
// Output: ["42", "5000.50"]
```

---

### **Challenge 2: Validate a strong password (min 8 chars, 1 digit, 1 special char)**

```js
let password = "Test@1234";
let regex = /^(?=.*[0-9])(?=.*[!@#$%^&*])[A-Za-z0-9!@#$%^&*]{8,}$/;
console.log(regex.test(password)); 
// Output: true
```

---

### **Challenge 3: Find all capitalized words**

```js
let sentence = "Manoj Surulivel is a Frontend Developer";
console.log(sentence.match(/\b[A-Z][a-z]+\b/g)); 
// Output: ["Manoj", "Surulivel", "Frontend", "Developer"]
```

---

### **Challenge 4: Replace all special characters with empty string**

```js
let messy = "Welcome@Home#2025!";
console.log(messy.replace(/[^a-zA-Z0-9 ]/g, '')); 
// Output: "WelcomeHome2025"
```

---

### **Challenge 5: Extract domain name from email**

```js
let email = "manoj1882000@gmail.com";
console.log(email.match(/@(\w+\.\w+)/)[1]); 
// Output: "gmail.com"
```

---

## **2. Interactive Practice Tasks (Try First, Then See Answer)**

### **Q1. Extract all numbers from this string:**

```js
let input = "Bought 2 books for ₹350 and ₹450";
```

**Your Task:** Extract only the numbers
**Expected Output:** `["2", "350", "450"]`

<details><summary>Answer</summary>

```js
console.log(input.match(/\d+/g)); 
```

</details>

---

### **Q2. Validate Indian mobile number (10 digits, starts with 6-9):**

```js
let phone = "9876543210";
```

**Expected:** `true`

<details><summary>Answer</summary>

```js
console.log(/^[6-9]\d{9}$/.test(phone)); 
```

</details>

---

### **Q3. Remove all whitespaces from a string:**

```js
let messy = "   Hello   World  ! ";
```

**Expected Output:** `"HelloWorld!"`

<details><summary>Answer</summary>

```js
console.log(messy.replace(/\s+/g, '')); 
```

</details>

---

### **Q4. Find duplicate words**

```js
let line = "hello hello world test test";
```

**Expected Output:** `["hello", "test"]`

<details><summary>Answer</summary>

```js
console.log([...line.matchAll(/\b(\w+)\b(?=.*\b\1\b)/g)].map(m => m[1]));
```

</details>

---

### **Q5. Extract initials from full name**

```js
let name = "Manoj Surulivel";
```

**Expected Output:** `"M.S."`

<details><summary>Answer</summary>

```js
console.log(name.match(/\b\w/g).join('.') + '.'); 
```

</details>

---

Awesome! Here's **everything you asked for** — both **mini projects** and **quiz-style challenges** across difficulty levels.

---

## **Mini Projects (Real-World String Parsing)**

### **1. Email Validator**

```js
function isValidEmail(email) {
  return /^[a-zA-Z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,}$/i.test(email);
}
console.log(isValidEmail("manoj1882000@gmail.com")); // true
```

---

### **2. Password Strength Checker**

```js
function isStrongPassword(password) {
  return /^(?=.*[A-Z])(?=.*\d)(?=.*[@#$%^&+=!]).{8,}$/.test(password);
}
console.log(isStrongPassword("Hello@123")); // true
```

---

### **3. Auto-Suggestion System**

```js
let data = ["apple", "banana", "mango", "grapes", "melon"];
function suggest(input) {
  return data.filter(item => item.startsWith(input.toLowerCase()));
}
console.log(suggest("ma")); // ["mango"]
```

---

### **4. Form Field Validator (Name, Email, Phone)**

```js
function validateForm({ name, email, phone }) {
  const nameOk = /^[A-Za-z ]+$/.test(name);
  const emailOk = /^[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,}$/i.test(email);
  const phoneOk = /^[6-9]\d{9}$/.test(phone);
  return nameOk && emailOk && phoneOk;
}
console.log(validateForm({ name: "Manoj", email: "manoj@gmail.com", phone: "9876543210" })); // true
```

---

## **Quiz-Style Practice Challenges (Easy/Medium/Hard)**

### **Easy**

1. **Extract numbers from string:**
   `"I have 2 dogs and 3 cats"`
   → `["2", "3"]`
   **Answer:** `str.match(/\d+/g)`

2. **Check if a string contains only alphabets:**
   `"HelloWorld"` → true
   **Answer:** `/^[A-Za-z]+$/.test(str)`

---

### **Medium**

3. **Remove all special characters except space from a string:**
   `"Hello@# World!$%"` → `"Hello World"`
   **Answer:** `str.replace(/[^\w ]/g, '')`

4. **Mask all but last 4 digits in phone number:**
   `"9876543210"` → `"******3210"`
   **Answer:** `str.replace(/\d(?=\d{4})/g, "*")`

---

### **Hard**

5. **Extract hashtags from a tweet:**
   `"Loving #JavaScript and #React!"` → `["#JavaScript", "#React"]`
   **Answer:** `str.match(/#\w+/g)`

6. **Find and count duplicate words in a string:**
   `"hi hi hello hello world"`
   → `{hi: 2, hello: 2}`
   **Answer:**

   ```js
   let str = "hi hi hello hello world";
   let counts = {};
   str.toLowerCase().match(/\b\w+\b/g).forEach(word => {
     counts[word] = (counts[word] || 0) + 1;
   });
   console.log(counts);
   ```

---

Would you like:

* **Timer-based quiz app** (auto-evaluate regex questions)?
* **Mini Project: Live form validation with error messages (real-time typing)?**
* Or **Build your own Regex Cheat Sheet Web Tool (React)**?

Awesome! Let’s get started with all three. I’ll guide you step by step:

---

### **1. Timer-Based Regex Quiz App (React)**

**Features:**

* Timer for each question
* Input field to answer regex tasks
* Auto-evaluation of answers
* Score tracking

**Tech:** React + Tailwind (optional)

**Code Structure:**

```jsx
// RegexQuizApp.jsx
import { useState, useEffect } from 'react';

const questions = [
  { question: "Match any 3-digit number", answer: "\\d{3}" },
  { question: "Match an email", answer: "\\S+@\\S+\\.\\S+" },
  // Add more...
];

export default function RegexQuizApp() {
  const [index, setIndex] = useState(0);
  const [input, setInput] = useState('');
  const [timeLeft, setTimeLeft] = useState(15);
  const [score, setScore] = useState(0);

  useEffect(() => {
    const timer = setInterval(() => setTimeLeft(t => t - 1), 1000);
    if (timeLeft === 0) handleNext();
    return () => clearInterval(timer);
  }, [timeLeft]);

  const handleNext = () => {
    if (input.trim() === questions[index].answer) setScore(score + 1);
    setInput('');
    setTimeLeft(15);
    setIndex((i) => (i + 1) % questions.length);
  };

  return (
    <div className="p-4">
      <h2>Q: {questions[index].question}</h2>
      <input value={input} onChange={e => setInput(e.target.value)} />
      <p>Time left: {timeLeft}s</p>
      <button onClick={handleNext}>Submit</button>
      <p>Score: {score}</p>
    </div>
  );
}
```

---

### **2. Live Form Validation Mini Project**

**Features:**

* Email validation
* Password strength checker
* Real-time error messages

**Code Sample:**

```jsx
import { useState } from 'react';

export default function LiveFormValidator() {
  const [email, setEmail] = useState('');
  const [password, setPassword] = useState('');

  const emailValid = /^\S+@\S+\.\S+$/.test(email);
  const passwordStrong = /^(?=.*[A-Z])(?=.*[a-z])(?=.*\d).{8,}$/.test(password);

  return (
    <div className="p-4">
      <input
        type="email"
        placeholder="Email"
        value={email}
        onChange={e => setEmail(e.target.value)}
      />
      {!emailValid && email && <p className="text-red-500">Invalid email</p>}

      <input
        type="password"
        placeholder="Password"
        value={password}
        onChange={e => setPassword(e.target.value)}
      />
      {!passwordStrong && password && (
        <p className="text-red-500">Weak password</p>
      )}
    </div>
  );
}
```

---

### **3. Regex Cheat Sheet Tool (React Project)**

**Features:**

* Searchable list of common regex patterns
* Copy button
* Real-time example explanation

**Basic Layout:**

```jsx
const regexPatterns = [
  { title: "Digits only", pattern: "\\d+" },
  { title: "Alphabets only", pattern: "[a-zA-Z]+" },
  { title: "Email", pattern: "\\S+@\\S+\\.\\S+" },
];

export default function RegexCheatSheet() {
  const [search, setSearch] = useState('');

  const filtered = regexPatterns.filter(item =>
    item.title.toLowerCase().includes(search.toLowerCase())
  );

  return (
    <div className="p-4">
      <input
        placeholder="Search pattern..."
        value={search}
        onChange={e => setSearch(e.target.value)}
      />
      {filtered.map((item, i) => (
        <div key={i}>
          <h4>{item.title}</h4>
          <code>{item.pattern}</code>
          <button onClick={() => navigator.clipboard.writeText(item.pattern)}>Copy</button>
        </div>
      ))}
    </div>
  );
}
```

---

Let me know which project you want to start with first, and I’ll give you full UI polish, component split, and bonus challenges.

