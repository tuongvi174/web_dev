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

**Block là gì?**

Phần tử khối (Block Elements) là thuật ngữ chỉ chung các thẻ HTML có chức năng tạo một khu vực hay nói dễ nghe xíu là một khối. Khối này có nghĩa là một thẻ khi mà bạn khai báo thì nó sẽ được hiển thị ở mỗi dòng riêng biệt bao gồm các nội dung nằm bên trong. Ở các bài học HTML cơ bản bạn có thể đã biết qua một số thẻ block cơ bản như `<p>`, `<ul>`, `<ol>`, `<h1>`,…

**Inline là gì?**

Phần tử nội dòng (Inline Elements) là thuật ngữ chỉ chung các thẻ HTML khi mà khai báo vào nội dung thì nó vẫn sẽ nằm chung một dòng với các văn bản khác. Một số thẻ inline rất hay dùng đó là `<b>`, `<strong>`, `<i>`, `<u>`,…và đặc biệt là `<span>` nếu bạn cần gộp nhóm các phần tử nào đó mà không ảnh hưởng đến các văn bản chung một hàng, thẻ `<span>` này có ý nghĩa và cách sử dụng giống như `<div>` nhưng nó được dùng trong inline.

<img src="http://i.imgur.com/r3oqgBY.png">

<img src="http://i.imgur.com/NxcQmM0.png">

####2.7. Thẻ div và vai trò khi tạo bố cục<a name="9"></a>

**Thẻ `div` là gì?**

Đây là cái thẻ mà nó là chữ viết tắt của division (nghĩa là khu trong tiếng Việt theo từ điển kỹ thuật chung) được sử dụng để tạo ra một khu vực kiểu block nào đó trên một website, hay bạn có thể hiểu là gom nhóm tập hợp các phần tử trên website vào một khu vực với thẻ `<div>`.

<img src="http://i.imgur.com/jBWfvoQ.png">

Thường thì một website sẽ có 4 phần chính là header (hiển thị banner, logo), content (hiển thị nội dung), sidebar (cột bên cạnh nội dung) và footer (khu vực chân website). Vậy thì bây giờ mình có thể tạo ra 4 thẻ `<div>` với 4 id khác nhau nhằm chia khu vực ra. Trong mỗi khu vực mình có thể thêm nội dung riêng cho nó vào, ví dụ:

<img src="http://i.imgur.com/Wv5Hz6N.png">

<img src="http://i.imgur.com/y0gBkIW.png">

####2.8. Kỹ thuật Box Model cơ bản<a name="10"></a>

**Box Model** là một kỹ thuật cơ bản nhất trong CSS Layout và được sử dụng để bạn mô tả về khoảng cách mà mỗi phần tử trên website được sở hữu, hay nói cách khác là kỹ thuật tinh chỉnh khoảng cách hiển thị cho mỗi phần tử trên website.

*Kỹ thuật Box Model trong CSS bao gồm 4 phần quan trọng đó là:*

 + **Margin**: Khoảng cách tính từ bên ngoài của phần tử.
 + **Border**: Đường viền của phần tử.
 + **Padding**: Khoảng cacsch tính từ bên trong của phần tử.
 + **Content**: Nội dung trong phần tử.

<img src="http://i.imgur.com/J4G502D.png">

Và trong 4 thành phần trên thì phần content chúng ta sẽ không có thuộc tính CSS nào đại diện cả vì nó là nội dung trong phần tử. Còn 3 phần còn lại thì sẽ có các thuộc tính CSS đại diện như sau:

```sh
margin: top right bottom left;
 
border: top right bottom left;
 
padding: top right bottom left;
```

**Padding**

Padding nghĩa là chúng ta sẽ thiết lập khoảng cách được tính từ phần Content trở ra viền của phần tử, đơn giản vậy thôi. Padding được khai báo trong CSS bởi thuộc tính `padding` với giá trị theo tuần tự top right bottom left (trên > phải > dưới > trái) và giá trị là số kèm theo đơn vị đo lường.

<img src="http://i.imgur.com/rs229Ra.png">

<img src="http://i.imgur.com/HtPghjd.png">

<img src="http://i.imgur.com/eP5qcGk.png">

Ngoài thuộc tính padding thì thuộc tính này còn có 4 thuộc tính con khác đó là `padding-top`, `padding-bottom`, `padding-left` và `padding-right` và mỗi thuộc tính là để thiết lập giá trị cho từng mặt cụ thể.

**Border**

Border nghĩa là thuộc tính để bạn tạo viền cho phần tử và nó sẽ được khai báo bằng thuộc tính `border` trong CSS.

Thuộc tính border này bạn sẽ viết theo cấu trúc như sau:

```sh
border: [size] [type] [color];
```

Trong border có hỗ trợ một số type như `solid`, `dotted`, `double`, `groove`, `ridge`, `inset` và `outset`.

Giống như các thẻ trong Box Model khác, border cũng có các thẻ con là `border-top`, `border-right`, `border-bottom` và `border-left`.

**Margin**

Trong khi Padding có nhiệm vụ tạo khoảng cách giữa phần Content với Border thì Margin sẽ có tác dụng tạo khoảng cách từ Border trở ra ngoài, nói dễ hiểu thì nó sẽ giúp bạn tinh chỉnh khoảng cách giữa các phần tử với nhau.

<img src="http://imgur.com/LZYwxml">

<img src="http://i.imgur.com/pR0oYaF.png">

<img src="[Imgur](http://i.imgur.com/vdAC8xG.png)">

Và nó cũng có một số thuộc tính con là `margin-top`, `margin-right`, `margin-bottom` và `margin-left`.

####2.9. Tính toán lại kích thước của box với box-sizing<a name="11"></a>

Trong CSS thì hiện tại có tất cả 6 thuộc tính để bạn tùy biến chiều rộng và chiều cao của phần tử bao gồm:

| Tên thuộc tính | Mô tả | Các kiểu giá trị |
|----------------|-------|------------------|
| Height | Thiết lập chiều cao của một phần tử | auto, lengh, %, inherit |
| Max-height | Thiết lập chiều cao tối đa của một phần tử | none, length, %, inherit |
| Max-width | Thiết lập chiều rộng tối đa của một phần tử | none, length, %, inherit |
| Min-height | Thiết lập chiều cao tối thiểu của một phần tử | length, %, inherit |
| Min-width | Thiết lập chiều rộng tối thiểu của một phần tử | length, %, inherit |
| Width | Thiết lập chiều rộng của phần tử | auto, lengh, %, inherit |

Ở cột các kiểu giá trị, `length` nghĩa là kiểu giá trị kèm đơn vị như `px`, `pt`, `em`, `rem` và `%`, `none` là bỏ thiết lập, `auto` là tự động tính dựa theo chiều còn lại và `inherit` là thừa kế giá trị đã thiết lập trước đó cho thuộc tính này.

Và xin lưu ý thêm là bạn chỉ có thể thiết lập kích thước với các phần tử Block, Table và các đối tượng (hình ảnh, video, flash,…) chứ không thể thiết lập cho các phần tử Inline.

Đối với các thuộc tính dạng `min-*`, `max-*` thì nghĩa là nó sẽ căn độ dài của phần tử dựa vào các nội dung bên trong nhưng sẽ có kích thước tối thiểu/tối đa được phép sử dụng. Ví dụ bạn có phần `#content`, bên trong `#content` bạn có phần `#post` và thiết lập chiều rộng cho `#post` là 500px. Thì nếu bạn đặt thuộc tính `max-width` cho `#content` là 400px thì cái thằng `#post` nó cũng chỉ giãn được tối đa là 400px chứ không thể hơn.

**Box-sizing**

Nếu bây giờ bạn muốn làm cho phần tử của mình phải giữ nguyên kích thước mặc dù có cộng thêm padding và border thì sẽ cần phải dùng đến thuộc tính box-sizing. box-sizing là một thuộc tính sẽ giúp bạn có thể tính toán và làm chủ được kích thước của một phần tử dựa vào thuộc tính width và height đã được thiết lập bên trong. Hay nói cách khác, là bạn sẽ muốn thuộc tính `width` và `height` là kích thước đã bao gồm border và padding.

`box-sizing` là một thuộc tính trong CSS3 nên khi viết bạn phải viết thành 3 lần với các tiền tố khác nhau, ví dụ:

```sh
box-sizing: border-box;
-moz-box-sizing: border-box;
-webkit-box-sizing: border-box;
```

Trong đó, nếu viết không có tiền tố là dành cho trình duyệt IE8, Opera 7, Firefox và Google chrome bản mới. `-webkit` là dành cho Google Chrome bản cũ và `-moz` là dành cho Firefox bản cũ.

*Các giá trị của box-sizing*

Hiện tại `box-sizing` có hỗ trợ một số giá trị như sau:

 + `content-box`: Giá trị mặc định, nghĩa là giá trị width và height chỉ áp dụng cho khu vực nội dung bên trong, không bao gồm padding, border và margin.
 + `border-box`: Khi thiết lập giá trị này, thì width và heigh sẽ bao gồm cho cả phần nội dung, padding và border nhưng không bao gồm margin.
 + `padding-box`: Với giá trị này thì width và height chỉ bao gồm cho phần nội dung và padding, không bao gồm border và margin. (Chỉ có tác dụng với trình duyệt Firefox)


####2.10. Thêm nền cho block<a name="12"></a>

**Màu nền với background-color**

Nếu bạn muốn thiết lập màu nền bằng CSS thì có thể sử dụng thuộc tính `background-color` và giá trị của nó là tên màu, hoặc mã màu HEX/RBG.

<img src="http://i.imgur.com/kdJpXwh.png">

<img src="http://i.imgur.com/RgLHV6Y.png">

**Ảnh nền với background-image**

Đối với thuộc tính thêm ảnh nền thì chúng ta sẽ sử dụng `background-image` và nó còn có thêm khá nhiều thuộc tính khác nữa kèm theo.

Ngoài ra, bạn có thể thêm nhiều ảnh nền khác nhau trên cùng một block bằng cách sử dụng nhiều giá trị `url()` và các giá trị phải được cách nhau bởi dấu phẩy. Ví dụ:

```sh
background-image: url('ảnh 1'), url('ảnh 2');
```

**Tùy chỉnh lặp lại ảnh nền với background-repeat**

Mặc định khi sử dụng ảnh nền, thì hình ảnh sẽ được lặp đi lặp lại theo cả chiều ngang và chiều dọc cho đến khi ảnh nền lấp toàn bộ phần tử. Nhưng bạn cũng có thể tùy chỉnh lại việc lặp ảnh nền thông qua thuộc tính `background-repeat`, nó hỗ trợ các giá trị như sau:

 + `no-rêpat`: Không lặp.
 + `repeat-x`: Lặp theo chiều ngang.
 + `repeat-y`: Lặp theo chiều dọc.
 + `space`: Lặp đều theo chiều ngang và chiều dọc, ảnh nền sẽ cách nhau bằng khoảng trắng.
 + `round`: Chưa hiểu lắm nên không giải thích.
 + `repeat`: Mặc định.

**Đổi vị trí ảnh nền với background-position**

Đối với các tấm ảnh nền cỡ nhỏ hoặc dùng background-size để sửa lại kích thước thì có thể bạn sẽ cần thay đổi vị trí hiển thị của ảnh nền đó, và bạn có thể dùng thuộc tính background-position này. Nó có một số giá trị như sau:

 + `top`: hiển thị ở trên đầu phần tử.
 + `bottom`: hiển thị bên dưới phần tử.
 + `left`: hiển thị bên trái phần tử.
 + `right`: hiển thị bên phải phần tử.
 + `center`: hiển thị chính giữa phần tử.
 + `y-x`: tùy biến vị trí hiển thị theo tọa độ, giá trị đứng trước là y và đứng sau là x. Ví dụ: `15px` `10px`.

Đối với thuộc tính này thì bạn có thể viết tối đa cùng lúc hai giá trị. Ví dụ bạn muốn ảnh của bạn sẽ nằm bên phải phía trên phần tử thì sẽ có giá trị là `left top`. Bạn cũng có thể thiết lập giá trị cho nhiều ảnh nền cùng lúc kiểu `left top`, `top center`.

####2.11. Float và Clear Float<a name="13"></a>

**Chia cột trong CSS**

Việc chia cột trong CSS là việc bạn thiết lập những phần tử con trong một phần tử mẹ nằm trên cùng một hàng. Ví dụ, mình muốn phần nội dung website của mình có hai cột thì mình sẽ tạo ra 3 cái `<div>`, một cái `<div>` mình gọi nó là container hoặc phần tử mẹ, hai cái `<div>` còn lại mình gọi là column (cột).

```sh
<div id="content" class="container">
 
   <div id="post">Nội dung của #post</div>
 
   <div id="sidebar">Nội dung của #sidebar</div>
 
</div>
```

**Các bước chia cột trong CSS**

Trước tiên, chúng ta sẽ tiến hành thiết lập chiều rộng cho class `container`, nên thêm một cái border để tí nữa bạn sẽ hiểu clear float là thế nào:

```sh
/*==Thiết lập container==*/
 
.container {
   width: 960px;
   border: 1px solid #333;
   padding: 10px;
}
```

Tiếp tục, chúng ta thiết lập chiều rộng của #post và mình sẽ muốn cột #post sẽ chiếm 660px, đồng thời thêm màu sắc cho hai thằng này để dễ nhìn một xíu.

```sh
/*==cột #post==*/
#post {
   width: 660px;
   height: 150px;
   background: #e8e8e8;
}
```

Bây giờ mình muốn cái #post nó sẽ nằm bên trái của `#sidebar`, nên mình sẽ gắn thêm cho `#post` một thuộc tính float với giá trị là `left`.

```sh
float: left;
```

Đồng thời, mình muốn `#sidebar` sẽ nhảy qua bên phải nên mình sẽ có thuộc tính `float` cho nó với giá trị là `right`.

```sh
float: right;
```

**Clear float**

Khi chúng ta sử dụng thuộc tính float thì nghĩa là sẽ thiết lập cho một phần tử được đẩy sang trái hoặc phải và cho phép các phần tử gần đó có thể hiển thị bao bọc xung quanh nó.

Do vậy khi tiến hành float các phần tử, việc bạn nên làm là phải tạo ra điểm kết thúc cho việc float này, tức là bạn sẽ muốn nó bắt đầu không float ở đâu nữa. Gọi theo thuật ngữ CSS là clear float.

Về clear float thì có rất nhiều cách, tùy theo trường hợp mà chúng ta sẽ sử dụng cách phù hợp.

*Cách 1: Sử dụng thẻ div trống*

Cách này khá phổ biến từ rất lâu rồi, đó là chúng ta sẽ tạo ra một class riêng cho việc clear float và khai báo thêm một thẻ `<div>`` nữa với class này rồi đặt nó bên dưới của cột cuối cùng.

Bây giờ mình sẽ viết một đoạn CSS cho class tên là `.clear` như sau:

```sh
.clear {clear:both}
```

Thuộc tính clear này nghĩa là thiết lập không cho phép các phần tử khác float xuống nó, nó có các giá trị là `left` `right` `both` và `none`. Và bạn chỉ nên dùng giá trị both thôi để clear cả 2 bên.

Bây giờ, mình sẽ khai báo một thẻ `<div>` với class là clear và đặt nó ngay bên dưới cái cột `#sidebar` (cột cuối cùng của hàng).

```sh
<div id="content" class="container">
 
   <div id="post">Nội dung của #post</div>
   <div id="sidebar">Nội dung của #sidebar</div>
   <div class="clear"></div>
 
</div>
```

*Cách 2: Sử dụng overflow*

Cách này thì gọn lẹ hơn, không cần sửa HTML mà chỉ cần viết thêm `overflow: auto;` cho container là được.

####2.12. Reset CSS là gì?<a name="14"></a>

Khi viết CSS cho website, bạn nên đưa tất cả các giá trị của các phần tử trên website về bằng 0 hết và xóa một số định dạng có sẵn để khi cần chúng ta sẽ dùng CSS viết lại theo ý của mình để đảm bảo nó hiển thị tốt trên tất cả các trình duyệt. Việc làm này người ta gọi là Reset CSS.

Nếu bạn muốn tự reset CSS đơn giản nhất thì hãy viết đoạn sau vào tập tin CSS là có thể đưa toàn bộ giá trị liên quan tới Box Model về 0.

```sh
* {
 
padding: 0;
 
margin: 0;
 
border: none;
 
}
```

Nhưng như vậy có vẻ không tối ưu cho lắm, thay vì reset CSS như vậy thì chúng ta sẽ dùng các bộ Reset CSS có sẵn mà nhiều designer/developer chuyên nghiệp thường sử dụng.

**Một số bộ Reset CSS thông dụng**

Bạn có thể sử dụng các bộ reset CSS thông dụng dưới đây để tiết kiệm thời gian và tối ưu hơn. Cách sử dụng là copy code bỏ vào đầu file CSS của bạn.

[normalize.css](https://github.com/necolas/normalize.css/blob/master/normalize.css)

Đây là bộ reset CSS thông dụng nhất hiện tại, phù hợp với cả HTML5 và CSS3. Đặc điểm của bộ này là sẽ điều chỉnh các phần tử trong website hiển thị phù hợp với tất cả các trình duyệt thông dụng, xóa bỏ toàn bộ margin và padding mặc định, có sẵn style cho các thẻ khá có ích như <sub>, <sup>, <code>,….Bạn có thể xem thêm các lý do nên sử dụng normalize.css tại [http://stackoverflow.com/a/8357635](http://stackoverflow.com/a/8357635).

[Reset CSS 2.0 by Eric Meyer](http://meyerweb.com/eric/tools/css/reset/)

Nếu bạn cần một đoạn reset CSS đưa toàn bộ các phần tử website về “thời đồ đá”, không có bất cứ một định dạng gì thì có thể sử dụng bộ này. Bộ reset CSS này thích hợp cho những ai muốn tự mình viết lại CSS cho toàn bộ các thành phần trong website, kể cả việc thiết lập kích thước chữ cho các thẻ tiêu đề.

####2.15. Trang trí danh sách với list-style<a name="17"></a>

Mặc định các thẻ list (danh sách) trong HTML sẽ được hiển thị dựa trên quy tắt hiển thị ở các trình duyệt cho các thẻ đó. Ví dụ khi bạn sử dụng `<ol>` thì sẽ hiển thị danh sách có đánh số, thẻ `<ul>` sẽ hiển thị dấu chấm tròn cho mỗi mục con bên trong. Nhưng với CSS, bạn có thể tùy biến lại được cách hiển thị của nó, chẳng hạn như bạn muốn dùng hình ảnh thay cho dấu chấm tròn ở thẻ `<ul>` chẳng hạn.

Và để tùy biến danh sách trong CSS, chúng ta sẽ sử dụng thuộc tính list-style để làm.

**Quy tắc viết thuộc tính list-style**

Ở thuộc tính này, bạn có thể viết giá trị theo thứ tự như sau:

```sh
list-style: <list-style-type> <list-style-position> <list-style-image>;
```

 + `list-style-type`: Thay đổi loại hiển thị của danh sách.
 + `list-style-position`: Tùy chỉnh vị trí hiển thị các dấu đầu dòng của mục con nằm bên trong danh sách hoặc bên ngoài danh sách.
 + `list-style-image`: Sử dụng hình ảnh làm các dấu đầu dòng cho danh sách.

####2.16. Thuộc tính display<a name="18"></a>

Làm thế nào để chuyển một phần tử inline sang block và ngược lại? Giải pháp trong CSS đó là sẽ sử dụng thuộc tính `display`.

Thuộc tính `display` có một số giá trị cơ bản như:

 + `inline`: Chuyển phần tử về hiển thị trên cùng một hàng.
 + `inline-block`: Chuyển phần tử về hiển thị trên cùng một hàng nhưng nó vẫn thừa hưởng các đặc tính của block như có thể tùy chỉnh kích thước, thêm background,…
 + `block`: Chuyển phần tử về hiển thị kiểu block, sở hữu một hàng riêng.
 + `list-item`: Chuyển phần tử về hiển thị như một mục danh sách, để có thể sử dụng thuộc tính list-style.
 + `none`: Đơn giản là ẩn phần tử đó đi không cho hiển thị nữa, nó cũng sẽ ẩn luôn toàn bộ các khoảng trống mà nó sở hữu. Nếu bạn muốn ẩn đi mà vẫn đề lại “dấu vết” thì có thể sử dụng visibility: hidden.

<img src="http://i.imgur.com/P46Ts08.png">

<img src="http://i.imgur.com/UA8u8Kc.png">

####2.17. Thuộc tính position<a name="19"></a>

Nếu như bạn muốn di chuyển một phần tử nào đó mà không ảnh hưởng đến bố cục của website thì sẽ có một giải pháp đó là sử dụng thuộc tính `position`. Cái tên nói lên tất cả, `position` là thuộc tính giúp bạn tùy chỉnh khu vực hiển thị cho phần tử và việc tùy chỉnh này không hề làm ảnh hưởng đến các phần tử khác.

**Các giá trị của thuộc tính position**

Hiện tại position hỗ trợ cho một số giá trị như sau:

 + `relative`: Dùng để thiết lập một phần tử sử dụng các thuộc tính position mà không làm ảnh hưởng đến việc hiển thị ban đầu.
 + `absolute`: Dùng để thiết lập vị trí của một phần tử nhưng nó sẽ luôn nằm trong một phần tử mẹ đang là relative.
 + `fixed`: Hiển thị luôn đi theo trình duyệt khi cuộn trang.
 + `static`: Đưa phần tử về hiển thị theo kiểu mặc định.

Sau khi thiết lập một phần tử sử dụng position, chúng ta sẽ sử dụng thêm một số thuộc tính position để căn chỉnh vị trí của nó và giá trị là số kèm theo đơn vị, có 4 thuộc tính position là:

 + `top`: Căn vị trí hiển thị của phần tử theo hướng từ trên xuống dưới. Giá trị càng cao thì phần tử càng thụt xuống dưới.
 + `bottom`: Căn vị trí hiển thị của phần tử theo hướng từ dưới lên trên. Giá trị càng cao thì phần tử càng hiển thị lên cao.
 + `left`: Căn vị trí hiển thị từ trái sang phải. Giá trị càng cao thì phần tử sẽ càng thụt về bên phải.
 + `right`: Căn vị trí hiển thị từ phải sang trái. Giá trị càng cao thì phần tử sẽ càng thụ về bên trái.

####2.18. Pseudo-classes cơ bản<a name="20"></a>

**Pseudo Class trong CSS là gì?**

Pseudo Class trong CSS được sử dụng để viết CSS cho một trạng thái nào đó của một phần tử. Ví dụ viết CSS đổi màu các liên kết khi rê chuột vào, đổi thuộc tính một phần tử khi nhấp vào,….Các pseudo class được khai báo tại vùng chọn, đặt đằng sau vùng chọn và có dấu hai chấm (:) ngăn cách. Ví dụ: `#link:hover` (vùng chọn của #link khi rê chuột vào).

<img src="http://i.imgur.com/TVZpReZ.png">

<img src="http://i.imgur.com/gkPHTFh.png">

####2.19. Cách làm menu ngang dropdown cơ bản<a name="21"></a>

**Cách tạo menu ngang cơ bản**

Để tạo menu ngang, chúng ta sẽ sử dụng thẻ `<ul>` để tạo khu vực menu và `<li>` để tạo từng mục trong menu đó. Do vậy, trước tiên chúng ta có đoạn cấu trúc menu bằng HTML như sau, mình sẽ đặt menu vào trong một cái thẻ `<div>` với id là `#menu`.

```sh
<div id="menu">
  <ul>
    <li><a href="#">Trang chủ</a></li>
    <li><a href="#">Diễn đàn</a></li>
    <li><a href="#">Tin tức</a></li>
    <li><a href="#">Hỏi đáp</a></li>
    <li><a href="#">Liên hệ</a></li>
  </ul>
</div>
```

Kế tiếp là ta có thêm một đoạn CSS sau để reset CSS cho dễ viết CSS về sau, và thêm một số style cho toàn trang web như dùng font chữ có chân chẳng hạn.

```sh
/*==Reset CSS==*/
* {
  margin: 0;
  padding: 0;
}
 
/*==Style cơ bản cho website==*/
body {
  font-family: sans-serif;
  color: #333;
}
```

Bây giờ chúng ta sẽ tiến hành xử lý cái menu.

Trước tiên là phần bao bọc menu (tức là thẻ `<ul>` trong `#menu`), chúng ta sẽ sử dụng thuộc tính `list-style-type` để xóa các dấu đầu dòng, thêm màu nền và đưa văn bản bên trong ra giữa.

```sh
/*==Style cho menu===*/
#menu ul {
  background: #1F568B;
  list-style-type: none;
  text-align: center;
}
```

<img src="http://i.imgur.com/siqQxqL.png">

Kế tiếp, chúng ta sẽ muốn cho các mục con nằm dàng ngang nên sẽ dùng gì nè? Vâng, bạn có thể sử dụng float: left cho tất cả thẻ `<li>` hoặc đưa về kiểu hiển thị `inline-block`.

*Cách 1: Kiểu inline-block*

```sh
#menu li {
  color: #f1f1f1;
  display: inline-block;
  width: 120px;
  height: 40px;
  line-height: 40px;
  margin-left: -5px;
}
```

*Cách 2: Kiểu float*

```sh
#menu li {
  color: #f1f1f1;
  float: left;
  width: 120px;
  height: 40px;
  line-height: 40px;
}
```

Sở dĩ kiểu float mình không có `margin-left: -5px` là vì cái 5px kia là kiểu `display`: inline-block nó tự sinh ra nên phải xóa nó đi bằng cách này.

Nếu float thì nên thêm một vài thuộc tính như sau cho `#menu ul`.

```sh
#menu ul {
  background: #1F568B;
  list-style-type: none;
  overflow: hidden;
  width: 100%;
}
```

<img src="http://i.imgur.com/EnOzEIK.png">

Và cuối cùng là thêm style cho các thẻ `<a>` bên trong, quan trọng nhất là sẽ đưa kiểu hiển thị cho các thẻ này thành block để nó được phủ kín cái `#menu ul`.
```sh
#menu a {
  text-decoration: none;
  color: #fff;
  display: block;
}
#menu a:hover {
  background: #F1F1F1;
  color: #333;
}
```

Kết quả khi hoàn thành:

<img src="http://i.imgur.com/U22M04R.png">

**Cách tạo menu dropdown đơn giản**

Bây giờ ta cũng có một menu giống như cái ở trên, nhưng mình muốn ở phần Tin tức sẽ có thêm một vài menu con nữa, như vậy mình sẽ đặt thêm một thẻ `<ul>` lồng bên trong item Tin tức và thẻ `<ul>` này sẽ mang class `sub-menu` để sau này dễ tái sử dụng.

```sh
<div id="menu">
  <ul>
    <li><a href="#">Trang chủ</a></li>
    <li><a href="#">Diễn đàn</a></li>
    <li><a href="#">Tin tức</a>
      <ul class="sub-menu">
        <li><a href="#">WordPress</a></li>
        <li><a href="#"><a href="https://thachpham.com/category/seo" data-wpel-link="internal">SEO</a></a></li>
        <li><a href="#">Hosting</a></li>
      </ul>
    </li>
    <li><a href="#">Hỏi đáp</a></li>
    <li><a href="#">Liên hệ</a></li>
  </ul>
</div>
```

Và đoạn CSS y hệt bên trên để làm cái menu đơn giản trước.

```sh
/*==Reset CSS==*/
* {
  margin: 0;
  padding: 0;
}
 
/*==Style cơ bản cho website==*/
body {
  font-family: sans-serif;
  color: #333;
}
 
/*==Style cho menu===*/
#menu ul {
  background: #1F568B;
  list-style-type: none;
  text-align: center;
}
#menu li {
  color: #f1f1f1;
  display: inline-block;
  width: 120px;
  height: 40px;
  line-height: 40px;
  margin-left: -5px;
}
#menu a {
  text-decoration: none;
  color: #fff;
  display: block;
}
#menu a:hover {
  background: #F1F1F1;
  color: #333;
}
```

<img src="http://i.imgur.com/2El9ONm.png">

Trước tiên, chúng ta cần phải cho `.sub-menu` ẩn đi.

```sh
/*==Dropdown Menu==*/
.sub-menu li {
  display: none;
}
```

Bây giờ, chúng ta muốn tùy biến lại cái `.sub-menu` sẽ hiển thị (nếu có hiển thị) nằm bên ngoài cái phần `#menu ul` để nó không bị đẩy lên như vậy. Như bài trước ta đã học rồi, để tùy biến vị trí một phần tử mà không ảnh hưởng đến các phần tử khác thì sẽ sử dụng thuộc tính `position`. Nhưng mà chúng ta muốn cái `.sub-menu` nó phải nằm gần menu mẹ, vậy thì chúng ta phải thiết lập `#menu li` thành kiểu `relative` vì `#menu li` là các item cấp lớn nhất, mình gọi đó là menu mẹ.

```sh
#menu li {
 position: relative;
}
```

Và tiếp theo là cho cái `.sub-menu` thành kiểu `absolute` để nó luôn luôn nằm trong phạm vi menu mẹ, tức là nằm trong `#menu li` ấy. Chúng ta viết lại đoạn `.sub-menu` như sau:

```sh
.sub-menu {
 display: none;
 position: absolute;
}
```

Và cuối cùng, là chúng ta sẽ cho thằng `.sub-menu` sẽ hiển thị ra khi ta rê chuột vào menu mẹ, như vậy ta sẽ kết hợp với một pseudo-class là `:hover` để làm việc này. Để hiển thị ra chúng ta gán `display: block` cho nó.

```sh
#menu li:hover .sub-menu {
 display: block;
}
```

Đoạn `#menu li:hover .sub-menu` nghĩa là khi chúng ta rê chuột vào `#menu li` thì nó sẽ thực hiện các thay đổi cho `.sub-menu`.

Thêm một chút CSS cho cái menu con bên trong để nó xóa cái margin không cần thiết đi.

```sh
.sub-menu li {
 margin-left: 0 !important;
}
```

<img src="http://i.imgur.com/NfY6jCv.png">

####2.20. Làm menu dọc có dropdown đơn giản<a name="22"></a>

Về cách tạo menu dọc thì chúng ta có thể làm giống như tạo menu ngang, đó là tạo một cái danh sách với `<ul>` rồi xóa `list-style-type` cho các thẻ `<li>` bên trong là được chứ không cần làm nhiều bước như khi làm menu ngang.

**Tạo menu dọc cơ bản**

Ban đầu mình sẽ có một danh sách menu như sau:

```sh
<div id="menu">
 <ul>
 <li><a href="#">Trang chủ</a></li>
 <li><a href="#">Tin tức</a></li>
 <li><a href="#">Sản phẩm</a></li>
 <li><a href="#">Liên hệ</a></li>
 </ul>
</div
```

Trước tiên là thêm CSS cho `#menu ul` để thêm màu nền này nọ một xíu cho đẹp, và nhất là bỏ đi mấy cái dấu chấm đầu dòng của danh sách..

```sh
#menu ul {
  background: #8AD385;
  width: 250px;
  padding: 0;
  list-style-type: none;
  text-align: left;
}
```

Sau đó viết CSS cho các thẻ `<li>` để thêm chiều cao cho nó với `height` và thêm `line-height` bằng với chiều cao để nó đứng giữa block.

```sh
#menu li {
  width: auto;
  height: 40px;
  line-height: 40px;
  border-bottom: 1px solid #e8e8e8;
  padding: 0 1em;
}
```

Cuối cùng là viết CSS cho thẻ a bên trong menu, chuyển nó qua thành block và thêm các style cần thiết, đồng thời tạo thêm hiệu ứng background khác khi rê chuột vào mục menu.

```sh
#menu li a {
  text-decoration: none;
  color: #333;
  font-weight: bold;
  display: block;
}
#menu li:hover {
  background: #CDE2CD;
}
```

<img src="http://i.imgur.com/CtTBEkD.png">

**Tạo menu dọc có đổ xuống (dropdown)**

Bây giờ bạn hãy làm lại cái menu đơn giản phía trên và bổ sung các menu con vào như thế này:

```sh
<div id="menu">
  <ul>
    <li><a href="#">Trang chủ</a></li>
    <li><a href="#">Tin tức</a>
      <ul class="sub-menu">
        <li><a href="#">WordPress</a></li>
        <li><a href="#"><a href="https://thachpham.com/category/seo" data-wpel-link="internal">SEO</a></a></li>
        <li><a href="#">Hosting</a></li>
      </ul>
    </li>
    <li><a href="#">Sản phẩm</a></li>
    <li><a href="#">Liên hệ</a></li>
  </ul>
</div>
```

Bây giờ bạn có thể thấy các menu con trong mục Tin tức bị lỗi hiển thị, nên chúng ta sẽ viết thêm CSS cho nó như sau.

Trước tiên là bạn hãy đưa thằng `#menu` li về hiển thị kiểu `relative`.

```sh
#menu ul li {
 position: relative;
}
```

Và chuyển `#menu .sub-menu` (menu cấp 2) về dạng `absolute` rồi chỉnh vị trí hiển thị của nó thụt sang bên phải là 250px (bằng với chiều rộng menu), đồng thời đưa nó về sát mép top của phần tử mẹ.

```sh
#menu .sub-menu {
 position: absolute;
 left: 250px;
 top: 0;
}
```

<img src="http://i.imgur.com/xpZmkzE.png">

Bây giờ chỉ cần viết thêm CSS để `.sub-menu` ẩn đi và hiện ra khi rê chuột vào `#menu li` có chứa `.sub-menu` nhé.

```sh
#menu .sub-menu {
 position: absolute;
 left: 250px;
 top: 0;
 display: none;
}
#menu li:hover .sub-menu {
 display: block;
}
```

<img src="http://i.imgur.com/7lioE1S.png">

####2.21. Thiết kế giao diện đơn giản<a name="23"></a>

Dưới đây là bài ví dụ mẫu:

**Tài nguyên**

Trước khi bắt đầu làm theo các hướng dẫn này thì bạn hãy tải về một số tài nguyên cần thiết dưới đây, nó bao gồm 4 bức ảnh và file normalize.css để reset CSS.

[Tải starter resources](https://thachpham.com/wp-content/uploads/2015/04/hoc-css-basic-layout-starter-resources.zip)

**Bắt đầu**

Bây giờ bạn hãy tạo một thư mục riêng và copy file `normalize.css` và thư mục img vào. Sau đó tạo thêm file `index.html` (tập tin website) và `style.css` (chứa các CSS của website).

Bây giờ hãy mở file `index.html` lên và bắt đầu viết HTML cho website nhé.

Việc trước tiên bạn cần viết là hãy viết các thẻ đầu tiên nhất của website bằng HTML là khai báo loại tập tin, thẻ `<html>`, cặp `<head>` và cặp `<body>`.

```sh
<!DOCTYPE html>
<html lang="vi">
 <head>
 
 </head>
 <body>
 
 </body>
</html>
```

**Thêm thẻ khia báo thông tin**

Như chúng ta đã học ở phần đầu rồi, chúng ta sẽ có các thẻ sau để khai báo thông tin cho tài liệu HTML tropng cặp thẻ `<head>`.

```sh
<head>
<meta charset="utf-8" />
<title>Thach Pham Blog</title>
<meta name="description" content="Thực hành tạo layout bằng HTML và CSS cơ bản" />
<meta name="author" content="ThachPham" />
<meta name="keyword" content="hoc css,css co ban,css layout" />
<link type="text/css" rel="stylesheet" href="style.css" />
<link type="text/css" rel="stylesheet" href="normalize.css" />
</head>
```

**Tạo khu vực trong website**

```sh
<body>
        <div id="container">
 
                <div id="menu">
 
                </div><!--#menu-->
 
                <div id="content">
 
                        <div id="header">
                                <div id="logo"></div>
                                <div id="slogan"></div>
                        </div><!--#header-->
 
                        <div class="call-to-action">
 
                        </div><!--.call-to-action-->
 
                        <div class="row">
                                <div id="box1" class="col"></div>
                                <div id="box2" class="col"></div>
                                <div id="box3" class="col"></div>
                        </div>
 
                </div><!--#content-->
 
                <div id="footer">
 
                </div><!--#footer-->
 
        </div><!--#container-->
</body>
```

**Viết nội dung cho từng phần**

*Phần menu*

```sh
<div id="menu">
  <ul>
    <li><a href="#">Trang chủ</a></li>
    <li><a href="#">Dịch vụ</a></li>
    <li><a href="#">Sản phẩm</a></li>
    <li><a href="#">Tin tức</a></li>
    <li><a href="#">Diễn đàn</a></li>
    <li><a href="#">Liên hệ</a></li>
  </ul>
</div><!--END #menu-->
```

*Phần header*

```sh
<div id="header">
  <div id="logo"><img src="img/tplogo2014.png" /></div>
  <div id="slogan"><h3><a href="https://thachpham.com/series/html-co-ban" data-wpel-link="internal">Học HTML</a> và CSS cơ bản miễn phí</h3></div>
</div><!--#header-->
```

*Phần .call-to-action*

```sh
<div class="call-to-action">
 <h3>Bạn sẽ được học những gì?</h3>
 
 <p>Nếu bạn là người mới tìm hiểu về website thì serie này sẽ giúp các bạn hình dung rõ hơn việc làm một giao diện website tĩnh bằng HTML và CSS vì tất cả giao diện website đều sử dụng HTML & CSS để lên bố cục cho giao diện, giúp bạn tự làm một giao diện website cho riêng mình.</p>
</div><!--.call-to-action-->
```

*Phần row*

```sh
<div class="row">
  <div id="box1" class="col">
    <h2>Lorem ipsum dolor sit amet</h2>
    <img src="img/css-icon.png" alt="CSS" />
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed non dui sodales, faucibus libero ut, posuere felis. Donec imperdiet suscipit accumsan. Aenean consequat condimentum velit ut tempor. Nam porta massa in metus bibendum congue. Pellentesque ultrices vestibulum mattis. Aliquam egestas nunc at ullamcorper ultricies. Donec feugiat velit nulla, vel sodales est ullamcorper id.</p>
  </div>
  <div id="box2" class="col">
    <h2>Lorem ipsum dolor sit amet</h2>
    <img src="img/url-icon.png" alt="URL" />
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed non dui sodales, faucibus libero ut, posuere felis. Donec imperdiet suscipit accumsan. Aenean consequat condimentum velit ut tempor. Nam porta massa in metus bibendum congue. Pellentesque ultrices vestibulum mattis. Aliquam egestas nunc at ullamcorper ultricies. Donec feugiat velit nulla, vel sodales est ullamcorper id.</p>
  </div>
  <div id="box3" class="col">
    <h2>Lorem ipsum dolor sit amet</h2>
    <img src="img/html-icon.png" alt="HTML" />
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed non dui sodales, faucibus libero ut, posuere felis. Donec imperdiet suscipit accumsan. Aenean consequat condimentum velit ut tempor. Nam porta massa in metus bibendum congue. Pellentesque ultrices vestibulum mattis. Aliquam egestas nunc at ullamcorper ultricies. Donec feugiat velit nulla, vel sodales est ullamcorper id.</p>
  </div>
</div><!--.call-to-action-->
```

*Phần footer*

```sh
<div id="footer">
  <p>Copyright &copy; 2015 - Serie học HTML & CSS cơ bản tại www.thachpham.com.</p>
</div><!--#footer-->
```

**Viết CSS cho giao diện**

```sh
/*==Style cơ bản cho website==*/
* {
 box-sizing: border-box;
 -webkit-box-sizing: border-box;
 -moz-box-sizing: border-box;
}
body {
 font-family: Helvetica,Arial,sans-serif;
 font-size: 16px;
 line-height: 1.254em;
 margin: 0;
 padding: 0;
}
a {
 text-decoration: none;
 color: #3B8BBA;
}
a:hover,
a:visited {
 color: #265778;
}
```

**Chia khung cho website**

```sh
/*==Lên khung cho website==*/
#container {
 padding-left: 150px;
 position: relative;
 left: 0;
 width: 100%;
}
#menu {
 position: fixed;
 height: 100%;
 background-color: #191818;
 width: 150px;
 left: 0;
}
```

**Viết CSS cho menu**

```sh
/*==Trang trí menu==*/
#menu ul {
 list-style-type: none;
 padding: 0;
 margin: 0;
}
```

Và thêm chiều cao cho từng mục bên trong menu.

```sh
#menu ul li {
 line-height: 2.9em;
 height: 2.9em;
}
```

Tiếp đến là chuyển các thẻ liên kết về dạng block, thêm màu chữ và các style linh tinh.

```sh
#menu li a {
 display: block;
 color: #fff;
 padding: 0 1em;
 border-bottom: 1px solid #333;
}
```

Cuối cùng là thêm style khi rê chuột vào từng menu.

```sh
#menu li:hover {
 background-color: #454545;
}
```

**Viết CSS chung cho content**

```sh
/*==Trang trí khung content==*/
#content {
 padding: 1em 8em;
}
#header,
.call-to-action {
 text-align: center;
}
```

Thêm màu chữ.

```sh
/*==Trang trí header của content==*/
#header{}
#slogan {
 color: #8997A0;
 font-size: 0.8em;
}
```

Tiếp theo là phần `.call-to-action`, mình sẽ thêm màu nền cho nó và cho một cái viền để nó nổi bật.

```sh
/*==Call to Action==*/
.call-to-action {
 padding: 1.5em 20%;
 background: #EFEFEF;
 border: 1px solid#E8E8E8;
}
```

```sh
/*==Chia cột phần content==*/
.row {
 overflow: auto;
 margin: 1.5em auto;
}
.row .col {
 float: left;
 width: 31.3333%;
 margin-right: 2.99%;
}
.row .col:last-child {
 float: right;
 margin-right: 0;
}
```

**Viết CSS cho footer**

```sh
/*==Footer==*/
#footer {
 font-size: 85%;
 border-top: 1px solid #E6E6E6;
 color: #838383;
 padding: 1em 3em;
}
```


####2.22. CSS Framework là gì và cách sử dụng<a name="24"></a>

**CSS Framework là gì?**

CSS Framework ra đời như một công cụ hỗ trợ các designer thiết kế giao diện website nhanh chóng và đẹp mắt với thời gian ngắn nhất nhưng ít lỗi nhất. CSS Framework là một bộ mã nguồn CSS đã được viết một số chức năng nhất định và khai báo mỗi chức năng đó vào một class riêng, để người sử dụng sẽ dễ dàng áp dụng nó vào dự án của họ bằng cách thêm class của thành phần muốn sử dụng vào phần tử họ cần áp dụng lên, ví dụ như thêm style cho một nút bấm chẳng hạn.

Hiện nay CSS thì có 2 loại chính đó là:

 + *Grid System*: Khi bạn muốn tự mình viết CSS cho các thành phần bên trong website và chỉ muốn có sẵn một framework hỗ trợ chia cột nhanh gọn. Ưu điểm là nhẹ vì không có nhiều CSS.
 + *CSS UI Framework*: Khi bạn muốn sử dụng framework như một công cụ hỗ trợ làm giao diện website từ A đến Z bao gồm có sẵn các CSS cho nút bấm, menu, form, chữ,….để bạn tập trung thời gian vào thiết kế layout tổng thể. Tuy nhiên các bộ UI này sẽ nặng hơn nhiều so với Grid System.

####2.23. Tạo chuyển động với Transition<a name="25"></a>

Cấu trúc khai báo `transition` như sau:

```sh
transition: [thuộc tính chuyển động] [thời gian chuyển động] [thời gian delay] [kiểu chuyển động];
```

Lưu ý rằng transition là thuộc tính CSS3 nên bạn cần nên khai báo thêm hai thuộc tính tương tự kèm hai tiền tố `-moz-` và `-webkit-` để nó hoạt động tốt trên mọi trình duyệt.

####2.24. Thay đổi hình dạng đối tượng với Transform<a name="26"></a>

Với transform, bạn có thể xoay, co giãn kích thước hoặc bóp nghiêng hình dạng một phần tử. Ngoài ra nó cũng còn một số tính năng khác cũng liên quan đến việc làm thay đổi hình dạng.

```sh
transform: function( value );
-moz-transform: function( value );
-webkit-transform: function( value );
```

Trong đó, `function()` là tên hàm làm thay đổi hình dạng và value là giá trị của hàm, mỗi hàm có thể sẽ có cách viết giá trị khác nhau.

**Xoay - `rotate()`**

Với hàm `rotate()` bạn có thể thiết lập một đối tượng bị xoay theo độ góc. Ở hàm này bạn có thể thiết lập giá trị kiểu `[n]deg` (thiết lập giá trị góc, tức là độ) hoặc `[n]turn` (1 turn = 360 độ). Bạn hãy xem ví dụ live dưới đây để hiểu hơn.

**Co giãn - `scale()`**

Với hàm `scale()` bạn có thể thiết lập co giãn kích thước của một phần tử dựa vào trục y (trục thẳng đứng) và trục x (trục ngang), và hàm này bạn sẽ thiết lập là `scale(X)` hoặc `scaleX()` và `scaleY()`.

**Kéo nghiêng - `skew()`**

Bạn có thể kéo một đối tượng nghiêng dựa theo trục Y và trục X với hàm `skewX()` và `skewY()`, giá trị bên trong là số `[n]deg` tương tự `rotate()`.

**Tùy chỉnh tâm hình dạng với transform-origin**

Một thuộc tính thú vị nữa mà bạn có thể dùng kèm theo transform đó là `transform-origin`, nó sẽ cho phép bạn dịch chuyển phần tử dựa vào kiểu thay đổi hình dạng ở transform. Nói nghe có vẻ khó hiểu, ví dụ bạn sử dụng `rotate()` để xoay ảnh và khi dùng thêm `transform-origin` thì nó sẽ cho phép bạn chỉnh độ lớn của vòng xoay tính từ tâm phần tử. Thuộc tính `transform-origin` phải được dùng kèm với `transform` và có thể áp dụng cho bất kỳ hàm nào.

Thuộc tính `transform-origin` có hai giá trị là X (phương thẳng đứng) và Y (phương nằm ngang) và giá trị nó sẽ dựa vào kích thước của phần tử.