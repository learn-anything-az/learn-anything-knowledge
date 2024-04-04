---
date: 2024-02-04
title: Hướng dẫn sử dụng Terminal trong Google Colab với Xterm miễn phí
alias: Hướng dẫn sử dụng Terminal trong Google Colab với Xterm miễn phí
description: Cách sử dụng Terminal hoàn toàn miễn phí trong Google Colab để thực hiện các thao tác nâng cao với hệ điều hành Ubuntu của máy ảo Google.
tags:
  - terminal
  - ubuntu
  - linux
  - google colab
  - chuyên sâu
categories:
  - Hướng dẫn
authors:
  - thinh-vu
---

## Giới thiệu

!!! tip "Giới thiệu"
    Google Colab Terminal được cung cấp trong gói thuê bao hàng tháng bắt đầu với 9.99 USD. Tuy nhiên không phải lúc nào chúng ta cũng thực sự cần tính năng này. Xterm là một giải pháp tuyệt vời để bạn có thể khởi động Temrinal riêng trong Colab để sử dụng trong một số trường hợp đặc biệt. Nói một cách dễ hiểu, Xtern là chương trình giả lập cho phép sử dụng giao diện dòng lệnh trong Linux, ở đây bạn sử dụng với Colab để tương tác với phần hệ thống máy ảo Ubuntu.

Về căn bản, Google sử dụng máy ảo với hệ điều hành Ubuntu để cung cấp dịch vụ Google Colab tới người dùng. Do đó, các thao tác trực tiếp với Terminal cho phép bạn cài đặt và bổ sung các tính năng mình muốn tùy ý (không thể thực hiện với giao diện Colab đồ họa).

```
/content# lsb_release -a
----
No LSB modules are available.
Distributor ID: Ubuntu
Description:    Ubuntu 22.04.3 LTS
Release:        22.04
Codename:       jammy
```

## Sử dụng

### Demo notebook

Để sử dụng tính năng Terminal trong Colab, bạn có thể bắt đầu nhanh bằng việc mở Notebook dưới đây và tương tác trực tiếp. Một số gợi ý trong hướng dẫn này cũng giúp bạn sử dụng tính năng terminal hiệu quả và tránh các hành vi bị cấm bởi Google.

[Khởi động Demo Notebook](https://colab.research.google.com/drive/1PxWbJ-knmRDzw7IEvW3sOmZO7zGNQxPI#scrollTo=7BTt-5s8TGGu){ .md-button }

### Cài đặt
Mở một ô lệnh bất kỳ, paste và chạy câu lệnh sau (Đã có trong file demo):

```
!pip install colab-xterm
%load_ext colabxterm
```


### Khởi động Terminal với Xterm

```
window_height = 800 # Cài đặt chiều cao cửa sổ Terminal
port = 1001

%xterm height={window_height} port={port}
```

### Các câu lệnh căn bản

- `ls`: Liệt kê các file và folder trong thư mục hiện tại
- `lsb_release -a`: Hiển thị thông tin phiên bản hệ điều hành. Hệ thống sử dụng Ubuntu LTS, phiên bản 22.04 tại thời điểm 4/4/2024
- `sudo apt install nano`: Cài đặt text editor Nano. Terminal này cho phép bạn sử dụng Colab như một máy Ubuntu thông thường.
- `nano hello.txt`: Mở hoặc tạo 1 file tên hello.txt để soạn thảo lệnh hoặc ghi chú.
- `sudo apt install cron`: Cài đặt cron để thao tác lên lịch tác vụ cần chạy.

## Cách hành vi bị cấm trong Google Colab

!!! warning "Lưu ý"
    Để duy trì dịch vụ luôn miễn phí cho mọi người, Google Colab nghiêm cấm các hành vi gây ra tác động tiêu cực tới hệ thống hoặc thực hiện các hoạt động gây hại không được phép. Bạn cần lưu ý một số thao tác không được Google khuyến khích trong [FAQ](https://research.google.com/colaboratory/faq.html), cụ thể như dưới đây:

```
- file hosting, media serving, or other web service offerings not related to interactive compute with Colab
- downloading torrents or engaging in peer-to-peer file-sharing
- connecting to remote proxies
- mining cryptocurrency
- running denial-of-service attacks
- password cracking
- using multiple accounts to work around access or resource usage restrictions
- creating deepfakes
```

Ngoài các hành vi kể trên, các hành vi dưới đây không được khuyến khích với người dùng sử dụng bản Colab miễn phí và có thể bị ngăn chặn bất cứ lúc nào mà không cần thông báo trước.

```
- remote control such as SSH shells, remote desktops
- bypassing the notebook UI to interact primarily via a web UI
- chess training
- running distributed computing workers
```