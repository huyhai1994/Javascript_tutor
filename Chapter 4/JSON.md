**Summary (English):**
JavaScript’s **JSON** (JavaScript Object Notation) is a text‐based format for **serializing** data—turning objects and arrays (with their nested structure) into a plain string for storage or network transfer, then parsing that string back into live values. JSON syntax resembles JavaScript literals but with restrictions:

* **Property names** must be in **double quotes**.
* Only **data**—no functions, variables, or comments—may appear.
* Values can be objects (`{}`), arrays (`[]`), strings, numbers, booleans, or `null`.

To work with JSON in JavaScript:

* **`JSON.stringify(value)`** → returns a JSON‐encoded string of the given value.
* **`JSON.parse(string)`**  → parses a JSON string back into the corresponding object/array/value.

**Example:**

```js
let entry = {
  squirrel: false,
  events: ["work", "weekend"]
};
let json = JSON.stringify(entry);
// → '{"squirrel":false,"events":["workend"]}'
let data = JSON.parse(json);
console.log(data.events);  // → ["work", "weekend"]
```

---

**Tóm tắt (Tiếng Việt):**
**JSON** (JavaScript Object Notation) là định dạng văn bản dùng để **chuyển đổi** (serialize) các đối tượng và mảng trong JavaScript thành chuỗi, rồi sau đó **phân tích** (parse) chuỗi đó trở lại thành giá trị ban đầu. Cú pháp JSON giống với literal trong JavaScript nhưng có một số quy tắc:

* **Tên thuộc tính** phải nằm trong **dấu nháy kép** (`"key"`).
* Chỉ cho phép **dữ liệu**—không có hàm, biến, hay chú thích.
* Giá trị có thể là object (`{}`), array (`[]`), string, number, boolean, hoặc `null`.

Hai hàm chính để làm việc với JSON:

* **`JSON.stringify(value)`** → trả về chuỗi JSON mã hoá giá trị.
* **`JSON.parse(string)`**  → chuyển chuỗi JSON về lại đối tượng hoặc giá trị tương ứng.

**Ví dụ:**

```js
let entry = {
  squirrel: false,
  events: ["work", "weekend"]
};
let json = JSON.stringify(entry);
// → '{"squirrel":false,"events":["work","weekend"]}'
let data = JSON.parse(json);
console.log(data.events);  // → ["work", "weekend"]
```
