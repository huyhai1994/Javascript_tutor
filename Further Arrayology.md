**Summary (English):**
JavaScript arrays come with a few more useful methods beyond `push`/`pop`:

1. **`unshift(...items)`** – adds items to the **start** of the array and returns the new length.
2. **`shift()`** – removes and returns the **first** element of the array.

These let you treat an array as a **queue** (FIFO).

```js
let todoList = [];
function remember(task)       { todoList.push(task); }
function getTask()             { return todoList.shift(); }
function rememberUrgently(task){ todoList.unshift(task); }
```

3. **`indexOf(value[, fromIndex])`** – finds the first index at which `value` appears (or `-1`).

4. **`lastIndexOf(value[, fromIndex])`** – finds the last index (searching from the end).

5. **`slice(start[, end])`** – returns a **new array** containing elements from `start` (inclusive) up to `end` (exclusive). Omitting `end` includes everything to the end; omitting `start` copies the whole array.

```js
[0,1,2,3,4].slice(2,4); // → [2,3]
[0,1,2,3,4].slice(2);   // → [2,3,4]
```

6. **`concat(...values)`** – returns a new array by appending each argument. If an argument is itself an array, its elements are flattened in; if not, the value is added as a single element.

```js
[1,2].concat([3,4],5); // → [1,2,3,4,5]
```

A common pattern is to **remove** an element at a given index without mutating the original array:

```js
function remove(array, index) {
  return array
    .slice(0, index)
    .concat(array.slice(index + 1));
}
// remove(["a","b","c","d","e"], 2) → ["a","b","d","e"]
```

---

**Tóm tắt (Tiếng Việt):**
Các phương thức bổ sung trên mảng JavaScript:

1. **`unshift(...items)`** – thêm phần tử vào **đầu** mảng, trả về độ dài mới.
2. **`shift()`** – xoá và trả về phần tử **đầu tiên** của mảng.

Dùng để xử lý mảng như hàng đợi (FIFO):

```js
let todoList = [];
function remember(task)       { todoList.push(task); }
function getTask()             { return todoList.shift(); }
function rememberUrgently(task){ todoList.unshift(task); }
```

3. **`indexOf(value[, fromIndex])`** – tìm chỉ số xuất hiện đầu tiên của `value` (hoặc `-1`).

4. **`lastIndexOf(value[, fromIndex])`** – tìm chỉ số xuất hiện cuối cùng (tìm từ cuối mảng).

5. **`slice(start[, end])`** – trả về mảng mới gồm các phần tử từ `start` (bao gồm) đến trước `end` (không bao gồm). Bỏ `end` để lấy đến cuối; bỏ `start` để sao chép toàn bộ mảng.

```js
[0,1,2,3,4].slice(2,4); // → [2,3]
[0,1,2,3,4].slice(2);   // → [2,3,4]
```

6. **`concat(...values)`** – tạo mảng mới bằng cách nối các đối số lên mảng gốc. Nếu đối số là mảng thì “trải phẳng” các phần tử, nếu không thì thêm nguyên giá trị đó.

```js
[1,2].concat([3,4],5); // → [1,2,3,4,5]
```

Một ví dụ hay để **xoá** phần tử ở chỉ số xác định mà không thay đổi mảng gốc:

```js
function remove(array, index) {
  return array
    .slice(0, index)
    .concat(array.slice(index + 1));
}
// remove(["a","b","c","d","e"], 2) → ["a","b","d","e"]
```
