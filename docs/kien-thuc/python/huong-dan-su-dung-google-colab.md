---
date: 2023-11-23
title: Hướng dẫn sử dụng Google Colab toàn tập
description: Học cách sử dụng Google Colab hiệu quả thông qua hướng dẫn chi tiết và dễ hiểu.
tags:
  - code editor
  - google colab
  - chuyên sâu
categories:
  - Hướng dẫn
authors:
  - thinh-vu
---

## Google Colab là gì?

> _Google Colab là một dạng Jupyter Notebook tùy biến cho phép thực thi Python trên nền tảng đám mây, được cung cấp bởi Google. Sử dụng Google Colab có những lợi ích ưu việt như: sẵn sàng chạy Python ở bất kỳ thiết bị nào có kết nối internet mà không cần cài đặt, chia sẻ và làm việc nhóm dễ dàng, sử dụng miễn phí GPU cho các dự án về AI._

Ngoài những lợi ích được tóm tắt như trên, Google Colab còn cung cấp cho bạn trải nghiệm lập trình Python tuyệt vời với những nâng cấp cực kỳ hữu ích không có trong Jupyter Notebook, JupyterLab đơn thuần. Những tính năng tôi đánh giá cao ở Google Colab phải kể đến như:

- **Tạo mục lục dựa trên các Heading viết bằng ngôn ngữ markdown** giúp bạn dễ dàng cấu trúc Notebook làm việc của mình. Bạn cũng có thể Thu gọn (Collapse) hay Mở rộng (Expand) các phần nội dung khi soạn thảo cực kỳ tiện lợi. Tôi làm việc với Visual Studio Code, Jupyter Lab hay Jupyter Notebook đều cầu mong phải chi chúng có tính năng tương tự Google Colab. Tôi cũng đã sử dụng Google Colab để soạn thảo 1 giáo trình hoàn chỉnh có khả năng tương tác cao cho khoá học Python.
- **Thêm hình ảnh, biểu mẫu dễ dàng với markdown** giúp bạn trình bày báo cáo hoặc làm dashboard cực tiện lợi. Thậm chí bạn có thể ẩn các dòng code để trông Notebook gọn gàng hơn với tính năng biểu mẫu.
- **Kết nối dễ dàng với Google Drive, Google Sheets** để bắt tay vào phân tích dữ liệu “trên mây” hoàn toàn.
- **Chạy Python trên Cloud hay Local Runtime (Python trên máy tính cá nhân) của bạn đều cho trải nghiệm tốt**. Bạn vẫn tận dụng được tính năng tuyệt vời của Google Colab khi chạy với Python trên Local Runtime trong khi không bị Google tự động xóa dữ liệu khi kết thúc phiên làm việc như khi chạy trên Cloud.
- **Tự động lưu lịch sử chỉnh sửa thành các phiên bản giúp bạn dễ dàng khôi phục lại phiên bản gần nhất nếu cần khi bạn gặp lỗi**. Tính năng này tương tự như trên Google Sheets hay Google Docs, bạn thậm chí không cần đến Github để lưu trữ các phiên bản chỉnh sửa này.
- **Cho phép tìm kiếm và chèn các đoạn mã được soạn thảo sẵn trong các Template (bởi bạn) vào Notebook**. Tính năng này rất hay bởi bạn không cần phải mở thêm nhiều file lưu trữ để tìm lại các đoạn code mẫu mình đã biết khi cần. Workflow lập trình Python trở nên đơn giản và hiệu quả hơn rất nhiều.
- **Tạo dashboard viết bằng Python và chia sẻ với team dễ dàng** nếu cần tương tự như Google DataStudio nhưng linh hoạt và mạnh mẽ hơn rất nhiều.

Tuy nhiên Google Colab có 1 nhược điểm gây khó chịu không ít đó là dữ liệu (bộ nhớ tạm) của phiên làm việc sẽ bị xóa sau khi bạn không active trong 1 thời gian nhất định để Colab đảm bảo có thể cung cấp tài nguyên miễn phí cho nhiều người. Do đó mỗi khi mở Google Colab, nếu bạn cần sử dụng các thư viện của bên thứ 3 thì bạn cần install và import lại từ đầu để có thể sử dụng. Phiên bản Colab Pro giúp khắc phục điều này nhưng hiện tại không áp dụng cho thị trường Việt Nam.


## Thao tác cơ bản với Colab

### Giao diện làm việc

[![Giao diện Google Colab](https://thinhvu.com/wp-content/uploads/2021/07/Giao-dien-Google-Colab.png "Hướng dẫn sử dụng Google Colab đầy đủ - Python Tutorial 2")](https://thinhvu.com/wp-content/uploads/2021/07/Giao-dien-Google-Colab.png)

### Thiết lập hữu ích

#### Ngữ hiển thị

Google Colab mặc định hiển thị ngôn ngữ tiếng Việt cho tôi nhưng tôi luôn lựa chọn làm việc với phiên bản tiếng Anh cho tiện giao tiếp và tìm kiếm hỗ trợ dễ dàng khi cần. Nếu bạn cũng cần thay đổi ngôn ngữ, hãy tìm lựa chọn này ở menu `Trợ giúp` >> `Xem bằng tiếng Anh`.

<div style="display: flex; justify-content: center;">
<iframe width="914" height="514"src="https://www.youtube.com/embed/SG17IaxkDV0?si=tfc9P2aC-Ers7kOQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>

Bạn cũng có thể sử dụng cách thay đổi `hl=vi` thành `hl=en` trong địa chỉ của Notebook ở thanh địa chỉ trên trình duyệt. Ví dụ, thay đôỉ `https://colab.research.google.com/drive/1WdRrOmnTI1s-KppcGGkBjBA9ZU_X2LiK?authuser=1&hl=vi`  sang `https://colab.research.google.com/drive/1WdRrOmnTI1s-KppcGGkBjBA9ZU_X2LiK?authuser=1&hl=en` sau đó Enter.

#### Bật Dark mode

Nếu các bạn ưu thích chế độ làm việc Darkmode thì có thể bật nó lên dễ dàng bằng cách: Tìm trên thanh Menu và chọn `Tools` >> `Settings` hoặc click vào hình chiếc bánh răng ở góc phải phía trên của Notebook bên cạnh avatar của bạn để mở mục Cài đặt. Chọn tùy chọn `dark` ở mục Theme và click vào `Save` để lưu cài đặt.

<div style="display: flex; justify-content: center;">
<iframe width="914" height="514"src="https://www.youtube.com/embed/jFTMBqD48BM?si=0dVN9oNzP6Vo4U2K" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>

#### Tùy chọn lập trình

Mở mục cài đặt và chọn Editor, tick chọn hết tất cả các tùy chọn trong mục này. Trong đó đặc biệt là `Show line numbers` giúp bạn hiển thị số thứ tự của dòng code trong 1 code cell và `Show indentation guides` giúp hiển thị căn thụt đầu dòng rất hữu ích, hạn chế xảy ra lỗi định dạng khoảng cách không đúng trong Python.

<div style="display: flex; justify-content: center;">
<iframe width="914" height="514"src="https://www.youtube.com/embed/xMZAVqwu5Sc?si=NWSKUP4YJamBU_vO" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>

### Thao tác với File & Folder

#### Tạo mới, mở hoặc upload Notebook

Để mở File với Google Colab, bạn có thể sử dụng tổ hợp phím tắt Ctrl + O (hoặc Command + O trên Macbook). Bạn có 5 tùy chọn chính trong đó có :

- `Examples` cho phép mở các dataset ví dụ
- `Recent`: Mở notebook được chạy gần đây
- `Google Drive:` mở Jupyter Notebook từ Drive (file định dạng `.ipynb`)
- `Github:` Cho phép bạn kết nối với Github và clone các project của mình cũng như mở bằng Colab
- `Upload` cho phép bạn duyệt file trên máy tính cá nhân và tải lên file notebook có định dạng `.ipynb`

<div style="display: flex; justify-content: center;">
<iframe width="914" height="514"src="https://www.youtube.com/embed/e3tntBqUpwk?si=wBr4H0BG2JImm5ts" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>

#### Lưu Notebook

Google Colab thực hiện lưu dữ liệu làm việc của bạn hoàn toàn tự động tuy nhiên trong trường hợp bạn chưa yên tâm hoặc muốn có nhiều tùy chọn lưu trữ hơn thì có thể tìm đến `Menu` >> `File` và chọn lưu file trên Google Drive hay Github tùy mục đích của mình.

#### Download Notebook

Bạn có thể tải Notebook về máy dưới dạng file Jupyter Notebook có định dạng `.ipynb` hoặc file Python có định dạng `.py` bằng cách mở menu `File` >> `Download` sau đó chọn định dạng file tương ứng.

#### Upload Dữ liệu

Để upload dữ liệu vào bộ nhớ tạm của session làm việc trong Colab, bạn có thể chọn mục Folder như trong hình sau đó chọn icon Upload dữ liệu như hình minh họa dưới đây. Trong trường hợp bạn sử dụng dữ liệu từ Google Drive để làm việc, hãy theo dõi hướng dẫn ở phần tiếp theo của bài viết.

![](https://thinhvu.com/wp-content/uploads/2021/07/Inked_colab_file_open-1024x476.jpg)

#### Copy File Path

Để có thể copy đường dẫn file hoặc thư mục khi bạn cần thao tác mở hoặc lưu trữ file, bạn có thể nhấp chuộc phải vào file hoặc folder trong cây thư mục và chọn `Copy path`.

![](https://thinhvu.com/wp-content/uploads/2021/07/Inked_colab_copy_path-e1625758884600.jpg)

### Edit – Soạn thảo Notebook

- Ngoài việc copy text thông thường, Google Colab cho phép bạn copy/paste Code cell và Text cell khá tiện lợi. Tính năng này khá hay nhưng tôi không thấy trên Jupyter Notebook, Jupyter Lab và Visual Studio Code. Để copy/paste các cell này, bạn sử dụng Ctrl và Click chọn các cell cần copy/paste sau đó sử dụng tổ hợp phím tắt `Ctrl` + `C` và `Ctrl` + `V` quen thuộc.
- Bạn có thể kích hoạt tính năng `Find and replace` bằng tổ hợp phím `Ctrl` + `H` hoặc chọn icon kính lúp ở thanh công cụ bên cạnh trái màn hình.

### View – Tuỳ chọn hiển thị

Chọn Menu >> View:

- Executed Code History: Xem lịch sử các dòng lệnh đã được thực thi trong Notebook
- Collapse sections: cho phép thu gọn các nội dung phân cấp nhỏ hơn ở mỗi 1 cấp độ heading (ví dụ Collapse tại cell chứa heading 1 thì các nội dung thuộc heading từ 2 trở đi và text thông thường sẽ được thu gọn lại). Bạn có thể chọn 1 cell bất kỳ trong Notebook và sử dụng tổ hợp phím tắt `Ctrl` + `]` để Collapse.
- Expand sections: Tác dụng ngược lại so với Collapse sections – cho phép mở rộng các mục nội dung dưới 1 cấp heading bất kỳ. Tổ hợp phím tắt `Ctrl` + `[` cho kết quả tương tự.

### Insert – Thêm nội dung

- Để thêm 1 Code cell (thực thi lệnh) hoặc Text cell (văn bản), bạn có thể di chuột vào 1 cell sẵn có và chọn đối tượng cần thêm tương ứng. Nếu là Notebook mới hoàn toàn bạn có thể thêm cell bằng 2 nút ở góc trái màn hình như khoanh đỏ ở hình minh họa sau. Bạn cũng có thể sử dụng tổ hợp phím tắt mặc định `Ctrl` + `M` `B` để thêm 1 Code cell.
- Để thêm 1 Section header bạn có thể dùng tùy chọn tương ứng tron mục Menu >> Insert hoặc thêm 1 Text cell sau đó tạo Heading bằng định dạng markdown. Ví dụ để tạo Heading 1 là mục giới thiệu như trong hình, bạn cần viết `# I. GIỚI THIỆU` vào Text cell. Thêm 1 dấu # trước đầu mục cho mỗi cấp độ Heading nhỏ hơn.
- Scratch Code Cell: Bằng cách kích hoạt tùy chọn này, bạn mở ra 1 Code cell sử dụng như bản nháp thực thi code bên cạnh việc soạn thảo chính trong Notebook.

![](https://thinhvu.com/wp-content/uploads/2021/07/colab_insert_block-1024x480.png)

### Runtime – Môi trường thực thi Python

#### Thực thi lệnh Python

Để thực thi các dòng lệnh trên Google Colab, bạn click vào nút Play ở đầu mỗi code cell hoặc chọn code cell cần thực thi sau đó dùng tổ hợp phím tắt Shift + Enter. Bạn cũng có thể sử dụng Menu `Runtime` với các tuỳ chọn thực thi đa dạng như:

- Run all: thực thi toàn bộ các dòng lệnh có trong Colab
- Run before: Thực thi các dòng lệnh xuất hiện trước code cell bạn đang chọn
- Run the focus cell: Thực thi code cell bạn đang chọn
- Run the selection: Thực thi các code cell bạn lựa chọn (ấn giữ phím Shift và dùng chuột để lựa chọn nhiều code cell)
- Run after: Thực thi các code cell kể từ code cell bạn đang chọn về sau

<div style="display: flex; justify-content: center;">
<iframe width="914" height="514"src="https://www.youtube.com/embed/I_PR8vGQV8Y?si=WzlxoYAHpCuxEGGK" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>

#### Dừng thực thi & khởi động lại

Đôi khi việc thực thi xảy ra không như mong muốn, bạn có thể muốn dừng thực thi hoặc khởi động lại môi trường làm việc của Google Colab (runtime). Các tuỳ chọn dưới đây của Runtime menu sẽ giúp ích cho bạn:

- Interrupt execution: Dừng thực thi các câu lệnh
- Restart runtime: Khởi động lại runtime để cập nhật các thay đổi (ví dụ khi bạn cài đặt thư viện mới và bắt buộc phải restart runtime để áp dụng các thay đổi) hoặc đơn giản là xoá các lỗi & chạy lại runtime.
- Restart and run all: Khởi động lại runtime và chạy toàn bộ câu lệnh trong Colab
- Factory reset runtime: Xoá toàn bộ trạng thái thực thi hiện tại của runtime bao gồm các khai báo biến, file sau đó khởi động lại runtime.

#### Thay đổi loại Runtime

Khi sử dụng Colab cho các project liên quan đến Machine Learning có thể bạn sẽ muốn khai thác tối đa sức mạnh của Google Colab để thực thi lệnh với ít thời gian hơn. Khi đó tuỳ chọn tăng tốc phần cứng với GPU hoặc TPU sẽ trở nên cực kỳ hữu ích.

Để thay đổi tuỳ chọn Runtime, bạn tìm từ `Menu > Runtime > Change runtime type`

### Sử dụng thư viện Python
#### Cài đặt thư viện không có sẵn

Để cài đặt thư viện mới không có sẵn trong Google Colab, bạn thực thi câu lệnh `pip install package_name` ở 1 code cell bất kỳ trong đó `package_name` là tên thư viện bạn muốn cài đặt thêm. Ví dụ, để cài đặt thư viện facebook business sdk cho Python, chúng ta thực thi câu lệnh `pip install facebook_business`. 

Thông thường bạn sẽ phải cài đặt lại các thư viện không có sẵn khi làm việc với Colab sau khi kết thúc session làm việc trước đó 1 thời gian (không có con số cụ thể, có thể là 15 – 30 phút không hoạt động). Điều này cũng gây ra đôi chút khó chịu và mất thời gian để cài lại các thư viện nếu bạn sử dụng nhiều thư viện bên ngoài.

#### Import thư viện vào dự án

Để import 1 thư viện bất kỳ vào Colab bạn sử dụng câu lệnh `import package_name as something` trong đó `package_name` là thư viện bạn muốn import, `something` ở đây là tên ngắn gọn (alias) bạn muốn đặt cho thư viện đó để tiện gọi thư viện khi làm việc. Ví dụ, tôi muốn import thư viện `pandas` và gán cho nó cái tên rút gọn là `pd`, tôi sẽ nhập câu lệnh sau vào 1 code cell và thực thi: `import pandas as pd`

Trong một số trường hợp tên thư viện của bạn đã ngắn gọn sẵn thì không cần thiết phải gán alias, bạn có thể import thư viện với câu lệnh đơn giản `import package_name`.

## Mẹo sử dụng Google Colab

### Code Snippet - Đoạn mã

Đây là một tính năng khá hay ho của Google Colab cho phép bạn tìm kiếm và chèn các đoạn mã được soạn sẵn vào Notebook bạn đang làm việc, bạn có thể tiết kiệm rất nhiều thời gian của mình với tính năng này.

Để chèn 1 code snippet bạn sử dụng tổ hợp phím tắt Ctrl + Alt + P (Control + Option + P trên Mac) hoặc click icon Code Snippet ở thanh công cụ phía bên trái màn hình, hoặc mở từ `Menu > Insert > Code snippets`.

<div style="display: flex; justify-content: center;">
<iframe width="914" height="514"src="https://www.youtube.com/embed/QfhVarMPV_I?si=jdCgkj7FHnDOvT-l" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>

Để thêm 1 Notebook do bạn soạn thảo chứa các đoạn mã mẫu vào Colab, bạn chỉ cần copy URL của Notebook trên trình duyệt và paste vào mục `Custom snippet notebook URL` trong phần cài đặt Colab.

![](https://thinhvu.com/wp-content/uploads/2021/07/colab_custom_code_snippet_setting-1024x582.png)

Lưu ý rằng, để dễ dàng tìm kiếm các đoạn mã, bạn cần cấu trúc các heading 1 ở trước mỗi đoạn mã (chỉ cho phép tìm kiếm heading 1 ở mục Code snippets). Bạn chỉ cần thêm 1 dấu # trước tên đề mục (dấu # biểu thị 1 cấp độ heading, bạn có thể tham khảo thêm về ngôn ngữ Markdown để hiểu rõ).

![](https://thinhvu.com/wp-content/uploads/2021/07/colab_template_code_snippet-1024x581.png)

### Scratch code cell – Ô mã tạm thời

Ô chứa mã tạm thời cho phép bạn thực hiện các câu lệnh dưới dạng bản nháp mà không tác động đến kết quả hoặc việc trình bày Notebook của bạn. Bạn có thể kích hoạt tính năng này với tổ hợp phím tắt Ctrl + Alt + N (Control + Option + N với Mac) hoặc mở từ `Menu > Insert > Scratch code cell`. Một cách khác để kích hoạt tính năng này là bạn mở Command Palette với tổ hợp phím Ctrl + Shift + P sau đó tìm scratch code cell và Enter để chọn.

### Command pallete – Bảng lệnh

Command palette là 1 tính năng tiện lợi để tìm kiếm các thao tác cần thực hiện với Colab nhanh chóng khi bạn đang “coding” tương tự như khi bạn sử dụng với Visual Studio Code. Để mở nhanh tính năng này, bạn sử dụng tổ hợp phím tắt Ctrl + Shift + P trên máy tính (shortcut đúng với cả Windows lẫn Mac).

### Shortcuts – Phím tắt

Google Colab cung cấp cho bạn bộ phím tắt đa dạng để kích hoạt các tính năng hữu ích. Để mở danh mục phím tắt và có thể cài đặt lại phím tắt, bạn ấn giữ đồng thời tổ hợp phím Ctrl + M + H (Command + M + H cho Mac).

### TOC - Mục lục

TOC (Table of Contents) là tính năng rất hay của Google Colab mà tôi mong sao Visual Studio Code và Jupyter Lab sớm bổ sung. Mục lục cho phép bạn di chuyển nhanh giữa các phần nội dung của Colab, bạn cũng có thể Thu gọn hoặc Mở rộng các nội dung thuộc mỗi cấp heading để làm việc gọn gàng hơn với Colab. Ngoài ra tính năng này giúp bạn trải nghiệm làm việc với Python như đang soạn thảo văn bản thông thường hay viết sách. Tôi đã tận dụng tính năng này để trình bày toàn bộ giáo trình khoá học Python của mình và chia sẻ cho các bạn học viên 1 cách thuận tiện.

![](https://thinhvu.com/wp-content/uploads/2021/07/google_colab_table_of_contents-1024x583.png)

### Chạy Colab với môi trường cục bộ

Google Colab cho phép bạn lựa chọn Cloud Runtime được cung cấp bởi Google giúp bạn tận dụng sức mạnh GPU, TPU trên môi trường Cloud, hoặc bạn có thể sử dụng Local Runtime do bạn thiết lập (môi trường Python trên máy tính cá nhân). Sử dụng Local Runtime giúp bạn tránh phải cài đặt lại thư viện cần thiết mỗi lần sử dụng Google Colab. Khi đó, Google Colab hoạt động tương tự như Jupyter Lab hay Jupyter Notebook, được mở trên trình duyệt web vậy.

Vì 1 lý do nào đó, hướng dẫn thiết lập Colab có sẵn của Google để chạy với Local Runtime không hoạt động đúng như tài liệu, tôi đã thực hiện 1 vài sửa đổi nhỏ với các câu lệnh Terminal do Google cung cấp. Có thể hướng dẫn này sẽ giúp bạn khỏi bối rối.

> Lưu ý nhỏ: Nếu bạn sử dụng máy tính Windows, hãy thực hiện cài đặt các bước dưới đây với môi trường Python Anaconda, sử dụng Anaconda Prompt thay vì Command Prompt mặc định của Windows. Nếu không sử dụng Anaconda Prompt bạn có thể gặp lỗi `jupyter-serverextension' is not recognized as an internal or external command, operable program or batch file` khi cố gắng enable extension `jupyter_http_over_ws`

![](https://thinhvu.com/wp-content/uploads/2021/09/anaconda_prompt-812x1024.jpg)

**Bước 1: Cài đặt [Jupyter](https://jupyter.org/install) trên máy tính**

Chọn 1 trong 2 cách dưới đây, mở terminal/command prompt và chạy câu lệnh tương ứng. Nếu bạn đã cài đặt anaconda thì có thể bỏ qua bước này. Thao tác này chỉ cần thực hiện 1 lần duy nhất.

- Cài đặt với Anaconda: `conda install -c conda-forge jupyterlab`
- Cài đặt với pip: `pip install jupyterlab`

**Bước 2: Cài đặt và kích hoạt tiện ích mở rộng _jupyter_http_over_ws_**

Nhập đoạn code sau và thực thi trên Terminal/Command prompt (chỉ cài đặt 1 lần). Nếu bạn sử dụng runtime của anaconda thì cần mở command prompt (trên máy tính Windows) để chạy lệnh này. Riêng với Mac bạn có thể chay lệnh dưới đây với Terminal mặc định.

```shell
pip install jupyter_http_over_wsjupyter serverextension enable --py jupyter_http_over_ws
```

**Bước 3: Khởi động server và xác thực**

Mỗi khi muốn chạy Colab trên môi trường local, bạn cần thực hiện bước này. Nhập đoạn mã dưới đây vào Terminal/command prompt (hoặc anaconda prompt trên windows). Sau khi server được khởi động thì Terminal sẽ hiển thị URL dưới dạng https://.. mà bạn cần copy để sử dụng. Ấn nút connect ở góc phải notebook Colab và paste URL bạn vừa copy để kết nối.

```shell
jupyter notebook --NotebookApp.allow_origin='https://colab.research.google.com' --port=8888 --NotebookApp.port_retries=0
```

<div style="display: flex; justify-content: center;">
<iframe width="914" height="514"src="https://www.youtube.com/embed/QfhVarMPV_I?si=ooT3uRSrYDPtz5UZ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>

Nếu bạn muốn mở 1 folder cụ thể khi chạy Google Colab với local runtime, có thể tùy biến câu lệnh ở bước 3 để chạy với Terminal/Command Prompt. Dưới đây, mình muốn Google Colab sẽ làm việc tại folder `D:\OneDrive\Github`

`jupyter notebook --NotebookApp.allow_origin='https://colab.research.google.com' --port=8888 --NotebookApp.port_retries=0 --notebook-dir="D:\OneDrive\Github"`

### Chuyển đổi nhanh

Tôi thường xuyên soạn thảo các Notebook và lập trình Python để sử dụng trên nhiều môi trường máy tính khác nhau như Google colab, Macbook, Windows, Raspberry Pi, Linux Server vì vậy việc cấu hình điạ chỉ thư mục sao cho sử dụng tiện lợi nhất là hết sức cần thiết.

![](https://thinhvu.com/wp-content/uploads/2021/07/google_colab_switching_between_multiple_runtimes-1024x453.png)

Một mẹo nhỏ tôi thường xuyên sử dụng đó là gán địa chỉ thư mục làm việc với biến `project_folder`, gán demiliter của máy tính Windows/Mac/Linux với biến `lmt` (các bạn có thể đã biết Windows sử dụng backslash `\` để ngăn cách thư mục còn Mac/Linux lại sử dụng forwardslash `/`. Google Colab thực chất chạy trên môi trường Linux). Do đó mỗi khi cần tham chiếu đến 1 folder, file trong thư mục làm việc, tôi dùng hàm `join` để nối các thành phần của tên này với nhau. Ví dụ để đọc 1 file sample.csv, tôi dùng câu lệnh:

`df = pd.read_csv(lmt.join([project_folder, 'sample.csv'])`

### Kết nối Google Drive

Để tương tác với file & folder trong Google Drive của bạn trong Google Colab, bạn sẽ cần thực hiện thao tác mount drive. Việc này rất đơn giản, bạn click vào icon Folder và chọn Google Drive icon sau đó 1 đoạn code sẽ được chèn tự động vào Colab, bạn cần thực thi đoạn code này, 1 tab mới được mở ra yêu cầu bạn xác thực quyền truy cập tài khoản > xác thực và copy token key sau đó quay trở lại Colab và paste vào ô yêu cầu nhập liệu của đoạn code mount drive sau đó enter. Do mình đã kết nối Drive nhiều lần gần đây nên video demo dưới đây khi mount drive, Google không bắt mình xác thực quyền truy cập 1 lần nữa.

<div style="display: flex; justify-content: center;">
<iframe width="914" height="514"src="https://www.youtube.com/embed/Qlfqb2MWxcE?si=siNQriGeQRZPV8zU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>

Với những người sử dụng nhiều tài khoản Google trong cùng 1 trình duyệt như mình, đôi khi xác thực nhầm tài khoản để kết nối khiến các bạn không khỏi bối rối không biết làm sao để thay đổi tài khoản và truy cập các thư mục cần thiết. Đây là đoạn code bạn cần thực thi:

`from google.colab import drive`

`drive.flush_and_unmount()`

Bạn có thể chèn đoạn code này vào 1 file Colab mẫu để truy cập nhanh từ giao diện Code Snippet của Colab Notebook như trong video demo mình thực hiện.

### Kết nối với  Google Sheets

Trong Google Colab đã có sẵn code snippet để bạn import / export đơn giản nhất nhưng cũng bất tiện vì mỗi lần thực thi lệnh để đọc/ghi dữ liệu với Google Sheets trong 1 session làm việc mới, bạn phải xác thực quyền truy cập 1 cách thủ công khá bất tiện. Bài hướng dẫn toàn tập của mình giúp các bạn thiết lập kết nối với Google Sheets thông qua 1 service account thuận tiện tại đây: [Đọc và xuất dữ liệu Google Sheets với Python & Jupyter Notebook](https://thinhvu.com/2021/05/27/doc-va-xuat-du-lieu-google-sheets-voi-python/)

### Lịch sử phiên bản

Trong nhiều trường hợp, do thao tác nhầm bạn có thể xoá 1 hoặc nhiều code block, thậm chí xoá cả chương nội dung, hẳn bạn sẽ cần 1 thao tác giúp Undo thao tác này. Đôi khi bạn cũng muốn khôi phục 1 phiên bản Notebook cũ hơn và bỏ qua các thay đổi đã thực hiện gần đây. Tính năng Revision history sẽ là cứu cánh cho bạn. Để truy cập tính năng này, tìm `Menu > File > Revision history`. Như vậy, mặc dù không sử dụng Github, bạn vẫn có thể kiểm soát các phiên bản khác nhau của Notebook mình thực hiện với Colab.

<div style="display: flex; justify-content: center;">
<iframe width="914" height="514"src="https://www.youtube.com/embed/kuQ6Ctsi4-E?si=Dc8hRhgMg4KLrmfm" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>

### Tạo dashboard

Nếu bạn có ý định sử dụng Google Colab như 1 python dashboard “trên mây” thì cũng hoàn toàn khả thi. Để thực hiện ý tưởng này, bạn có thể sẽ cần sử dụng các script để đồng bộ file với Google Drive thông qua thư viện Python PyDrive như tôi đang sử dụng (lên lịch refresh dữ liệu tự động bằng crontab trên máy Raspberry Pi) hoặc đơn giản là lưu file trên máy local và đồng bộ với công cụ [Backup & Sync](https://www.google.com/drive/download/) của Google trên máy tính Windows và Mac.

### Kết nối với Github

Để đọc các repository trên Github hoặc lưu Notebook của bạn trên Github, bạn có thể thực hiện rất đơn giản.

- Mở file từ Github: sử dụng `Menu > File > Open notebook` và chọn nguồn lưu trữ là Github sau đó xác thực truy cập tài khoản nếu bạn muốn mở các file trong repo dưới dạng private.
- Lưu file vào Github: sử dụng `Menu > File > Save a copy in Github` sau đó xác thực tài khoản và chọn repo với branch bạn cần lưu trữ file.

### So sánh 2 Notebook

Google Colab cung cấp tính năng so sánh giữa 2 notebook với nhau rất tiện lợi. Bạn có thể kích hoạt tính năng này từ `Menu > Tool > Diff Notebooks`.

![](https://thinhvu.com/wp-content/uploads/2021/07/google_colab_diff_notebook-1024x582.png)