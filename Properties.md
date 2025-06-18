**Summary (English):**

* Almost every JavaScript value (except `null` and `undefined`) has **properties** you can access.
* There are two ways to get or set a property on an object:

  1. **Dot notation** (`value.propName`) — the name after the dot is taken **literally** as the property key.
  2. **Bracket notation** (`value[keyExpr]`) — the expression inside `[]` is **evaluated** to a string, which is then used as the property key.
* Use **dot notation** when you know the property name is a valid identifier (starts with letter or `_`, contains only letters, digits, and `_`).
* Use **bracket notation** when the property name is dynamic, not a valid identifier (e.g. starts with a digit or contains spaces), or stored in a variable:

  ```js
  obj.color          // property "color"
  obj["primary-color"]  // property "primary-color"
  let key = "size";  
  obj[key]           // also property "size"
  ```
* **Arrays** are just objects whose keys are the string versions of non-negative integers (`"0"`, `"1"`, …). Since array indices aren’t valid identifier names, you access elements with bracket notation:

  ```js
  let arr = [2, 3, 5];
  console.log(arr[0]);       // → 2
  console.log(arr["2"]);     // → 5
  ```
* Both strings and arrays have a built-in `.length` property, accessible with dot notation:

  ```js
  "hi".length;   // → 2
  arr.length;    // → 3
  ```
* Trying to read a property from `null` or `undefined` throws a `TypeError`.

---

**Tóm tắt (Tiếng Việt):**

* Gần như mọi giá trị trong JavaScript (ngoại trừ `null` và `undefined`) đều có **thuộc tính** (properties).
* Có hai cách để truy cập hoặc gán thuộc tính:

  1. **Cú pháp chấm** (`value.propName`) — từ khóa sau dấu chấm được hiểu **nguyên xi** là tên thuộc tính.
  2. **Cú pháp ngoặc vuông** (`value[keyExpr]`) — biểu thức trong `[]` được **tính toán** thành một chuỗi, rồi dùng làm tên thuộc tính.
* Dùng **chấm** khi tên thuộc tính là một **identifier hợp lệ** (bắt đầu bằng chữ cái hoặc `_`, chỉ gồm chữ cái, chữ số và `_`).
* Dùng **ngoặc vuông** khi:

  * Tên thuộc tính không phải là identifier hợp lệ (ví dụ bắt đầu bằng số, có dấu cách).
  * Bạn muốn truy cập tên thuộc tính nằm trong biến:

    ```js
    obj.color            // thuộc tính "color"
    obj["primary-color"] // thuộc tính "primary-color"
    let key = "size";
    obj[key]             // cũng truy cập thuộc tính "size"
    ```
* **Mảng** thực chất là đối tượng có các key là chuỗi các số (“0”, “1”, …). Vì vậy, bạn phải dùng ngoặc vuông để lấy phần tử qua chỉ số:

  ```js
  let arr = [2, 3, 5];
  console.log(arr[0]);      // → 2
  console.log(arr["2"]);    // → 5
  ```
* Cả chuỗi và mảng đều có thuộc tính `.length`, có thể lấy bằng cú pháp chấm:

  ```js
  "hi".length;   // → 2
  arr.length;    // → 3
  ```
* Cố gắng đọc thuộc tính trên `null` hoặc `undefined` sẽ ném ra lỗi `TypeError`.
