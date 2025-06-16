**Recursion (English Summary):**

* A **recursive function** is one that calls itself. As long as each call makes progress toward a stopping condition, recursion works fine—JavaScript manages the call stack for you.

* **Example – Exponentiation:**

  ```js
  function power(base, exponent) {
    if (exponent === 0) {
      return 1;
    } else {
      return base * power(base, exponent - 1);
    }
  }
  console.log(power(2, 3));  // → 8
  ```

  Each call multiplies by `base` and decrements the exponent until it reaches 0.

* **Trade-offs:**

  * Recursion often mirrors the mathematical definition and can make code clearer.
  * However, recursive calls incur overhead on the call stack and can be slower or risk a stack overflow if too deep.
  * For simple repetition, loops may be faster; recursion shines when the problem naturally divides into smaller subproblems (e.g. tree traversal).

* **Example – Searching for a solution:**
  Find a sequence of operations (either “+5” or “×3”) that transforms 1 into a target number:

  ```js
  function findSolution(target) {
    function find(current, history) {
      if (current === target) {
        return history;
      } else if (current > target) {
        return null;
      } else {
        return find(current + 5, `(${history} + 5)`) ||
               find(current * 3, `(${history} * 3)`);
      }
    }
    return find(1, "1");
  }

  console.log(findSolution(24));
  // → "(((1 * 3) + 5) * 3)"
  ```

  The inner `find` explores both branches recursively and uses `||` to choose the first successful path.

---

**Tóm tắt & Giải thích đơn giản (Tiếng Việt):**

* **Đệ quy** là khi một hàm gọi chính nó. Mỗi lần gọi phải đưa bài toán về trạng thái nhỏ hơn để tiến gần đến điều kiện dừng, tránh vòng lặp vô tận và lỗi tràn ngăn xếp (stack overflow).

* **Ví dụ tính lũy thừa:**

  ```js
  function power(base, exponent) {
    if (exponent === 0) {
      return 1;
    } else {
      return base * power(base, exponent - 1);
    }
  }
  console.log(power(2, 3));  // → 8
  ```

  Mỗi lời gọi nhân thêm `base` và giảm `exponent` đi 1, đến khi `exponent` = 0 thì trả về 1.

* **Ưu & nhược điểm:**

  * Đệ quy thường viết gần giống công thức toán, dễ hiểu.
  * Nhưng mỗi lần gọi hàm tốn tài nguyên ngăn xếp, có thể chậm hơn vòng lặp và gặp lỗi nếu quá sâu.
  * Vòng lặp có thể nhanh và an toàn hơn với các bài toán lặp đơn giản; đệ quy phù hợp với các cấu trúc phân nhánh hoặc chia nhỏ (như cây, đồ thị).

* **Ví dụ tìm đường giải (findSolution):**
  Tìm cách từ số 1 biến thành `target` bằng liên tiếp các phép “+5” hoặc “×3”:

  ```js
  function findSolution(target) {
    function find(current, history) {
      if (current === target) {
        return history;
      } else if (current > target) {
        return null;
      } else {
        return find(current + 5, `(${history} + 5)`) ||
               find(current * 3, `(${history} * 3)`);
      }
    }
    return find(1, "1");
  }

  console.log(findSolution(24));
  // → "(((1 * 3) + 5) * 3)"
  ```

  Hàm `find` thử cả hai nhánh “cộng 5” và “nhân 3” bằng đệ quy; khi một nhánh tìm ra đúng `target`, nó trả về chuỗi lịch sử phép tính, và `||` đảm bảo ta lấy kết quả đầu tiên thành công.

---

**Khi áp dụng đệ quy:**

* Bài toán có thể chia nhỏ thành cùng kiểu bài toán (ví dụ lũy thừa, tìm đường, duyệt cây).
* Bạn muốn code mô tả trực tiếp ý tưởng toán học hoặc thuật toán (clearer).
* Luồng đệ quy đủ nông để không tràn ngăn xếp; nếu quá sâu, bạn có thể chuyển sang vòng lặp hoặc tối ưu tail-call (nếu trình duyệt hỗ trợ).
