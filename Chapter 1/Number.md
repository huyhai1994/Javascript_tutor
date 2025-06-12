* JavaScript’s **number** type represents all numeric values—whole or fractional—as 64-bit binary patterns.
* Writing `13` in code allocates the 64-bit bit pattern for 13 in memory.
* With  [[64-bit number]](2⁶⁴ ≈ 1.8×10¹⁹ patterns), JavaScript can represent about 18 quintillion distinct values.
* One bit is reserved for the sign, and the remaining bits encode an exponent and mantissa, yielding a maximum exact integer around 9 quadrillion (10¹⁵).
* Fractional numbers use a decimal point (e.g., `9.81`) or scientific notation with `e` (e.g., `2.998e8` for 2.998×10⁸).
* Integer operations below \~9 quadrillion are exact; fractional operations can incur rounding errors because many real numbers can’t be precisely encoded in a finite number of bits.
* Treat fractional values as **approximations**, not perfectly precise quantities.

---

* Kiểu **number** trong JavaScript biểu diễn mọi giá trị số—nguyên hoặc thập phân—dưới dạng mẫu nhị phân 64-bit.
* Viết `13` trong mã sẽ tạo ra mẫu 64-bit tương ứng với số 13 trong bộ nhớ.
* Với 64 bit (2⁶⁴ ≈ 1,8×10¹⁹ mẫu), JavaScript có thể biểu diễn khoảng 18 tỉ tỉ giá trị khác nhau.
* Một bit dành cho dấu, các bit còn lại mã hóa luỹ thừa và mantissa, cho phép lưu chính xác số nguyên tối đa khoảng 9 nghìn tỉ (10¹⁵).
* Số thập phân được viết với dấu chấm (ví dụ `9.81`) hoặc ký hiệu khoa học với `e` (ví dụ `2.998e8` cho 2,998×10⁸).
* Phép toán nguyên dưới \~9 nghìn tỉ luôn chính xác; phép toán với số thập phân có thể bị sai số do nhiều số thực không thể mã hóa chính xác trong một số bit hữu hạn.
* Cần coi các giá trị thập phân là **xấp xỉ**, không phải giá trị chính xác tuyệt đối.

## Arithmetic / phép toán

* The primary operations on numbers in JavaScript are **arithmetic**: addition (`+`), subtraction (`-`), multiplication (`*`), division (`/`), and the remainder (modulo) operator (`%`).
* You write an expression by placing an operator between two values (e.g. `100 + 4 * 11`), which produces a new value.
* **Operator precedence** determines the order of evaluation when no parentheses are present:

  * Multiplication (`*`), division (`/`), and remainder (`%`) come **before** addition (`+`) and subtraction (`-`).
  * Operators with the same precedence associate **left to right** (e.g. `1 - 2 + 1` is evaluated as `(1 - 2) + 1`).
* Use **parentheses** to override the default precedence (e.g. `(100 + 4) * 11`).
* The `%` operator returns the remainder after dividing its left operand by its right operand (e.g. `314 % 100 === 14` and `144 % 12 === 0`).

---

* Các phép toán chính trên số trong JavaScript là **số học**: cộng (`+`), trừ (`-`), nhân (`*`), chia (`/`) và phép chia lấy dư (`%`).
* Viết biểu thức bằng cách đặt toán tử giữa hai giá trị (ví dụ `100 + 4 * 11`) để tạo ra giá trị mới.
* **Độ ưu tiên toán tử** xác định thứ tự tính khi không có ngoặc:

  * Nhân (`*`), chia (`/`) và chia lấy dư (`%`) được thực hiện **trước** cộng (`+`) và trừ (`-`).
  * Các toán tử cùng mức ưu tiên liên kết **từ trái sang phải** (ví dụ `1 - 2 + 1` được tính là `(1 - 2) + 1`).
* Sử dụng **ngoặc đơn** để ghi đè thứ tự ưu tiên (ví dụ `(100 + 4) * 11`).
* Toán tử `%` trả về phần dư của phép chia: ví dụ `314 % 100 === 14` và `144 % 12 === 0`.

## Special Number

JavaScript defines three **special numeric values** that don’t behave like ordinary numbers:

* **Infinity** and **-Infinity**

  * Represent positive and negative infinity.
  * Arithmetic with them “sticks” at infinity (e.g. `Infinity - 1 // → Infinity`).
  * Not mathematically rigorous—using them often leads quickly to NaN.

* **NaN** (“Not-a-Number”)

  * Although of the number type, it signals an undefined or unrepresentable result.
  * Produced by operations such as `0/0`, `Infinity - Infinity`, or other invalid numeric computations.

---

JavaScript định nghĩa ba giá trị số **đặc biệt** không hoạt động như số thông thường:

* **Infinity** và **-Infinity**

  * Biểu diễn vô cực dương và vô cực âm.
  * Phép tính với chúng sẽ “bám” ở vô cực (ví dụ `Infinity - 1 // → Infinity`).
  * Không tuân theo quy tắc toán học chặt chẽ—việc sử dụng thường nhanh chóng dẫn đến NaN.

* **NaN** (“Not-a-Number”)

  * Dù thuộc loại number, NaN báo hiệu kết quả không xác định hoặc không thể biểu diễn.
  * Xuất hiện khi thực hiện các phép toán vô nghĩa như `0/0`, `Infinity - Infinity` hoặc các phép tính số học bị lỗi.
