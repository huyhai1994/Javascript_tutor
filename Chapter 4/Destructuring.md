**Destructuring (English Summary):**

* **Array destructuring:** lets you “peek inside” an array and bind its elements to named variables in one step.

  ```js
  // Instead of letting table refer to [a,b,c,d] and using table[0], table[1],…
  function phi([n00, n01, n10, n11]) {
    // now n00 === table[0], n01 === table[1], etc.
    return (n11 * n00 - n10 * n01) /
      Math.sqrt((n10 + n11) * (n00 + n01) * (n01 + n11) * (n00 + n10));
  }
  ```
* **Object destructuring:** similarly unpacks properties by name into local variables, using `{}` syntax:

  ```js
  let { name, age } = { name: "Faraji", age: 23 };
  // now name === "Faraji", age === 23
  ```
* You can destructure any binding created with `let`, `const`, or `var`.
* If you try to destructure **`null`** or **`undefined`**, you get a runtime error—just like accessing any property on those non-objects.

**Tóm tắt (Tiếng Việt):**

* **Phá vỡ mảng (Array destructuring):** cho phép bạn “mở hộp” một mảng và gán từng phần tử vào biến ngay khi khai báo:

  ```js
  // Thay vì dùng table[0], table[1],…
  function phi([n00, n01, n10, n11]) {
    // n00 tương ứng table[0], n01 tương ứng table[1],…
    return (n11 * n00 - n10 * n01) /
      Math.sqrt((n10 + n11) * (n00 + n01) * (n01 + n11) * (n00 + n10));
  }
  ```
* **Phá vỡ đối tượng (Object destructuring):** mở các thuộc tính của object theo tên, dùng cú pháp `{}`:

  ```js
  let { name, age } = { name: "Faraji", age: 23 };
  // name === "Faraji", age === 23
  ```
* Bạn có thể dùng destructuring với bindings khai báo qua `let`, `const` hoặc `var`.
* Nếu bạn cố gắng destructure **`null`** hoặc **`undefined`**, chương trình sẽ **báo lỗi** lúc chạy—giống như khi bạn truy cập thuộc tính trên non-object.
