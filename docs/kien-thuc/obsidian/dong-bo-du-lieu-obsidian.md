---
date: 2023-11-21
title: Đồng bộ dữ liệu cho Obsidian trên nhiều thiết bị
description: Hướng dẫn cách đồng bộ dữ liệu trên các thiết bị khác nhau dùng Obsidian.
tags:
  - obsidian
  - thiết lập ban đầu
categories:
  - Hướng dẫn
authors:
  - thinh-vu
---
## Đồng bộ máy tính với đám mây

### macOS

Nếu bạn sử dụng Obsidian trên thiết bị iOS, macOS của Apple thì iCloud là lựa chọn duy nhất để đồng bộ Obsidian với các thiết bị khác nhau từ macbook tới cloud và iphone. Các bước thực hiện như sau:

1. Tạo Obsidian vault là thư mục chứa các ghi chú của bạn trong iCloud folder (mở bằng Finder)
2. Chọn `Open folder as Vault` trong Obsidian sau đó chọn thư mục bạn vừa tạo với iCloud để sử dụng.

Bạn có thể lựa chọn sử dụng thư mục cấu hình sẵn Obsidian Go V3 mà tôi chia sẻ để bắt đầu  nhanh. Chỉ cần giải nén file và copy toàn bộ thư mục được chia sẻ vào vị trí bạn muốn lưu trữ trong iCloud rồi `Open folder as vault` từ Obsidian để sử dụng.

<figure markdown>
 ![Chọn thư mục lưu trữ ghi chú trong Obsidian. Open as Vault](https://thinhvu.com/wp-content/uploads/2023/01/Obsidian-open-folder-as-vaultjpg-scaled.jpg)
  <figcaption>Chọn thư mục lưu trữ ghi chú trong Obsidian. Open as Vault</figcaption>
</figure>

### Windows/Linux

Bạn có thể sử dụng dịch vụ [OneDrive](https://www.microsoft.com/vi-vn/microsoft-365/onedrive/download) được tích hợp sẵn vào hệ điều hành Windows để đồng bộ dữ liệu. Các bước thực hiện đồng bộ tương tự như với macOS, trong trường hợp này nơi lưu trữ thư mục Obsidian là OneDrive thay vì iCloud. Tải OneDrive để cài đặt [tại đây](https://www.microsoft.com/vi-vn/microsoft-365/onedrive/download).

Nếu bạn sử dụng Google Drive hay để đồng bộ dữ liệu thì sẽ cần cài [ứng dụng Google Drive trên máy tính](https://www.google.com/drive/download/) của mình, các bước thực hiện tương tự như Onedrive và iCloud. 

## Đồng bộ thiết bị di động với đám mây

### iPhone/iPad

Cài đặt Obsidian trên iPhone/iPad và mở thư mục Obsidian từ bộ nhớ iCloud trên máy để sử dụng.

### Android

Bạn có thể chọn một ứng dụng của bên thứ 3 như:

- [Folder Sync](https://play.google.com/store/apps/details?id=dk.tacit.android.foldersync.lite&hl=en_US) cho phép sử dụng miễn phí kèm quảng cáo hoặc trả phí với giá phải chăng (~100K)
- [Drop Sync](https://play.google.com/store/apps/details?id=com.ttxapps.dropsync). 

Các dịch vụ như OneDrive, Google Drive, vv không hỗ trợ đồng bộ dữ liệu theo một thư mục cụ thể trên thiết bị di động, do đó bạn cần dùng dịch vụ của bên thứ 3 như trên.

Dưới đây là video tôi hướng dẫn cụ thể cách thiết lập đồng bộ Folder Sync với Onedrive.

<iframe width="940" height="529" src="https://www.youtube.com/embed/aW5Xn2Y3VfE?si=k9PCfL39RvRIHmmP" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
