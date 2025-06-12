**Summary (English):**

* **Loops** allow you to run a block of code repeatedly instead of copying and pasting.
* The **`while` loop** repeatedly executes its body as long as a Boolean condition remains true:

  ```js
  let number = 0;
  while (number <= 12) {
    console.log(number);
    number += 2;
  }
  // Outputs: 0, 2, 4, …, 12
  ```
* You can use multiple bindings to track progress inside a loop. For example, to add 1, 2, 3, …, up to 100 and sum them:

  ```js
  let result = 0;
  let counter = 1;
  while (counter <= 100) {
    result += counter;
    counter++;
  }
  console.log(result);  // → 5050
  ```
* The **`do…while` loop** executes its body **at least once**, then repeats as long as its condition is true:

  ```js
  let yourName;
  do {
    yourName = prompt("Who are you?");
  } while (!yourName);
  console.log("Hello " + yourName);
  ```

  This forces the prompt to appear until the user provides a nonempty name.

---

**Tóm tắt (Tiếng Việt):**

* **Vòng lặp** cho phép chạy lặp lại một khối mã thay vì sao chép dán nhiều lần.
* **`while` loop** thực thi thân vòng lặp miễn là biểu thức điều kiện còn đúng:

  ```js
  let number = 0;
  while (number <= 12) {
    console.log(number);
    number += 2;
  }
  // In ra: 0, 2, 4, …, 12
  ```
* Có thể dùng nhiều biến (binding) để theo dõi tiến trình bên trong vòng lặp. Ví dụ, tính tổng 1 + 2 + … + 100:

  ```js
  let result = 0;
  let counter = 1;
  while (counter <= 100) {
    result += counter;
    counter++;
  }
  console.log(result);  // → 5050
  ```
* **`do…while` loop** luôn thực thi thân vòng lặp ít nhất một lần, sau đó lặp lại nếu điều kiện còn đúng:

  ```js
  let yourName;
  do {
    yourName = prompt("Who are you?");
  } while (!yourName);
  console.log("Hello " + yourName);
  ```

  Vòng lặp này sẽ hiện hộp thoại hỏi tên cho đến khi người dùng nhập một chuỗi không rỗng.
