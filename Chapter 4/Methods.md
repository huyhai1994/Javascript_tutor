**Summary (English):**

* Both **strings** and **arrays** have **methods**, which are properties holding function values.
* **String methods** (examples):

  * `toUpperCase()` returns a new string with all letters converted to uppercase.
  * `toLowerCase()` similarly returns a lowercase version.
* Even when you call a string’s method without arguments, the method has access to the string it belongs to (`this`), so it knows which value to transform.
* **Array methods** (stack-style examples):

  * `push(value)` adds `value` to the **end** of the array.
  * `pop()` removes the **last** element from the array and returns it.
* The names “push” and “pop” come from the **stack** data-structure terminology, where you push items on top and pop them off in reverse order (LIFO).

---

**Tóm tắt (Tiếng Việt):**

* Cả **chuỗi** và **mảng** đều có **phương thức** (method), tức các property chứa giá trị hàm.
* **Phương thức chuỗi** (ví dụ):

  * `toUpperCase()` trả về chuỗi mới với toàn bộ ký tự viết hoa.
  * `toLowerCase()` tương tự nhưng viết thường.
* Dù gọi mà không truyền đối số, phương thức chuỗi vẫn “biết” được chuỗi gốc nhờ cơ chế `this`.
* **Phương thức mảng** (ví dụ theo kiểu ngăn xếp – stack):

  * `push(value)` thêm `value` vào **cuối** mảng.
  * `pop()` xoá và trả về phần tử **cuối cùng** của mảng.
* Tên “push” và “pop” bắt nguồn từ cấu trúc dữ liệu **ngăn xếp**, nơi bạn đẩy (push) phần tử lên trên cùng và lấy (pop) phần tử ra theo thứ tự ngược lại (LIFO).
