## Knuth quote

That Knuth quote—“many people doing things that build on each other, like a wall of mini stones”—is a great lens for how **functions** work in JavaScript:
That Knuth quote—“many people doing things that build on each other, like a wall of mini stones”—is a great lens for how **functions** work in JavaScript:

1. **Functions as “mini stones”**
   Each function you write is a small, self‐contained piece of logic:

   ```js
   function add(a, b) {
     return a + b;
   }
   function double(x) {
     return x * 2;
   }
   ```

   By themselves they’re tiny—but you can stack and compose them to do more complex things.

2. **Composition = building walls**
   Just like stones in a wall, you put functions together:

   ```js
   function addAndDouble(a, b) {
     // reuse our two “mini stones”
     return double(add(a, b));
   }

   console.log(addAndDouble(2, 3)); // 10
   ```

   Here `addAndDouble` builds on the smaller `add` and `double` pieces.

3. **Community & libraries**
   JavaScript’s ecosystem (Node, React, Lodash, etc.) is literally thousands of functions written by many people—each one a “stone” you can pick up and reuse.

4. **Abstraction layers**
   As you learn about default parameters, closures, callbacks and promises, you’re stacking new “stones” on top of the old ones—gradually raising the wall (your app’s functionality) higher.

---

### Key takeaways in the “Functions” chapter

* **Declaration vs. Expression**: Two ways to define your stones.
* **Parameters & return values**: How each stone accepts inputs and hands back outputs.
* **Scope & closures**: Where your stones “live” and how they keep references to one another.
* **Higher-order functions**: Functions that accept or return other functions—think of them as mortar that binds your stones together.

So when you’re studying JS functions, remember: you’re not reinventing genius algorithms every time—you’re mastering how to craft and assemble a collection of simple, reusable “mini stones” into a sturdy wall of code.


---
JavaScript functions let you package code into named, reusable units. They help you:

* Structure large programs and isolate parts from each other
* Reduce repetition by encapsulating common logic
* Create new “vocabulary” (function names) to express intent clearly
* Extend the language’s limited built-in commands so your code stays concise and flexible

---

Hàm trong JavaScript cho phép bạn đóng gói mã thành những khối có tên, có thể tái sử dụng. Chúng giúp bạn:

* Cấu trúc chương trình lớn và cô lập các phần với nhau
* Giảm lặp lại bằng cách gói logic chung vào hàm
* Tạo “từ vựng” mới (tên hàm) để diễn đạt ý đồ rõ ràng
* Mở rộng số lệnh tích hợp sẵn của ngôn ngữ, giữ cho mã ngắn gọn và linh hoạt

## 1. [[Defining A Function]]

## 2. [[Bindings and Scopes]]

## 3. [[Nested Scope]]

## 4.  [[Function as Values]]

## 5. [[Declaration Notation]]

## 6. [[Arrow Function]]

## 7. [[Call Stack]]
