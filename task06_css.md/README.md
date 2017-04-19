##Task 6
------------------------
>Người thực hiện: Hồ Nguyễn Tường Vi
>
>Tên tài liệu: 
 + [https://www.w3schools.com](https://www.w3schools.com/css/)
 + [https://www.youtube.com](https://www.youtube.com/playlist?list=PLl4nkmb3a8w1cnIhegAj5_mE8w_mbYvY4)
 + [ http://thachpham.com](http://thachpham.com)
 >
 >Ngày cập nhật: 25/04/2017
 >
 ----------------------------

##Mục Lục:

[1. CSS là gì?](#1)

[2. CSS cơ bản](#2)

##Nội dung:

####1. CSS là gì?<a name="1"></a>

<img src="http://i.imgur.com/l9DTfK7.gif">

CSS là chữ viết tắt của Cascading Style Sheets, nó là một ngôn ngữ được sử dụng để tìm và định dạng lại các phần tử được tạo ra bởi các ngôn ngữ đánh dấu (ví dụ như HTML).

####2. CSS cơ bản<a name="2"></a>

[2.1. Nhúng CSS vào website](#3)

[2.2. Vùng chọn và các kiểu vùng chọn cơ bản](#4)

[2.3. Các đơn vị đo lường cơ bản](#5)

[2.4. Các thuộc tính trang trí văn bản](#6)

[2.5. Các thuộc tính trang trí chữ viết](#7)

[2.6. Phần tử Block và Inline](#8)

[2.7. Thẻ div và vai trò khi tạo bố cục](#9)

[2.8. Kỹ thuật Box Model cơ bản](#10)

[2.9. Tùy chỉnh kích thước box (block)](#11)

[2.10. Tính toán lại kích thước của box với box-sizing](#12)

[2.11. Thêm nền cho block](#13)

[2.12. Float và Clear Float](#14)

[2.13. Reset CSS là gì?](#15)

[2.14. Trang trí danh sách với list-style](#16)

[2.15. Thuộc tính Display](#17)

[2.16. Thuộc tính Position](#18)

[2.17. Pseudo-classes cơ bản](#19)

[2.18. Cách làm menu ngang dropdown cơ bản](#20)

[2.19. Làm menu dọc có dropdown đơn giản](#21)

[2.20. Thiết kế giao diện đơn giản](#22)

[2.21. CSS Framework là gì và cách sử dụng](#23)

[2.22. Tạo chuyển động với Transition](#24)

[2.23. Thay đổi hình dạng đối tượng với Transform](#25)

####*Nào chúng ta cùng bắt đầu tìm hiểu về CSS nhé!*

####2.1. Nhúng CSS vào website<a name="3"></a>

Chúng ta có hai cách nhúng CSS vào website:

 + **Inline Styles** - Nhúng trực tiếp vao tài liệu HTML thông qua cặp thẻ `<style> </style>`
 + **External Styles** - Tạo một tập tin .css riêng và nhúng vào tài liệu HTML thông qua cặp thẻ `<link>`

Mỗi cách tùy theo trường hợp sẽ có ưu nhược điểm khác nhau:

**Inline Styles**

 + Thích hợp với việc chèn một vài đoạn CSS ngắn
 + Trình duyệt không mất thời gian tải tập tin CSS

*Cách nhúng CSS bằng Inline Styles*

Để nhúng CSS vào website thông qua kiểu Inline Styles, bạn sẽ khai báo cặp thẻ `<style>` vào vị trí bất kỳ của website (tốt nhất là bên trong cặp thẻ `<head>`) như sau:

```sh
<style type="text/css">

</style>
```

<img src="http://i.imgur.com/Sw5Mjut.png">

**External Styles**

 + Thích hợp với việc chèn nhiều đoạn CSS, dễ quản lý
 + Nhưng trình duyệt sẽ mất thêm thời gian để tải tập tin CSS

*Cách nhúng CSS bằng External Styles*

Khi sử dụng cách này, việc đầu tiên là bạn cần tạo ra một tập tin .css với tên bất kỳ, bạn có thể dùng bất cứ chương trình soạn thảo văn bản nào để tạo. Sau đó dán một đoạn CSS đơn giản vào như thế này:

```sh
p {
color: blue;
font-family: Arial;
}
```

Và cuối cùng là chèn vào tập tin HTML bằng thẻ `<link>` và thẻ này phải đặt bên trong cặp thẻ `<head>`.

```sh
<link rel="stylesheet" href="name.css" />
```

Trong đó, thuộc tính rel là khai báo loại tập tin nhúng và href là đường dẫn khai báo tên tập tin .css cần nhúng vào.

<img src="http://i.imgur.com/FwNxID2.png">

**Nhúng tập tin CSS vào bên trong một tập tin CSS**

Chẳng hạn bây giờ bạn có 3 tập tin CSS mà bạn không muốn thêm tất cả tụi nó vào website mà chỉ muốn thêm một tập tin CSS thôi, thì bạn có thể sử dụng cách nhúng các tập tin CSS vào bên trong một tập tin CSS với từ khóa `@import`, và các từ khóa `@import` này phải được đặt ở đầu tập tin .css (không bao gồm các đoạn comment).

Ví dụ bạn có thể nhúng một tập tin demo.css vào trong tập tin style.css bằng cách chèn đoạn này vào tập tin style.css:

```sh
@import "demo.css";
```

##2.2. Vùng chọn và các kiểu vùng chọn cơ bản<a name="4"></a>

Vùng chọn đóng vai trò rất quan trọng khi viết CSS, bởi khi bạn sử dụng vùng chọn sai thì điều đó có nghĩa là các quy tắc CSS sẽ không được thực thi hoặc thực thi không đúng chỗ. Việc nẵm rõ quy tắc sử dụng vùng chọn là kỹ thuật quan trọng đầu tiên khi bạn sử dụng CSS.

Vùng chọn trong CSS rất linh hoạt, hầu như bạn có thể chọn bất cứ cái gì từ thẻ `<body>` đi sâu vào các thẻ bên trong nó.

----------------------------------------
>**Vùng chọn là gì?**
>
>Trong CSS, vùng chọn nghĩa là khu vực mà bạn muốn nó sẽ được áp dụng các quy tắc CSS mà bạn muốn chỉ định cho nó. Ví dụ bạn muốn tăng kích thước font chữ của các thẻ h1 thì vùng chọn của bạn sẽ là h1.
>
>*Vùng chọn có thể là tên thẻ HTML hoặc thuộc tính của HTML*
-------------------------------------------------------

