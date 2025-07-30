- regular expressions are useful because they allow us to describe more complicated patterns.
- In a regular expression, putting a set of characters between square brackets makes that part of the expression match any of the characters between the brackets.
 ```javascript

console.log(/[0123456789]/.test("in 1992));
// -> true

console.log(/[0-9]/.test("in 1992));
// -> true

```
- With in square brackets, a hyphen(-) between two characters can be used to indicate a range of characters, where the ordering is determined by the character's Unicode number. 