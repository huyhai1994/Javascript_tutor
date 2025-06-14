**Summary (English):**

* **Arrow functions** are a concise alternative to the traditional `function` syntax, using `=>` instead of the `function` keyword.
* **Syntax:**

  ```js
  const fn = (param1, param2) => {
    // function body
    return result;
  };
  ```
* If there’s **only one parameter**, you can drop the parentheses:

  ```js
  const square = x => x * x;
  ```
* If the body is **a single expression**, you can omit both the braces `{}` and the `return` keyword; that expression’s value is returned automatically.
* For **no parameters**, use empty parentheses:

  ```js
  const horn = () => console.log("Toot");
  ```
* Arrow functions behave much like regular function expressions but with less boilerplate, making small functions easier to write.

---

**Tóm tắt (Tiếng Việt):**

* **Hàm mũi tên** (arrow functions) là cách viết ngắn gọn thay thế cú pháp `function`, dùng ký hiệu `=>`.
* **Cú pháp cơ bản:**

  ```js
  const fn = (thamSố1, thamSố2) => {
    // thân hàm
    return kếtQuả;
  };
  ```
* Nếu chỉ có **một tham số**, bạn có thể bỏ ngoặc đơn:

  ```js
  const square = x => x * x;
  ```
* Nếu thân hàm chỉ gồm **một biểu thức**, bạn có thể bỏ cả dấu `{}` và từ khóa `return`—biểu thức đó sẽ được trả về tự động.
* Với **không tham số**, dùng ngoặc đơn trống:

  ```js
  const horn = () => console.log("Toot");
  ```
* Arrow functions hoạt động giống như function expression thông thường nhưng gọn hơn, rất tiện để viết các hàm nhỏ.
