**Summary (English):**

* JavaScript’s environment includes built-in **functions**—values you can call to perform actions.
* To **invoke** (call) a function, use its name followed by parentheses, optionally with arguments inside. For example, in a browser:

  ```js
  prompt("Enter passcode:");
  ```

  brings up a dialog asking for input.
* The **console.log** function prints values to the console; most other JS environments provide a similar logging function.
* Functions may have **side effects** (like showing a dialog or writing to the console) or may **return** a value.
* When you use a function call in an expression, the call itself produces the function’s return value, so you can write things like:

  ```js
  console.log(Math.max(2, 4));  // → 4
  let x = Math.min(2, 4) + 100; // x becomes 102
  ```

---

**Tóm tắt (Tiếng Việt):**

* Môi trường JavaScript có sẵn các **hàm**—giá trị có thể được gọi (invoke) để thực thi hành động.
* Để **gọi** hàm, viết tên hàm kèm ngoặc đơn, có thể có đối số bên trong, ví dụ trong trình duyệt:

  ```js
  prompt("Enter passcode:");
  ```

  hiển thị hộp thoại yêu cầu nhập.
* Hàm **console.log** in giá trị ra bảng điều khiển (console); hầu hết môi trường JS khác cũng có chức năng tương tự.
* Hàm có thể sinh ra **tác dụng phụ** (side effect) như hiển thị hộp thoại hoặc ghi log, hoặc có thể **trả về** một giá trị.
* Khi dùng lời gọi hàm trong biểu thức, lời gọi đó **trả về** giá trị mà hàm trả về, ví dụ:

  ```js
  console.log(Math.max(2, 4));   // → 4
  let x = Math.min(2, 4) + 100;  // x = 102
  ```
