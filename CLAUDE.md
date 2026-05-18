# CLAUDE.md — ftrack-docs

## Dự án là gì

Documentation site cho [ftrack.vn](https://ftrack.vn) — nền tảng quản lý field force, HR và in-store cho doanh nghiệp tại Việt Nam. Remake lại bộ hướng dẫn sử dụng hiện tại (đang nằm trong admin panel tại `https://ftrack.vn/admin/?route=publish/docs`) thành static site phục vụ tại `docs.ftrack.vn` qua GitHub Pages.

## Tech Stack

- **MkDocs Material** — static site generator từ markdown
- **GitHub Pages** — hosting, custom domain `docs.ftrack.vn`
- **GitHub Actions** — CI/CD tự build khi push vào `main`
- **Obsidian** — markdown editor (local), dùng để review/edit nội dung
- **Cloudflare R2** — host hình ảnh, reference bằng URL trong markdown
- **Bilingual**: Vietnamese (mặc định) + English, dùng MkDocs i18n plugin

## Cấu trúc docs cũ (tham khảo)

Docs cũ có 11 tài liệu, chia theo 2 ngôn ngữ. Cấu trúc chính gồm 4 phần lớn:

### PHẦN I — CHUẨN BỊ DỮ LIỆU (Prepare Data)
Thông tin bắt buộc để thiết lập một dự án/chương trình khảo sát trên Ftrack:
1. Danh sách điểm bán/cửa hàng — import file danh sách điểm bán vào hệ thống
2. Danh sách nhân viên/tài khoản — tạo và quản lý tài khoản nhân viên
3. Tạo bộ câu hỏi/chương trình khảo sát — thiết lập survey/program
4. Kế hoạch viếng thăm (Visit Plan) — lên lịch viếng thăm cho nhân viên

### PHẦN II — CÀI ĐẶT (Setting)
1. Cài đặt chung
2. Cài đặt tài khoản
3. Quản lý tài khoản
4. Cài đặt hình ảnh
5. Tình trạng ghé thăm (Visit Status)
6. Tạo điểm bán/cửa hàng
7. Cài đặt chương trình
8. Import Visit
9. Bán hàng
10. Tài sản/POSM
11. Kiểm soát chất lượng
12. Thiết lập thông tin

### PHẦN III — CẬP NHẬT THÔNG TIN TỪ ỨNG DỤNG (Update Data on App)
Hướng dẫn cho nhân viên thị trường thực hiện trên app mobile:
1. Đăng nhập
2. Check In
3. Thực hiện khảo sát
4. Check Out
5. Map
6. Tạo cửa hàng/điểm bán mới trên app
7. Tạo Visit Plan trên danh sách cửa hàng có sẵn
8. Xóa dữ liệu đang thực hiện
9. Chức năng chia sẻ dữ liệu khi thực hiện
10. Yêu cầu nhập liệu trong Survey

### PHẦN IV — DỮ LIỆU THỰC HIỆN (Report)
1. Danh sách thực hiện
2. Danh sách cửa hàng
3. Quản lý đơn hàng
4. Quản lý tài sản
5. Lộ trình nhân viên
6. Biểu đồ
7. Map
8. Báo cáo

### Tài liệu bổ sung
- 0. Đăng nhập hệ thống (Login)

## Cấu trúc thư mục mới

```
ftrack-docs/
├── docs/
│   ├── vi/                              # Vietnamese (default)
│   │   ├── index.md                     # Trang chủ — giới thiệu Ftrack
│   │   ├── login.md                     # Đăng nhập hệ thống
│   │   ├── prepare-data/                # Phần I: Chuẩn bị dữ liệu
│   │   │   ├── index.md                 # Tổng quan chuẩn bị dữ liệu
│   │   │   ├── store-list.md            # 1. Danh sách điểm bán
│   │   │   ├── staff-accounts.md        # 2. Danh sách nhân viên/tài khoản
│   │   │   ├── survey-program.md        # 3. Tạo bộ câu hỏi/chương trình khảo sát
│   │   │   └── visit-plan.md            # 4. Kế hoạch viếng thăm
│   │   ├── settings/                    # Phần II: Cài đặt
│   │   │   ├── index.md                 # Tổng quan cài đặt
│   │   │   ├── general.md               # 1. Cài đặt chung
│   │   │   ├── account-settings.md      # 2. Cài đặt tài khoản
│   │   │   ├── account-management.md    # 3. Quản lý tài khoản
│   │   │   ├── image-settings.md        # 4. Cài đặt hình ảnh
│   │   │   ├── visit-status.md          # 5. Tình trạng ghé thăm
│   │   │   ├── store-setup.md           # 6. Tạo điểm bán/cửa hàng
│   │   │   ├── program-settings.md      # 7. Cài đặt chương trình
│   │   │   ├── import-visit.md          # 8. Import Visit
│   │   │   ├── sales.md                 # 9. Bán hàng
│   │   │   ├── posm-assets.md           # 10. Tài sản/POSM
│   │   │   ├── quality-control.md       # 11. Kiểm soát chất lượng
│   │   │   └── info-setup.md            # 12. Thiết lập thông tin
│   │   ├── mobile-app/                  # Phần III: Sử dụng ứng dụng
│   │   │   ├── index.md                 # Tổng quan
│   │   │   ├── login.md                 # 1. Đăng nhập app
│   │   │   ├── check-in.md              # 2. Check In
│   │   │   ├── survey.md                # 3. Thực hiện khảo sát
│   │   │   ├── check-out.md             # 4. Check Out
│   │   │   ├── map.md                   # 5. Map
│   │   │   ├── create-store.md          # 6. Tạo cửa hàng mới trên app
│   │   │   ├── create-visit-plan.md     # 7. Tạo Visit Plan trên app
│   │   │   ├── delete-data.md           # 8. Xóa dữ liệu đang thực hiện
│   │   │   ├── share-data.md            # 9. Chia sẻ dữ liệu
│   │   │   └── survey-requirements.md   # 10. Yêu cầu nhập liệu trong Survey
│   │   ├── reports/                     # Phần IV: Dữ liệu thực hiện
│   │   │   ├── index.md                 # Tổng quan báo cáo
│   │   │   ├── execution-list.md        # 1. Danh sách thực hiện
│   │   │   ├── store-list.md            # 2. Danh sách cửa hàng
│   │   │   ├── order-management.md      # 3. Quản lý đơn hàng
│   │   │   ├── asset-management.md      # 4. Quản lý tài sản
│   │   │   ├── employee-route.md        # 5. Lộ trình nhân viên
│   │   │   ├── charts.md               # 6. Biểu đồ
│   │   │   ├── map.md                   # 7. Map
│   │   │   └── report.md               # 8. Báo cáo
│   │   └── faq.md                       # Câu hỏi thường gặp
│   └── en/                              # English (mirror 1:1 với vi/)
│       ├── index.md
│       ├── login.md
│       ├── prepare-data/
│       ├── settings/
│       ├── mobile-app/
│       ├── reports/
│       └── faq.md
├── overrides/                           # MkDocs Material theme overrides
├── mkdocs.yml                           # MkDocs config chính
├── requirements.txt                     # mkdocs-material + plugins
├── .github/
│   └── workflows/
│       └── deploy.yml                   # GitHub Actions: build & deploy
├── .gitignore
├── CLAUDE.md                            # File này
└── README.md
```

## Quy tắc viết docs

### Ngôn ngữ
- **Vietnamese** là ngôn ngữ mặc định, viết trước
- **English** là bản dịch, cấu trúc mirror 1:1 với Vietnamese
- Mỗi file `.md` trong `vi/` phải có file tương ứng trong `en/`

### Tone & Style
- Viết cho 2 nhóm user:
  - **Admin/Quản lý**: người setup hệ thống, chuẩn bị dữ liệu, xem báo cáo (Phần I, II, IV)
  - **Nhân viên thị trường**: người dùng app mobile tại điểm bán (Phần III)
- Ngôn ngữ đơn giản, trực tiếp, tránh thuật ngữ kỹ thuật khi không cần
- Mỗi trang tập trung 1 chủ đề
- Dùng step-by-step cho hướng dẫn thao tác (B1, B2, B3...)
- Vietnamese: dùng "bạn", thân thiện nhưng chuyên nghiệp
- English: dùng "you", active voice
- Giữ lại các thuật ngữ chuyên ngành không dịch: Check In, Check Out, Visit Plan, POSM, Survey, Map

### Hình ảnh
- Hình ảnh host trên **Cloudflare R2**, KHÔNG commit vào repo
- URL format: `https://img.ftrack.vn/docs/{section}/{tên-file}.png`
  - Ví dụ: `https://img.ftrack.vn/docs/prepare-data/import-store-list.png`
- Placeholder cho hình chưa có: `<!-- TODO: screenshot - {mô-tả ngắn} -->`
- Alt text bắt buộc cho mọi hình: `![Màn hình import danh sách điểm bán](https://img.ftrack.vn/docs/...)`
- Docs cũ có rất nhiều screenshot hướng dẫn từng bước — cần giữ lại approach này

### Markdown conventions
- Dùng standard markdown links `![alt](url)`, KHÔNG dùng Obsidian wiki-links `![[]]`
- Heading bắt đầu từ `##` trong nội dung (H1 do MkDocs tự render từ title)
- Dùng admonitions cho tips/warnings:
  ```markdown
  !!! tip "Mẹo"
      Nội dung tip ở đây.
  
  !!! warning "Lưu ý"
      Nội dung cảnh báo.
  
  !!! info "Thông tin"
      Nội dung bổ sung.
  ```
- Dùng numbered steps cho quy trình:
  ```markdown
  **Bước 1:** Vào Cài đặt → Chọn mục Tạo điểm bán/Cửa hàng
  
  **Bước 2:** Tải template mẫu về trên hệ thống
  
  **Bước 3:** Điền thông tin và upload file lên hệ thống
  ```

## Workflow với Claude Code

### Session 1: Khởi tạo dự án
```
Khởi tạo project MkDocs Material với bilingual support (vi/en). 
Tạo mkdocs.yml, requirements.txt, .gitignore, GitHub Actions deploy workflow.
Custom domain: docs.ftrack.vn. Default language: vi.
```

### Session 2: Scaffold toàn bộ cấu trúc trang
```
Tạo toàn bộ file .md theo cấu trúc trong CLAUDE.md (cả vi/ và en/). 
Mỗi file chứa front matter + heading + placeholder nội dung.
Cấu hình navigation trong mkdocs.yml theo đúng thứ tự 4 phần.
```

### Session 3: Viết nội dung Phần I — Chuẩn bị dữ liệu
```
Viết nội dung chi tiết cho docs/vi/prepare-data/ và docs/en/prepare-data/.
Tham khảo cấu trúc docs cũ trong CLAUDE.md phần "Cấu trúc docs cũ".
Dùng placeholder cho screenshots: <!-- TODO: screenshot - mô tả -->
```

### Session 4: Viết nội dung Phần II — Cài đặt
```
Viết nội dung chi tiết cho docs/vi/settings/ và docs/en/settings/.
12 trang con. Tham khảo cấu trúc docs cũ.
```

### Session 5: Viết nội dung Phần III — Ứng dụng mobile
```
Viết nội dung chi tiết cho docs/vi/mobile-app/ và docs/en/mobile-app/.
10 trang con. Đây là phần dành cho nhân viên thị trường, tone đơn giản hơn.
```

### Session 6: Viết nội dung Phần IV — Báo cáo
```
Viết nội dung chi tiết cho docs/vi/reports/ và docs/en/reports/.
8 trang con. Dành cho admin/quản lý.
```

### Session 7: Trang chủ, Login, FAQ
```
Viết docs/vi/index.md, docs/vi/login.md, docs/vi/faq.md 
và bản English tương ứng.
```

### Session 8: Review & Polish
```
Review toàn bộ nội dung, fix broken links, kiểm tra navigation,
đảm bảo bilingual consistency, test mkdocs serve.
```

## Tham khảo docs cũ

- Danh sách docs: `https://ftrack.vn/admin/?route=publish/docs`
- Từng trang: `https://ftrack.vn/admin/?route=publish/docs/info&doc_id={ID}`
  - Vietnamese: doc_id = 1, 2, 3, 4, 5, 11
  - English: doc_id = 6, 7, 8, 9, 10
- Trang docs cũ KHÔNG cần login (route `publish/docs`, không phải `tool/docs`)

## Lưu ý cho Claude Code sessions

1. Đọc CLAUDE.md này đầu tiên mỗi session — nó chứa toàn bộ context
2. Khi viết nội dung, luôn tạo cả bản `vi/` và `en/` cùng lúc
3. Nếu chưa biết chi tiết tính năng, viết cấu trúc + placeholder rõ ràng
4. Không bịa tính năng — nếu không chắc, đánh dấu `<!-- TODO: verify -->`
5. Hình ảnh dùng placeholder `<!-- TODO: screenshot - {mô tả} -->`
6. Mỗi session nên focus 1 phần (I/II/III/IV), không cố viết hết cùng lúc
7. Test `mkdocs serve` sau khi thay đổi để đảm bảo build không lỗi
8. Giữ lại thuật ngữ chuyên ngành: Check In, Check Out, Visit Plan, POSM, Survey

## Commands

```bash
# Setup
pip install -r requirements.txt

# Local preview
mkdocs serve                    # http://localhost:8000

# Build
mkdocs build                    # Output → site/

# Deploy (tự động qua GitHub Actions khi push main)
git push origin main
```
