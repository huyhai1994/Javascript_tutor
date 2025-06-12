**Summary (English):**

1. **Control Flow**

   * A JavaScript program is a sequence of statements executed **in order**, from top to bottom.
   * Each statement may produce a value or cause a side effect (like showing a prompt or logging to the console).

2. **Conditional Execution**

   * To make your code **branch**—running some statements only when a condition holds—you use the `if` keyword:

     ```js
     let theNumber = Number(prompt("Pick a number"));
     if (!Number.isNaN(theNumber)) {
       console.log("The square of your number is " + theNumber * theNumber);
     }
     ```
   * An `if` without braces applies only to the next single statement; with `{ … }`, you can group multiple statements.
   * You can extend an `if` with `else` for the “false” case, and chain multiple tests with `else if`:

     ```js
     let num = Number(prompt("Pick a number"));
     if (num < 10) {
       console.log("Small");
     } else if (num < 100) {
       console.log("Medium");
     } else {
       console.log("Large");
     }
     ```
   * This creates a **branching** program flow, choosing exactly one path based on the tested conditions.

---

**Tóm tắt (Tiếng Việt):**

1. **Luồng điều khiển**

   * Một chương trình JavaScript là chuỗi các câu lệnh được thực thi **tuần tự**, từ trên xuống dưới.
   * Mỗi câu lệnh có thể trả về giá trị hoặc gây ra tác dụng phụ (ví dụ: hiển thị hộp thoại, in ra console).

2. **Thực thi có điều kiện**

   * Để làm cho chương trình **phân nhánh**—chỉ thực thi một số câu lệnh khi thỏa mãn điều kiện—dùng từ khóa `if`:

     ```js
     let theNumber = Number(prompt("Pick a number"));
     if (!Number.isNaN(theNumber)) {
       console.log("Bình phương của số bạn nhập là " + theNumber * theNumber);
     }
     ```
   * Nếu không dùng `{ … }`, `if` chỉ áp dụng cho đúng câu lệnh kế tiếp; có `{}` thì có thể gom nhiều câu lệnh lại.
   * Bạn có thể mở rộng `if` với `else` cho trường hợp điều kiện sai, và dùng `else if` để kiểm tra nhiều nhánh:

     ```js
     let num = Number(prompt("Pick a number"));
     if (num < 10) {
       console.log("Nhỏ");
     } else if (num < 100) {
       console.log("Vừa");
     } else {
       console.log("Lớn");
     }
     ```
   * Cấu trúc này cho phép chương trình **chọn** duy nhất một trong các nhánh dựa trên điều kiện.
