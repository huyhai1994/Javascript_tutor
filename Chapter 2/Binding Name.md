**Summary (English):**

* **Binding names** (identifiers) in JavaScript must start with a letter, `$`, or `_`; they may then include digits as well.
* They **cannot** start with a digit, nor include any punctuation or special characters beyond `$` and `_`.
* **Reserved words**—keywords like `let`, `class`, `function`, `if`, `else`, `return`, and many more—**cannot** be used as binding names.
* There’s a long list of future‐reserved words (e.g. `enum`, `implements`, `interface`, `package`, `private`, `protected`, `public`, `static`, `yield`, etc.) that also may not be used.

---

**Tóm tắt (Tiếng Việt):**

* **Tên binding** (tên biến, hàm, v.v.) trong JavaScript phải bắt đầu bằng chữ cái, `$` hoặc `_`; sau đó có thể gồm các chữ số.
* **Không được** bắt đầu bằng số, cũng không được dùng ký tự đặc biệt hoặc dấu câu nào khác ngoài `$` và `_`.
* **Từ khóa** (keywords) như `let`, `class`, `function`, `if`, `else`, `return`… và rất nhiều từ khóa dành cho tương lai (ví dụ `enum`, `implements`, `interface`, `package`, `private`, `protected`, `public`, `static`, `yield`…) **không thể** dùng làm tên binding.
* Nếu bạn cố đặt tên trùng với một từ bị cấm, JavaScript sẽ báo **syntax error**.
