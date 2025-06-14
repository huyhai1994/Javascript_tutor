**Summary (English):**

* When the `function` keyword appears at the start of a statement, it creates a **function declaration**, e.g.:

  ```js
  function square(x) {
    return x * x;
  }
  ```
* A function declaration defines a binding (here, `square`) and points it to the given function. It’s slightly shorter to write and doesn’t need a trailing semicolon.
* **Hoisting:** Declarations are conceptually moved to the top of their scope before code runs. This means you can call a declared function **before** its definition appears in the code:

  ```js
  console.log(future());  // → "You’ll never have flying cars"

  function future() {
    return "You’ll never have flying cars";
  }
  ```
* Because of hoisting, you can organize your code freely—declare helper functions below their usage if that makes the top‐level logic clearer.

---

**Tóm tắt (Tiếng Việt):**

* Khi từ khóa `function` đứng ở đầu một câu lệnh, bạn đang dùng **khai báo hàm** (function declaration), ví dụ:

  ```js
  function square(x) {
    return x * x;
  }
  ```
* Khai báo hàm sẽ tạo một binding (ở đây là `square`) trỏ tới hàm đó. Cú pháp này ngắn gọn hơn và không cần dấu chấm phẩy ở cuối.
* **Hoisting (nâng lên):** Các khai báo hàm được “nâng” lên đầu phạm vi của chúng trước khi thực thi mã. Do đó, bạn có thể **gọi hàm trước khi định nghĩa** xuất hiện trong tệp:

  ```js
  console.log(future());  // → "You’ll never have flying cars"

  function future() {
    return "You’ll never have flying cars";
  }
  ```
* Nhờ hoisting, bạn có thể tự do sắp xếp mã—định nghĩa các hàm trợ giúp ở dưới vị trí gọi nếu điều đó làm cho logic chính rõ ràng hơn.
