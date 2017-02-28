##Task 3 & 4:
------------------------------
>Người thực hiện: Hồ Nguyễn Tường Vi
>
>Tên tài liệu:
 - [https://thachpham.com/web-development/html-css/html-la-gi-va-vi-sao-no-quan-trong.html](https://thachpham.com/web-development/html-css/html-la-gi-va-vi-sao-no-quan-trong.html)
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
> - *Website tĩnh(static web)* - Là một website không giao tiếp với máy chủ web để gửi nhận dữ liệu mà chỉ có các dữ liệu được khia báo sắn bằng HTML và trình duyệt đọc.
>
> - *Website động(dynamic web)* - Là một website sẽ giao tiế với một máy chủ để gửi nhận dữ liệu, các dữ liệu đó sẽ gửi ra ngoài cho người dùng bằng avwn bản HTML và trình duyệt sẽ hiển thị nó. Để một website có thể giao tiếp với máy chủ web thì sẽ dùng một số ngôn ngữ lập trifng dạng server side như PHP, ASP.NET, Ruby,... để thực hiện. Ví dụ như một website làm bằng WordPress là một website động.




**Các thẻ cơ bản trong HTML

HTML sẽ được khai báo bằng các phân tử bởi các từ khóa. Nội dung nằm bên trong cặp từ khóa sẽ là nội dung bạn cần định dạng với HTML. Ví dụ dưới đây là một đoạn HTML khai báo một đoạn văn bản.

`<p>Đây là một đoạn văn bản trong HTML.</p>`

**In đậm**

Chúng ta sử dụng thẻ sau:

`<strong>đoạn in đậm</strong>`

Kết quả là: **đoạn in đậm**

**In nghiêng**

Chúng ta sử dụng thẻ sau:

`<p>đoạn in nghiêng</p>`

Kết quả là: *đoạn in nghiêng*

Ngoài ra, trong các thẻ còn có các thuộc tính, và các thuộc tính luôn luôn có giá trị. Trong một thẻ có thẻ có nhiều thuộc tính.



