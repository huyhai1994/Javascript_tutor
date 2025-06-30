**Summary (English):**

* Strings in JavaScript are **immutable** primitives, but the language **wraps** them in temporary String objects so you can access built-in **properties** and **methods**.
* You can read `.length` and call methods like:

  * **`slice(start[, end])`** – returns a substring.

    ```js
    "coconuts".slice(4,7);   // → "nut"
    ```
  * **`indexOf(substr[, pos])`** – finds the first occurrence of `substr`.

    ```js
    "one two three".indexOf("ee"); // → 11
    ```
  * **`trim()`** – removes whitespace at both ends.

    ```js
    "  okay \n".trim();      // → "okay"
    ```
  * **`padStart(targetLength, padString)`** – pads the start to reach a given length.

    ```js
    String(6).padStart(3, "0"); // → "006"
    ```
  * **`split(sep)`** and **`join(sep)`** – split into an array and join back:

    ```js
    "a b c".split(" ");     // → ["a","b","c"]
    ["a","b","c"].join("-"); // → "a-b-c"
    ```
  * **`repeat(count)`** – repeats the string `count` times.

    ```js
    "LA".repeat(3);         // → "LALALA"
    ```
* You **cannot** add your own properties to a string primitive—attempting `someString.age = 88` has no effect.

---

**Tóm tắt (Tiếng Việt):**

* Chuỗi (string) trong JavaScript là giá trị **bất biến** (immutable), nhưng khi bạn truy cập thuộc tính hoặc gọi phương thức, ngôn ngữ tự tạo tạm thời một đối tượng String để thực thi rồi vứt đi.
* Bạn có thể đọc `.length` và dùng các phương thức như:

  * **`slice(start[, end])`** – trích lấy đoạn con của chuỗi.

    ```js
    "coconuts".slice(4,7);   // → "nut"
    ```
  * **`indexOf(substr[, pos])`** – tìm vị trí xuất hiện đầu tiên của `substr`.

    ```js
    "one two three".indexOf("ee"); // → 11
    ```
  * **`trim()`** – loại bỏ khoảng trắng ở đầu và cuối chuỗi.

    ```js
    "  okay \n".trim();      // → "okay"
    ```
  * **`padStart(targetLength, padString)`** – chèn ký tự vào đầu chuỗi cho đủ độ dài.

    ```js
    String(6).padStart(3, "0"); // → "006"
    ```
  * **`split(sep)`** và **`join(sep)`** – tách chuỗi thành mảng và nối mảng thành chuỗi.

    ```js
    "a b c".split(" ");     // → ["a","b","c"]
    ["a","b","c"].join("-"); // → "a-b-c"
    ```
  * **`repeat(count)`** – lặp lại chuỗi `count` lần.

    ```js
    "LA".repeat(3);         // → "LALALA"
    ```
* Bạn **không thể** thêm thuộc tính tùy ý lên chuỗi nguyên thủy—việc `someString.age = 88` sẽ không tạo ra bất kỳ thay đổi nào.
