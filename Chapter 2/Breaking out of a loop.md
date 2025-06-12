**Summary (English):**

* The **`break` statement** immediately exits the **nearest** enclosing loop (or `switch`), skipping any remaining iterations.
* It’s commonly used when you detect a condition that means “we’re done”—for example, finding the first number divisible by both 2 and 7:

  ```js
  for (let current = 2; ; current = current + 1) {
    if (current % 7 == 0 && current % 2 == 0) {
      console.log(current);
      break;
    }
  }
  // → 14
  ```
* Without a `break`, loops with always-true conditions (`for (;;)` or `while (true)`) run forever.
* **Important:** `break` only stops the loop it’s directly inside. Nested loops require a `break` in each level you want to exit.

---

**Tóm tắt (Tiếng Việt):**

* Câu lệnh **`break`** **ngay lập tức** thoát khỏi **vòng lặp gần nhất** (hoặc khối `switch`), bỏ qua các lượt lặp còn lại.
* Thường dùng khi phát hiện một điều kiện “đã xong” – ví dụ, tìm số đầu tiên chia hết cho cả 2 và 7:

  ```js
  for (let current = 2; ; current = current + 1) {
    if (current % 7 == 0 && current % 2 == 0) {
      console.log(current);
      break;
    }
  }
  // → 14
  ```
* Không có `break`, vòng lặp có điều kiện luôn đúng (`for (;;)` hoặc `while (true)`) sẽ **chạy vô hạn**.
* **Lưu ý:** `break` chỉ dừng vòng lặp chứa nó trực tiếp. Với vòng lặp lồng nhau, bạn cần `break` trong mỗi cấp muốn thoát.
