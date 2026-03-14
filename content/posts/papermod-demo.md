---
title: "PaperMod Demo — Full Features"
date: 2025-03-12T10:00:00+07:00
tags: ["papermod", "demo", "hugo"]
categories: ["Tech", "Hugo"]
author: "Me"

showToc: true
tocOpen: false
draft: false
hidemeta: false
comments: false
description: "Bài viết mẫu dùng gần như full tính năng PaperMod: cover, TOC, code block, search, share, breadcrumbs…"
canonicalURL: "https://thevietronin.github.io/posts/papermod-demo/"

disableHLJS: false
disableShare: false
hideSummary: false
searchHidden: false

ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true

cover:
  image: "images/papermod-demo-cover.png"
  alt: "Minh hoạ PaperMod demo cover"
  relative: false
  hidden: false
---

## 1. Giới thiệu

Đây là **bài viết demo** để bạn thấy hầu hết tính năng của theme PaperMod hoạt động như thế nào:

- Cover image ở trên đầu bài.
- Bảng mục lục (TOC) tự động.
- Breadcrumbs, thời gian đọc, số chữ, share button, điều hướng bài trước/sau.
- Code block có nút copy.
- Tìm kiếm full‑text bằng Fuse.js.

Các thiết lập chính nằm trong `hugo.toml` (`[params]` và `params.fuseOpts`) theo tài liệu PaperMod [Features](https://github.com/adityatelange/hugo-PaperMod/wiki/Features).

## 2. Mục lục (TOC) và heading

Vì `showToc: true` và `UseHugoToc: true`, mọi heading cấp 2/3 trong bài sẽ xuất hiện ở TOC bên cạnh.

### 2.1. Heading cấp 3

Đoạn này chỉ để TOC có thêm mục nhỏ hơn.

## 3. Code block + nút copy

Với `ShowCodeCopyButtons = true` trong `hugo.toml`, mọi code block sẽ có nút **copy**.

```bash
hugo new posts/another-post.md
hugo server -D
```

```toml
[params]
  ShowReadingTime = true
  ShowCodeCopyButtons = true
```

## 4. Cover image

Phần `cover` trong front matter:

- `image`: đường dẫn ảnh (có thể là URL tuyệt đối hoặc trong `static/`).
- `alt`: text mô tả cho SEO và accessibility.
- `caption`: chú thích dưới ảnh.
- `hidden`: `false` để hiển thị cover trên trang bài.

Bạn có thể đặt file thật trong `static/images/papermod-demo-cover.png` để cover hiển thị đúng khi deploy.

## 5. Breadcrumbs, thời gian đọc, số chữ

Các flag:

- `ShowBreadCrumbs: true`
- `ShowReadingTime: true`
- `ShowWordCount: true`

giúp PaperMod render thêm **breadcrumb** phía trên tiêu đề, thời gian đọc ước lượng và số chữ dưới meta.

## 6. Search và hiển thị trong kết quả

Vì:

- `searchHidden: false` trong front matter, và
- `params.fuseOpts` đã cấu hình trong `hugo.toml`,

bài viết này sẽ xuất hiện trong trang **Search** (`/search/`) khi bạn gõ từ khóa trùng với `title`, `summary` hoặc nội dung bài (Fuse.js sẽ xử lý).

## 7. Điều hướng bài và share buttons

Các flag:

- `ShowPostNavLinks: true`
- `ShowShareButtons: true`

làm xuất hiện block điều hướng **Previous / Next** và các nút share (X, LinkedIn, Facebook, v.v.) ở cuối bài.

Khi bạn thêm nhiều bài hơn, điều hướng này sẽ nối các bài lại với nhau theo thời gian.

