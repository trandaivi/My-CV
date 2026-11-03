# Portfolio cá nhân - Trần Đại Vĩ

## Mô tả

Trang portfolio cá nhân giới thiệu Trần Đại Vĩ, Frontend Developer. Dự án được xây dựng dưới dạng website tĩnh, trình bày thông tin cá nhân, kỹ năng, một số dự án tiêu biểu và các kênh liên hệ.

## Chức năng

- Hiển thị phần giới thiệu và ảnh đại diện.
- Trình bày danh sách kỹ năng và các thẻ dự án mẫu.
- Điều hướng đến các phần Giới thiệu, Kỹ năng, Dự án và Liên hệ bằng liên kết trong trang.
- Giao diện responsive, ưu tiên thiết bị di động và tự điều chỉnh trên màn hình lớn.
- Có liên kết email, GitHub và LinkedIn.

> Đây là website tĩnh dùng để giới thiệu portfolio; không có máy chủ, cơ sở dữ liệu hay bước biên dịch. Các liên kết “Xem chi tiết” trong thẻ dự án hiện là liên kết mẫu.

## Công nghệ

- HTML5: cấu trúc nội dung và các liên kết điều hướng.
- CSS3: giao diện, bố cục Flexbox/Grid, thiết kế responsive và hiệu ứng trình bày.
- Không sử dụng framework, thư viện JavaScript hay công cụ đóng gói.

## Cấu trúc dự án

```text
KT A2.1/
├── index.html
├── README.md
└── assets/
    ├── css/
    │   └── styles.css
    └── img/
        └── avatar.jpg
```

## Yêu cầu môi trường

- Trình duyệt hiện đại như Google Chrome, Microsoft Edge, Firefox hoặc Safari.
- Để mở trực tiếp: không cần cài thêm phần mềm.
- Để chạy máy chủ cục bộ: Python 3 (hoặc tiện ích Live Server trong Visual Studio Code).
- Để chạy bằng Docker: Docker Engine hoặc Docker Desktop đang hoạt động.
- Không cần Node.js, npm hay cài đặt thư viện.

## Cài đặt

1. Tải hoặc sao chép toàn bộ thư mục dự án về máy.
2. Đảm bảo giữ nguyên cấu trúc thư mục, đặc biệt là `assets/css/styles.css` và `assets/img/avatar.jpg`.
3. Mở thư mục dự án trong Terminal/PowerShell hoặc Visual Studio Code.

Nếu dự án được lấy từ Git, thay `<URL-repository>` bằng địa chỉ repository:

```bash
git clone <URL-repository>
cd "KT A2.1"
```

Nếu đã tải tệp ZIP, hãy giải nén rồi mở thư mục chứa `index.html`.

## Cấu hình và tùy chỉnh

Dự án không có tệp cấu hình môi trường hoặc khóa API.

- Nội dung giới thiệu, kỹ năng, dự án và thông tin liên hệ: chỉnh sửa trong `index.html`.
- Màu sắc, kiểu chữ, khoảng cách và bố cục: chỉnh sửa trong `assets/css/styles.css`.
- Ảnh đại diện: thay `assets/img/avatar.jpg` hoặc cập nhật đường dẫn ảnh trong `index.html`.
- Khi thay ảnh, nên giữ đường dẫn tương đối hợp lệ và cập nhật nội dung `alt` để hỗ trợ khả năng truy cập.

## Chạy thử

Chọn một trong các cách sau. Với mọi hệ điều hành, hãy chạy lệnh tại thư mục chứa `index.html`.

### Cách nhanh: mở trực tiếp

Nhấp đúp vào `index.html`, hoặc mở tệp này từ trình duyệt. Cách này phù hợp để xem trang cơ bản; máy chủ cục bộ được khuyến nghị nếu sau này dự án cần tải tài nguyên hoặc tính năng phụ thuộc HTTP.

### Windows

**Dùng Python 3** — mở PowerShell tại thư mục dự án và chạy:

```powershell
py -m http.server 8000
```

Nếu lệnh `py` không có nhưng đã cài Python:

```powershell
python -m http.server 8000
```

### macOS

Mở Terminal tại thư mục dự án và chạy:

```bash
python3 -m http.server 8000
```

### Linux

Mở Terminal tại thư mục dự án và chạy:

```bash
python3 -m http.server 8000
```

Trên Windows, macOS hoặc Linux, sau khi máy chủ khởi động, mở <http://localhost:8000> trong trình duyệt. Dừng máy chủ bằng `Ctrl+C`.

### Chạy với Visual Studio Code

1. Mở thư mục dự án trong Visual Studio Code.
2. Cài tiện ích **Live Server** nếu máy chưa có.
3. Nhấp chuột phải vào `index.html` và chọn **Open with Live Server**.

### Docker

Cần cài và khởi động Docker trước. Chạy lệnh từ thư mục dự án để phục vụ trang bằng Nginx:

**Windows PowerShell**

```powershell
docker run --rm --name portfolio-cv -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

**macOS / Linux**

```bash
docker run --rm --name portfolio-cv -p 8080:80 -v "$(pwd):/usr/share/nginx/html:ro" nginx:alpine
```

Lần chạy đầu tiên, Docker có thể cần tải image `nginx:alpine`. Khi container đang chạy, mở <http://localhost:8080>. Dừng bằng `Ctrl+C`; tùy chọn `--rm` sẽ tự xóa container sau khi dừng. Lệnh trên mount thư mục dự án chỉ-đọc và không yêu cầu tạo Dockerfile.

## Thông tin liên hệ

- **Tác giả:** Trần Đại Vĩ
- **Email:** [trdaivi2911@gmail.com](mailto:trdaivi2911@gmail.com)
- **GitHub:** [github.com/trandaivi](https://github.com/trandaivi)
- **LinkedIn:** [linkedin.com/in/trandaivi](https://linkedin.com/in/trandaivi)