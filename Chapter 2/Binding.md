**Summary (English):**
A **binding** (commonly called a “variable”) is JavaScript’s way of giving a name to a value so the program can store and later retrieve it.

* You create a binding with the `let` keyword:

  ```js
  let caught = 5 * 5;
  ```

  This defines a binding named `caught` holding the value `25`.

* Once defined, you can use the binding name as an expression (its value is whatever it currently holds):

  ```js
  let ten = 10;
  console.log(ten * ten);  // → 100
  ```

* Bindings are like **tentacles** rather than boxes—they “grasp” values but don’t own them. You can reassign a binding at any time:

  ```js
  let mood = "light";
  console.log(mood);  // → "light"
  mood = "dark";
  console.log(mood);  // → "dark"
  ```

* If you declare a binding without initializing it, it starts out as `undefined`:

  ```js
  let something;
  console.log(something);  // → undefined
  ```

* You can define **multiple** bindings in one statement, separated by commas:

  ```js
  let one = 1, two = 2;
  console.log(one + two);  // → 3
  ```

* Besides `let`, JavaScript also offers `var` (the old, function-scoped way to declare variables) and `const` (for bindings that cannot be reassigned). In modern code, prefer `let` and `const`—use `const` by default, and `let` when you know you’ll need to reassign.

---

**Tóm tắt (Tiếng Việt):**
**Binding** (thường gọi là “biến”) là cách JavaScript gán tên cho một giá trị để chương trình có thể lưu và truy xuất sau này.

* Dùng từ khóa `let` để tạo binding:

  ```js
  let caught = 5 * 5;
  ```

  Đoạn này định nghĩa binding tên là `caught` giữ giá trị `25`.

* Sau khi định nghĩa, bạn dùng tên binding như một biểu thức (giá trị của nó là giá trị hiện tại):

  ```js
  let ten = 10;
  console.log(ten * ten);  // → 100
  ```

* Bindings hoạt động giống **vòi xúc tu** hơn là hộp—chúng “bám lấy” giá trị nhưng không sở hữu. Bạn có thể gán lại binding bất cứ lúc nào:

  ```js
  let mood = "light";
  console.log(mood);  // → "light"
  mood = "dark";
  console.log(mood);  // → "dark"
  ```

* Khi khai báo binding mà không khởi tạo, nó có giá trị `undefined`:

  ```js
  let something;
  console.log(something);  // → undefined
  ```

* Có thể khai báo **nhiều** binding trong một câu lệnh, ngăn cách bằng dấu phẩy:

  ```js
  let one = 1, two = 2;
  console.log(one + two);  // → 3
  ```

* Bên cạnh `let`, còn có `var` (cách cũ, phạm vi function) và `const` (binding không cho phép gán lại). Trong code hiện đại, nên ưu tiên `const` cho biến không đổi và `let` cho biến cần gán lại.
