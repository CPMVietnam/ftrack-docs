# ftrack-docs

Tài liệu hướng dẫn sử dụng cho [ftrack.vn](https://ftrack.vn) — nền tảng quản lý field force toàn diện cho doanh nghiệp.

🌐 **Live site**: [docs.ftrack.vn](https://docs.ftrack.vn)

## Tổng quan

Repo này chứa source markdown cho documentation site của Ftrack, bao gồm:

- **Chuẩn bị dữ liệu** — Danh sách điểm bán, tài khoản nhân viên, chương trình khảo sát, kế hoạch viếng thăm
- **Cài đặt hệ thống** — Cấu hình chung, tài khoản, hình ảnh, chương trình, bán hàng, POSM, kiểm soát chất lượng
- **Ứng dụng mobile** — Hướng dẫn cho nhân viên thị trường: Check In/Out, khảo sát, tạo cửa hàng, báo cáo
- **Báo cáo & Dữ liệu** — Danh sách thực hiện, đơn hàng, tài sản, lộ trình nhân viên, biểu đồ

## Tech Stack

| Thành phần | Công cụ |
|-----------|---------|
| Site Generator | [MkDocs Material](https://squidfunk.github.io/mkdocs-material/) |
| Hosting | GitHub Pages |
| Custom Domain | `docs.ftrack.vn` |
| CI/CD | GitHub Actions |
| Ngôn ngữ | Vietnamese (mặc định) + English |
| Image Hosting | Cloudflare R2 |
| Editor | Obsidian (markdown editing local) |

## Bắt đầu nhanh

### Yêu cầu

- Python 3.9+
- pip

### Chạy local

```bash
# Cài dependencies
pip install -r requirements.txt

# Chạy dev server (http://localhost:8000)
mkdocs serve
```

### Build

```bash
mkdocs build
```

Output sẽ nằm trong thư mục `site/`.

## Cấu trúc dự án

```
docs/
├── vi/                     # Tài liệu Tiếng Việt (mặc định)
│   ├── index.md            # Trang chủ
│   ├── login.md            # Đăng nhập hệ thống
│   ├── prepare-data/       # I. Chuẩn bị dữ liệu
│   ├── settings/           # II. Cài đặt
│   ├── mobile-app/         # III. Sử dụng ứng dụng
│   ├── reports/            # IV. Dữ liệu thực hiện
│   └── faq.md
└── en/                     # English docs (cấu trúc y hệt vi/)
    └── ...
```

## Hướng dẫn đóng góp

### Viết nội dung

- Viết cho người dùng cuối (nhân viên văn phòng, quản lý, nhân viên thị trường)
- Mỗi trang 1 chủ đề, heading rõ ràng
- Dùng hướng dẫn step-by-step cho các thao tác
- Vietnamese: dùng "bạn", thân thiện nhưng chuyên nghiệp
- English: dùng "you", active voice

### Hình ảnh

Hình ảnh được host trên Cloudflare R2, **không commit vào repo**. Sử dụng format:

```markdown
![Mô tả screenshot](https://img.ftrack.vn/docs/section/filename.png)
```

Placeholder cho hình chưa có:

```markdown
<!-- TODO: screenshot - mô tả ngắn -->
```

### Markdown

- Dùng standard markdown links, **không** dùng Obsidian wiki-links
- Heading nội dung bắt đầu từ `##`
- Sử dụng [admonitions](https://squidfunk.github.io/mkdocs-material/reference/admonitions/) cho tips và warnings

## Triển khai (Deploy)

Triển khai tự động qua GitHub Actions. Push vào branch `main` sẽ trigger build và deploy lên GitHub Pages với custom domain `docs.ftrack.vn`.

### Cách hoạt động

1. Push code lên `main`
2. GitHub Actions chạy `mkdocs build`
3. Output HTML được deploy lên GitHub Pages
4. Site tự động cập nhật tại `docs.ftrack.vn`

### Setup custom domain (1 lần duy nhất)

1. Trong repo GitHub: Settings → Pages → Custom domain → nhập `docs.ftrack.vn`
2. Bên Cloudflare DNS: thêm CNAME record `docs` → `<github-username>.github.io`
3. GitHub tự cấp SSL certificate

## License

© 2025 VNMARKETER Co., Ltd. All rights reserved.
