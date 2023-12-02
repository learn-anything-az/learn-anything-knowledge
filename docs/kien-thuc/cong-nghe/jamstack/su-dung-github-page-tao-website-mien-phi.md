---
date: 2023-12-02
title: su-dung-github-page-tao-website-mien-phi
aliases:
  - Sử dụng tính năng Github Pages để để tạo và chia sẻ trang web miễn phí.
description: Tạo một website và chia sẻ hoàn toàn miễn phí với Github Pages từ một kho chứa mã nguồn Github (repository).
tags:
  - jamstack
  - github pages
  - blog
categories:
  - Hướng dẫn
authors:
  - thinh-vu
---

!!! abstract "Github Pages là gì?"
	**[Github Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages)** cho phép bạn chia sẻ (host) một trang web cá nhân/tổ chức hay dự án của mình từ một kho chứa mã nguồn Github (repository, gọi tắt là repo) một cách nhanh chóng và miễn phí.

Bản chất của **[Github Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages)** là một nền tảng lưu trữ và chia sẻ các website  (hosting), sử dụng các file HTML, CSS, và JavaScript trực tiếp từ một repo Github. Bạn có thể tạo ra các file mã nguồn này thông qua quá trình "tạo" trang web (build process) sử dụng các công cụ tạo trang web tĩnh như Jekyll.

Bạn có nhiều lựa chọn về công cụ tạo trang web tĩnh, trong đó có thể kể đến [Jekyll](https://jekyllrb.com/), [Gatsby](https://www.gatsbyjs.com/), [MkDocs Material](https://squidfunk.github.io/mkdocs-material/), [Docusaurus](https://docusaurus.io/), [Gitbook](https://www.gitbook.com/), JetBrain [Writerside](https://www.jetbrains.com/help/writerside/discover-writerside.html), vv.
Mỗi một công cụ sẽ có ưu và nhược điểm khác nhau do đó công cụ phù hợp cho bạn là công cụ có thể đáp ứng được yêu cầu của dự án bạn theo đuổi một cách tốt nhất.

Bạn có thể tham khảo một số trang web mà tôi tạo ra và đang sử dụng thực tế với Github Pages dưới đây:

- **[Trang tài liệu dự án vnstock](http://docs.vnstock.site/)** và chính trang [Learn Anything](http://learn-anything.vn/) này, đang sử dụng MkDocs Material
- Trang web **[learn-anything.online](http://learn-anything.online/)** phong cách Blog sử dụng [Jekyll](https://jekyllrb.com/) theme [YAT](https://github.com/jeffreytse/jekyll-theme-yat)