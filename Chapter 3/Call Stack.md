![[call stack.png]]
**Summary (English):**

* When one function calls another, JavaScript remembers **where to return** by pushing a frame onto the **call stack**.
* Each stack frame holds the context of a function call—its local variables and the point in the code to resume after the call returns.
* Execution proceeds by:

  1. Pushing a frame for the calling context.
  2. Jumping into the called function’s frame and running its code.
  3. When that function finishes (hits `return` or the end), its frame is **popped**, and execution **resumes** in the caller’s frame right after the call site.
* This LIFO (last-in, first-out) structure ensures that nested and recursive calls return in the correct order.
* If the call stack grows without bound (for example, via infinite recursion), the program eventually runs out of stack space and crashes with a “stack overflow” error.

**Tóm tắt (Tiếng Việt):**

* Khi một hàm gọi hàm khác, JavaScript lưu lại **vị trí cần quay về** bằng cách đẩy (“push”) khung (frame) của ngữ cảnh gọi lên **ngăn xếp cuộc gọi** (call stack).
* Mỗi khung lưu giữ ngữ cảnh của một lần gọi hàm—các biến cục bộ và điểm sẽ tiếp tục chạy khi hàm đó trả về.
* Trình tự thực thi:

  1. Đẩy khung của hàm hiện tại lên stack.
  2. Chuyển vào khung mới của hàm được gọi và chạy mã trong đó.
  3. Khi hàm hoàn thành (`return` hoặc hết thân hàm), khung đó được **pop** ra, rồi chương trình tiếp tục trong khung của hàm gọi, ngay sau chỗ gọi hàm.
* Cấu trúc LIFO (vào trước – ra sau) đảm bảo các cuộc gọi lồng nhau và đệ quy được trả về đúng thứ tự.
* Nếu stack cứ tiếp tục lớn lên (ví dụ do đệ quy vô hạn), chương trình sẽ cạn bộ nhớ ngăn xếp và gặp lỗi “stack overflow.”
