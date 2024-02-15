# Hướng dẫn đóng gói thư viện python và phân phối qua PyPI

## I. GIỚI THIỆU

Năm 2021, khi tôi lần đầu tiên cố gắng đóng gói một gói Python (thư viện Python) của mình, với tên là "vnstock", tôi đã gặp khó khăn khi đọc các tài liệu hướng dẫn. Dù đã tìm hiểu qua các bài viết tiếng Anh và tiếng Việt, nhưng vẫn cảm thấy khá mơ hồ và phức tạp. Đến ngày hôm nay, khi tìm kiếm trên Google với từ khóa "cách tạo thư viện PyPI" hoặc "how to create pypi package", tôi vẫn chưa tìm thấy một hướng dẫn dễ hiểu và thực hiện, đặc biệt dành cho những người mới bắt đầu muốn chia sẻ thư viện Python của mình. Điều này đã thúc đẩy tôi quyết định dành thời gian chia sẻ bài viết và làm video hướng dẫn này, nhằm giúp nhiều người trải nghiệm việc chia sẻ mã nguồn Python mã nguồn mở một cách dễ dàng. Trong bài viết này, tôi sẽ hướng dẫn bạn cách đóng gói một thư viện Python dựa trên hướng dẫn gốc từ The Python Foundation Tại đây. Trong hướng dẫn này, quá trình tạo một gói python bắt đầu từ việc sử dụng 1 Github repo mẫu tên là py_packaging_template.

> py_packaging_template là một repo trên Github chứa cấu trúc mẫu của một thư viện Python, bạn có thể bắt đầu clone repo này về máy để thực hiện chỉnh sửa theo bài hướng dẫn này và phân phối thư viện python đầu tay của mình.

<div style="display: flex; justify-content: center;">
<iframe width="914" height="514"src="https://www.youtube.com/embed/WuN4nRttNkQ?si=68S70UJOGZO1SeXG" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>

### 1.1. Vì sao cần đóng gói python package

Có nhiều lý do cho mục đích đóng gói và phân phối gói python package trong đó tôi làm rõ 2 lý do chính dưới đây:

Cho bạn: sử dụng các dự án của mình đã phát triển một cách dễ dàng. Bạn có thể dùng công cụ pip để cài đặt thư viện của mình trên bất kỳ thiết bị nào. Các đoạn code phức tạp bạn viết được đóng gói trong các hàm (function) để sẵn sàng import code vào dự án mới mà không cần lặp lại các đoạn code này giúp dự án của bạn trình bày thanh thoát và hiệu quả.
Cho cộng đồng: chia sẻ tới cộng đồng sử dụng dự án bạn đã phát triển, công khai mã nguồn để cộng đồng có thể đóng góp phát triển.

### 1.2. Cấu trúc thư viện mẫu

Nội dung của thư viện này được clone từ một thư mục mà tôi chia sẻ tên là ur_gadget để bạn có thể hình dung thực tế 1 thư viện chứa những thông tin chính xác như thế nào. Thư viện này cũng đã được chia sẻ lên Pypi và Github.

Thư viện mẫu này bao gồm các thành phần sau:

```
py_packaging_template/
├─.gitattributes
├─.gitignore
├─code/
│ ├─datetime_intel.py
│ ├─gadget.py
│ └─__init__.py
└─src/
└─github_desktop_clone.png
├─LICENSE
├─README.md
├─pyproject.toml
├─setup.cfg
├─requirements.txt
```

Trong đó:

`code/` chứa các file mã nguồn của thư viện

`src/` chứa các file tài nguyên đính kèm bao gồm hình ảnh, video, tài liệu hướng dẫn, ...

LICENSE: chứa thông tin về giấy phép sử dụng thư viện, trong trường hợp này là giấy phép MIT.

README.md: chứa thông tin về thư viện, cách cài đặt và sử dụng thư viện, đây là file người dùng đọc trước khi cài đặt thư viện và được hiển thị mặc định khi bạn chia sẻ thư viện lên Pypi.

pyproject.toml: cho biết các công cụ quản lý thư viện như pip và build sẽ sử dụng thêm các gói thư viện nào để tạo các gói thư viện của bạn khi người dùng cài đặt vào máy của họ. Bạn cần chỉ rõ các gói thư viện phụ thuộc (dependencies) trong file này. Hướng dẫn này sử dụng setuptools để tạo gói thư viện.

setup.cfg: chứa các thông tin cấu hình cho thư viện như tên thư viện, tác giả, phiên bản, ...

requirements.txt: chứa các gói thư viện cần thiết để phát triển thư viện, trong trường hợp này là setuptools và wheel. Bạn có thể chỉ rõ các gói thư viện khác nếu cần thiết, thông thường khi bạn tham chiếu một thư viện python không có sẵn khi cài đặt Python, bạn cần chỉ rõ các gói thư viện này trong file này để người dùng cài đặt thư viện này mới có thể sử dụng thư viện của bạn.

## II. HƯỚNG DẪN SỬ DỤNG


### 2.1. Clone repo này về máy của bạn

Trong hướng dẫn này, bạn có thể clone dự án về máy của mình thông qua 2 cách là dùng Terminal/Command Prompt hoặc Github Desktop.



#### a. Sử dụng Terminal / Command Prompt

Mở Terminal/Command Prompt

Di chuyển đến thư mục bạn muốn lưu trữ dự án với lệnh 

```
cd ĐƯỜNG_DẪN_TỚI_THƯ_MỤC. Ví dụ: cd C:\Users\thinh\Github\
```

Clone dự án về máy của bạn với lệnh git clone https://github.com/thinh-vu/py_packaging_template.git

Chờ một lát, bạn sẽ thấy một thư mục mới được tạo ra với tên py_packaging_template bên trong thư mục bạn chọn để lưu trữ dự án.

#### b. Sử dụng Github Desktop

Nếu bạn chưa từng sử dụng Github Desktop, bước đầu tiên cần làm là cài đặt Github Desktop trên máy tính và đăng nhập với một tài khoản Github. Bạn có thể tải Github Desktop tại đây. Sử dụng Github (và Git nói chung) là một cách không thể thiếu để quản lý mã nguồn của bạn.

- Mở Github Desktop
- Chọn File > Clone repository
- Paste link của repo vào cửa sổ hiện ra và chọn thư mục lưu trữ dự án để tiếp tục

![Clone dự án với Github Desktop](https://thinhvu.com/wp-content/uploads/2023/08/github_desktop_clone.png)

### 2.2. Cập nhật mã nguồn của bạn vào thư viện
Bạn cần tạo các file mã nguồn của thư viện, ví dụ ở đây là `gadget.py` và `datetime_intel.py` trong thư mục `/code`

Thiết lập tham chiếu các file mã nguồn này trong file `__init__.py`.

Thêm các dòng code để import các thành phần của thư viện vào file `__init__.py`. Ví dụ: `from .gadget import *` để import toàn bộ các phần tử (hàm, biến, vv) từ file `gadget.py` vào thư viện. Mỗi file mã nguồn sẽ có một dòng import tương ứng.

.gadget là tên file mã nguồn (chính là file gadget.py), vì file này đặt cùng thư mục với file __init__.py bạn đang thiết lập nên dùng dấu . để tham chiếu.


### 2.3. Thiết lập thư viện
`setup.cfg`: Thay đổi thông tin mô tả thư viện của bạn như tên, phiên bản, tác giả, email, loại giấy phép, URL mã nguồn ...

pyproject.toml:
- Mục [build-system] không cần thay đổi.

- Mục [project]:

  - `name` và `description` là tên và mô tả ngắn gọn gói thư viện được tạo ra để làm gì.
  - `version` là số hiệu phiên bản của gói phần mềm, khi chia sẻ lên Pypi, bạn cần tăng số hiệu phiên bản này lên 1 đơn vị so với phiên bản trước đó. Ví dụ: phiên bản trước đó là 0.0.1 thì phiên bản mới sẽ là 0.0.2. Số hiệu này là duy nhất trên Pypi, nếu bạn cố tình tạo ra một phiên bản trùng với phiên bản đã có trên Pypi, bạn sẽ nhận được thông báo lỗi. Sau khi đã upload thư viện thành công lên Pypi, bạn có thể xóa thư viện nhưng không thể dùng lại số hiệu phiên bản đã được sử dụng đó.

- `dependencies:` các gói phụ thuộc được sử dụng trong thư viện của bạn, tên mỗi gói được viết một dòng, phân cách nhau bởi dấu phẩy ,. Trong ví dụ mẫu này, bạn cần thêm gói thư viện phụ thuộc là trafilatura, gói này không có sẵn khi cài python.

- `README.md:` Cung cấp mô tả về thư viện và hướng dẫn sử dụng để người dùng tham chiếu. File này sẽ được hiển thị mặc định khi bạn chia sẻ thư viện lên Pypi và Github.

- `LICENSE:` Chứa thông tin về giấy phép sử dụng thư viện, trong trường hợp này là giấy phép MIT. Bạn có thể tham khảo các giấy phép khác tại đây. MIT là loại giấy phép phổ biến nhất và được sử dụng rộng rãi trong cộng đồng mã nguồn mở. Bạn có thể yên tâm sử dụng giấy phép này cho thư viện của mình mà không cần làm gì thêm.

- `requirements.txt:` Chứa các gói thư viện cần thiết để cài đặt thư viện của bạn, trong trường hợp này là setuptools, wheel và trafilatura. Bạn có thể chỉ rõ các gói thư viện khác nếu cần thiết, thông thường khi bạn tham chiếu một thư viện python không có sẵn khi cài đặt Python, bạn cần chỉ rõ các gói thư viện này trong file này để người dùng cài đặt thư viện này mới có thể sử dụng thư viện của bạn.

### 2.4. Chuẩn bị các công cụ cần thiết

- Cài đặt công cụ build để đóng gói thư viện: Sử dụng câu lệnh `pip install --upgrade build` hoặc `python3 -m pip install --upgrade build` hoặc `python -m pip install --upgrade build` tùy thuộc vào môi trường python bạn đang sử dụng là macOS/Linux hay Windows.

- Cài đặt công cụ `twine` để upload thư viện lên Pypi: Sử dụng câu lệnh `pip install --upgrade twine` để cài đặt, nếu gặp lỗi, thử đặt python -m hoặc python3 -m trước câu lệnh trên.

- Tạo tài khoản PypiTest để thử nghiệm upload thư viện và Pypi để upload chính thức. 

- Sau khi tạo tài khoản, bạn cần tạo một API token bằng cách mở mục Account Setting, tìm mục API tokens và chọn Add API tokens. Tại đây bạn chọn scope, nếu là lần đầu tiên tạo token thì chỉ cần chọn scope mặc định, áp dụng cho toàn bộ account của bạn, khi đã chia sẻ ít nhất 1 thư viện, bạn có thể chọn scope chính xác cho thư viện đó để bảo mật tài khoản, giới hạn phạm vi tác động của API tới chính xác thư viện bạn muốn làm việc. PypiTest là bản sao của Pypi để bạn làm quen và thử nghiệm trước khi tải chính thức.

Khi mới làm quen với việc chia sẻ thư viện, bạn nên bắt đầu với PypiTest, sau khi Test (kiểm thử) hoàn chỉnh và xác thực thư viện bạn có thể chạy hoàn hảo cho người dùng tải về thì có thể chuyển sang chia sẻ chính thức tại Pypi.

![H1. Thao tác với PyPI](https://thinhvu.com/wp-content/uploads/2023/08/add_a_token-1024x510.png)

![H2. Thao tác với PyPI](https://thinhvu.com/wp-content/uploads/2023/08/generate_pypi_token-1024x509.png)

### 2.5. Đóng gói thư viện
Mở Terminal/Command Prompt từ thư mục chứa thư viện của bạn. Sử dụng cd ĐƯỜNG_DẪN_TỚI_THƯ_MỤC để di chuyển đến thư mục chứa thư viện của bạn như ở bước 2.1.

Bắt đầu đóng gói khóa học với lệnh python -m build trong Terminal/Command Prompt

![Phân phối thư viện lên PyPI](https://thinhvu.com/wp-content/uploads/2023/08/build_succeed.png)

### 2.6. Kiểm thử thư viện với PypiTest

Upload thư viện lên PypiTest. Tiếp tục chạy câu lệnh sau với Terminal/Command Prompt `python3 -m twine upload --repository testpypi dist/*`. Bạn sẽ thấy trong Terminal/Command Prompt yêu cầu cung cấp username và password.

- Nhập `__token__` cho username
- Nhập token của PypiTest bạn đã tạo ở bước trước cho password

Bạn sẽ nhận được thông báo gói thư viện được upload thành công trong Terminal/Command Prompt.
Nội dung kiểm thử để xác nhận thư viện của mình hoạt động tốt khi phân phối:
Xác nhận gói thư viện của bạn có thể cài đặt được trên các hệ điều hành khác nhau gồm Linux/macOS và Windows.

Các gói phụ thuộc (dependencies) có được tự động cài đặt đầy đủ khi cài thư viện của bạn không? Có cần chạy câu lệnh cài dependencies với file requirements.txt hay không? python -r requirements.txt
import thư viện như thế nào thì thành công? import từng module có hoạt động không?

Các hàm có hoạt động đúng như thiết kế không? Bạn nên có sẵn 1 Jupyter Notebook, file .ipynb để chạy toàn bộ hàm cần kiểm tra và xác nhận không có lỗi nào xảy ra.
Docstring (phần hướng dẫn nhập các tham số của hàm) có hiển thị thân thiện và đầy đủ không?

### 2.7. Phân  phối thư viện lên Pypi

Các bước thực hiện khi phân phối thư viện của bạn chính thức trên Pypi tương tự như với bản PypiTest, khác chút ở câu lệnh upload, cần thay thế testpypi thành pypi. Cụ thể như dưới đây.

- Upload thư viện lên PypiTest. Tiếp tục chạy câu lệnh sau với Terminal/Command Prompt `python3 -m twine upload --repository pypi dist/*`.

- Bạn sẽ thấy trong Terminal/Command Prompt yêu cầu cung cấp username và password.

- Nhập `__token__` cho username

- Nhập token của PypiTest bạn đã tạo ở bước trước cho password

Các bước kiểm tra cần được thực hiện thêm 1 lần nữa với bản chính thức này, tương tự như với PypiTest để đảm bảo thư viện hoạt động hoàn hảo.

### 2.8. Chia sẻ mã nguồn lên Github

Sau khi thực hiện hoàn tất các bước trên, thư viện của bạn đã sẵn sàng. Hãy hoàn tất quá trình này bằng 1 bước nữa đó là chia sẻ mã nguồn của bạn lên Github nếu bạn thực sự muốn công khai mã nguồn dự án. Để làm điều này, bạn có thể sử dụng Github Desktop để commit và đẩy mã nguồn lên tài khoản Github của bạn. Bước này có thể thực hiện trước khi phân phối thư viện của bạn lên Pypi để có thể lấy thông tin URL của dự án và đặt vào phần thông tin tác giả/mã nguồn trong file `setup.cfg`

![Tạo Github repo từ Github Desktop](https://thinhvu.com/wp-content/uploads/2023/08/create_github_repo-1024x533.png)

![Nhập mô tả để commit](https://thinhvu.com/wp-content/uploads/2023/08/publish_repo_github_1-1024x533.png)

![Công bố các thay đổi lên Github](https://thinhvu.com/wp-content/uploads/2023/08/publish_repo_github_2-1024x533.png)

## III. LỜI KẾT

Chúc mừng bạn trở thành tác giả của một gói thư viện python đầu tay mã nguồn mở chia sẻ tới cộng đồng sau khi thực hiện thành công bài hướng dẫn này.
Nếu thấy bài viết này hữu ích, hãy đánh giá 5 sao và để lại bình luận để chia sẻ cảm nghĩ của bạn với tôi. Hãy chia sẻ bài viết tới nhiều người được biết hơn bạn nhé.

