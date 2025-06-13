**Summary (English):**

* A **function definition** binds a name to a function value.

  ```js
  const square = function(x) {
    return x * x;
  };
  console.log(square(12)); // → 144
  ```
* The `function` keyword starts the definition; the **parameters** (e.g. `x`) and the **body** (in `{ … }`) are required, even if there’s only one statement.
* Functions can have **zero**, **one**, or **multiple parameters**:

  ```js
  const makeNoise = function() {
    console.log("Pling!");
  };
  makeNoise(); // → Pling!

  const roundTo = function(n, step) {
    let rem = n % step;
    return n - rem + (rem < step/2 ? 0 : step);
  };
  console.log(roundTo(23, 10)); // → 20
  ```
* Some functions **return** a value (using `return`), others only cause **side effects** and return `undefined` by default.
* Parameter names act like local bindings whose values are supplied by the **caller** when the function is invoked.

---

**Tóm tắt (Tiếng Việt):**

* Một **định nghĩa hàm** gán tên cho một giá trị hàm.

  ```js
  const square = function(x) {
    return x * x;
  };
  console.log(square(12)); // → 144
  ```
* Từ khóa `function` khởi đầu định nghĩa; **tham số** (ví dụ `x`) và **thân hàm** (trong `{ … }`) luôn bắt buộc, dù chỉ có một câu lệnh.
* Hàm có thể không có tham số, hoặc có một, hoặc nhiều tham số:

  ```js
  const makeNoise = function() {
    console.log("Pling!");
  };
  makeNoise(); // → Pling!

  const roundTo = function(n, step) {
    let rem = n % step;
    return n - rem + (rem < step/2 ? 0 : step);
  };
  console.log(roundTo(23, 10)); // → 20
  ```
* Một số hàm **trả về** giá trị (dùng `return`), số khác chỉ tạo **tác dụng phụ** và ngầm trả về `undefined`.
* Tên tham số hoạt động như biến cục bộ, được gán giá trị bởi **người gọi** hàm khi thực thi.
