**Summary (English):**
To work with an ordered collection of values in JavaScript, you use an **array**, written with square brackets and commas, for example:

```js
let listOfNumbers = [2, 3, 5, 7, 11];
```

* **Accessing elements:** Use `array[index]`, where indexing starts at **0**:

  ```js
  console.log(listOfNumbers[0]);            // → 2
  console.log(listOfNumbers[2]);            // → 5
  ```
* **Last element:** Since `length` gives the number of elements, the last index is `length − 1`:

  ```js
  console.log(listOfNumbers[listOfNumbers.length - 1]);  // → 11
  ```

Arrays give a clear, efficient way to store and retrieve sequences of values, unlike juggling custom string formats.

---

**Tóm tắt (Tiếng Việt):**
Để làm việc với một tập hợp có thứ tự trong JavaScript, ta dùng **mảng** (array), viết giữa dấu ngoặc vuông và phân tách bằng dấu phẩy, ví dụ:

```js
let listOfNumbers = [2, 3, 5, 7, 11];
```

* **Truy cập phần tử:** Dùng `array[index]`, bắt đầu từ **0**:

  ```js
  console.log(listOfNumbers[0]);            // → 2
  console.log(listOfNumbers[2]);            // → 5
  ```
* **Phần tử cuối cùng:** Vì `.length` cho biết số phần tử, chỉ số của phần tử cuối là `length − 1`:

  ```js
  console.log(listOfNumbers[listOfNumbers.length - 1]);  // → 11
  ```

Mảng cung cấp cách lưu trữ và truy xuất dãy giá trị rõ ràng, hiệu quả, thay vì phải dùng các chuỗi định dạng thủ công.
