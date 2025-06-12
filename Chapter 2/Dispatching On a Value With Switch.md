**Summary (English):**

* A **`switch` statement** offers a cleaner alternative to a long chain of `if…else if…else` when you need to “dispatch” based on the value of a single expression.
* Syntax:

  ```js
  switch (expression) {
    case value1:
      // code to run if expression === value1
      break;
    case value2:
      // code to run if expression === value2
      break;
    // …you can have as many cases as you like…
    default:
      // code to run if no case matches
      break;
  }
  ```
* **How it works:**

  1. Evaluate the `expression`.
  2. Find the first `case` whose label strictly equals that value.
  3. Execute statements starting at that `case` **until** you hit a `break` (or the end of the `switch`).
  4. If no `case` matches, run the `default` block (if present).
* **Important details:**

  * Without a `break`, execution **falls through** to subsequent cases.
  * You can group multiple case labels for the same block by stacking `case` lines before a shared body.
  * A `default` is optional but useful for handling unexpected values.

---

**Tóm tắt (Tiếng Việt):**

* **Câu lệnh `switch`** là cách gọn gàng hơn so với chuỗi `if…else if…else` khi bạn chỉ cần phân nhánh dựa trên giá trị của một biểu thức duy nhất.
* Cú pháp:

  ```js
  switch (biểu_thức) {
    case giá_trị1:
      // mã chạy khi biểu_thức === giá_trị1
      break;
    case giá_trị2:
      // mã chạy khi biểu_thức === giá_trị2
      break;
    // …có thể có bao nhiêu case tùy ý…
    default:
      // mã chạy khi không case nào khớp
      break;
  }
  ```
* **Cách hoạt động:**

  1. Đánh giá `biểu_thức`.
  2. Tìm `case` đầu tiên có nhãn **bằng hẳn** giá trị đó.
  3. Thực thi các câu lệnh từ đó cho đến khi gặp `break` (hoặc hết `switch`).
  4. Nếu không có `case` nào khớp, chạy khối `default` (nếu có).
* **Lưu ý quan trọng:**

  * Thiếu `break` sẽ dẫn đến **fall-through**—tiếp tục chạy các case sau.
  * Có thể gom nhiều nhãn `case` trước cùng một khối mã để chia sẻ hành vi.
  * `default` là tùy chọn nhưng hữu ích để xử lý giá trị không ngờ tới.
