**Summary (English):**

* When you treat functions as values and return an inner function that uses a local binding, that inner function “remembers” the binding even after the outer function has finished executing.
* This mechanism is called a **closure**: a function together with the environment in which it was created.
* **Example 1 – Capturing a value:**

  ```js
  function wrapValue(n) {
    let local = n;
    return () => local;
  }

  let wrap1 = wrapValue(1);
  let wrap2 = wrapValue(2);
  console.log(wrap1()); // → 1
  console.log(wrap2()); // → 2
  ```

  Each call to `wrapValue` creates a fresh `local` binding that its returned function closes over.
* **Example 2 – Creating custom multipliers:**

  ```js
  function multiplier(factor) {
    return number => number * factor;
  }

  let twice = multiplier(2);
  console.log(twice(5)); // → 10
  ```

  Here, each returned function retains its own `factor`.
* **Key idea:** a function value carries with it the **lexical environment** where it was defined, not where it’s later called. Closures let you build powerful abstractions by bundling code with its surrounding state.

---

**Tóm tắt (Tiếng Việt):**

* Khi bạn xem hàm như một giá trị và trả về một hàm con sử dụng biến cục bộ, hàm con đó sẽ “ghi nhớ” biến cục bộ ngay cả sau khi hàm ngoài đã kết thúc.
* Cơ chế này gọi là **closure** (đóng): tức hàm kèm theo môi trường (các binding) nơi nó được tạo.
* **Ví dụ 1 – Đóng biến giá trị:**

  ```js
  function wrapValue(n) {
    let local = n;
    return () => local;
  }

  let wrap1 = wrapValue(1);
  let wrap2 = wrapValue(2);
  console.log(wrap1()); // → 1
  console.log(wrap2()); // → 2
  ```

  Mỗi lần gọi `wrapValue` tạo ra một binding `local` riêng mà hàm trả về đóng lại.
* **Ví dụ 2 – Tạo bộ nhân tùy ý:**

  ```js
  function multiplier(factor) {
    return number => number * factor;
  }

  let twice = multiplier(2);
  console.log(twice(5)); // → 10
  ```

  Mỗi hàm trả về sẽ giữ lại tham số `factor` riêng của nó.
* **Ý chính:** giá trị hàm mang theo **môi trường tĩnh** (lexical environment) nơi nó được định nghĩa, không phải môi trường gọi. Closure cho phép bạn xây dựng các trừu tượng mạnh mẽ bằng cách đóng gói mã lẫn trạng thái xung quanh nó.

## Simple explain
Một **closure** túm gọn lại hai thứ:

1. **Mã của hàm** (function code)
    
2. **Các biến xung quanh** (môi trường) tại thời điểm hàm được tạo
    

Nghĩ đơn giản như sau:

> Khi bạn tạo một hàm bên trong hàm khác, hàm con đó mang theo “một túi nhỏ” (đóng gói) tất cả các biến của hàm cha mà nó cần dùng, dù hàm cha đã chạy xong.


- **Closure** = hàm + “túi” (đóng gói) các biến từ môi trường mà nó được sinh ra.
    
- Dù hàm cha đã kết thúc, túi biến vẫn **tồn tại** cho đến khi hàm con không còn được dùng nữa.
    
- Nhờ closure, bạn có thể:
    
    - Giữ lại trạng thái (state) an toàn bên trong hàm.
        
    - Tạo ra các hàm “cấu hình sẵn” (như `multiplier(2)` rồi sinh ra hàm nhân đôi).
        
    - Xây dựng các trừu tượng mạnh mẽ mà không cần biến toàn cục.