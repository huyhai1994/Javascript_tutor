## Theory
**Summary (English):**

* Every variable (binding) lives in a **scope**, the region of code where it can be accessed.
* **Global scope:** Bindings defined outside any function or block—visible everywhere.
* **Function scope:** Parameters and bindings declared inside a function—each call gets its own fresh set.
* **Block scope (ES2015+):** `let` and `const` bindings exist only inside the `{…}` block where they’re declared.
* **`var` bindings** (pre-2015) ignore block boundaries and are hoisted to the enclosing **function** (or global) scope.
* **Shadowing:** If a binding in an inner scope has the same name as one outside, references resolve to the innermost binding.
* **Examples:**

  ```js
  let x = 10;      // global
  if (true) {
    let y = 20;    // visible only inside this block
    var z = 30;    // function/global scope, not block-scoped
  }
  console.log(x);  // → 10
  // console.log(y); // ReferenceError: y is not defined
  console.log(z);  // → 30

  const halve = function(n) {
    return n / 2;  // here n refers to the function’s own parameter
  };

  let n = 10;
  console.log(halve(100)); // → 50
  console.log(n);          // → 10  (global n is untouched)
  ```

---

**Tóm tắt (Tiếng Việt):**

* Mỗi biến (binding) tồn tại trong một **phạm vi** (scope), tức vùng mã nơi biến đó có thể được truy cập.
* **Phạm vi toàn cục (global):** Biến khai báo bên ngoài mọi hàm hoặc khối—có thể dùng ở bất cứ đâu.
* **Phạm vi hàm (function):** Tham số và biến khai báo bên trong một hàm—mỗi lần gọi hàm tạo ra một bộ biến mới.
* **Phạm vi khối (block, ES2015+):** Biến khai báo bằng `let` hoặc `const` chỉ tồn tại trong khối `{…}` chứa chúng.
* Biến khai báo bằng **`var`** (trước ES2015) không quan tâm tới khối, mà được “nâng” (hoisted) lên phạm vi hàm chứa nó (hoặc global nếu không trong hàm).
* Phạm vi bên trong có thể “nhìn ra” và dùng biến ở phạm vi ngoài, nhưng phạm vi ngoài **không nhìn thấy** biến khai báo trong khối hoặc hàm con.
* **Che khuất (shadowing):** Khi có biến cùng tên ở phạm vi trong, các tham chiếu sẽ dùng biến ở phạm vi gần nhất.
* **Ví dụ:**

  ```js
  let x = 10;      // global
  if (true) {
    let y = 20;    // chỉ có trong khối này
    var z = 30;    // được hoisted lên phạm vi hàm hoặc global
  }
  console.log(x);  // → 10
  // console.log(y); // ReferenceError: y is not defined
  console.log(z);  // → 30

  const halve = function(n) {
    return n / 2;  // n là tham số cục bộ của hàm
  };

  let n = 10;
  console.log(halve(100)); // → 50
  console.log(n);          // → 10  (n toàn cục không bị thay đổi)
  ```

## Inner Scopes "look out"
It’s just the rule of **lexical (static) scope** in JavaScript. In plain English:

- **Inner scopes “look out”**: Any code inside a function or block can freely use variables defined **in its outer environment** (the surrounding function or the global scope).
    
- **Outer scopes can’t see in**: Code that lives in that outer environment does **not** know about variables you declared down inside the inner block or function—they’re invisible there.
    

---

### Example

```js
let greeting = "Hello";   // (1) global binding

function sayHello() {
  // This function body is an “inner scope” relative to the global scope.

  console.log(greeting);  // ✅ Can “look out” and read `greeting`
  
  let name = "Alice";     // (2) local binding, exists only inside sayHello
  console.log("Name is", name);
}

sayHello();

console.log(greeting);    // ✅ Still works
// console.log(name);     // ❌ ReferenceError: name is not defined
```

1. `sayHello` can read `greeting` because it’s defined in an outer (global) scope.
    
2. But the global code **cannot** access `name`, because `name` only exists inside the `sayHello` function. Outside of it, that binding doesn’t even exist.
    

That’s what “inner can see outer, outer can’t see inner” means.