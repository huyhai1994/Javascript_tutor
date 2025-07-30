- A regular expression is a type of object. 
- Can be either constructed with the `RegExp` constructor or written as a literal value by enclosing a pattern in forward slash (`/`) characters.
``` javascript

let re1 = new RegExp('abc');
let re2 = /abc/;



```

- Some characters, such as question marks and plus signs, have special meaning in regular expressions and must be preceded by a backslash if they are meant to represent the character itself. 