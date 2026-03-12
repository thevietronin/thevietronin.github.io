# Blog — Hugo + PaperMod

Site dùng [Hugo](https://gohugo.io/) và theme [PaperMod](https://github.com/adityatelange/hugo-PaperMod) (cài qua **Hugo Modules**).

## Chạy site

```bash
hugo server -D
```

Mở http://localhost:1313

## Cập nhật theme PaperMod (auto update từ tác giả)

Theme được lấy trực tiếp từ repo của tác giả, không copy vào `themes/`. Để luôn dùng bản mới nhất:

```bash
hugo mod get -u
```

Sau đó build lại: `hugo` hoặc `hugo server`.

- Cập nhật tất cả module (gồm theme): `hugo mod get -u`
- Chỉ cập nhật PaperMod: `hugo mod get -u github.com/adityatelange/hugo-PaperMod`

## Tạo bài viết mới

```bash
hugo new posts/ten-bai-viet.md
```

Chỉnh front matter trong file (tags, author, cover, v.v.) theo [Variables / Front Matter](https://github.com/adityatelange/hugo-PaperMod/wiki/Variables).

## Cấu hình

- **hugo.toml** — toàn bộ cấu hình site và params của PaperMod (profile mode, home-info, menu, search, analytics, v.v.).
- Bật **profile mode** hoặc **home-info**: sửa `[params.profileMode]` / `[params.homeInfoParams]` trong `hugo.toml`.
- Thêm/xóa mục menu: sửa `[menu.main]` trong `hugo.toml`.

Tài liệu đầy đủ: [PaperMod Wiki](https://github.com/adityatelange/hugo-PaperMod/wiki).
# thevietronin.github.io
