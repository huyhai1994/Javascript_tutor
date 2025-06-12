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

## Why tentacles ?
Haverbeke deliberately chose “tentacles” to stress that a JavaScript binding doesn’t “own” a value like a little box holding something inside. Instead, it merely reaches out and grabs (“grasps”) a value that lives independently in memory.

* **Shared references:** Multiple bindings can grab the same value—just like several tentacles can all hang onto the same object—whereas a “box” metaphor often implies each variable has its own private copy.
* **Reattachment vs. mutation:** When you reassign a binding, you aren’t changing the value itself (you don’t “open the box and swap its contents”); you’re detaching the tentacle from one value and attaching it to another.
* **Garbage collection:** Values in JavaScript persist only as long as at least one tentacle holds them. When no binding “grasps” a value, it can be reclaimed—just as an untethered object would drift away.

In short, “tentacles” better captures the idea of references (shared, reattachable, and collectible) than “boxes,” which can misleadingly suggest ownership and isolation.

---
Haverbeke đã chủ đích dùng hình ảnh “vòi xúc tu” để nhấn mạnh rằng một binding trong JavaScript không “sở hữu” giá trị như một chiếc hộp khép kín. Thay vào đó, binding chỉ với ra và “bám” lấy một giá trị tồn tại độc lập trong bộ nhớ.

* **Tham chiếu chung:** Nhiều binding có thể cùng “quấn lấy” một giá trị—giống như nhiều vòi xúc tu bám vào cùng một đối tượng—trong khi phép ẩn dụ “hộp” thường ngầm hiểu mỗi biến giữ một bản sao riêng tư.
* **Tách rời và gắn lại:** Khi bạn gán lại binding, bạn không thay đổi giá trị ban đầu (không “mở hộp ra rồi đổi nội dung”); bạn chỉ tách vòi xúc tu khỏi một giá trị và gắn nó vào giá trị khác.
* **Thu gom rác:** Một giá trị trong JavaScript chỉ tồn tại miễn là còn ít nhất một vòi xúc tu bám giữ nó. Khi không còn binding nào “ôm” giá trị đó nữa, nó sẽ được thu hồi—giống như đối tượng trôi đi khi không còn ràng buộc.

Tóm lại, “vòi xúc tu” diễn tả chính xác hơn khái niệm tham chiếu (có thể chia sẻ, tái gắn và thu gom) so với “hộp”, vốn dễ gây hiểu nhầm về quyền sở hữu và sự độc lập.

## Example
Đúng vậy — khi bạn viết

```js
let a = { v: 5 };
let b = a;
```

thì cả hai “vòi xúc tu” `a` và `b` đều quấn vào **cùng** một đối tượng `{ v: 5 }`. Vì thế:

* **Mutate (thay đổi thuộc tính)** qua một trong hai vòi sẽ ảnh hưởng lên đối tượng chung:

  ```js
  b.v = 100;
  console.log(a.v); // → 100
  ```
* **Reassign (gán lại biến)** thì khác hẳn: bạn rút vòi ra khỏi đối tượng cũ và quấn vào một đối tượng khác, mà không đụng chạm đến đối tượng đầu tiên:

  ```js
  b = { v: 200 };  
  console.log(a.v); // → 100  (a vẫn giữ đối tượng cũ)
  ```

### Tóm lại:

1. **Gán tham chiếu** (`let b = a`) → vòi `b` quấn vào cùng đối tượng với vòi `a`.
2. **Đổi thuộc tính** qua `b` hay `a` đều sửa chung một đối tượng.
3. **Gán lại biến** (`b = …`) chỉ thay đổi “đích” của vòi `b`, không làm ảnh hưởng đến vòi `a` hay đối tượng cũ.
