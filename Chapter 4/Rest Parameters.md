**Rest Parameters (English Summary):**

* By putting **`...`** before the last function parameter, you turn it into a **rest parameter**, which collects *all remaining* arguments into a real JavaScript array.
* Example—reimplementing `Math.max`:

  ```js
  function max(...numbers) {
    let result = -Infinity;
    for (let n of numbers) {
      if (n > result) result = n;
    }
    return result;
  }

  console.log(max(4, 1, 9, -2)); // → 9
  ```

  Here, calling `max(4,1,9,-2)` binds `numbers` to `[4,1,9,-2]`.
* You can also mix fixed parameters before the rest:

  ```js
  function joinWithDash(separator, ...words) { /* … */ }
  ```
* The **spread syntax** uses the same `...` notation at call‐sites or in literals to **expand** an array (or object) into individual elements (or properties):

  ```js
  let nums = [5, 1, 7];
  console.log(max(...nums));       // → 7
  console.log(max(9, ...nums, 2)); // → 9

  console.log(["will", ...["never","fully"], "understand"]);
  // → ["will","never","fully","understand"]

  let coords = { x: 10, y: 0 };
  console.log({ ...coords, z: 10 });
  // → { x:10, y:0, z:10 }
  ```

---

**Tham số còn lại & cú pháp trải (Tiếng Việt):**

* Đặt **`...`** trước tham số cuối cùng trong khai báo hàm sẽ biến nó thành **rest parameter**, tự động gom *tất cả* đối số còn lại thành một mảng JavaScript.
* Ví dụ—tái tạo `Math.max`:

  ```js
  function max(...numbers) {
    let result = -Infinity;
    for (let n of numbers) {
      if (n > result) result = n;
    }
    return result;
  }

  console.log(max(4, 1, 9, -2)); // → 9
  ```

  Gọi `max(4,1,9,-2)` sẽ gán `numbers = [4,1,9,-2]`.
* Bạn có thể kết hợp **tham số cố định** trước rest parameter:

  ```js
  function greet(greeting, ...names) { /* … */ }
  ```
* **Spread syntax** cũng dùng `...` nhưng ở chỗ *gọi hàm* hoặc *tạo literal*, để **mở rộng** (expand) mảng hoặc object thành các phần tử (hoặc thuộc tính) riêng biệt:

  ```js
  let nums = [5, 1, 7];
  console.log(max(...nums));       // → 7
  console.log(max(9, ...nums, 2)); // → 9

  console.log(["will", ...["never","fully"], "understand"]);
  // → ["will","never","fully","understand"]

  let coords = { x: 10, y: 0 };
  console.log({ ...coords, z: 10 });
  // → { x:10, y:0, z:10 }
  ```
