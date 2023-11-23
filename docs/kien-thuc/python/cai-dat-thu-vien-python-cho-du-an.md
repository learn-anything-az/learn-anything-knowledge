---
date: 2023-11-20
title: Hướng dẫn cách cài đặt thư viện Python
description: Hiểu cách cài đặt thư viện Python cho dự án của bạn.
tags:
  - python
categories:
  - Hướng dẫn
authors:
  - thinh-vu
---

# Cài đặt các gói thư viện Python cần thiết

!!! abstract "Giới thiệu"
	Thư viện hay gói phần mềm Python (package) bản chất là các đoạn mã chứa hàm / chức năng trong Python được lập trình sẵn cho phép bạn nạp (import) vào dự án của mình để sử dụng thay vì phải tự lập trình. Để cài đặt các gói thư viện Python, bạn sử dụng công cụ quản lý gói tên là `pip` trong cửa sổ lệnh hoặc ô lệnh trong Jupyter Notebook.

Các gói thư viện Python được lưu trữ trên dịch vụ [PyPI](https://pypi.org/) (Python Package Index) - là kho lưu trữ các phần mềm Python của bên thứ ba. Bạn sẽ cài đặt một gói thư viện Python nếu nó được phân phối qua PyPI với câu lệnh đơn giản `pip install tên_gói_thư_viện_muốn_cài`. Các lựa chọn khác có thể là cài thông qua mã nguồn Github, cài thông qua file tarball (file nén chứa phần mềm Python). Thông thường, để cài một gói thư viện Python, bạn sẽ tham khảo hướng dẫn cài đặt chính thức từ trang thông tin của phần mềm/thư viện đó tại mục nội dung Install.
## Sử dụng Jupyter Notebook

> Nếu bạn học phân tích dữ liệu với Python, hầu hết trường hợp bạn sẽ làm việc với Jupyter Notebook (Jupyter Lab hay Google Colab). Đây là cách đơn giản nhất bạn nên sử dụng trong mọi trường hợp.

=== "Cài đặt thư viện Python với Pip trong Google Colab"
	![](../../assets/images/cai-dat-thu-vien-python-voi-pip-trong-google-colab.png)
=== "Cài đặt thư viện Python với Pip trong Visual Studio Code"
	![](../../assets/images/cai-dat-thu-vien-python-voi-pip-visual-studio-code-jupyter-notebook.png)
## Sử dụng Terminal / Command Prompt

> Nếu bạn sử dụng macbook, chỉ cần mở ứng dụng dòng lệnh Terminal và chạy dòng lệnh, còn nếu sử dụng Windows thì có thể rắc rối hơn 1 chút. Bạn sử dụng Terminal/Command Prompt để cài đặt thư viện nếu cài bản Python thuần, còn với bản Python Anaconda sẽ cần dùng ứng Anaconda Prompt (cũng là giao diện dòng lệnh tương tự nhưng thiết lập cho Anaconda) để cài đặt.



<figure markdown>
  ![Cài đặt thư viện Python với Pip](../../assets/images/cai-dat-thu-vien-vnstock-voi-terminal-tren-windows.png)
  <figcaption>Cài đặt thư viện vnstock cho Python với Pip</figcaption>
</figure>