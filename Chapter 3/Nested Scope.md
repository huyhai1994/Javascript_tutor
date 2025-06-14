**Summary (English):**
JavaScript supports **nested scopes**, meaning you can define blocks or functions inside other blocks/functions, creating multiple levels of visibility:

1. **Outer scope:** For example, a function `hummus(factor)` defines a binding `factor`.
2. **Inner scope:** Inside it, you define another function `ingredient(amount, unit, name)`. That inner function can **see** and use `factor` from its outer scope.
3. **Local bindings:** Variables declared inside `ingredient`—like `amount`, `unit`, and `ingredientAmount`—are **not visible** outside of `ingredient`.
4. **Lexical scoping:** Each scope has access to its own bindings and all bindings in the scopes that **lexically** contain it, up to the global scope. Outer scopes cannot see bindings declared in inner scopes.

---

**Tóm tắt (Tiếng Việt):**
JavaScript cho phép **lồng phạm vi** (nested scopes), tức bạn có thể định nghĩa khối hoặc hàm bên trong khối/hàm khác, tạo ra nhiều cấp độ phạm vi:

1. **Phạm vi ngoài:** Ví dụ hàm `hummus(factor)` khai báo biến `factor`.
2. **Phạm vi trong:** Bên trong đó, ta định nghĩa hàm `ingredient(amount, unit, name)`. Hàm này có thể **nhìn thấy** và sử dụng `factor` từ phạm vi ngoài.
3. **Biến cục bộ:** Các biến khai báo trong `ingredient`—như `amount`, `unit`, `ingredientAmount`—**không thể** truy cập ra bên ngoài hàm `ingredient`.
4. **Phạm vi tĩnh (lexical scoping):** Mỗi phạm vi có thể dùng biến của chính nó và biến trong phạm vi bao quanh (từ nội đến ngoại), nhưng phạm vi ngoài không thể thấy biến khai báo trong phạm vi con.

## Example
**Bài toán minh hoạ “nested scope” (phạm vi lồng nhau) trong JavaScript**

> Viết một hàm `makeCounter(start)` tạo bộ đếm khởi đầu từ `start`. Hàm này trả về một **hàm con** (inner function) khi gọi sẽ tăng biến đếm lên 1 và trả về giá trị mới.

```js
function makeCounter(start) {
  // Đây là PHẠM VI NGOÀI (outer scope) của inner function
  let count = start;

  // Hàm getNext có PHẠM VI NỘI (inner scope), nó "nhìn thấy" biến count
  function getNext() {
    count = count + 1;   // inner scope dùng biến ở outer scope
    return count;
  }

  return getNext;        // trả về hàm con
}

// Tạo một bộ đếm bắt đầu từ 10
const counter = makeCounter(10);

console.log(counter()); // → 11
console.log(counter()); // → 12
console.log(counter()); // → 13
```

### Giải thích

1. Khi gọi `makeCounter(10)`, ta tạo ra:

   * **Outer scope** của `makeCounter` có binding `count = 10`.
   * **Inner scope** của `getNext` nằm bên trong, nên nó **nhìn thấy** `(lexical scope)` biến `count`.

2. Mỗi khi `counter()` (chính là `getNext`) được gọi:

   * Nó tăng `count` rồi trả về kết quả.
   * `count` được giữ lại giữa các lần gọi nhờ closure – giá trị không bị “dội” hay mất đi.

3. Phạm vi **ngoài** (nơi ta gọi `counter()`) **không thể** truy cập trực tiếp biến `count` hay nội dung của `getNext`:

   ```js
   console.log(count);    // ❌ ReferenceError: count is not defined
   console.log(getNext);  // ❌ ReferenceError: getNext is not defined
   ```

   Chỉ có code bên trong `makeCounter` mới “thấy” được `count` và `getNext`.

---

**Tóm lại**, đây là ví dụ kinh điển về **nested scope** và **closure**:

* Inner function có thể sử dụng biến của outer scope.
* Outer scope không thể truy cập biến cục bộ của inner.
* Những binding “lồng nhau” theo cấu trúc tĩnh của mã (lexical scoping).
