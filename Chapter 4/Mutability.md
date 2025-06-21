**Summary (English):**

* Primitive values—numbers, strings, and booleans—are **immutable**: once you’ve created a string (say `"cat"`), you cannot change any of its characters. Any operation that looks like it modifies a primitive actually produces a **new** value.
* **Objects**, by contrast, are **mutable**: you can change their properties at any time. An object lives independently, and any “tentacle” (binding) that grasps it will see those mutations.
* **Identity vs. content:**

  ```js
  let object1 = {value: 10};
  let object2 = object1;
  let object3 = {value: 10};

  console.log(object1 == object2); // → true   (same octopus)
  console.log(object1 == object3); // → false  (two separate octopuses)

  object1.value = 15;
  console.log(object2.value);      // → 15   (tentacle 2 sees the change)
  console.log(object3.value);      // → 10   (tentacle 3 grasps a different object)
  ```
* **`const` bindings** only fix which octopus a tentacle holds; they do **not** freeze the octopus’s contents. You can mutate properties of a `const` object, but you cannot reassign the binding itself:

  ```js
  const score = { visitors: 0, home: 0 };
  score.visitors = 1;  // ✅ mutate the octopus
  score = { visitors: 1, home: 0 }; // ❌ error—cannot reattach a const tentacle
  ```
* **Equality operators** (`==` or `===`) compare object identity, not deep structural equality. Two distinct objects with identical contents are still unequal. JavaScript has no built-in “deep equals,” though you can write one yourself.

---

**Tóm tắt (Tiếng Việt):**

* Các giá trị nguyên thủy—số, chuỗi, boolean—là **bất biến** (immutable): sau khi tạo (ví dụ `"cat"`), bạn không thể thay đổi nội dung của nó; mọi “thao tác” sẽ sinh ra **giá trị mới** chứ không sửa đổi giá trị cũ.
* **Đối tượng** thì **thay đổi được** (mutable): bạn có thể sửa, thêm, hoặc xoá thuộc tính bất cứ lúc nào. Mỗi đối tượng giống như một con bạch tuộc; bất kỳ xúc tu (binding) nào đang quấn vào nó sẽ nhìn thấy mọi biến đổi.
* **Nhận dạng so với nội dung:**

  ```js
  let object1 = {value: 10};
  let object2 = object1;
  let object3 = {value: 10};

  console.log(object1 == object2); // → true   (hai xúc tu cùng quấn chung một bạch tuộc)
  console.log(object1 == object3); // → false  (hai bạch tuộc khác nhau)

  object1.value = 15;
  console.log(object2.value);      // → 15   (xúc tu 2 thấy được thay đổi)
  console.log(object3.value);      // → 10   (xúc tu 3 vẫn quấn con bạch tuộc cũ)
  ```
* **Binding `const`** chỉ cố định xúc tu quấn vào con bạch tuộc nào, **không** đóng băng nội dung con bạch tuộc đó. Bạn vẫn có thể thay đổi thuộc tính của một object được gán cho `const`, nhưng không thể gán lại binding:

  ```js
  const score = { visitors: 0, home: 0 };
  score.visitors = 1;  // ✅ mutating—đổi nội dung bạch tuộc
  score = { visitors: 1, home: 0 }; // ❌ lỗi—không thể reattach const tentacle
  ```
* Toán tử **so sánh** (`==` hoặc `===`) so sánh **nhận dạng** (identity) của đối tượng, không so sánh sâu về nội dung. Hai object khác nhau, dù có cùng nội dung, vẫn **không** bằng nhau về identity. JavaScript không có hàm so sánh sâu tích hợp sẵn—nếu cần, bạn phải tự triển khai.
