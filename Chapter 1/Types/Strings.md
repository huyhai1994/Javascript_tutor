* **Strings** represent text in JavaScript and are written by surrounding content with single quotes (`'…'`), double quotes (`"…"`), or backticks (`` `…` ``).
* **Escaping:** Use a backslash (`\`) before special characters (e.g. `\'`, `\"`, `\\`) so they become part of the string rather than ending it. Common escapes include `\n` (newline) and `\t` (tab).
* **Unicode:** JavaScript strings are sequences of 16-bit code ([[16 bits Strings]]) units (`UTF-16`). Characters outside the Basic Multilingual Plane—like many emoji—use *two* code units (surrogate pairs).
* **Concatenation:** The `+` operator glues strings together:

  ```js
  "con" + "cat" + "e" + "nate"  // "concatenate"
  ```
* **Template literals:** Backtick-quoted strings can span multiple lines and embed expressions with `${…}`:

  ```js
  `Half of 100 is ${100 / 2}`  // "Half of 100 is 50"
  ```
* **String methods:** Strings have built-in methods (e.g. `.slice()`, `.toUpperCase()`) for common operations.

---

* **Chuỗi** trong JavaScript biểu diễn văn bản và được tạo bằng cách đặt nội dung vào trong dấu nháy đơn (`'…'`), nháy kép (`"…"`), hoặc dấu backtick (`` `…` ``).
* **Ký tự thoát:** Dùng dấu gạch chéo ngược (`\`) trước các ký tự đặc biệt (ví dụ `\'`, `\"`, `\\`) để chúng không kết thúc chuỗi. Các ký tự thoát phổ biến là `\n` (xuống dòng) và `\t` (tab).
* **Unicode:** Chuỗi JavaScript là dãy các phần tử 16-bit (UTF-16). Những ký tự ngoài Phần Đãng Cơ Bản—như emoji—sẽ chiếm *hai* phần tử (surrogate pair).
* **Nối chuỗi:** Toán tử `+` dùng để ghép chuỗi:

  ```js
  "con" + "cat" + "e" + "nate"  // "concatenate"
  ```
* **Template literal:** Chuỗi backtick có thể trải nhiều dòng và nhúng biểu thức với `${…}`:

  ```js
  `Half of 100 is ${100 / 2}`  // "Half of 100 is 50"
  ```
* **Phương thức chuỗi:** Chuỗi có các phương thức tích hợp (ví dụ `.slice()`, `.toUpperCase()`) để thao tác thường gặp.

