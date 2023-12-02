---
date: 2023-12-02
title: Tạo trang blog cá nhân đẹp và đơn giản với Jekyll YAT theme và Github Pages
aliases:
  - Tạo trang blog cá nhân đẹp và đơn giản với Jekyll YAT theme và Github Pages
description: Chia sẻ các bài viết từ Obsidian lên blog sử dụng Jekyll YAT theme và Github Pages hoàn toàn miễn phí
tags:
  - jamstack
  - obsidian
  - blog
categories:
  - Hướng dẫn
authors:
  - thinh-vu
---

## Cài đặt Jekyll
Xem chi tiết tại [Cài đặt công cụ tạo trang tĩnh Jekyll](cai-dat-cong-cu-tao-trang-web-tinh-jekyll-ssg.md)

## YAT theme

> Để sao chép giao diện đang hiển thị của trang web này, bạn có thể clone mã nguồn github [tại đây](https://github.com/thinh-vu/learn-anything)

Bạn cũng có thể truy cập trang dự án của giao diện nguyên bản trên Github: [yekyll theme yat](https://jeffreytse.github.io/jekyll-theme-yat/about.html)

### Thiết lập
- File `Gemfile` chứa thông tin thiết lập về theme được sử dụng, các gói phụ thuộc cần được chỉ rõ. Trong hướng dẫn ban đầu tác giả nêu không đầy đủ do đó khi sử dụng sẽ gặp lỗi khi thiết lập và người dùng không có kinh nghiệm sẽ loay hoay.
- File `_config.yml` chứa tất cả các cài đặt cho site. Uncomment và thay thế các giá trị mặc định để cập nhật.
- Chạy lệnh `bundle install` để cài đặt các gói phụ thuộc
- Cuối cùng, chạy lệnh `bundle exec jekyll serve` để chạy local server và xem trước nội dung để có thể tùy biến trang web.
- Để build (generate site) tại môi trường local, chạy lệnh `bundle exec jekyll build` từ thư mục dự án. Khi chạy lệnh buid, các thay đổi tự động được gán cho nhánh `gh-` 
### Build local hay github action và github page?
- Nên sử dụng local mặc dù mất công thiết lập môi trường (1 lần), về sau chạy lệnh build nhanh chóng và cho phép preview trang để dễ dàng debug. Sau khi thành công hãy push vào 1 nhánh riêng và đẩy lên github page branch để hiển thị.
- Github page chạy mất thời gian, không thể preview, lỗi thì khó debug hơn hoặc reverse lại phiên bản cũ.

### Tính năng
#### Viết bài
- Diagram: Có thể sử dụng [PlantUML](https://plantuml.com/guide) hoặc Mermaid
- Table: Hỗ trợ nhiều cài đặt như gộp ô, headless
- Hỗ trợ đa dạng các cú pháp markdown cơ bản lẫn nâng cao.

#### Giao diện
- Đặt properties `sidebar: []` để ẩn TOC bên phải
- Cấu hình sidebar tại file `article_menu` tại đường dẫn `jekyll-theme-yat\_includes\sidebar`
- Thay đổi tên `Dark/Light` thành `Tối/Sáng` tại file `jekyll-theme-yat/_includes/extensions/theme-toggle.html`
- Thay đổi màu sắc chủ đạo cho theme trong `_config.yml`

#### Theo dõi & phân tích website
- Sửa đổi đoạn mã theo dõi GA thành GTM (nếu cần) tại file `jekyll-theme-yat/_includes/extensions/google-analytics.html`

## Thiết lập tên miền riêng