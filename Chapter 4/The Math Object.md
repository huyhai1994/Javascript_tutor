**Summary (English)**
The built-in **Math** object in JavaScript is a single, globally available container (“octopus”) holding a grab-bag of number-related utility functions and constants—things like:

* **Constants**: `Math.PI` (π), `Math.E` (Euler’s number), etc.
* **Basic operations**:

  * `Math.min(…)` / `Math.max(…)`
  * `Math.sqrt(x)`
  * Trigonometry: `Math.sin(x)`, `Math.cos(x)`, `Math.tan(x)`
  * Inverse trig: `Math.asin(x)`, `Math.acos(x)`, `Math.atan(x)`
* **Randomness**:

  * `Math.random()` returns a pseudorandom number in \[0, 1).
  * To get a random integer in a range, you commonly multiply by the range size and apply `Math.floor`, `Math.ceil`, or `Math.round`.

    ```js
    // Random integer 0–9
    Math.floor(Math.random() * 10);
    ```
* **Rounding and absolute value**:

  * `Math.floor(x)` → largest integer ≤ x
  * `Math.ceil(x)` → smallest integer ≥ x
  * `Math.round(x)` → nearest integer to x
  * `Math.abs(x)`  → absolute value of x

Because there’s only one `Math` object, you don’t risk accidentally overwriting its methods (unless you really try to). It keeps all these functions grouped under the single global name `Math`, avoiding pollution of the global namespace.

---

**Tóm tắt (Tiếng Việt)**
Đối tượng **Math** có sẵn trong JavaScript là một “bạch tuộc” duy nhất chứa rất nhiều hàm tiện ích và hằng số toán học—như:

* **Hằng số**: `Math.PI` (π), `Math.E`, v.v.
* **Các phép tính cơ bản**:

  * `Math.min(…)` / `Math.max(…)`
  * `Math.sqrt(x)`
  * Hàm lượng giác: `Math.sin(x)`, `Math.cos(x)`, `Math.tan(x)`
  * Hàm lượng giác ngược: `Math.asin(x)`, `Math.acos(x)`, `Math.atan(x)`
* **Sinh số ngẫu nhiên**:

  * `Math.random()` trả về số giả ngẫu nhiên trong khoảng \[0, 1).
  * Muốn lấy số nguyên trong một miền, thường ta nhân ra rồi dùng `Math.floor`, `Math.ceil` hoặc `Math.round`:

    ```js
    // Số nguyên ngẫu nhiên từ 0 đến 9
    Math.floor(Math.random() * 10);
    ```
* **Làm tròn và trị tuyệt đối**:

  * `Math.floor(x)` → số nguyên lớn nhất ≤ x
  * `Math.ceil(x)`  → số nguyên nhỏ nhất ≥ x
  * `Math.round(x)` → làm tròn về số nguyên gần nhất
  * `Math.abs(x)`   → trị tuyệt đối của x

Vì chỉ có **một** đối tượng `Math`, bạn không sợ vô tình ghi đè mất các hàm này trừ khi thật sự cố ý. Tất cả được gom gọn dưới tên `Math`, tránh làm “ô nhiễm” không gian tên toàn cục.
