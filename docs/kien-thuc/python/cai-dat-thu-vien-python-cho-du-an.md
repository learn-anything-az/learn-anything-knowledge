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

# Soạn thảo lệnh với IDE và cài đặt thư viện Python

## IDE là gì?

!!! abstract "Giới thiệu"
    IDE là thuật ngữ viết tắt của **I**ntegrated **D**evelopment **E**nvironment chỉ môi trường tích hợp dùng để soạn thảo lệnh và lập trình ứng dụng. **IDE** tích hợp các công cụ hỗ trợ quan trọng cho việc lập trình như Code Editor để soạn thảo lệnh, Compiler để biên dịch lệnh sang ngôn ngữ máy, Debugger để kiểm tra lỗi, định dạng hoặc highlight (tô sáng màu) cho các từ khoá của ngôn ngữ lập trình, quản lý thư mục, vv

Trong khuôn khổ các hướng dẫn tại LEarn Anything hướng đến việc giúp bạn làm quen bộ công cụ lập trình Python cho mục đích phân tích, xử lý dữ liệu thay vì trở thành một lập trình viên do đó bạn sẽ được làm quen với Visual Studio Code cho môi trường cục bộ Google Colab cho môi trường đám mây.

<iframe width="914" height="514"src="https://www.youtube.com/embed/3e1rvi6UW-E?si=d313pezGj1GzmHU8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Thư viện Python là gì?

!!! abstract "Giới thiệu"
	Thư viện hay gói phần mềm Python (package) bản chất là các đoạn mã chứa hàm / chức năng trong Python được lập trình sẵn cho phép bạn nạp (import) vào dự án của mình để sử dụng thay vì phải tự lập trình. Để cài đặt các gói thư viện Python, bạn sử dụng công cụ quản lý gói tên là `pip` trong cửa sổ lệnh hoặc ô lệnh trong Jupyter Notebook.

Các gói thư viện Python được lưu trữ trên dịch vụ [PyPI](https://pypi.org/) (Python Package Index) - là kho lưu trữ các phần mềm Python của bên thứ ba. Bạn sẽ cài đặt một gói thư viện Python nếu nó được phân phối qua PyPI với câu lệnh đơn giản `pip install tên_gói_thư_viện_muốn_cài`. Các lựa chọn khác có thể là cài thông qua mã nguồn Github, cài thông qua file tarball (file nén chứa phần mềm Python). Thông thường, để cài một gói thư viện Python, bạn sẽ tham khảo hướng dẫn cài đặt chính thức từ trang thông tin của phần mềm/thư viện đó tại mục nội dung Install.

## Cài đặt thư viện Python

### Sử dụng Jupyter Notebook

> Nếu bạn học phân tích dữ liệu với Python, hầu hết trường hợp bạn sẽ làm việc với Jupyter Notebook (Jupyter Lab hay Google Colab). Đây là cách đơn giản nhất bạn nên sử dụng trong mọi trường hợp.

=== "Cài đặt thư viện Python với Pip trong Google Colab"
	![](../../assets/images/cai-dat-thu-vien-python-voi-pip-trong-google-colab.png)
=== "Cài đặt thư viện Python với Pip trong Visual Studio Code"
	![](../../assets/images/cai-dat-thu-vien-python-voi-pip-visual-studio-code-jupyter-notebook.png)

### Sử dụng Terminal / Command Prompt

> Nếu bạn sử dụng macbook, chỉ cần mở ứng dụng dòng lệnh Terminal và chạy dòng lệnh, còn nếu sử dụng Windows thì có thể rắc rối hơn 1 chút. Bạn sử dụng Terminal/Command Prompt để cài đặt thư viện nếu cài bản Python thuần, còn với bản Python Anaconda sẽ cần dùng ứng Anaconda Prompt (cũng là giao diện dòng lệnh tương tự nhưng thiết lập cho Anaconda) để cài đặt.



<figure markdown>
  ![Cài đặt thư viện Python với Pip](../../assets/images/cai-dat-thu-vien-vnstock-voi-terminal-tren-windows.png)
  <figcaption>Cài đặt thư viện vnstock cho Python với Pip</figcaption>
</figure>