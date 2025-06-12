Modern computers manage an immense “sea of bits,” subdividing these raw bits into meaningful chunks called **values**. In JavaScript, values—though all ultimately bits—are typed (e.g., numbers, text strings, functions), and each type determines how the value behaves. You create a value simply by naming it; behind the scenes it’s allocated memory until it’s no longer needed, at which point its bits are reclaimed for future use. The rest of the chapter will explore JavaScript’s basic (atomic) value types and the operators that work on them.

Máy tính hiện đại quản lý một “biển” bit khổng lồ, chia nhỏ các bit thô này thành những khối có ý nghĩa gọi là **giá trị**. Trong JavaScript, các giá trị—mặc dù cuối cùng đều là bit—đều có kiểu (ví dụ: số, chuỗi văn bản, hàm), và mỗi kiểu xác định cách giá trị đó hoạt động. Bạn chỉ cần gọi tên để tạo ra một giá trị; phía sau, giá trị đó sẽ được cấp phát bộ nhớ cho đến khi không còn được sử dụng, lúc đó các bit sẽ được thu hồi để tái sử dụng. Phần còn lại của chương sẽ giới thiệu các kiểu giá trị cơ bản (nguyên tố) trong JavaScript và các toán tử có thể thao tác trên chúng.

## Number

