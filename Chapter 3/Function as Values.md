**Summary (English):**

* In JavaScript, **functions are just values**, not special entities tied permanently to their names.
* A function binding (the name you give a function) is itself a normal variable—it can appear in any expression, be passed as an argument, stored in another binding, or even reassigned.
* This flexibility means you can conditionally swap out behavior by assigning a different function to the same name:

  ```js
  let launchMissiles = function() {
    missileSystem.launch("now");
  };
  if (safeMode) {
    // In “safe mode,” replace it with a no-op
    launchMissiles = function() { /* do nothing */ };
  }
  ```
* Treating functions as values unlocks powerful patterns—later chapters explore passing functions around to build abstractions.

---

**Tóm tắt (Tiếng Việt):**

* Trong JavaScript, **hàm cũng là một giá trị** như bất kỳ giá trị nào khác, không phải thứ gì gắn liền vĩnh viễn với tên gọi của nó.
* Khi bạn gán hàm cho một biến (binding), biến đó chỉ là một biến bình thường—bạn có thể đưa vào bất cứ biểu thức nào, truyền làm đối số, lưu vào biến khác, hoặc thậm chí gán lại hàm mới cho nó.
* Nhờ vậy, bạn có thể thay đổi hành vi chương trình bằng cách gán hàm khác khi cần:

  ```js
  let launchMissiles = function() {
    missileSystem.launch("now");
  };
  if (safeMode) {
    // Ở chế độ “an toàn,” thay hàm bằng một hàm không làm gì
    launchMissiles = function() { /* không làm gì */ };
  }
  ```
* Việc xem hàm như giá trị mở đường cho nhiều mô hình lập trình linh hoạt—các chương sau sẽ hướng dẫn cách truyền hàm vào hàm để xây dựng các trừu tượng mạnh mẽ.
