Great, Manoj! I’ll start by giving you the **JavaScript String Exercise Questions with Answers** step-by-step—starting from the **Easy** section. Here's the first set:

---

### **Easy String Exercises with Answers**

1. **Reverse a string**

   ```js
   function reverseString(str) {
     return str.split('').reverse().join('');
   }
   console.log(reverseString("hello")); // "olleh"
   ```

2. **Check if a string is a palindrome**

   ```js
   function isPalindrome(str) {
     const reversed = str.split('').reverse().join('');
     return str === reversed;
   }
   console.log(isPalindrome("madam")); // true
   ```

3. **Count the number of vowels in a string**

   ```js
   function countVowels(str) {
     return (str.match(/[aeiou]/gi) || []).length;
   }
   console.log(countVowels("hello world")); // 3
   ```

4. **Convert a string to uppercase**

   ```js
   let str = "hello";
   console.log(str.toUpperCase()); // "HELLO"
   ```

5. **Convert a string to lowercase**

   ```js
   let str = "HELLO";
   console.log(str.toLowerCase()); // "hello"
   ```

6. **Find the length of a string without using `.length`**

   ```js
   function getLength(str) {
     let count = 0;
     for (let char of str) {
       count++;
     }
     return count;
   }
   console.log(getLength("hello")); // 5
   ```

7. **Remove all spaces from a string**

   ```js
   function removeSpaces(str) {
     return str.replace(/\s+/g, '');
   }
   console.log(removeSpaces("hello world")); // "helloworld"
   ```

8. **Concatenate two strings without using `+` operator**

   ```js
   let str1 = "Hello";
   let str2 = "World";
   console.log(str1.concat(" ", str2)); // "Hello World"
   ```

9. **Find the first non-repeated character**

   ```js
   function firstNonRepeatedChar(str) {
     for (let char of str) {
       if (str.indexOf(char) === str.lastIndexOf(char)) {
         return char;
       }
     }
     return null;
   }
   console.log(firstNonRepeatedChar("swiss")); // "w"
   ```

10. **Replace all occurrences of a substring**

    ```js
    let str = "JavaScript is great. I love JavaScript.";
    console.log(str.replace(/JavaScript/g, "JS")); 
    // "JS is great. I love JS."
    ```

11. **Remove all occurrences of a specified character**

    ```js
    function removeChar(str, char) {
      let regex = new RegExp(char, 'g');
      return str.replace(regex, '');
    }
    console.log(removeChar("hello", "l")); // "heo"
    ```

12. **Check if a string starts with a substring**

    ```js
    let str = "JavaScript";
    console.log(str.startsWith("Java")); // true
    ```

13. **Check if a string ends with a substring**

    ```js
    let str = "JavaScript";
    console.log(str.endsWith("Script")); // true
    ```

14. **Count the number of words in a sentence**

    ```js
    function countWords(sentence) {
      return sentence.trim().split(/\s+/).length;
    }
    console.log(countWords("I am learning JavaScript")); // 4
    ```

15. **Remove duplicate characters from a string**

    ```js
    function removeDuplicates(str) {
      return [...new Set(str)].join('');
    }
    console.log(removeDuplicates("aabbcc")); // "abc"
    ```

16. **Convert a sentence to title case**

    ```js
    function toTitleCase(sentence) {
      return sentence.toLowerCase().split(" ")
        .map(word => word.charAt(0).toUpperCase() + word.slice(1))
        .join(" ");
    }
    console.log(toTitleCase("hello world")); // "Hello World"
    ```

17. **Swap case of each character**

    ```js
    function swapCase(str) {
      return str.split('').map(char =>
        char === char.toUpperCase() ? char.toLowerCase() : char.toUpperCase()
      ).join('');
    }
    console.log(swapCase("Hello")); // "hELLO"
    ```

18. **Find the most frequent character**

    ```js
    function mostFrequentChar(str) {
      let map = {};
      for (let char of str) {
        map[char] = (map[char] || 0) + 1;
      }
      let max = 0, char = '';
      for (let key in map) {
        if (map[key] > max) {
          max = map[key];
          char = key;
        }
      }
      return char;
    }
    console.log(mostFrequentChar("aabbbccde")); // "b"
    ```

19. **Truncate a string longer than a certain length**

    ```js
    function truncate(str, length) {
      return str.length > length ? str.slice(0, length) + "..." : str;
    }
    console.log(truncate("This is a long sentence", 10)); // "This is a ..."
    ```

20. **Check if a string is a valid URL**

    ```js
    function isValidURL(str) {
      try {
        new URL(str);
        return true;
      } catch (e) {
        return false;
      }
    }
    console.log(isValidURL("https://www.google.com")); // true
    ```

---

**Medium-level** 

Here are **all the Medium-Level JavaScript String Exercises with answers** (as requested, no PDF):

---

### **1. Check if two strings are anagrams**

```javascript
function areAnagrams(str1, str2) {
  return str1.split('').sort().join('') === str2.split('').sort().join('');
}
console.log(areAnagrams("listen", "silent")); // true
```

---

### **2. Check if a string contains only digits**

```javascript
function onlyDigits(str) {
  return /^\d+$/.test(str);
}
console.log(onlyDigits("12345")); // true
console.log(onlyDigits("123abc")); // false
```

---

### **3. Count the occurrences of a specific word in a paragraph**

```javascript
function countWord(paragraph, word) {
  const regex = new RegExp(`\\b${word}\\b`, 'gi');
  return (paragraph.match(regex) || []).length;
}
console.log(countWord("Apple banana apple. Apple pie!", "apple")); // 3
```

---

### **4. Reverse the order of words in a sentence**

```javascript
function reverseWords(sentence) {
  return sentence.split(' ').reverse().join(' ');
}
console.log(reverseWords("I love JavaScript")); // "JavaScript love I"
```

---

### **5. Capitalize the first letter of each word in a sentence**

```javascript
function titleCase(sentence) {
  return sentence
    .split(' ')
    .map(word => word[0].toUpperCase() + word.slice(1))
    .join(' ');
}
console.log(titleCase("hello world")); // "Hello World"
```

---

### **6. Find the longest substring without repeating characters**

```javascript
function longestUniqueSubstring(s) {
  let maxLen = 0, start = 0, seen = {}, longest = "";
  for (let i = 0; i < s.length; i++) {
    if (seen[s[i]] >= start) start = seen[s[i]] + 1;
    seen[s[i]] = i;
    if (i - start + 1 > maxLen) {
      maxLen = i - start + 1;
      longest = s.slice(start, i + 1);
    }
  }
  return longest;
}
console.log(longestUniqueSubstring("abcabcbb")); // "abc"
```

---

### **7. Rotate a string to the left by a given number of positions**

```javascript
function rotateLeft(str, n) {
  return str.slice(n) + str.slice(0, n);
}
console.log(rotateLeft("abcdef", 2)); // "cdefab"
```

---

### **8. Check if a string is a valid email address**

```javascript
function isValidEmail(email) {
  const regex = /^[\w.-]+@[a-zA-Z\d.-]+\.[a-zA-Z]{2,}$/;
  return regex.test(email);
}
console.log(isValidEmail("test@example.com")); // true
```

---

### **9. String Compression (e.g., "aabcccccaaa" => "a2b1c5a3")**

```javascript
function compressString(str) {
  let result = "", count = 1;
  for (let i = 1; i <= str.length; i++) {
    if (str[i] === str[i - 1]) {
      count++;
    } else {
      result += str[i - 1] + count;
      count = 1;
    }
  }
  return result;
}
console.log(compressString("aabcccccaaa")); // "a2b1c5a3"
```

---

### **10. Levenshtein Distance**

```javascript
function levenshtein(a, b) {
  const dp = Array(a.length + 1).fill().map(() => Array(b.length + 1).fill(0));
  for (let i = 0; i <= a.length; i++) dp[i][0] = i;
  for (let j = 0; j <= b.length; j++) dp[0][j] = j;

  for (let i = 1; i <= a.length; i++) {
    for (let j = 1; j <= b.length; j++) {
      if (a[i - 1] === b[j - 1]) {
        dp[i][j] = dp[i - 1][j - 1];
      } else {
        dp[i][j] = 1 + Math.min(dp[i - 1][j], dp[i][j - 1], dp[i - 1][j - 1]);
      }
    }
  }
  return dp[a.length][b.length];
}
console.log(levenshtein("kitten", "sitting")); // 3
```

---

### **11. Convert string to camelCase**

```javascript
function toCamelCase(str) {
  return str
    .split(/[\s_-]+/)
    .map((word, i) =>
      i === 0 ? word.toLowerCase() : word[0].toUpperCase() + word.slice(1).toLowerCase()
    )
    .join('');
}
console.log(toCamelCase("hello world example")); // "helloWorldExample"
```

---

### **12. Validate an IPv4 address**

```javascript
function isValidIPv4(str) {
  const parts = str.split('.');
  return parts.length === 4 && parts.every(p => p >= 0 && p <= 255 && /^\d+$/.test(p));
}
console.log(isValidIPv4("192.168.1.1")); // true
console.log(isValidIPv4("999.999.999.999")); // false
```

---

### **13. Reverse words and their characters in a sentence**

```javascript
function reverseWordsAndChars(sentence) {
  return sentence
    .split(' ')
    .map(word => word.split('').reverse().join(''))
    .reverse()
    .join(' ');
}
console.log(reverseWordsAndChars("hello world")); // "dlrow olleh"
```

---

### **14. Remove HTML tags from a string**

```javascript
function removeHTMLTags(str) {
  return str.replace(/<[^>]*>/g, '');
}
console.log(removeHTMLTags("<p>Hello <b>world</b></p>")); // "Hello world"
```

---

### **15. Run-Length Encoding**

```javascript
function runLengthEncode(str) {
  let result = "", count = 1;
  for (let i = 1; i <= str.length; i++) {
    if (str[i] === str[i - 1]) count++;
    else {
      result += str[i - 1] + count;
      count = 1;
    }
  }
  return result;
}
console.log(runLengthEncode("aaabbbbbcc")); // "a3b5c2"
```

---

### **16. Find longest common prefix in an array of strings**

```javascript
function longestCommonPrefix(strs) {
  if (!strs.length) return '';
  let prefix = strs[0];
  for (let str of strs) {
    while (!str.startsWith(prefix)) {
      prefix = prefix.slice(0, -1);
    }
  }
  return prefix;
}
console.log(longestCommonPrefix(["flower", "flow", "flight"])); // "fl"
```

---

### **17. Decode Run-Length Encoded string**

```javascript
function decodeRLE(str) {
  return str.replace(/([a-zA-Z])(\d+)/g, (_, char, num) => char.repeat(+num));
}
console.log(decodeRLE("a3b5c2")); // "aaabbbbbcc"
```

---

### **18. Base64 encode and decode**

```javascript
function base64Encode(str) {
  return btoa(str);
}
function base64Decode(encoded) {
  return atob(encoded);
}
console.log(base64Encode("hello")); // "aGVsbG8="
console.log(base64Decode("aGVsbG8=")); // "hello"
```

---

### **19. Validate string date (MM/DD/YYYY)**

```javascript
function isValidDate(str) {
  return /^(0[1-9]|1[0-2])\/(0[1-9]|[12]\d|3[01])\/\d{4}$/.test(str);
}
console.log(isValidDate("12/25/2020")); // true
```

---

### **20. Convert to snake\_case**

```javascript
function toSnakeCase(str) {
  return str
    .replace(/\s+/g, '_')
    .replace(/[A-Z]/g, letter => `_${letter.toLowerCase()}`)
    .replace(/^_/, '')
    .toLowerCase();
}
console.log(toSnakeCase("Hello World Example")); // "hello_world_example"
```

---

**Tough Level** 

Here are the **Tough-Level JavaScript String Exercises with Answers** — no PDF, just clean Q\&A format:

---

### **1. Find all permutations of a string**

```javascript
function getPermutations(str) {
  if (str.length <= 1) return [str];
  const perms = [];
  for (let i = 0; i < str.length; i++) {
    const char = str[i];
    const remaining = str.slice(0, i) + str.slice(i + 1);
    for (let subPerm of getPermutations(remaining)) {
      perms.push(char + subPerm);
    }
  }
  return perms;
}
console.log(getPermutations("abc"));
// Output: [ 'abc', 'acb', 'bac', 'bca', 'cab', 'cba' ]
```

---

### **2. Check if a string is a valid palindrome after removing at most one character**

```javascript
function validPalindrome(str) {
  function isPal(s, left, right) {
    while (left < right) {
      if (s[left] !== s[right]) return false;
      left++;
      right--;
    }
    return true;
  }
  let left = 0, right = str.length - 1;
  while (left < right) {
    if (str[left] !== str[right]) {
      return isPal(str, left + 1, right) || isPal(str, left, right - 1);
    }
    left++;
    right--;
  }
  return true;
}
console.log(validPalindrome("abca")); // true
```

---

### **3. Implement a simple template engine**

```javascript
function render(template, data) {
  return template.replace(/{{(\w+)}}/g, (_, key) => data[key] || '');
}
const template = "Hello, {{name}}! Welcome to {{place}}.";
const data = { name: "Manoj", place: "India" };
console.log(render(template, data)); // Hello, Manoj! Welcome to India.
```

---

### **4. Count number of palindromic substrings**

```javascript
function countPalindromes(s) {
  let count = 0;
  for (let i = 0; i < s.length; i++) {
    count += expand(i, i) + expand(i, i + 1);
  }
  function expand(left, right) {
    let res = 0;
    while (left >= 0 && right < s.length && s[left] === s[right]) {
      res++;
      left--;
      right++;
    }
    return res;
  }
  return count;
}
console.log(countPalindromes("aaa")); // 6
```

---

### **5. Find the minimum window substring that contains all characters of another string**

```javascript
function minWindow(s, t) {
  const need = {}, window = {};
  for (let c of t) need[c] = (need[c] || 0) + 1;
  let left = 0, right = 0, valid = 0, start = 0, len = Infinity;

  while (right < s.length) {
    let c = s[right++];
    if (need[c]) {
      window[c] = (window[c] || 0) + 1;
      if (window[c] === need[c]) valid++;
    }

    while (valid === Object.keys(need).length) {
      if (right - left < len) {
        start = left;
        len = right - left;
      }
      let d = s[left++];
      if (need[d]) {
        if (window[d] === need[d]) valid--;
        window[d]--;
      }
    }
  }
  return len === Infinity ? "" : s.slice(start, start + len);
}
console.log(minWindow("ADOBECODEBANC", "ABC")); // "BANC"
```

---

### \**6. Implement string wildcard pattern matching (?, *)**

```javascript
function isMatch(s, p) {
  const dp = Array(s.length + 1).fill().map(() => Array(p.length + 1).fill(false));
  dp[0][0] = true;

  for (let j = 1; j <= p.length; j++) {
    if (p[j - 1] === '*') dp[0][j] = dp[0][j - 1];
  }

  for (let i = 1; i <= s.length; i++) {
    for (let j = 1; j <= p.length; j++) {
      if (p[j - 1] === '?' || s[i - 1] === p[j - 1]) {
        dp[i][j] = dp[i - 1][j - 1];
      } else if (p[j - 1] === '*') {
        dp[i][j] = dp[i][j - 1] || dp[i - 1][j];
      }
    }
  }

  return dp[s.length][p.length];
}
console.log(isMatch("abcde", "a*e")); // true
```

---

### **7. Implement a Trie and use it for prefix search**

```javascript
class TrieNode {
  constructor() {
    this.children = {};
    this.isWord = false;
  }
}
class Trie {
  constructor() {
    this.root = new TrieNode();
  }
  insert(word) {
    let node = this.root;
    for (let c of word) {
      if (!node.children[c]) node.children[c] = new TrieNode();
      node = node.children[c];
    }
    node.isWord = true;
  }
  startsWith(prefix) {
    let node = this.root;
    for (let c of prefix) {
      if (!node.children[c]) return false;
      node = node.children[c];
    }
    return true;
  }
}
const trie = new Trie();
trie.insert("apple");
console.log(trie.startsWith("app")); // true
```

---

### **8. Encode string to UTF-8 byte array**

```javascript
function encodeToUTF8(str) {
  return new TextEncoder().encode(str);
}
console.log(encodeToUTF8("hello")); // Uint8Array [104, 101, 108, 108, 111]
```

---

### **9. Find the longest repeated substring**

```javascript
function longestRepeatedSubstring(s) {
  let substrings = [];
  for (let i = 0; i < s.length; i++) {
    substrings.push(s.slice(i));
  }
  substrings.sort();
  let max = "";
  for (let i = 0; i < substrings.length - 1; i++) {
    let lcp = commonPrefix(substrings[i], substrings[i + 1]);
    if (lcp.length > max.length) max = lcp;
  }
  return max;

  function commonPrefix(a, b) {
    let i = 0;
    while (i < a.length && i < b.length && a[i] === b[i]) i++;
    return a.slice(0, i);
  }
}
console.log(longestRepeatedSubstring("banana")); // "ana"
```

---

### **10. Detect and return all duplicate substrings of a given length**

```javascript
function findDuplicates(str, k) {
  const seen = new Set();
  const duplicates = new Set();
  for (let i = 0; i <= str.length - k; i++) {
    const substr = str.substring(i, i + k);
    if (seen.has(substr)) duplicates.add(substr);
    seen.add(substr);
  }
  return [...duplicates];
}
console.log(findDuplicates("banana", 2)); // ['an', 'na']
```

---

Here are the remaining **Tough JavaScript String Exercises with Answers** (from question 11 to 20):

---

### **11. Reverse words in a sentence but preserve the relative word order**

```javascript
function reverseWordsKeepOrder(sentence) {
  return sentence
    .split(' ')
    .map(word => word.split('').reverse().join(''))
    .join(' ');
}

console.log(reverseWordsKeepOrder("The quick brown fox"));
// Output: "ehT kciuq nworb xof"
```

---

### **12. Find the longest substring with at most K distinct characters**

```javascript
function longestSubstringKDistinct(s, k) {
  let left = 0, maxLength = 0;
  const map = new Map();

  for (let right = 0; right < s.length; right++) {
    const char = s[right];
    map.set(char, (map.get(char) || 0) + 1);

    while (map.size > k) {
      const leftChar = s[left];
      map.set(leftChar, map.get(leftChar) - 1);
      if (map.get(leftChar) === 0) map.delete(leftChar);
      left++;
    }

    maxLength = Math.max(maxLength, right - left + 1);
  }

  return maxLength;
}

console.log(longestSubstringKDistinct("eceba", 2)); // Output: 3 ("ece")
```

---

### **13. Format multi-line text into paragraph (word wrap at certain width)**

```javascript
function wordWrap(text, maxWidth) {
  const words = text.split(' ');
  let lines = [], line = "";

  for (let word of words) {
    if ((line + word).length <= maxWidth) {
      line += word + " ";
    } else {
      lines.push(line.trim());
      line = word + " ";
    }
  }

  if (line) lines.push(line.trim());

  return lines.join('\n');
}

console.log(wordWrap("This is an example of text that needs to be wrapped into lines.", 20));
```

---

### **14. Check if a string follows a pattern (e.g., "abab" matches "redblueredblue")**

```javascript
function wordPatternMatch(pattern, str) {
  function dfs(pIndex, sIndex, map, used) {
    if (pIndex === pattern.length && sIndex === str.length) return true;
    if (pIndex === pattern.length || sIndex === str.length) return false;

    const patternChar = pattern[pIndex];

    for (let i = sIndex + 1; i <= str.length; i++) {
      const word = str.slice(sIndex, i);

      if (!map.has(patternChar) && !used.has(word)) {
        map.set(patternChar, word);
        used.add(word);
        if (dfs(pIndex + 1, i, map, used)) return true;
        map.delete(patternChar);
        used.delete(word);
      } else if (map.get(patternChar) === word) {
        if (dfs(pIndex + 1, i, map, used)) return true;
      }
    }

    return false;
  }

  return dfs(0, 0, new Map(), new Set());
}

console.log(wordPatternMatch("abab", "redblueredblue")); // true
```

---

### **15. Find the shortest palindrome by adding characters at the end**

```javascript
function shortestPalindrome(str) {
  for (let i = 0; i < str.length; i++) {
    let suffix = str.slice(i);
    if (suffix === suffix.split('').reverse().join('')) {
      return str + str.slice(0, i).split('').reverse().join('');
    }
  }
  return str;
}

console.log(shortestPalindrome("race")); // "racecar"
```

---

### **16. Count anagrams of a given word in a list**

```javascript
function countAnagrams(word, wordList) {
  const sortedWord = word.split('').sort().join('');
  return wordList.filter(w => w.split('').sort().join('') === sortedWord).length;
}

console.log(countAnagrams("listen", ["enlist", "google", "inlets", "banana"])); // 2
```

---

### **17. Minimum window in a string that contains all characters of another string**

```javascript
function minWindow(s, t) {
  if (t.length > s.length) return "";

  let map = {};
  for (let c of t) map[c] = (map[c] || 0) + 1;

  let left = 0, right = 0, count = t.length, minLen = Infinity, minStart = 0;

  while (right < s.length) {
    if (map[s[right]] > 0) count--;
    map[s[right]] = (map[s[right]] || 0) - 1;
    right++;

    while (count === 0) {
      if (right - left < minLen) {
        minLen = right - left;
        minStart = left;
      }

      map[s[left]] = (map[s[left]] || 0) + 1;
      if (map[s[left]] > 0) count++;
      left++;
    }
  }

  return minLen === Infinity ? "" : s.substr(minStart, minLen);
}

console.log(minWindow("ADOBECODEBANC", "ABC")); // "BANC"
```

---

### **18. Check if a string is a valid Roman numeral**

```javascript
function isValidRoman(str) {
  const regex = /^(M{0,3})(CM|CD|D?C{0,3})(XC|XL|L?X{0,3})(IX|IV|V?I{0,3})$/;
  return regex.test(str);
}

console.log(isValidRoman("XIV")); // true
console.log(isValidRoman("IIII")); // false
```

---

### **19. Generate all valid IP addresses from a given string**

```javascript
function restoreIpAddresses(s) {
  let res = [];

  function backtrack(start = 0, parts = []) {
    if (parts.length === 4 && start === s.length) {
      res.push(parts.join('.'));
      return;
    }
    if (parts.length === 4) return;

    for (let len = 1; len <= 3; len++) {
      if (start + len > s.length) break;
      let part = s.substring(start, start + len);
      if ((part.length > 1 && part[0] === '0') || +part > 255) continue;
      backtrack(start + len, [...parts, part]);
    }
  }

  backtrack();
  return res;
}

console.log(restoreIpAddresses("25525511135")); // ["255.255.11.135", "255.255.111.35"]
```

---

### **20. Reverse words in sentence while preserving spaces and punctuation**

```javascript
function reverseWordsPreserveFormat(sentence) {
  return sentence.split(/(\s+)/)
    .map(word => word.trim() ? word.split('').reverse().join('') : word)
    .join('');
}

console.log(reverseWordsPreserveFormat("Hello, world!  How are you?"));
// Output: ",olleH !dlrow  woH era ?uoy"
```

---

Here’s your **JavaScript String Methods Revision Sheet** — focused, interview-ready, and with examples:

---

### **1. `charAt(index)`**

* Returns the character at a specified index.

```javascript
let str = "Manoj";
console.log(str.charAt(2)); // "n"
```

---

### **2. `charCodeAt(index)`**

* Returns the Unicode of the character at the given index.

```javascript
console.log("A".charCodeAt(0)); // 65
```

---

### **3. `slice(start, end)`**

* Extracts a section of a string.

```javascript
console.log("FrontendDeveloper".slice(0, 8)); // "Frontend"
console.log("FrontendDeveloper".slice(-9));  // "Developer"
```

---

### **4. `substring(start, end)`**

* Similar to `slice` but **doesn’t accept negative indexes**.

```javascript
console.log("Frontend".substring(0, 5)); // "Front"
```

---

### **5. `substr(start, length)`** *(Deprecated, but still asked sometimes)*

* Extracts from start position for given length.

```javascript
console.log("Frontend".substr(0, 5)); // "Front"
```

---

### **6. `split(separator, limit)`**

* Splits the string into an array by a separator.

```javascript
console.log("React,Redux,Node".split(",")); // ["React", "Redux", "Node"]
```

---

### **7. `replace(searchValue, newValue)`**

* Replaces first match.

```javascript
console.log("I love JS".replace("JS", "JavaScript")); // "I love JavaScript"
```

---

### **8. `replaceAll(searchValue, newValue)`**

* Replaces all matches.

```javascript
console.log("haha haha".replaceAll("ha", "he")); // "hehe hehe"
```

---

### **9. `toUpperCase()` / `toLowerCase()`**

```javascript
console.log("hello".toUpperCase()); // "HELLO"
console.log("WORLD".toLowerCase()); // "world"
```

---

### **10. `trim()` / `trimStart()` / `trimEnd()`**

```javascript
console.log("  JavaScript  ".trim());     // "JavaScript"
console.log("  JS  ".trimStart());        // "JS  "
```

---

### **11. `startsWith()` / `endsWith()`**

```javascript
console.log("Frontend".startsWith("Front")); // true
console.log("ReactJS".endsWith("JS"));       // true
```

---

### **12. `includes(substring)`**

```javascript
console.log("I love JS".includes("love")); // true
```

---

### **13. `indexOf()` / `lastIndexOf()`**

```javascript
console.log("banana".indexOf("a"));      // 1
console.log("banana".lastIndexOf("a"));  // 5
```

---

### **14. `repeat(count)`**

```javascript
console.log("ha".repeat(3)); // "hahaha"
```

---

### **15. `padStart(length, char)` / `padEnd(length, char)`**

```javascript
console.log("5".padStart(3, "0")); // "005"
console.log("5".padEnd(3, "."));   // "5.."
```

---

### **16. `match(regex)`**

* Returns result of matching string with regex.

```javascript
console.log("abc123".match(/\d+/)); // ["123"]
```

---

### **17. `matchAll(regex)`**

```javascript
let text = "test1 test2";
let regex = /test\d/g;
console.log([...text.matchAll(regex)].map(m => m[0])); // ["test1", "test2"]
```

---

### **18. `localeCompare()`**

* Compares two strings in the current locale.

```javascript
console.log("a".localeCompare("b")); // -1
```

---

### **19. `concat()`**

```javascript
let a = "Hello ";
let b = "World";
console.log(a.concat(b)); // "Hello World"
```

---

### **20. `codePointAt(index)`**

* Works with emojis and UTF-16 characters.

```javascript
console.log("😄".codePointAt(0)); // 128516
```

---
Perfect! Here's your **JavaScript Array + String Quick Revision Theory Sheet** – concise and powerful for interviews:

---

## **JavaScript String Methods – Quick Revision**

### **1. `charAt(index)`**

Returns the character at the specified index.

```js
"hello".charAt(1); // 'e'
```

### **2. `charCodeAt(index)`**

Returns Unicode value of character.

```js
"A".charCodeAt(0); // 65
```

### **3. `slice(start, end)`**

Extracts part of a string (non-inclusive of end).

```js
"hello".slice(1, 4); // 'ell'
```

### **4. `substring(start, end)`**

Similar to `slice`, but doesn't accept negative indexes.

```js
"hello".substring(1, 4); // 'ell'
```

### **5. `substr(start, length)`** *(deprecated)*

```js
"hello".substr(1, 3); // 'ell'
```

### **6. `split(separator)`**

Splits string into array.

```js
"one,two,three".split(','); // ['one', 'two', 'three']
```

### **7. `replace(search, replace)`**

Replaces first match (use regex with `/g` for all).

```js
"hi hi".replace("hi", "hello"); // 'hello hi'
```

### **8. `toLowerCase()` / `toUpperCase()`**

```js
"Hello".toLowerCase(); // 'hello'
```

### **9. `trim()`**

Removes whitespace from both ends.

```js
"  hello  ".trim(); // 'hello'
```

### **10. `includes(substring)`**

Checks if substring exists.

```js
"hello".includes("ell"); // true
```

### **11. `startsWith()` / `endsWith()`**

```js
"hello".startsWith("he"); // true
```

### **12. `match(regex)`**

Returns matches based on regex.

```js
"abc123".match(/\d+/); // ['123']
```

---

## **JavaScript Array Methods – Quick Revision**

### **1. `push()` / `pop()`**

Add/remove at the end.

```js
let arr = [1,2];
arr.push(3); // [1,2,3]
arr.pop();   // [1,2]
```

### **2. `unshift()` / `shift()`**

Add/remove at the start.

```js
arr.unshift(0); // [0,1,2]
arr.shift();    // [1,2]
```

### **3. `map()`**

Transforms array elements.

```js
[1,2,3].map(x => x*2); // [2,4,6]
```

### **4. `filter()`**

Filters based on condition.

```js
[1,2,3].filter(x => x % 2 === 0); // [2]
```

### **5. `reduce()`**

Reduces to single value.

```js
[1,2,3].reduce((sum, x) => sum + x, 0); // 6
```

### **6. `find()` / `findIndex()`**

```js
[4,5,6].find(x => x > 4); // 5
```

### **7. `includes()`**

```js
[1,2,3].includes(2); // true
```

### **8. `sort()`**

Sorts **lexicographically** by default.

```js
[10,2,5].sort();         // [10,2,5]
[10,2,5].sort((a,b) => a-b); // [2,5,10]
```

### **9. `concat()`**

Merges arrays.

```js
[1].concat([2,3]); // [1,2,3]
```

### **10. `join()`**

Combines array into string.

```js
[1,2,3].join('-'); // '1-2-3'
```

---

### **BONUS: Useful One-Liners**

```js
// Reverse string
[...'hello'].reverse().join(''); // 'olleh'

// Count frequency
"banana".split('').reduce((acc, ch) => {
  acc[ch] = (acc[ch] || 0) + 1;
  return acc;
}, {}); // { b:1, a:3, n:2 }

// Remove duplicates from array
[...new Set([1,2,2,3])]; // [1,2,3]
```

---

Great! Here are **5 String + Array Mixed Logic Interview Practice Questions** with **JavaScript solutions**:

---

### **1. Find All Duplicates in an Array**

**Question:**
Write a function that takes an array and returns all duplicate elements.

```js
function findDuplicates(arr) {
  let seen = new Set();
  let duplicates = new Set();
  for (let num of arr) {
    if (seen.has(num)) {
      duplicates.add(num);
    } else {
      seen.add(num);
    }
  }
  return [...duplicates];
}

// Example
console.log(findDuplicates([1, 2, 3, 2, 4, 1, 5])); // [2, 1]
```

---

### **2. Remove All Non-Alphabetic Characters from a String**

**Question:**
Write a function that removes everything except letters.

```js
function cleanString(str) {
  return str.replace(/[^a-zA-Z]/g, '');
}

// Example
console.log(cleanString("Hello123!@ World#")); // "HelloWorld"
```

---

### **3. Count Words with Even Length in a Sentence**

**Question:**
Return how many words in a string have even length.

```js
function countEvenWords(sentence) {
  return sentence.split(' ').filter(word => word.length % 2 === 0).length;
}

// Example
console.log(countEvenWords("This is a test sentence")); // 3
```

---

### **4. Find the Longest Word in a String**

**Question:**
Return the longest word from a sentence.

```js
function longestWord(str) {
  return str.split(' ').reduce((longest, current) =>
    current.length > longest.length ? current : longest
  );
}

// Example
console.log(longestWord("JavaScript is super powerful")); // "JavaScript"
```

---

### **5. Check if Two Strings are One Edit Away**

**Question:**
One edit can be insert, remove, or replace a character. Return true if two strings are one edit away.

```js
function oneEditAway(s1, s2) {
  if (Math.abs(s1.length - s2.length) > 1) return false;

  let [i, j] = [0, 0], foundDifference = false;
  while (i < s1.length && j < s2.length) {
    if (s1[i] !== s2[j]) {
      if (foundDifference) return false;
      foundDifference = true;
      if (s1.length > s2.length) i++;
      else if (s2.length > s1.length) j++;
      else { i++; j++; }
    } else {
      i++; j++;
    }
  }
  return true;
}

// Example
console.log(oneEditAway("pale", "ple")); // true
console.log(oneEditAway("pale", "bale")); // true
console.log(oneEditAway("pale", "bake")); // false
```

---
Perfect! Here are **5 more slightly harder String + Array mixed logic interview practice questions** with **JavaScript solutions**:

---

### **1. Find the First Non-Repeating Character in a String**

**Question:**
Write a function to return the first character that doesn’t repeat.

```js
function firstUniqueChar(str) {
  let freq = {};
  for (let char of str) {
    freq[char] = (freq[char] || 0) + 1;
  }
  for (let char of str) {
    if (freq[char] === 1) return char;
  }
  return null;
}

// Example
console.log(firstUniqueChar("swiss")); // "w"
```

---

### **2. Group Anagrams from an Array of Strings**

**Question:**
Write a function to group all anagrams from a list of words.

```js
function groupAnagrams(words) {
  let map = {};
  for (let word of words) {
    let sorted = word.split('').sort().join('');
    if (!map[sorted]) map[sorted] = [];
    map[sorted].push(word);
  }
  return Object.values(map);
}

// Example
console.log(groupAnagrams(["bat", "tab", "tap", "pat", "cat"]));
// [["bat", "tab"], ["tap", "pat"], ["cat"]]
```

---

### **3. Check if Two Arrays Have the Same Elements (Ignoring Order)**

**Question:**
Write a function to check if two arrays contain the same elements (ignoring order and duplicates).

```js
function arraysEqual(a, b) {
  let setA = new Set(a);
  let setB = new Set(b);
  if (setA.size !== setB.size) return false;
  for (let item of setA) {
    if (!setB.has(item)) return false;
  }
  return true;
}

// Example
console.log(arraysEqual([1, 2, 3], [3, 2, 1])); // true
console.log(arraysEqual([1, 2, 3], [3, 2, 4])); // false
```

---

### **4. Find the Common Characters Across All Strings**

**Question:**
Write a function to return characters that appear in every string in the array.

```js
function commonChars(arr) {
  return arr.reduce((acc, str) => {
    return acc.split('').filter(char => str.includes(char)).join('');
  });
}

// Example
console.log(commonChars(["apple", "plea", "leap"])); // "ple"
```

---

### **5. Convert Array of Words to a Sentence in CamelCase**

**Question:**
Write a function to join an array of words into a camelCase sentence.

```js
function toCamelCase(arr) {
  return arr
    .map((word, i) => i === 0 ? word.toLowerCase() : word[0].toUpperCase() + word.slice(1).toLowerCase())
    .join('');
}

// Example
console.log(toCamelCase(["hello", "world", "today", "rocks"])); // "helloWorldTodayRocks"
```

---

 **5 more expert-level** 

 Great! Here are **5 expert-level String + Array mixed logic interview challenges** with **JavaScript solutions**:

---

### **1. Minimum Window Substring**

**Question:**
Find the smallest substring in `s` that contains all the characters of `t`.

```js
function minWindow(s, t) {
  let map = {};
  for (let c of t) map[c] = (map[c] || 0) + 1;

  let start = 0, end = 0, minStart = 0, minLen = Infinity, counter = t.length;

  while (end < s.length) {
    if (map[s[end++]]-- > 0) counter--;
    while (counter === 0) {
      if (end - start < minLen) {
        minStart = start;
        minLen = end - start;
      }
      if (++map[s[start++]] > 0) counter++;
    }
  }

  return minLen === Infinity ? "" : s.slice(minStart, minStart + minLen);
}

// Example
console.log(minWindow("ADOBECODEBANC", "ABC")); // "BANC"
```

---

### **2. Longest Consecutive Sequence in an Array**

**Question:**
Given an unsorted array, return the length of the longest consecutive elements sequence.

```js
function longestConsecutive(nums) {
  let set = new Set(nums);
  let max = 0;

  for (let num of set) {
    if (!set.has(num - 1)) {
      let current = num;
      let streak = 1;
      while (set.has(current + 1)) {
        current++;
        streak++;
      }
      max = Math.max(max, streak);
    }
  }

  return max;
}

// Example
console.log(longestConsecutive([100, 4, 200, 1, 3, 2])); // 4 (1,2,3,4)
```

---

### **3. Find All Substrings with Exactly K Distinct Characters**

**Question:**
Write a function that returns all substrings of a string that contain exactly K distinct characters.

```js
function substringsWithKDistinct(s, k) {
  let result = new Set();

  for (let i = 0; i < s.length; i++) {
    let set = new Set();
    let temp = "";
    for (let j = i; j < s.length; j++) {
      set.add(s[j]);
      temp += s[j];
      if (set.size === k) result.add(temp);
      if (set.size > k) break;
    }
  }

  return [...result];
}

// Example
console.log(substringsWithKDistinct("abcba", 2)); // ["ab", "abc", "bc", "bcb", "cb", "ba"]
```

---

### **4. Decode Encoded String (e.g., "3\[a2\[c]]")**

**Question:**
Implement a function to decode an encoded string like `"3[a2[c]]"` → `"accaccacc"`.

```js
function decodeString(s) {
  let stack = [];
  let num = 0, curr = '';

  for (let char of s) {
    if (!isNaN(char)) {
      num = num * 10 + Number(char);
    } else if (char === '[') {
      stack.push([curr, num]);
      curr = '';
      num = 0;
    } else if (char === ']') {
      let [prevStr, repeat] = stack.pop();
      curr = prevStr + curr.repeat(repeat);
    } else {
      curr += char;
    }
  }

  return curr;
}

// Example
console.log(decodeString("3[a2[c]]")); // "accaccacc"
```

---

### **5. Remove Invalid Parentheses to Make a Valid Expression**

**Question:**
Remove the minimum number of parentheses to make the string valid.

```js
function minRemoveToMakeValid(s) {
  let stack = [], arr = s.split('');

  for (let i = 0; i < arr.length; i++) {
    if (arr[i] === '(') stack.push(i);
    else if (arr[i] === ')') {
      if (stack.length) stack.pop();
      else arr[i] = '';
    }
  }

  for (let i of stack) arr[i] = '';
  return arr.join('');
}

// Example
console.log(minRemoveToMakeValid("a)b(c)d")); // "ab(c)d"
```

---

Great! Let's start with **System Design-based JS Logic Questions** first, followed by **DOM Manipulation Practice Tasks**.

---

## **Part 1: System Design-Based JavaScript Logic Questions**

These questions focus on how you'd build and structure real-world features in JavaScript—like in a scalable web app.

### 1. **Design a Rate Limiter Function**

```js
function rateLimiter(limit, interval) {
  let calls = 0;
  let startTime = Date.now();

  return function () {
    const now = Date.now();
    if (now - startTime > interval) {
      calls = 0;
      startTime = now;
    }
    if (calls < limit) {
      calls++;
      console.log("Allowed");
    } else {
      console.log("Blocked");
    }
  };
}

const apiCall = rateLimiter(3, 5000);
apiCall(); apiCall(); apiCall(); apiCall(); // 4th will be blocked
```

---

### 2. **Implement a Custom Event Emitter**

```js
class EventEmitter {
  constructor() {
    this.events = {};
  }

  on(event, listener) {
    (this.events[event] ||= []).push(listener);
  }

  emit(event, data) {
    (this.events[event] || []).forEach(fn => fn(data));
  }

  off(event) {
    delete this.events[event];
  }
}

const emitter = new EventEmitter();
emitter.on("message", msg => console.log("Got:", msg));
emitter.emit("message", "Hello!");
```

---

### 3. **Implement a Simple Caching Mechanism**

```js
function createCache() {
  const cache = new Map();
  return function (key, value = null) {
    if (value !== null) cache.set(key, value);
    return cache.get(key);
  };
}

const cache = createCache();
cache("user", { name: "John" });
console.log(cache("user")); // { name: "John" }
```

---

### 4. **Design a Debounce Function**

```js
function debounce(fn, delay) {
  let timer;
  return function (...args) {
    clearTimeout(timer);
    timer = setTimeout(() => fn.apply(this, args), delay);
  };
}

const log = debounce(() => console.log("Called!"), 1000);
log(); log(); log(); // Only called once after 1 sec
```

---

### 5. **Implement a Priority Queue using Array**

```js
class PriorityQueue {
  constructor() {
    this.queue = [];
  }

  enqueue(item, priority) {
    this.queue.push({ item, priority });
    this.queue.sort((a, b) => b.priority - a.priority);
  }

  dequeue() {
    return this.queue.shift().item;
  }
}

const pq = new PriorityQueue();
pq.enqueue("Low", 1);
pq.enqueue("High", 10);
console.log(pq.dequeue()); // High
```

---

## **Part 2: DOM Manipulation Practice Tasks**

### 1. **Change the text content of a div with ID "output"**

```js
document.getElementById("output").textContent = "Hello, DOM!";
```

---

### 2. **Create a button dynamically and append it to the body**

```js
const btn = document.createElement("button");
btn.textContent = "Click Me";
document.body.appendChild(btn);
```

---

### 3. **Toggle class "active" on a div when clicked**

```js
document.getElementById("toggleDiv").addEventListener("click", function() {
  this.classList.toggle("active");
});
```

---

### 4. **Add a new list item to an unordered list with ID "myList"**

```js
const li = document.createElement("li");
li.textContent = "New Item";
document.getElementById("myList").appendChild(li);
```

---

### 5. **Capture input field value and display it on button click**

```html
<input type="text" id="inputBox" />
<button onclick="showValue()">Show</button>
<div id="display"></div>

<script>
  function showValue() {
    const val = document.getElementById("inputBox").value;
    document.getElementById("display").textContent = val;
  }
</script>
```

---

**Regex (Regular Expression)** in JavaScript is a powerful pattern-matching tool used to search, match, and manipulate strings based on specific patterns.

---

### **Why We Use Regex in JavaScript:**

1. **Validation:**

   * Validate email, phone numbers, passwords, etc.
   * Example: Check if a string is a valid email.

2. **Searching:**

   * Find whether a pattern exists in a string.
   * Example: Find all digits in a sentence.

3. **Replacing:**

   * Replace substrings that match a pattern.
   * Example: Replace all spaces with dashes.

4. **Extracting:**

   * Extract matching substrings from a larger string.
   * Example: Extract all hashtags from a post.

---

### **Basic Syntax:**

```js
const regex = /pattern/flags;
```

* **pattern**: The expression you want to match.
* **flags**: Optional modifiers (`g`, `i`, `m`, etc.)

  * `g`: global (match all)
  * `i`: case-insensitive
  * `m`: multiline

---

### **Examples:**

1. **Test if a string contains digits:**

```js
const regex = /\d+/;
console.log(regex.test("abc123")); // true
```

2. **Match all words starting with # (hashtags):**

```js
const str = "Loving #JavaScript and #Coding!";
const hashtags = str.match(/#\w+/g);
console.log(hashtags); // ["#JavaScript", "#Coding"]
```

3. **Replace all spaces with dashes:**

```js
const str = "Hello World Again";
console.log(str.replace(/\s+/g, "-")); // "Hello-World-Again"
```

---

### Common Regex Patterns:

| Pattern  | Meaning                            |
| -------- | ---------------------------------- |
| `\d`     | Any digit (0–9)                    |
| `\w`     | Word character (a-z, A-Z, 0-9, \_) |
| `\s`     | Any whitespace                     |
| `.`      | Any character except newline       |
| `^`      | Start of string                    |
| `$`      | End of string                      |
| `+`      | One or more                        |
| `*`      | Zero or more                       |
| `?`      | Optional                           |
| `{n,m}`  | Between n and m times              |
| `[abc]`  | Match a, b, or c                   |
| `[^abc]` | Not a, b, or c                     |

---

Would you like 10 regex-based coding exercises with JavaScript solutions next?

