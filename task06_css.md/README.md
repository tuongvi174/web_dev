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

**Các loại vùng chọn cơ bản**
#####2.2.1. Vùng chọn dựa vào tên thẻ

Đây là kiểu vùng chọn đơn giản nhất, đó là nó sẽ chọn toàn bộ các phần tử trên tài liệu HTML dựa vào tên thẻ có trong tài liệu rồi áp dụng CSS. Ví dụ muốn thay đổi sytle cho toàn bộ thẻ `h1` trong website thì sẽ có đoạn CSS sau với vùng chọn `h1`.

<img src="http://i.imgur.com/Ds6S2qg.png">

<img src="http://i.imgur.com/TgG9tsh.png">

<img src="http://i.imgur.com/gUQ1cis.png">

#####2.2.2. Vùng chọn dựa vào ID

Vùng chọn dựa vào ID (tên định danh) nghĩa là bạn có thể chọn một phần tử cụ thể dựa vào giá trị cuẩ thuộc tính `id` trong thẻ HTML. Sỡ dĩ vùng chọn id được sử dụng để chọn một phần tử cụ thể là vì trên một trang tài liệu HTML thì mỗi phần tử phải mang một id riêng biệt không trùng nhau.

Id được thiết lập dựa vào thuojc tính `id` trong thẻ HTML và bất cứ thẻ nào cũng có thể sử dụng id. Khi viết tên id vào CSS thì nó phải có dấu thăng `(#tên-id)` đặt trước tên id để phân biệt với các loại vùng chọn khác.

<img src="http://i.imgur.com/udSuH7U.png">

<img src="http://i.imgur.com/u9xHqWo.png">

<img src="http://i.imgur.com/kAhDyWO.png">

Ở ví dụ trên có hai thẻ `h1` nhưng nếu muốn viết CSS cho một thẻ `h1` cụ thể nào đó thì sẽ đặt id riêng cho phần tử mà mình cần viết CSS thay vì sử dụng vùng chọn dựa vào tên thẻ.

Ngoài ra còn có một cách viết vùng chọn theo id khác là viết kèm theo tên thẻ đang sử dụng id đó như `h1#post-title`, lưu ý là phải viết sát nhau.

Lưu ý rằng, một thẻ có thể sẽ chứa nhiều id khác nhau và mỗi tên id sẽ được cách nhau bởi khoảng trắng.

```sh
<h1 id="post-title sticky">Hello</h1>
```

#####2.2.3. Vùng chọn dựa vào Class

Class (lớp) cũng rất được sử dụng phổ biến như id nhưng một điểm khác biệt của class là một class có thể được sử dụng cho nhiều phần tử trên một trang tài liệu HTML, còn id thì chỉ được sử dụng một lần suy nhất cho một phần tử.

Class được khai báo trong một phần tử HTML bởi thuộc tính class như `<h1 class="tên-class">`. Khi khai báo vùng vhojn Class trong CSS, thie tên class phải được đặt sau dấu chấm `(tên-class)`.

<img src="http://i.imgur.com/5gxTlFZ.png">

<img src="http://i.imgur.com/2jw7ddg.png">

<img src="http://i.imgur.com/yxERwmq.png">\

#####2.2.4. Vùng chọn theo thứ cấp

Đây là kiểu mà bạn sẽ sử dụng rất thường xuyên, đặc biệt là khi tiến hành viết CSS cho website đó là chọn phần tử thep thứ cấp. Nghĩa là với vùng chọn này, bạn có thẻ chọn một phần tử con trong một phần tử mẹ nào đó.

```sh
<ul id="menu">
 <li>Menu 1</li>
 <li>Menu 2</li>
 <li>Menu 3</li>
</ul>
 
<ul id="social">
 <li>Facebook</li>
 <li>Twitter</li>
 <li>Google+</li>
</ul>
```

Ở đoạn trên, có hai danh sách với thẻ `<ul>` mang 2 id khác nhau. Bây giờ nếu muốn viết CSS cho các thẻ `<li>` trong cái danh sách `#menu` thì làm thế nào? Nếu viết vùng chọn dựa theo tên thẻ thì các thẻ `<li>` ở `#social` cũng sẽ được áp dụng. Lúc này, chúng ta sẽ sử dụng đến vùng chọn thứ cấp.

Để chọn các thẻ `<li>` bên trong `#menu`, mình sẽ viết vùng chọn là `#menu li` thay vì chỉ viết `li` trong CSS. Lúc này CSS sẽ hiểu rằng chúng ta muốn chọn tất cả các thẻ `<li>` nằm bên trong phần tử mang `#menu`.

<img src="http://i.imgur.com/kf3sH0R.png">

<img src="http://i.imgur.com/SHibUB0.png">

<img src="http://i.imgur.com/qpCx9Fx.png">

#####Vùng chọn theo thứ cấp liền nhau

Đây cũng là một kiểu vùng chọn dựa theo thứ cấp, cũng giúp bạn chọn các phần tử bên trong một phần tử nào đấy nhưng nó sẽ chỉ áp dụng cho các phần từ nằm dưới nó một bật.

```sh
<nav id="menu">
<ul>
<li>Menu 1
<ul>
<li>Menu 1.a</li>
<li>Menu 1.b</li>
</ul>
</li>
<li>Menu 2</li>
<li>Menu 3</li>
</ul>
</nav>
```

Nếu muốn viết CSS cho các thẻ `<li>` của Menu 1.a, Menu 1.b thì sẽ đặt vùng chọn là `#menu ul ul > li`. Nếu diễn giải bằng chữ thì nó sẽ chọn thẻ `<li>` nằm trong thẻ `<ul>` ở bật thứ hai và thẻ `<ul>` đó nằm trong id #menu.

<img src="http://i.imgur.com/QeShIui.png">

<img src="http://i.imgur.com/zekOE9z.png">

<img src="http://i.imgur.com/fw0eFMe.png">

Thường thì cách viết vùng chọn này bạn sẽ sử dụng khi tạo menu đổ xuống trong website.