##Task 3 & 4:
------------------------------
>Người thực hiện: Hồ Nguyễn Tường Vi
>
>Tên tài liệu:
 - [https://thachpham.com](https://thachpham.com)
 - [https://www.youtube.com](https://www.youtube.com)
>
>Ngày cập nhật: 01/03/2017
>
----------------------------------

##Mục lục:

[1. HTML là gì? Vai trò của HTML](#1)

[2. Soạn thảo văn bản HTML đầu tiên](#2)

[3. Tạo tài liệu web HTML](#3)

[4. Một số thẻ khai báo thông tin](#4)

[5. Các thẻ định dạng văn bản](#5)

[6. Ba thẻ tạo danh sách trong HTML](#6)

[7. Thẻ tạo liên kết](#7)

[8. Chèn hình ảnh, video, audio và website](#8)

[9. Tạo form nhập liệu](#9)

##Nội dung:

####1. HTML là gì? Vai trò của HTML<a name='1'></a>

<img src="http://i.imgur.com/qezbdFb.jpg">

HTML là chữ viết tắt của cụm từ **H**yper **T**ext **M**arkup **L**anguage (hay là *Ngôn ngữ đánh dấu siêu văn bản*) là một ngôn ngữ đánh dấu được thiết kế ra để tạo nên các trang web với các mẩu thông tin được trình bày trên World Wide Web. HTML được định nghĩa như là một ứng dụng đơn giản của SGML và được sử dụng trong các tổ chức cần đến các yêu cầu xuất bản phức tạp. HTML đã trở thành một chuẩn Internet do tổ chức World Wide Web Consortium (W3C) duy trì. Phiên bản chính thức mới nhất của HTML là HTML 4.01 (1999). Sau đó, các nhà phát triển đã thay thế nó bằng XHTML. Hiện nay, HTML đang được phát triển tiếp với phiên bản HTML5 hứa hẹn mang lại diện mạo mới cho Web.

Một tập tin HTML sẽ bao gồm các phần tử HTML và được lưu lại dưới đuôi mở rộng là .html hoặc .htm. Một đoạn HTML luôn luôn có thẻ mở và thẻ đóng.

*Mẹo*

>Nếu các bạn muốn tham khảo thêm về HTML, các bạn có thể truy cập vào trang [https://developer.mozilla.org/en-US/docs/Web/HTML](https://developer.mozilla.org/en-US/docs/Web/HTML) 

**Dùng chương trình gì để tạo tập tin HTML**

HTML là một tập tin siêu văn bản nên bạn có thể dùng các chương trình soạn thảo văn bản khong có chức năng định dạng văn bản để tạo ra một tập tin HTML. Trong window, bạn có thể dùng Notepad để tạo ra một tập tin HTML, còn trên MAC thì có thể dùng TextEdit và Vim trên các hệ điều hành Linux khác. Miễn là sau đó, bạn phải lưu tập tin thành đuôi .html và sử dụng trình duyệt website để đọc nó.

<img src="http://i.imgur.com/UaoQwXa.png">

Đối với Window, một trong các chương trình nổi bật nhất để soạn thảo html là Sublime Text, các bạn có thể download tại [đây](http://www.sublimetext.com/3)

**HTML đóng vai trò gì trong website?**

HTML là một ngôn ngữ đánh dấu siêu văn bản nên nó sẽ có vai trò xây dựng cấu trúc siêu văn bản trên một website, hoặc khai báo các tập tin kỹ thuật số (media) như hình ảnh, video, nhạc.

<img src="http://i.imgur.com/PhPpA92.png">

Điều đó không có nghĩa là chỉ sử dụng HTML để tạo ra một website mà HTML chỉ đóng một vai trò hình thành trên website. Ví dụ một website như [https://thachpham.com](https://thachpham.com) sẽ được hình thành bởi:

<li>HTML - Xây dựng cấu trúc và định dạng các siêu văn bản.</li>

<li>CSS - Định dạng các siêu văn bản dạng thô tạo ra từ HTML thành một bố cục website, có màu sắc, ảnh nền,...</li>

<li>Javascript - Tạo ra các sự kiện tương tác với hành vi của người dùng (ví dụ nhấp vào ảnh trên nó sẽ có hiệu ứng phóng to)</li>

<li>PHP - Ngôn ngữ lập trình để xử lý và trao đổi dữ liệu giữa máy chủ đến trình duyệt (ví dụ như các bài viết sẽ được lưu trong máy chủ)</li>

<li>MySQL - Hệ quản trị cơ sở dữ liệu truy vấn có cấu trúc (SQL - ví dụ như các bài viết sẽ được lưu lại với dạng dữ liệu SQL)</li>

<img src="http://i.imgur.com/R9AiexC.png">

Nhưng ở đây, bạn chỉ cần tạm thời quan tâm đến HTML mà thôi. Dễ hiểu hơn, bạn hãy nghĩ rằng nếu website là một cơ thể hoàn chỉnh thì HTML chính là bộ xương của cơ thể đó.

Như vậy, dù website thuộc thể loại nào, giao tiếp với ngôn ngữ lập trình nào để xử lý dữ liệu thì vẫn phải cần HTML để hiển thị nội dung ra cho người truy cập xem.

>Website có hai loại chính:
><li>*Website tĩnh(static web)* - Là một website không giao tiếp với máy chủ web để gửi nhận dữ liệu mà chỉ có các dữ liệu được khia báo sắn bằng HTML và trình duyệt đọc.</li>
>
><li>*Website động(dynamic web)* - Là một website sẽ giao tiế với một máy chủ để gửi nhận dữ liệu, các dữ liệu đó sẽ gửi ra ngoài cho người dùng bằng avwn bản HTML và trình duyệt sẽ hiển thị nó. Để một website có thể giao tiếp với máy chủ web thì sẽ dùng một số ngôn ngữ lập trifng dạng server side như PHP, ASP.NET, Ruby,... để thực hiện. Ví dụ như một website làm bằng WordPress là một website động.</li>

####2. Soạn thảo HTML đầu tiên<a name="2"></a>

>Soạn thảo văn bản HTML ở đây nghĩa là chúng ta sẽ tập viết một đoạn văn bản được định dạng bằng các thẻ HTML chứ không phải là tạo ra một tập tin HTML hoàn chỉnh.

Để soạn thảo văn bản, đầu tiên bạn mở chương trình soạn thảo lên (Sublime Text 3) và gõ một đoạn nội dung đơn giản.

<img src="http://i.imgur.com/r6zOD7P.png">

<img src="http://i.imgur.com/8vFRVAL.png">

Sau đó hãy lưu lại tập tin này với tên text.html và mở lên bằng trình duyệt, kết quả sẽ như thế này:

<img src ="http://i.imgur.com/3jPriGx.png">

Chúng ta có thể thấy rằng văn bản chúng ta soạn ra có xuống hàng đầy đủ mà khi in ra trình duyệt nó không xuống hàng, bởi vì các trình duyệt chỉ đọc hiểu các văn bản được định dạng bằng HTML, nên cho dù bạn soạn văn bản thông thường mà không có HTML thì trình duyệt vẫn sẽ hiểu rằng đó là một văn bản thô.

Bây giờ, chúng ta thử đặt cặp thẻ `<h1></h1>` để thiết lập tiêu đề cho văn bản, và đặt các văn bản nhỏ vào cặp thẻ `<p></p>` như thế này.

<img src="http://i.imgur.com/wyE0CVn.png">

Lưu lại và tải lại bằng trình duyệt website sẽ thấy một kết quả khác.

<img src="http://i.imgur.com/8eoX6VI.png">

Ngoài thẻ `<h1></h1>`, chúng ta còn có các thẻ khác theo size giảm dần như:

```sh
<h2></h2>
<h3></h3>
<h4></h4>
<h5></h5>
<h6></h6>
```

####3. Tạo tài liệu web HTML<a name="3"></a>

**Thẻ khai báo loại tập tin**

Ngay tại đoạn đầu tiên của tài liệu, chúng ta phải có một thẻ khai báo loại tập tin, ta se khai báo rằng đây là tập tin HTML.

```sh
<!DOCTYPE html>
```

Với thẻ <!DOCTYPE>, ta có thêm một tham số đó là html. Tham số này nghĩa là chúng ta khai báo với trình duyệt rằng đây là tài liệu HTML5, dù chúng ta có thể không sử dụng HTML5 nhưng hiện tại khi khai báo tập tin HTML thì bạn cứ sử dụng tham số này vừa ngắn gọn lại vừa dễ dàng sử dụng them HTML5 nếu thích.

Thẻ <!DOCTYPE> không phải là một thẻ của HTML, mà nó chỉ là một thẻ khai báo thông tin trên tài liệu để trình duyệt hiểu phiên bản HTML mà bạn đang dùng.

**Thẻ đóng mở tài liệu HTML**

Tiếp theo sẽ là thẻ `<html></html>` có nhiệm vụ khai báo cho trình duyệt biết rằng những nội dung bên trong cặp thẻ này là HTML.

Bên trong thẻ này mình sẽ thêm một thuộc tính tên là **lang** với giá trị là **vi**:

```sh
<html lang="vi">
```

Thuộc tính này nghĩa là chúng ta khai báo cho trình duyệt biết mã ngôn ngữ mà ta sử dụng trên website, mã **vi** nghĩa là Tiếng Việt, bạn có thể tham khảo các mã ngôn ngữ khác tại [đây](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes)

**Thẻ đóng và mở phần thông tin website**

Phần khai báo thông tin của website sẽ được đặt vào bên trong cặp thẻ `<head></head>`. Nội dung bên trong thẻ này là các thẻ chuyên khai báo thông tin website (meta), tên website (title), khai báo CSS (style), khia báo các đoạn Javascript (script) và một số thông tin khác. Thường các thông tin này sẽ không hiển thị thành siêu văn bản nhưng nó sẽ có nhiệm vụ chứa các thông tin về website.

**Thẻ đóng và mở phần nội dung website**

`<body></body>` là cặp thẻ để ta tiến hành viết nội dung vào đó. Đây là cặp thẻ để xác định phần thân của website, nó sẽ chứa toàn bộ các nội dung siêu văn bản hoặc media mà bạn muốn nó hiển thị lên trang web của bạn.

<img src="http://i.imgur.com/mkZCh2s.png">

<img src="http://i.imgur.com/ByZX5RY.png">

####4. Một số thẻ khai báo thông tin<a name="4"></a>

Ở đây chúng ta sẽ tìm hiểu các thẻ khai báo thông tin trong cặp thẻ `<head></head>`.

**Khai báo tên tài liệu với cặp thẻ title**

Cặp thẻ `<title></title>` có tác dụng khai báo tên tài liệu web của bạn đang soạn. Giúp trình duyệt hiển thị tên tài liệu khi mở và các cỗ máy tìm kiếm hiển thị nội dung  trong cặp thẻ này để lấy tài liệu.

<img src="http://i.imgur.com/Yp81IiH.png">

**Khai báo dữ liệu vĩ mô với thẻ <meta>**

Thẻ `<meta>` là thẻ đặc biệt vì nó không có thẻ đóng như các thẻ khác mà sẽ có dấu gạch chéo `/` ở trước ký tự `>` cuối cùng. Thẻ này có mục đích khai báo các dữ liệu vĩ mô trong tài liệu web HTML của bạn như mô tả, từ khóa, tên tác giả, bảng mã ký tự sử dụng,...

Thẻ meta luôn được khai báo kèm theo ít nhất là một thuojc tính và mỗi thuộc tính phải luôn có giá trị.

```sh
<meta charset="utf-8" />
```

**Thuộc tính Charset**

Thuộc tính này trong thẻ `<meta>` có nhiệm vụ khai báo cho trình duyệt biết bảng mã ký tự siêu văn bản bên trong tài liệu là gì. Hiện nay, hầu hết chúng ta đều sử dụng bảng mã UTF-8 cho tất cả ngôn ngữ.

**Thuộc tính Name**

Đối với thuộc tính naem thì thẻ meta của bạn phải có hai thuộc tính, đó là thuộc tính name và content, trong đó thuộc tính content được xem là thiết lập nội dung cho thuộc tính name.

```sh
<meta name="author" content="Tuong Vi" />
```

Trong đó, giá trị của thuộc tính name là một giá trị có sẵn vì hiện tại thuộc tính name hỗ trợ một số giá trị như:

<li>*author*: Khai báo tên tác giả tài liệu</li>

<li>*description*: Khai bao mô tả tài lêệu</li>

<li>*keyword*: Khai báo từ khóa của tài lêệu, các từ khóa này sẽ đóng vai trò hỗ trợ các trình tìm kiếm văn bản hoặc máy tìm kiếm website dò tìm</li>

Đó là các giá trị quan trọng thường dùng, ngoài ra còn một số giá trị khác như:

<li>*application-name*: Tên ứng dụng đại diện của tài liệu web</li>

<li>*generator*: Khai báo tên ứng dụng tạo ra tài liệu</li>

<img src="http://i.imgur.com/SgeT9hr.png">

####5. Các thẻ định dạng văn bản<a name="5"></a>

**Tiêu đề và đoạn văn bản**

Tiêu đề (Headline) và đoạn văn bản (Paragraph) là hai thành phần mà bạn cần phân biệt để sau này sử dụng cho đúng.

Trong HTML, các thẻ tiêu đề sẽ được định nghĩa bằng cặp thẻ `<hn>`, trong đó *n là số tự nhiên từ 1 đến 6* tương ứng với từng cấp độ, số càng nhỏ thì cấp độ càng lớn.

<img src="http://i.imgur.com/2d9iJzL.png">

<img src="http://i.imgur.com/qulmkOd.png">

Thẻ `<h1>` sẽ có kích thước lớn nhất và `<h6>` sẽ có kích thước nhỏ nhất.

Đoạn văn bản sẽ được khai báo băng cặp thẻ `<p></p>`. Các văn bản nằm trong thẻ này sẽ được hiểu là một đoạn văn bản, mỗi đoạn văn bản sẽ được xuống dòng và cách nhau với tỷ lệ nhất định.

<img src="http://i.imgur.com/RzoALi5.png">

<img src="http://i.imgur.com/Gvg7p7c.png">

**Các thẻ định dạng chữ viết**

 - *strong*: In đậm chữ viết
 - *i*: In nghiêng chữ viết
 - *u*: Gạch chân chữ viết
 - *strike*: Gạch ngang chữ viết
 - *em*: Nhấn mạnh câu
 - *code*: Định dạng cho một đoạn mã nào đó
 - *hr*: Thước kẻ ngang trên tài liệu
 - *mark*: Tô sáng chữ viết
 
 <img src="http://i.imgur.com/s2dRYEI.png">

 <img src="http://i.imgur.com/8Ml1P7e.png">

**Thẻ trích dẫn**

 Trích dẫn (Quote) là một thẻ có thể bạn sẽ thường sử dụng nếu thường xuyên viết báo cáo hay phóng sự, mục đích của nó là định dạng một câu nói như một câu trích dẫn và có thể định dạng thêm tên người trích dẫn một cách chuyên nghiệp hơn, thẻ trích dẫn được quy định là `<quote>` và tên tác giả trích dẫn được quy định là `<cite>`

 <img src="http://i.imgur.com/RtUrit3.png">

 <img src="http://i.imgur.com/j5p1qfY.png">

**Thẻ định dạng sẵn**

  Trong HTML hiện tại nó có một thẻ được gọi là thẻ định dạng sẵn (preformatted), thẻ này sẽ được viết là `<pre></pre>`. Sỡ dĩ nó được gọi là thẻ định dạng sẵn vì mặc định trình duyệt đã tự động định dạng cho các nội dung nằm bên trong thẻ đó như kích thước chữ, khaorng cách, kiểu chữ.

  Thẻ `<pre></pre>` thường được dùng để đăng một câu đối thoại hoặc in một đoạn mã để cho dễ phân biệt với các văn bản thông thường.

  <img src="http://i.imgur.com/n14GgNM.png">

  <img src="http://i.imgur.com/BpsjSWV.png">

**Thuộc tính style để định dạng chữ viết**

  Mặc dù việc lên màu sắc trên website là do CSS đảm nhận, nhưng nếu là một văn abrn HTML thông thường thì bạn vẫn có thể thêm màu sắc cho chữ viết bằng thuộc tính `style`. Thuộc tính `style` có thể đặt trong bất cứ thẻ nào và giá trị của thuộc tính đó là các thuộc tính của CSS.

  Cấu trúc viết thuộc tính sẽ là:

  ```sh
  <tên thẻ style="tên thuộc tính: giá trị">
  ```

**Màu chữ**
Để thiết lập màu chữ, bạn có thể sử dụng thuộc tính `color`. Giá trị của nó là tên màu trong tiếng anh hoặc [mã màu HEX](http://vforum.vn/diendan/showthread.php?61619-Bang-ma-mau-HEX-RGB-CMYK-day-du-cho-CSS-HTML)

```sh
<span style="color: red">chữ màu đỏ</span>
```

**Màu nền**

Màu nền có cách thiết lập giống màu chữ, tức là bạn có thể dùng giá trị của màu trong tiếng anh hoặc [mã màu HEX](http://vforum.vn/diendan/showthread.php?61619-Bang-ma-mau-HEX-RGB-CMYK-day-du-cho-CSS-HTML). Tên thuộc tính của màu nền là `background-color`

```sh
<span style="color: white; background-color:red">chữ trắng nền đỏ</span>
```

<img src="http://i.imgur.com/9rZjJh6.png">

<img src="http://i.imgur.com/TIEaVSe.png">

**Kích thước chữ**

Bạn có thể sử dụng thuộc tính `font-size` và giá trị là số kèm đơn vị. Bạn có thể sử dụng đơn vị `px`,`%`,`pt` hoặc `em` thùy thích, đơn giản nhất là dùng `px`

```sh
<span style="font-size: 32px">chữ có kích thước 32px</span>
```

**Font chữ**

Nếu bạn muốn sử dụng font chữ khác so với font chữ mặc định thì hãy dùng thuộc tính `font-family` với giá trị là tên font chữ có trên máy tính. Một số tên font chữ phổ biến nhất là Arial, Helvetica, Time New Roman, Verdana.

```sh
<span style="font-family: Arial">Font chữ Arial</span>
```

Ngoài ra bạn có thể thêm font chữ dự phòng băng cách khai báo nhiều tên font chữ khác nhau được ngăn cách bởi dấu phẩy.

```sh
<span style="font-family: Helvetica, Arial">Font chữ Arial</span>
```

Có nghĩa là nếu máy người đọc không có font chữ Helvetica thì nó sẽ sử dụng font chữ Arial.

**Căn lề văn bản**

Để căn lề, chúng ta sử dụng thuộc tính `text-align` với giá trị là `lefft`,`center`,`right` hoặc `justify`.

```sh
span style="text-align: center">Canh giữa văn bản</span>
```

####6. Ba thẻ tạo danh sách trong HTML<a name="6"></a>

Phần tử danh sách (list) được sử dụng rất thường xuyên trong một tài liệu web bằng HTML. Trong một trang web thường người ta sử dụng các phần tử danh sach rất nhiều, chẳng hạn như menu, danh sách thông tin nào đó,...đều được tạo ra bởi các thẻ tạo danh sách trong HTML.

Trong HTML có ba kiểu danh sách (list type) đó là kiểu sắp xếp (ordered list), kiểu không sắp xếp (unordered list) và kiểu danh sách mô tả (description list).

**Ordered List**

Để khai báo một danh sách với kiểu được sắp xếp, bạn phải bắt đầu bằng cặp thẻ `<ol></ol>`. Bên trong cặp thẻ này sẽ là danh sách như các mục con, mỗi mục sẽ đặt trong cặp thẻ `<li></li>`.

<img src="http://i.imgur.com/hQkV83L.png">

<img src="http://i.imgur.com/13lvPcq.png">

Thẻ `<ol>` cũng hỗ trợ thêm một thuộc tính nữa tên là `type`, thuộc tính này để bạn thiết lập kiểu sắp xếp các mục con bên trong danh sách. Giá trị của thuộc tính type là `1`,`i`,`I`,`a`,`A`.

**Unordered List**

Giống như Ordered List, kiểu danh sách Unordered List sẽ bắt đầu bằng cặp thẻ `<ul></ul>` và bên trong nó các mục con sẽ được khai báo băng cặp thẻ `<li></li>`.

<img src="http://i.imgur.com/qmDBYoU.png">

<img src="http://i.imgur.com/X8rJZeh.png">

Bạn cũng có thể thay đổi kiểu hiện thị của thẻ `<ol>` bằng cách thêm thuộc tính style với thuộc tính CSS là `list-style-type` và giá trị là `disc`,`square`,`circle`,`none`.

**Description List**

Với kiểu danh sách này thì cách viết hơi khác một tý, đó là nó sẽ bắt đầu danh sách băng cặp thẻ `<dl></dl>`, trong đó tên mỗi mục con sẽ được khai báo bằng cặp thẻ `<dl></dl>` và mô tả cho mục con sẽ được khai báo bằng cặp thẻ `<dd></dd>`.

<img src="http://i.imgur.com/OjjUbcd.png">

<img src="http://i.imgur.com/2Bjipud.png">

####7. Thẻ tạo liên kết<a name="7"></a>

Một trong những nét đặc trưng của siêu văn bản là có những đường liên kết (link) tới một tài liệu khác thông qua địa chỉ đường dẫn đến tài liệu hoặc địa chỉ website. Để tạo ra các đường liên kết trong HTML ta sẽ sử dụng cặp thẻ `<a></a>`

```sh
<a href="http://thachpham.com" title="Thach Pham Blog" target="_blank">nhấp vào đây</a>
```

<img src="http://i.imgur.com/BkRNe8h.png">

**Ý nghĩa các thuộc tính:

 - `href`: Địa chỉ của tài liệu muốn liên kết đến, đây có thể là một đường dẫn thư mục hoặc địa chỉ website. Nếu bạn muốn truy cập một tài liệu trên cùng một cấp thư mục thì chỉ cần ghi tên_tập_tin.định_dạng
 - `title`: Tiêu đề của liên kết, tiêu đề sẽ hiển thị như một thông tin thêm khi rê chuột vào liên kết.
 - `target`: Xác định nơi ơở tài liệu, nó có các giá trị như `_blank` (mở tài liệu trên cửa sổ mới), `_self` (mở tài liệu trên cửa sổ hiện tại, nếu bạn không khai báo thuộc tính `target` thì nó sẽ sử dụng giá trị này làm mặc định), `_top` (mở tài liệu trong nội dung trang hiện tại), `_parent` (mở tài liệu trên khung trình duyệt mẹ của nó).
 
 **Liên kết neo (Anchor Link)**

 Liên kết neo nghĩa là một liên kết trong siêu văn bản sẽ dẫn đến một vị trí đặc biệt trong cùng tài liệu mà không phải tải lại hoặc mở một tài liệu mới. Một liên kết neo sẽ có hai phần:

  - Khu vực được neo, được khai báo rằng thẻ bất kỳ với thuộc tính id (ví dụ: `<p id="noi_dung" </p>`).
  - Liên kết neo, được khai báo bằng thẻ `<a>` nhưng có thuộc tính là `href` nhưng giá trị là có dấu `#` và tên id khu vực cần truy cập đến (ví dụ: `<a href="#noi_dung">xem nội dung</a>`).

<img src="http://i.imgur.com/QehKtQC.png">

<img src="http://i.imgur.com/nGcO9CN.png">

####8. Chèn hình ảnh, video, audio và website<a name="8"></a>

Với HTMT chúng ta có thể dễ dàng chèn những loại tập tin kỹ thuật số vào tài liệu.

**Chèn hình ảnh vào HTML**

Để chèn hình ảnh vào HTML, chúng ta sử dụng thẻ `<img>` với các tham số bắt buộc, với thẻ này không có thẻ đóng.

```sh
<img src="Đường_link_ảnh" title="Tiêu_đề_ảnh" alt="Tên_định_danh_của_ảnh"
```

<img src="http://i.imgur.com/QoaiPdo.png">

<img src="http://i.imgur.com/8ecJzSg.png">

Ngoài ra chúng ta có thể sử dụng thêm thuộc tính `width` và `height` để điều chỉnh kích thước của ảnh.

Nếu bạn muốn upload ảnh lên Internet để lấy link trực tiếp thì có thể dùng [Imgur](https://imgur.com/)

**Chèn video**

Mạc dù hiện tại chưa học đến HTML5 nhưng ở chức năng chèn video này chúng ta sẽ sử dụng một thẻ trong HTML để chèn video nhanh chóng đó là cặp thẻ `<video></video`:

```sh
<video width="kích_cỡ_ngang" height="kích_cỡ_dọc" controls>

</video>
```

Trong cặp thẻ `<video></video>` sẽ có một thẻ `<source>` với các thuộc tính nhằm khai báo đường dẫn tập tin video và loại tập tin.

Để có thể đảm bảo tất cả các trình duyệt có thể đọc được, chỉ nên chèn video định dạng MP4

<img src="http://i.imgur.com/Vv2z9Ck.png">

<img src="http://i.imgur.com/ldsRRm9.png">

**Chèn âm thanh - nhạc**

Giống như thẻ `<video>`, để chèn âm thanh vào tài liệu HTML thì bạn có thể sử dụng thẻ `<audio>` và thẻ này cũng là HTML5.

<img src="http://i.imgur.com/UlcBmkQ.png">

<img src="http://i.imgur.com/aeb0dBR.png">

**Chèn đối tượng kỹ thuật với thẻ `<object>`**

Ngoài các thẻ đặc trưng cho từng loại tập tin ở trên thì bạn còn có một cách khác để chèn các đối tượng kỹ thuật số vào tài liệu HTML đó là dùng thẻ `<object>`, đây là một thẻ có thể giúp bạn chèn các loại đối tượng kỹ thuật số như Flash, Java, Audio, PDF, ActiveX. Nhưng thông thường thì các loại mã nhúng của một số website cho phép sử dụng mã nhúng như Youtube họ sẽ dùng thẻ này để chèn đối tượng vào web.

**Nhúng tài liệu HTML vào web**

Nếu bạn có nhu cầu nhúng thẳng một trang nào đó vào tài liệu HTML của bạn thì có thể sử dụng thẻ `<iframe>` như sau:

```sh
<iframe src="đường_dẫn_web" width="kích_cỡ_ngang" height="kích_cỡ_dọc" scrolling="auto"></iframe>
```

Thuộc tính `src` là đường dẫn của trang bạn muốn nhúng vào, `width` và `height` là kích thước của khung hiển thị.

Ngoài ra, còn một thuộc tính nữa để chèn một liên kết và ép nó mở bằng frame trên website đó là sử dụng thuộc tính `name` trong thẻ `<iframe>` và thuộc tính `target` trong thẻ `<a>`.

```sh
<p><a target="window" href="đường_dẫn_web_1">Truy cập</a></p>
<iframe src="đường_dẫn_web_2" name="window" width="kích_cỡ_ngang" height="kích_cỡ_dọc"></iframe>
```

####9. Tạo form nhập liệu<a name="9"></a>

Để tạo form, chúng ta sẽ sử dụng cặp thẻ `<form></form>`, thẻ này sẽ chứa một vài thuộc tính quan trọng và nội dung bên trong cặp thẻ đó là các thẻ `input` để khai báo các trường.

**Các thuộc tính trong thẻ `<form>`**

 - `action`: Đường dẫn đến một trang xử lý dữ liệu sau khi người dùng ấn nút gửi dữ liệu.
 - `method`: Phương thức gửi dữ liệu
 - `name`: Tên của form.

**Các thuộc tính trong thẻ `<input>`**

Các bạn có thể tham khảo tại [đây](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input)

<img src="http://i.imgur.com/iy6KGvj.png">
<img src="http://i.imgur.com/R7HTObx.png">























