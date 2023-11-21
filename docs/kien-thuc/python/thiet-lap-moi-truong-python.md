---
date: 2023-11-20
title: Hướng dẫn cách thiết lập môi trường Python
description: Làm quen nhanh chóng với Python qua hướng dẫn dễ hiểu.
tags:
  - python
categories:
  - Hướng dẫn
authors:
  - thinh-vu
---
# Khởi động môi trường Python

## Python trên cloud

!!! abstract "Chọn môi trường Python phù hợp"
	Bạn có thể sử dụng các chương trình python để thực thi trên môi trường đám mây mà không cần trải qua các bước cài đặt phức tạp. Dưới đây là các dịch vụ đám mây cho phép chạy Python ngay lập tức.

Để sử dụng dịch vụ cho phép chạy Python trên cloud, bạn cần đăng ký dịch vụ. Với tài khoản Github và Google, bạn có thể chọn đăng nhập các dịch vụ này ngay lập tức mà không phải trải qua các bước tạo tài khoản mất thời gian.
### Google Colab

> [Colaboratory](https://colab.research.google.com/) (hay Colab) là dịch vụ miễn phí của Google cho phép bạn soạn thảo và thực thi Python ngay trên trình duyệt web với nhiều tính năng ưu việt.

- Miễn phí, không giới hạn.
- Không cần cấu hình rườm rà, truy cập và chạy Python ngay lập tức.
- Tận dụng sức mạnh GPU trên dịch vụ đám mây của Google cho các dự án liên quan đến học máy, AI.
- Dễ dàng chia sẻ và cộng tác với nhóm và đồng nghiệp.

![](../../assets/images/giao-dien-google-colab-lap-trinh-python.png)

Dù là sinh viên, nhà khoa học dữ liệu hay người làm về AI thì Colab đều giúp công việc của bạn dễ dàng và thuận lợi hơn rất nhiều.

### Kaggle

> [Kaggle](https://www.kaggle.com/) là một cộng đồng khoa học dữ liệu và máy học được vận hành bởi Google. Bạn có thể tham gia Kaggle để thi đấu thông qua các dự án được treo giải thưởng hoặc sử dụng các dataset (tập dữ liệu) thực tế để thực hành. Ngoài ra, bạn cũng có thể sử dụng môi trường Python trên Kaggle hoàn toàn miễn phí, phục vụ cho các dự án về máy học và AI bên cạnh Google Colab.

### Github Codespace

> [Github Codespace](https://github.com/features/codespaces) là dịch vụ do Github cung cấp  - dịch vụ lưu trữ mã nguồn phần mềm trên web. Github Codespace cung cấp môi trường lập trình hoàn chỉnh bao gồm cả Terminal, port forwarding, vv như bạn đang làm việc với máy tính cá nhân cùng Visual Studio Code.  

Codespace tiên tiến hơn so với việc sử dụng Google Colab và Kaggle khi bạn cần làm việc với Github và dịch vụ kèm theo như Github Copilot để tận dụng sức mạnh của AI trong lập trình. Lợi ích quan trọng nữa là bạn có thể sử dụng Codespace trên tablet khi di chuyển nhưng vẫn có sức mạnh đầy đủ của một môi trường lập trình hoàn chỉnh.

=== "1. Chọn Jupyter Notebook để bắt đầu"
	![](../../assets/images/su-dung-jupyter-notebook-tren-github-codespace-lap-trinh-python.png)
=== "2. Sẵn sàng sử dụng Python"
	![](../../assets/images/chay-chuong-trinh-python-tren-github-codespace.png)
Bạn được sử dụng miễn phí 60 giờ/tháng cho dịch vụ miễn phí với cấu hình máy ảo với sức mạnh 2 nhân CPU (thấp nhất). [Nâng cấp](https://github.com/pricing/calculator) với giá $0.18/giờ với mức cấu hình này.

Tuy Github Codespace và Gitpod cung cấp môi trường Python và khả năng tương tự nhau nhưng trải nghiệm sử dụng Github Copilot đơn giản hơn khi cho phép người dùng chọn template môi trường lập trình (ví dụ Jupyter Notebook) và môi trường đã được cài đặt sẵn chỉ việc sử dụng. Đồng thời bạn không cần phải bắt đầu dự án với việc nạp một Github repo để sử dụng như Gitpod.
### Gitpod
> [Gitpod](https://www.gitpod.io/) cung cấp môi trường lập trình Online hoàn chỉnh thông qua dịch vụ đám mây tương tự Github Copilot. Bạn có thể sử dụng miễn phí 50h mỗi tháng cho dịch vụ, [nâng cấp](https://www.gitpod.io/pricing) thêm với giá $0.36/giờ.

=== "1. Tạo môi trường làm việc mới"
	![](../../assets/images/thiet-lap-moi-truong-lam-viec-python-voi-gitpod.png)
=== "2. Cài đặt các extension cho Python"
	![](../../assets/images/cai-dat-extension-python-tren-visual-studio-gitpod.png)
=== "3. Cài đặt thư viện cần thiết & sử dụng"
	![](../../assets/images/chay-python-tren-moi-truong-gitpod.png)

Để làm việc với Gitpod bạn cần có tài khoản Github để đăng nhập và lưu trữ mã nguồn dự án.

Khi sử dụng Gitpod, không có tính năng môi trường mẫu được thiết lập sẵn, do đó để chạy được Python bạn phải cài extension (tự động nhận diện) sau đó phải cài thêm các gói thư viện cơ bản kể cả pandas mà dự án bạn cần dùng. Như vậy bạn phải mất thời gian thiết lập môi trường thay vì sử dụng ngay lập tức như Github Codespace.

### Replit

> [Replit](https://replit.com/) cung cấp môi trường lập trình trực tuyến cho phép người dùng biến ý tưởng lập trình thành dự án thực tế thông qua bộ công cụ tích hợp của dịch vụ thông qua trình duyệt web hoặc app trên máy tính. Mặc định bạn có thể tạo và lưu trữ các dự án Python qua Replit một cách công khai và miễn phí. Bạn cần trả phí để có thể bảo mật mã nguồn dự án của mình với phí $120/năm hoặc $20/tháng.

![](../../assets/images/moi-truong-lap-trinh-python-mien-phi-voi-Replit.png)
Điểm thú vị của Replit là nó cung cấp công cụ AI ngay trong môi trường lập trình giúp bạn code "nhàn" hơn và tiết kiệm.
## Python trên máy tính cục bộ

### Python thuần

> Python "thuần" tức chỉ cài đặt gói phần mềm Python và cài đặt riêng lẻ các thư viện kèm theo khi cần thiết (bao gồm cả Jupyter Lab/Notebook cho phân tích dữ liệu). Điều này khác với việc cài gói Anaconda bao gồm hầu hết các thư viện python (package) dù bạn có sử dụng tới hay không. Cách tiếp cận này giúp bạn tiết kiệm dung lượng bộ nhớ máy khi máy tính có cấu hình phần cứng không mạnh mẽ vượt trội. 

### Python với Anaconda

> Anaconda là một gói phần mềm cho ngôn ngữ lập trình Python và R dành cho mục đích tính toán khoa học. Gói cài đặt Anaconda chứa hầu hết các thư viện Python phổ biến bạn cần dùng cho dự án của mình. Do đó cài Anaconda bạn có thể bỏ qua bước cài đặt các thư viện phụ thuộc. Đối với các bạn sử dụng Python cho phân tích dữ liệu thì chọn cách tiếp cận này giúp bạn có được môi trường sử dụng Python đầy đủ và nhanh chóng.

