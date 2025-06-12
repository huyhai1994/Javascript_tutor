**Summary (English):**

* **Logical operators** in JavaScript work on Boolean values:

  * **`&&` (AND):** Returns `true` only if **both** operands are truthy.

    ```js
    true && false  // → false
    true && true   // → true
    ```
  * **`||` (OR):** Returns `true` if **either** operand is truthy.

    ```js
    false || true  // → true
    false || false // → false
    ```
  * **`!` (NOT):** Unary operator that flips a Boolean:

    ```js
    !true  // → false
    !false // → true
    ```
* **Operator precedence:**

  1. Parentheses `(…)`
  2. Logical NOT `!`
  3. Logical AND `&&`
  4. Comparison (`>`, `==`, etc.)
  5. Logical OR `||`
* **Ternary (conditional) operator `?:`:** A three-operand operator that picks one of two values based on a condition:

  ```js
  condition ? valueIfTrue : valueIfFalse
  ```

  Examples:

  ```js
  1 + 1 == 2 && 10 * 10 > 50   // evaluates to true
  console.log(true ? 1 : 2);   // → 1
  console.log(false ? 1 : 2);  // → 2
  ```

---

**Tóm tắt (Tiếng Việt):**

* **Toán tử luận lý** trong JavaScript hoạt động trên giá trị Boolean:

  * **`&&` (VÀ):** Trả về `true` chỉ khi **cả hai** toán hạng đều đúng (truthy).

    ```js
    true && false  // → false
    true && true   // → true
    ```
  * **`||` (HOẶC):** Trả về `true` nếu **ít nhất một** toán hạng đúng.

    ```js
    false || true  // → true
    false || false // → false
    ```
  * **`!` (PHỦ ĐỊNH):** Toán tử đơn ngôi đảo ngược giá trị Boolean:

    ```js
    !true  // → false
    !false // → true
    ```
* **Độ ưu tiên toán tử:**

  1. Ngoặc `(…)`
  2. Phủ định `!`
  3. VÀ `&&`
  4. So sánh (`>`, `==`, v.v.)
  5. HOẶC `||`
* **Toán tử ba ngôi (ternary) `?:`:** Thực hiện lựa chọn giữa hai giá trị dựa trên điều kiện:

  ```js
  điều_kiện ? giá_trị_khi_đúng : giá_trị_khi_sai
  ```

  Ví dụ:

  ```js
  1 + 1 == 2 && 10 * 10 > 50   // cho kết quả true
  console.log(true ? 1 : 2);   // → 1
  console.log(false ? 1 : 2);  // → 2
  ```
