**Summary (English):**

* In JavaScript you can call a function with **any number of arguments**—extra ones are simply ignored, and missing ones become `undefined`.
* **Example:**

  ```js
  function square(x) { return x * x; }
  console.log(square(4, true, "hedgehog"));  // → 16
  ```

  Only `x` matters; the other two arguments are dropped.
* This flexibility lets you write functions that behave differently based on how many arguments you pass. For instance, a `minus` function that negates when given one argument and subtracts when given two:

  ```js
  function minus(a, b) {
    if (b === undefined) return -a;
    else return a - b;
  }
  console.log(minus(10));    // → -10
  console.log(minus(10, 5)); // → 5
  ```
* ES2015+ adds **default parameters**, allowing you to set a fallback when an argument is missing (or `undefined`):

  ```js
  function roundTo(n, step = 1) {
    let r = n % step;
    return n - r + (r < step / 2 ? 0 : step);
  }
  console.log(roundTo(4.5));    // → 5   (uses default step = 1)
  console.log(roundTo(4.5, 2)); // → 4
  ```
* Later you’ll learn about the **rest parameters** (`...args`), which let a function capture **all** passed arguments in an array, a technique used by `console.log` itself.

---

**Tóm tắt (Tiếng Việt):**

* Trong JavaScript bạn có thể gọi hàm với **bao nhiêu đối số tùy thích**—các đối số thừa sẽ bị bỏ qua, các đối số thiếu sẽ nhận giá trị `undefined`.
* **Ví dụ:**

  ```js
  function square(x) { return x * x; }
  console.log(square(4, true, "hedgehog"));  // → 16
  ```

  Chỉ `x` được sử dụng; hai đối số còn lại bị loại bỏ.
* Tính linh hoạt này cho phép viết hàm xử lý khác nhau tùy số lượng đối số. Ví dụ hàm `minus` nếu có một đối số thì trả về giá trị đối của nó, nếu có hai thì trừ bình thường:

  ```js
  function minus(a, b) {
    if (b === undefined) return -a;
    else return a - b;
  }
  console.log(minus(10));    // → -10
  console.log(minus(10, 5)); // → 5
  ```
* Từ ES2015, bạn có thể dùng **tham số mặc định** để gán giá trị thay thế khi đối số không cung cấp (hoặc `undefined`):

  ```js
  function roundTo(n, step = 1) {
    let r = n % step;
    return n - r + (r < step / 2 ? 0 : step);
  }
  console.log(roundTo(4.5));    // → 5   (dùng step mặc định = 1)
  console.log(roundTo(4.5, 2)); // → 4
  ```
* Ở chương sau, bạn sẽ học về **rest parameters** (`...args`) để hàm có thể nắm bắt **tất cả** đối số truyền vào dưới dạng mảng—điều mà `console.log` cũng đang sử dụng.
