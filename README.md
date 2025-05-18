# Regex Notes
---

### Regular Expressions (Regex) Notes

#### What is Regex?

* Patterns used to match character combinations in strings.
* In JavaScript, regex is implemented as **Regex Literals** or **RegExp Objects**:

  * **Regex Literal**: `/pattern/`
  * **RegExp Object**: `new RegExp("pattern")`

---

### Key Concepts and Examples

#### **Creating a Regex**

1. **Regex Literal:**

   ```javascript
   const regex = /pattern/;
   ```
2. **Using RegExp Constructor:**

   ```javascript
   const regex = new RegExp("pattern");
   ```

#### **Testing Strings with Regex**

* Use the `.test()` method to check if a pattern exists in a string:

  ```javascript
  const string = "The dog chased the cat";
  const regex = /the/i; // 'i' flag ignores case
  console.log(regex.test(string)); // Output: true
  ```

#### **Matching Multiple Possibilities**

* Use the `|` operator (OR) to match any of the provided patterns:

  ```javascript
  let petString = "James has a pet cat.";
  let petRegex = /dog|cat|bird|fish/;
  console.log(petRegex.test(petString)); // Output: true
  ```

#### **Case-Insensitive Matching**

* Add the `i` flag to ignore case:

  ```javascript
  let myString = "freeCodeCamp";
  let fccRegex = /freeCodeCamp/i;
  console.log(fccRegex.test(myString)); // Output: true
  ```

#### **Extracting Matches**

* Use `.match()` to retrieve matches from a string:

  ```javascript
  console.log('Abdul Awal Sajib'.match(/awal/i)); // Output: ["Awal"]
  ```

#### **Matching Multiple Characters**

* Use the `g` flag for global matching (find all matches, not just the first):

  ```javascript
  const string = "aaa bbb aaa";
  const regex = /aaa/g;
  console.log(string.match(regex)); // Output: ["aaa", "aaa"]
  ```

#### **Wildcard Matching**

* Use the wildcard character `.` to match any single character:

  ```javascript
  let exampleStr = "Let's have fun with regular expressions!";
  let unRegex = /.un/; // Matches "fun", "sun", etc.
  console.log(unRegex.test(exampleStr)); // Output: true
  ```

#### **Matching Character Ranges**

* Use square brackets `[]` to define character classes:

  ```javascript
  let quoteSample = "Beware of bugs in the above code.";
  let vowelRegex = /[aeiou]/ig; // Match vowels (case-insensitive)
  console.log(quoteSample.match(vowelRegex).length); // Output: 15
  ```

---

### Flags in Regex

* `i`: Case-insensitive matching.
* `g`: Global match (find all matches).
* `m`: Multiline matching.

---

