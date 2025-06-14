
1. **Looping a Triangle** – write a loop that builds and logs

   ```
   #
   ##
   ###
   ####
   #####
   ######
   #######
   ```

2. **FizzBuzz** – log numbers 1 through 100, but for multiples of 3 print “Fizz,” for multiples of 5 print “Buzz,” and for multiples of both print “FizzBuzz.”

3. **Chessboard** – generate an `n×n` grid of “ #” and spaces that alternates like a chessboard.

```
 # # # #
# # # # 
 # # # #
# # # # 
 # # # #
# # # # 
 # # # #
# # # # 
```

---
**Bài tập 1. Vòng lặp tạo tam giác**
Viết một vòng lặp sao cho gọi `console.log` bảy lần để in ra hình tam giác sau:

```
#
##
###
####
#####
######
#######
```

Bạn có thể cần biết rằng để lấy độ dài của một chuỗi, bạn dùng thuộc tính `.length`.

```js
let abc = "abc";
console.log(abc.length);  // → 3
```

---

**Bài tập 2. FizzBuzz**
Viết một chương trình dùng `console.log` để in ra tất cả các số từ 1 đến 100, nhưng có hai ngoại lệ:

* Với số chia hết cho 3, in `"Fizz"` thay vì in số đó.
* Với số chia hết cho 5 (nhưng không chia hết cho 3), in `"Buzz"`.
  Khi đã làm được, hãy sửa lại chương trình để với những số chia hết cho cả 3 và 5 thì in `"FizzBuzz"` (vẫn giữ nguyên in `"Fizz"` hoặc `"Buzz"` cho những số chỉ chia hết cho một trong hai).

> *(Đây là một câu hỏi phỏng vấn kinh điển, được cho là sẽ “lọc” khá nhiều ứng viên lập trình. Nếu bạn giải xong, giá trị thị trường lao động của bạn chắc chắn đã tăng lên.)*

---

**Bài tập 3. Bàn cờ (Chessboard)**
Viết một chương trình tạo ra một chuỗi (string) biểu diễn một lưới kích thước 8×8, dùng ký tự xuống dòng (`\n`) để tách các hàng. Ở mỗi vị trí trong lưới, in ra hoặc một dấu cách, hoặc ký tự `#`, sao cho tổng thể nhìn giống bàn cờ.
Gửi chuỗi này vào `console.log` sẽ cho ra:

```
 # # # #
# # # # 
 # # # #
# # # # 
 # # # #
# # # # 
 # # # #
# # # # 
```

Khi đã làm được, hãy định nghĩa biến `size = 8` và sửa chương trình để nó có thể vẽ bàn cờ với bất kỳ kích thước rộng-cao nào bạn muốn.


**Bài tập 4 . In bảng cửu chương từ 1×1 đến 9×9**

**Mô tả:**
Dùng hai vòng lặp lồng nhau để in ra bảng cửu chương 9×9 theo định dạng từng dòng, ví dụ:

```
1 × 1 = 1    1 × 2 = 2    …    1 × 9 = 9
2 × 1 = 2    2 × 2 = 4    …    2 × 9 = 18
…
9 × 1 = 9    9 × 2 = 18   …    9 × 9 = 81
```

**Yêu cầu:**

1. Vòng lặp ngoài chạy biến `i` từ 1 đến 9 (đại diện cho số bị nhân).
2. Vòng lặp trong chạy biến `j` từ 1 đến 9 (đại diện cho số nhân).
3. Mỗi lần lặp lồng, tính `i * j` và nối chuỗi theo mẫu `"i × j = result"`, rồi in hoặc dồn chung vào một chuỗi lớn với khoảng trắng giữa các mục.
4. Cuối mỗi vòng lặp ngoài, thêm ký tự xuống dòng `\n` để xuống dòng cho dòng mới.

