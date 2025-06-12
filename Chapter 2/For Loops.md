**Summary (English):**

* The **`for` loop** is a compact way to repeat code with a looping variable (counter). Its header has three parts, separated by semicolons:

  1. **Initialization:** executed once before the loop starts (e.g. `let number = 0;`).
  2. **Condition:** checked before each iteration; if `true`, the loop body runs (e.g. `number <= 12`); if `false`, the loop ends.
  3. **Final expression:** executed after each iteration to update the counter (e.g. `number += 2`).
* Example printing even numbers 0–12:

  ```js
  for (let number = 0; number <= 12; number += 2) {
    console.log(number);
  }
  // → 0, 2, 4, 6, 8, 10, 12
  ```
* A `for` loop is equivalent to a `while` loop with the same initialization, condition check, and counter update—but more concise.

---

**Tóm tắt (Tiếng Việt):**

* **Vòng lặp `for`** là cách viết gọn để lặp với một biến đếm. Phần tiêu đề gồm ba thành phần, ngăn cách bằng dấu chấm phẩy:

  1. **Khởi tạo:** thực thi một lần trước khi bắt đầu vòng lặp (ví dụ `let number = 0;`).
  2. **Điều kiện:** kiểm tra trước mỗi lần lặp; nếu `true`, thân vòng lặp chạy; nếu `false`, vòng lặp dừng (ví dụ `number <= 12`).
  3. **Cập nhật cuối:** thực thi sau mỗi lần lặp để tăng/giảm biến đếm (ví dụ `number += 2`).
* Ví dụ in các số chẵn từ 0 đến 12:

  ```js
  for (let number = 0; number <= 12; number += 2) {
    console.log(number);
  }
  // → 0, 2, 4, 6, 8, 10, 12
  ```
* Vòng lặp `for` tương đương với `while` có cùng khởi tạo, điều kiện và cập nhật, nhưng ngắn gọn hơn.
