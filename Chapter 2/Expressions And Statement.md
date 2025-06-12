**Summary (English):**

* A **fragment of code** that produces a value is called an **expression**. Examples include literals (`22`, `"hello"`), parenthesized expressions, and any use of operators.
* A **statement** is a complete syntactic unit—like a full sentence in English—often ending in a semicolon. A program is simply a list of statements.
* The simplest statement is just an expression followed by `;` (e.g. `1;  !false;`). By themselves these produce values but have **no side effects**, so running them does nothing visible.
* Statements that **do** something (e.g. `console.log("hi");`) are useful because they have side effects—printing to the screen, modifying variables, etc.
* JavaScript has **automatic semicolon insertion**, allowing you to sometimes omit semicolons, but the rules are subtle and error-prone. As a best practice, include a semicolon at the end of every statement that requires one.

---

**Tóm tắt (Tiếng Việt):**

* **Biểu thức** (expression) là đoạn mã trả về một giá trị, chẳng hạn literal (`22`, `"hello"`), biểu thức trong ngoặc, hoặc bất kỳ phép toán nào.
* **Câu lệnh** (statement) là đơn vị mã hoàn chỉnh—giống một câu tiếng Anh—thường kết thúc bằng dấu chấm phẩy. Một chương trình là tập hợp các câu lệnh.
* Câu lệnh đơn giản nhất là một biểu thức kèm `;` (ví dụ `1;  !false;`). Những lệnh này chỉ sinh ra giá trị mà **không có tác dụng phụ**, nên khi chạy sẽ không có gì xảy ra.
* Những câu lệnh **có tác dụng** (như `console.log("hi");`) mới hữu ích vì chúng gây ra **tác dụng phụ**—in ra màn hình, thay đổi biến, v.v.
* JavaScript có cơ chế **chèn chấm phẩy tự động**, cho phép đôi khi bỏ `;`, nhưng quy tắc khá phức tạp và dễ sai. Thông thường, bạn nên luôn viết `;` ở cuối mỗi câu lệnh cần nó.
