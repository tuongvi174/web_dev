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

####2.2. Vùng chọn và các kiểu vùng chọn cơ bản<a name="4"></a>

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

####2.3. Các đơn vị đo lường cơ bản<a name="5"></a>

Trong CSS có hai loại đơn vị là **Absolute Units** (đơn vị tuyệt đối) và **Relative Units** (đơn vị tương đối).

**ABSOLUTE UNITS**

Là các đơn vị vật lý đã được định nghĩa sẵn và đại diện cho các đơn vị đo lường vật lý. Các đơn vị này không bị phụ thuộc và không hề thay đổi bởi bất cứ tác động nào. Ví dụ như đơn vị mét, cen-ti-mét,..là các đơn vị tuyệt đối.

Các đơn vị tuyệt đối sử dụng trong CSS gồm có:

 + `px`: Đây là một đơn vị được sử dụng trên màn hình hiển thị, một px sẽ tương đương với một điểm ảnh trên màn hiển thị. Chất lượng của điểm ảnh sẽ hoàn toàn khác nhau trên một số thiết bị, ví dụ như một điểm ảnh trên các thiết bị in ấn sẽ khác với một điểm ảnh trên các thiết bị màn hình độ phân giải thấp.
 + `pt`: Đơn vị point và cứ *1 ich = 72pt*

<img src="http://i.imgur.com/mp06hPe.png">

<img src="http://i.imgur.com/kD3L8Gg.png">

**RELATIVE UNITS**

Là các đơn vị đo lường được sử dụng trong CSS ở mức tương đối, nghĩa là nó có thể sẽ được thay đổi bởi các thành phần khác ví dụ như thay đổi phụ thuộc vào kích thước màn hình.

Các đơn vị tương đối được sử dụng trong CSS gồm có:

 + `% (percentages)`: Là đơn vị tham chiếu tỷ lệ so với một phần tử mẹ của nó dựa vào kích thước. Nếu sử dụng đơn vị này để gán kích thước cho thẻ `<html>` tren website thì nó sẽ thay đổi theo kích thước màn hình hoặc/cửa sổ website.
 
 <img src="http://i.imgur.com/CUavdkj.png">

 <img src="http://i.imgur.com/kUlh2J6.png">

 <img src="http://i.imgur.com/yqSK7tU.png">

 + `em`: Là đơn vị tham chiếu tỷ lệ so với phần tử mẹ của nó dựa vào giá trị của thuộc tính `font-size`. Ví dụ, bạn đặt cho font-size cho phần tử mẹ của nó là 19px thì nếu bạn sử dụng em trong khu vực phần tử đó thì 1em = 19px.

<img src="http://i.imgur.com/38kWaIe.png">

<img src="http://i.imgur.com/8H2hjoO.png">

<img src="http://i.imgur.com/AvRkO6n.png">

 + `rem`: Là đơn vị tham chiếu tỷ lệ so với phần tử gốc của một website dựa vào thuộc tính font-size, nghĩa là sẽ biến đổi tùy theo giá trị của thuộc tính font-size trong thẻ `<html>`. Cũng như `rem`, nếu bạn khai báo font-size cho thẻ `<html>` là 16px thì 1rem = 16px.

####2.4. Các thuộc tính trang trí văn bản <a name="6"></a>

Một trong các loại thuộc tính đơn giản nhất nhưng lại dùng nhiều nhất là các thuộc tính được dùng để thay đổi cách hiển thị của văn bản, được gọi là **Text Styles**

Text Styles trong CSS hiện tại có khoảng 13 thuộc tính được sử dụng bao gồm căn lề văn bản, trang trí văn bản, định hướng văn bản,... Cụ thể là có các thuộc tính thường dùng sau:

 + `text-align`: Căn lề văn bản
 + `text-decoration`: Trang trí văn bản
 + `text-indent`: Thêm khoảng trống trước vản bản theo chiều ngang tuef trái sang phải.
 + `text-shadow`: Thêm bóng cho văn bản
 + `text-transform`: Tùy chỉnh việc hiển thị chữ in hoa

**Text-align**

Thuộc tính `text-align` này sẽ giúp bạn tùy chỉnh canh lề cho các đoạn văn bản bên trong website. Thuộc tính này hỗ trợ cho bạn các giá trị sau:

```sh
text-align: left; // Căn lề văn bản từ bên trái
 
text-align: right; // Căn lề văn bản từ bên phải
 
text-align: center; // Căn lề văn bản từ chính giữa
 
text-align: justify; // Căn lề văn bản đều hai bên
```

**Text-decorations**

Thuộc tính này sẽ giúp bạn trang trí lại văn bản hiển thị trên tài liệu theo một số kiểu nhất định.

```sh
text-decoration: overline | underline | line-through| none
```

 + `overline`: gạch trên chữ
 + `underline`: gạch dưới chữ
 + `line-through`: gạch ngang chữ
 + `none`: không có gạch gì cả

<img src="http://i.imgur.com/38kWaIe.png">

<img src="http://i.imgur.com/9kad7Zt.png">

<img src="http://i.imgur.com/bMRgWam.png">

Ngoài ra thuộc tính này còn có thêm một số thuộc tính con của nó nhưng lại chưa được hỗ trợ bởi các trình duyệt thông dụng, đó là text-decoration-color, text-decoration-line và text-decoration-style.

**Text-indent**

Thuộc tính này sẽ tạo ra một khoảng trắng bên trái của văn bản (hoặc bên phải của văn bản với các ngôn ngữ hiển thị từ phải sang trái), giá trị của nó là số kèm theo đơn vị đo lường.

```sh
p {
   text-indent: 15px;
   text-indent: 15%;
   text-indent: 1.5pt;
}
```

<img src="http://i.imgur.com/F7wjFwO.png">

<img src="http://i.imgur.com/ltSR2lr.png">

<img src="http://i.imgur.com/EFbFbJb.png">

**Text-shadow**

Thuộc tính này để thêm bóng đổ cho văn bản.

```sh
text-shadow: [màu sắc] [tọa độ x y] [độ mờ];
```

Trong đó, tọa độ x-y là giá trị kiểu đo lường và số đứng trước được xem là x và đứng sau là y, độ mờ nếu không khai báo thì có giá trị là 0 và giá trị của độ mờ luôn đứng sau giá trị của tọa độ.

```sh
#title {
   text-shadow: blue 2px 3px 4px;
}
```

Đoạn trên nghĩa là văn bản mang id #title sẽ có bóng đổ màu xanh, tọa độ x là 2px, tọa độ y là 3px và độ mờ là 4px.

Ngoài ra, bạn cũng có thể tạo ra nhiều bóng đổ cho một văn bản bằng cách viết nhiều đoạn cú pháp và mỗi đoạn sẽ được cách nhau bằng dấu phẩy, ví dụ:

```sh
text-shadow: red 2px -1px 3px, blue -2px 1px 2px;
```

<img src="http://i.imgur.com/YzrOEjO.png">

<img src="http://i.imgur.com/9AFKr4c.png">

<img src="http://i.imgur.com/yzrAiQn.png">

**Text-Transform**

Nếu bạn muốn tùy chỉnh việc hiển thị chữ in hoa hay in thường trong đoạn văn bản mà không cần viết thủ công cả đoạn văn bản thì có thể sử dụng thuộc tính `text-transform` này.

Thuộc tính này có 3 giá trị chính là `capitalize` (in hoa chữ cái đầu tiên của mỗi từ), `uppercase` (in hoa cả đoạn văn bản), `lowercase` (viết thường cả đoạn văn bản) và `none` (không có gì cả).

```sh
#title { text-transform: uppercase; }
```

<img src="http://i.imgur.com/2QffY4v.png">

<img src="http://i.imgur.com/Yp2AQS9.png">

<img src="http://i.imgur.com/NcL1Ai7.png">

Có một vấn đề bạn nên lưu ý là ở giá trị `capitalize`, nó chỉ có tác dụng với chữ cái đầu tiên của văn bản, còn các chữ cái tiếp theo nó vẫn hiển thị theo cách văn bản mà bạn soạn ra.

####2.5. Các thuộc tính trang trí chữ viết <a name="7"></a>

**Thiết lập font chữ với font-family**

Để thiết lập font chữ cho văn bản, chúng ta sẽ sử dụng thuộc tính `font-family` và giá trị của nó là tên các loại font chữ cần sử dụng.

```sh
font-family: tên-font, tên-font-backup, tên-font-backup,...;
```

Trong đó, tên font đầu tiên sẽ ưu tiên hiển thị, nếu máy tính người dùng không có font đó thì nó sẽ sử dụng font backup tiếp theo và cứ tiếp tục như thế.

Các font chữ được thiết lập trong CSS theo cách thông thường thì nó sẽ lấy font chữ trên máy tính ra để hiển thị. Điều này có nghĩa là nếu bạn thiết lập một font mà trên máy của người dùng không có thì nó sẽ không hiển thị được.

Khi thiết lập font chữ, bạn cần biết trước tiên là hai giá trị `serif` và `sans-serif`. Trong đó, `serif` là giá trị font kiểu có chân và `sans-serif` là giá trị kiểu font không chân và các font này sẽ lấy dựa theo font chữ cơ bản trên máy tính.

<img src="http://i.imgur.com/2QffY4v.png">

<img src="http://i.imgur.com/8JsJQfX.png">

<img src="http://i.imgur.com/qY2QwWw.png">

**Các font cơ bản trên máy tính**

Các font cơ bản trên máy tính bao gồm:

*Serif*

 + Palatino
 + Time New Roman
 + Georgia

*Sans Serif*

 + Arial
 + Helvetica
 + Verdana
 + Tahoma

Bạn có thể dùng một tập hợp font stack các font chữ cơ bản trên máy tính để dự phòng. Ví dụ:

```sh
font-family: Helvetica, Arial, Tahoma, sans-serif;
```

**Tra cứu font stack**

Nếu bạn có nhu cầu tham khảo các font chữ phổ biến nhất trên máy tính và copy đoạn code sử dụng font chữ tối ưu nhất thì bạn có thể tra cứu tại trang [www.cssfontstack.com](www.cssfontstack.com) để lấy font stack chuẩn và an toàn hơn để chắc chắn website mình hiển thị tốt với đại đa số người dùng, cả Windows và Mac.

**Font-style**

Thuộc tính `font-style` là để bạn thiết lập chữ viết được hiển thị dưới dạng in nghiêng hoặc bình thường. Thuộc tính này có 3 giá trị là `normal` (bình thường), `italic` (in nghiêng), `oblique` (cũng là nghiêng).

**In đậm chữ viết với font-weight**

Việc tùy chỉnh in đậm chữ viết có hẳn một thuộc tính riêng đó là `font-weight`. Giá trị của nó là là từ `100`,`200`,`300`,….`900`, số càng lớn thì chữ càng đậm và “mập” ra.

Ngoài ra nếu bạn không thích dùng số thì bạn có thể dùng các giá trị kiểu chữ là `normal`,`bold`. Nếu phần tử mẹ của nó đã được thiết lập `font-weight` thì có thể dùng giá trị `lighter` và `bolder` để thiết lập độ đậm tương đối.

**Màu chữ với thuộc tính color**

Để thiết lập màu chữ, bạn sẽ dùng thuộc tính `color` và thuộc tính này hiện tại hỗ trợ chính thức 3 kiểu giá trị biểu diễn màu sắc cần sử dụng đó là kiểu tên, kiểu HEX và kiểu RBG. Về ý nghĩa về các kiểu này mình sẽ giải thích ở một bài học khác, nhưng hiện tại bạn có thể tra cứu tên màu hay mã màu tại [đây](https://drafts.csswg.org/css-color-3/#svg-color).

```sh
body {
 
   color: #333333;
 
}
```

**Thay đổi kích thước chữ với font-size**

Để đổi kích thước của chữ, bạn có thể sử dụng thuộc tính font-size và thuộc tính này chỉ có một giá trị duy nhất là số kèm đơn vị đo lường. Ví dụ:

```sh
p {
 
font-size: 16px;
 
}
```


####2.6. Phần tử Block và Inline<a name="8"></a>

----------------
>`CSS Layout` là thuật ngữ chỉ chung về việc dựng bố cục cho website dựa trên việc sử dụng và tùy biến các khối, phần tử.
--------------------

Để dễ dàng hơn để sau này khi tìm hiểu về các kỹ thuật nâng cao, thì việc bạn cần làm bây giờ là nên hiểu thế nào là `Block`, thế nào là `Inline`. Đây là hai thuật ngữ rất thường sử dụng trong CSS.


