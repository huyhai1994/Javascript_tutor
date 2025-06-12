**Summary (English):**

* JavaScript provides **compound assignment operators** to update a binding relative to its current value.
* Instead of writing

  ```js
  counter = counter + 1;
  ```

  you can write

  ```js
  counter += 1;
  ```
* There are similar shortcuts for other operations:

  ```js
  counter -= 1;  // subtraction
  counter *= 2;  // multiplication
  counter /= 2;  // division
  ```
* For the common “add or subtract 1” case, there are even **increment** and **decrement** operators:

  ```js
  counter++;    // equivalent to counter += 1
  counter--;    // equivalent to counter -= 1
  ```
* These concise forms make loops and arithmetic expressions shorter, for example:

  ```js
  for (let number = 0; number <= 12; number += 2) {
    console.log(number);
  }
  ```

---

**Tóm tắt (Tiếng Việt):**

* JavaScript cung cấp các **toán tử gán kết hợp** (compound assignment) để cập nhật biến dựa trên giá trị hiện tại.
* Thay vì viết

  ```js
  counter = counter + 1;
  ```

  bạn có thể viết

  ```js
  counter += 1;
  ```
* Tương tự với các phép toán khác:

  ```js
  counter -= 1;  // trừ
  counter *= 2;  // nhân
  counter /= 2;  // chia
  ```
* Với trường hợp cộng hoặc trừ 1, có toán tử **tăng/giảm**:

  ```js
  counter++;    // tương đương counter += 1
  counter--;    // tương đương counter -= 1
  ```
* Các cú pháp ngắn gọn này giúp viết vòng lặp và biểu thức số học gọn hơn, ví dụ:

  ```js
  for (let number = 0; number <= 12; number += 2) {
    console.log(number);
  }
  ```
