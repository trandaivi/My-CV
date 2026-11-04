# BÁO CÁO KIỂM THỬ VÀ ĐỐI CHIẾU TRƯỚC BÀN GIAO

## 1. Thông tin chung

| Thông tin | Chi tiết |
|---|---|
| Tên dự án | Portfolio cá nhân — Trần Đại Vĩ |
| Phiên bản đối chiếu | v1.0 |
| Ngày kiểm thử | 05/11/2026 |
| Người thực hiện/đánh giá | Chưa cung cấp |
| Phạm vi | Đối chiếu tĩnh mã nguồn, cấu trúc repository và tài liệu hiện có |
| Phương pháp | Rà soát `index.html`, `assets/css/styles.css`, `README.md` và tài liệu phát hành |
| Giới hạn | Chưa chạy website trên trình duyệt, thiết bị thực, máy chủ hoặc công cụ kiểm thử tự động; không có số liệu hiệu năng thực tế |

### Quy ước trạng thái

- **Đạt:** Có thể xác nhận từ nội dung hoặc minh chứng đã kiểm tra.
- **Chưa đạt:** Có lỗi hoặc yêu cầu chưa được đáp ứng rõ ràng.
- **Cần cải thiện:** Chưa có đủ minh chứng để kết luận, hoặc còn điểm cần hoàn thiện trước bàn giao.

> Trạng thái “Cần cải thiện” không đồng nghĩa tính năng đã được kiểm thử đạt; cần thực hiện kiểm thử bổ sung và lưu minh chứng.

## 2. Bảng tổng quan trạng thái

| # | Nhóm tiêu chí | Trạng thái | Tóm tắt |
|---:|---|---|---|
| 1 | Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng | Cần cải thiện | Có đủ các khu vực portfolio chính; liên kết chi tiết dự án vẫn là mẫu và chưa được xác minh khi chạy. |
| 2 | Giao diện, trải nghiệm người dùng và khả năng tương thích | Chưa đạt | Phát hiện sai khác tên lớp phần đầu trang giữa HTML và CSS; chưa kiểm thử trên trình duyệt/kích thước màn hình. |
| 3 | Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản | Cần cải thiện | Có hướng dẫn chạy tĩnh; chưa chạy thử hoặc đo hiệu năng. |
| 4 | Bảo mật, quản lý cấu hình và dữ liệu | Cần cải thiện | README mô tả không dùng cấu hình môi trường, khóa API, máy chủ hay cơ sở dữ liệu; chưa thực hiện rà soát bảo mật chuyên sâu. |
| 5 | Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao | Chưa đạt | Cấu trúc đơn giản và có tài liệu; vẫn có lỗi đánh dấu HTML và nội dung/liên kết cần rà soát. |
| 6 | Khả năng triển khai, kiểm thử và cung cấp minh chứng | Cần cải thiện | Có hướng dẫn mở trực tiếp, dùng máy chủ cục bộ và Docker; chưa triển khai hoặc cung cấp ảnh chụp/kết quả chạy thử. |

## 3. Nội dung kiểm thử chi tiết

### 3.1 Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Có phần giới thiệu, kỹ năng, dự án và liên hệ | Đạt | Các khu vực `#about`, `#skills`, `#projects`, `#contact` được khai báo trong `index.html`. |
| Điều hướng nội trang đến các khu vực chính | Đạt | Menu và nút kêu gọi hành động dùng liên kết neo như `#about`, `#projects`, `#contact`; chưa xác nhận thao tác thực tế trên trình duyệt. |
| Ảnh đại diện có văn bản thay thế | Đạt | Ảnh đại diện khai báo `alt="Ảnh đại diện của Trần Đại Vĩ"` trong `index.html`; chưa kiểm tra ảnh tải thành công khi chạy. |
| Liên kết “Xem chi tiết” mở đúng nội dung dự án | Chưa đạt | Các thẻ dự án hiện dùng `href="#"`; README cũng ghi nhận đây là liên kết mẫu. |
| Thông tin và nội dung hiển thị chính xác, nhất quán | Cần cải thiện | Cần xác nhận nội dung cuối cùng với chủ sở hữu sản phẩm; tên hiển thị trong trang có biến thể viết hoa và phần tên thương hiệu có chuỗi “1111”. |

### 3.2 Giao diện, trải nghiệm người dùng và khả năng tương thích

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Có khai báo viewport cho thiết bị di động | Đạt | `index.html` có thẻ `meta viewport`. |
| CSS có bố cục mobile-first và breakpoint | Đạt | `assets/css/styles.css` mô tả chiến lược mobile-first và các breakpoint tablet/desktop; chưa kiểm thử trực quan ở các kích thước này. |
| Kiểu bố cục phần đầu trang được áp dụng đúng | Chưa đạt | HTML dùng `header-innetr`, trong khi CSS khai báo `.header-inner`; tên lớp không khớp nên quy tắc tương ứng không áp dụng cho phần tử này. |
| Menu, chữ, ảnh và thẻ dự án không tràn hoặc chồng lấn | Cần cải thiện | CSS có quy tắc responsive và ảnh co giãn; chưa có ảnh chụp hoặc kiểm tra trên viewport nhỏ/lớn để xác nhận. |
| Khả năng truy cập cơ bản | Cần cải thiện | Có `lang="vi"`, nhãn điều hướng và văn bản `alt` cho ảnh; cần kiểm tra tương phản, thứ tự bàn phím, focus và trình đọc màn hình. |

### 3.3 Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Có thể mở website theo hướng dẫn bàn giao | Cần cải thiện | README hướng dẫn mở `index.html`, chạy Python HTTP server, Live Server hoặc Docker/Nginx; chưa thực hiện chạy thử trong lần đối chiếu này. |
| Tài nguyên cục bộ được tham chiếu đúng | Cần cải thiện | HTML tham chiếu `assets/css/styles.css` và `assets/img/avatar.jpg`; chưa xác nhận tải thành công trong phiên chạy. |
| Xử lý lỗi khi liên kết/tài nguyên không khả dụng | Cần cải thiện | Chưa có kết quả kiểm thử khi thiếu ảnh, sai đường dẫn hoặc lỗi mạng; trang tĩnh hiện không mô tả cơ chế dự phòng. |
| Thời gian tải và hiệu năng cơ bản | Cần cải thiện | Chưa đo bằng Lighthouse, DevTools hoặc công cụ tương đương; không có số liệu để kết luận. |
| Kiểm tra cú pháp và lỗi console | Cần cải thiện | Chưa chạy validator HTML/CSS hoặc kiểm tra console của trình duyệt. |

### 3.4 Bảo mật, quản lý cấu hình và dữ liệu

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Cấu hình môi trường và thông tin nhạy cảm | Đạt | README nêu dự án không có tệp cấu hình môi trường hoặc khóa API; đây là rà soát tài liệu, không thay thế quét toàn bộ lịch sử Git. |
| Thu thập hoặc lưu trữ dữ liệu người dùng | Đạt | Theo README, website tĩnh không có máy chủ hay cơ sở dữ liệu; chưa kiểm tra lưu lượng mạng khi chạy. |
| Liên kết ngoài mở tab mới an toàn | Cần cải thiện | Một số liên kết GitHub/LinkedIn dùng `target="_blank"`; nên khai báo rõ `rel="noopener noreferrer"` và xác minh URL trước bàn giao. |
| Rà soát lỗ hổng và chính sách bảo mật | Cần cải thiện | Chưa thực hiện kiểm thử bảo mật chuyên sâu; phạm vi ứng dụng tĩnh không đủ để kết luận an toàn toàn diện. |

### 3.5 Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Cấu trúc dự án dễ nhận biết | Đạt | Có `index.html`, `assets/css/styles.css`, `assets/img/avatar.jpg` và thư mục `docs/`. |
| Tài liệu hướng dẫn cài đặt/chạy | Đạt | `README.md` có hướng dẫn mở trực tiếp, chạy máy chủ cục bộ, Live Server và Docker. |
| Tài liệu phiên bản và ghi nhận thay đổi | Đạt | Có `docs/RELEASENOTE.md` và `docs/AI_LOG.md`; cần bảo đảm nội dung luôn đồng bộ với bản bàn giao thực tế. |
| Đánh dấu HTML hợp lệ | Chưa đạt | Trong danh sách kỹ năng có ký tự `>` thừa sau mục GitHub (`</li>>`); cần chạy validator sau khi sửa. |
| Tính nhất quán giữa class HTML và CSS | Chưa đạt | Tên `header-innetr` trong HTML không khớp `.header-inner` trong CSS. |
| Chất lượng URL liên hệ | Chưa đạt | HTML hiện có `href="gmail: trdaivi2911@gmail.com"` và `href="github.com/trandaivi"`; cần sửa thành URL/protocol phù hợp và kiểm thử thao tác. |
| Tính nhất quán của nội dung portfolio | Cần cải thiện | Rà soát tên hiển thị, thông tin cá nhân và các dự án mẫu để bảo đảm đúng dữ liệu được duyệt trước bàn giao. |

### 3.6 Khả năng triển khai, kiểm thử và cung cấp minh chứng

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Có hướng dẫn triển khai/chạy cục bộ | Đạt | README cung cấp hướng dẫn cho Windows, macOS, Linux, Live Server và Docker/Nginx. |
| Có thể triển khai mà không cần bước build | Đạt | README mô tả website tĩnh, không cần Node.js/npm hoặc công cụ đóng gói; chưa xác nhận triển khai thực tế. |
| Có kịch bản và kết quả kiểm thử tái lập | Cần cải thiện | Chưa thấy bộ test tự động hoặc biên bản chạy kiểm thử kèm kết quả trong phạm vi tài liệu đã rà soát. |
| Có minh chứng trực quan và môi trường kiểm thử | Cần cải thiện | Chưa đính kèm ảnh chụp màn hình, phiên bản trình duyệt, kích thước viewport hoặc log kiểm thử. |
| Kiểm tra bản dựng/bản triển khai cuối cùng | Cần cải thiện | Chưa triển khai lên môi trường bàn giao; cần kiểm tra lại đường dẫn tài nguyên và các liên kết trên URL cuối cùng. |

## 4. Đánh giá tổng kết và đề xuất

### Nhận định chung

Sản phẩm có phạm vi phù hợp với một website portfolio tĩnh và đã có các phần nội dung chính cùng tài liệu hướng dẫn chạy. Tuy nhiên, đợt đối chiếu này chỉ rà soát tĩnh mã nguồn/tài liệu, chưa thực hiện kiểm thử trên trình duyệt hoặc môi trường triển khai. Một số lỗi cụ thể trong HTML, tên lớp và URL có thể ảnh hưởng trực tiếp đến giao diện và thao tác liên hệ.

**Kết luận: Chưa khuyến nghị bàn giao chính thức ở trạng thái hiện tại.** Cần xử lý các mục “Chưa đạt”, sau đó chạy kiểm thử hồi quy và lưu minh chứng trước khi xác nhận bàn giao.

### Các đề xuất ưu tiên

1. Sửa lỗi HTML (`</li>>`) và thống nhất tên lớp phần đầu trang giữa HTML/CSS.
2. Sửa, kiểm tra URL email/GitHub/LinkedIn; thay các liên kết dự án mẫu bằng đích đến thực tế hoặc thể hiện rõ trạng thái chưa có trang chi tiết.
3. Rà soát nội dung và thông tin nhận diện trong trang với chủ sở hữu sản phẩm.
4. Kiểm tra giao diện trên trình duyệt phổ biến và viewport di động, tablet, desktop; chụp ảnh minh chứng.
5. Chạy validator HTML/CSS và kiểm tra lỗi console, tài nguyên không tải được, điều hướng bằng bàn phím.
6. Đo hiệu năng cơ bản và kiểm thử lại trên URL triển khai cuối cùng; ghi lại môi trường, kết quả và các lỗi còn mở.

### Điều kiện đề nghị trước khi bàn giao

- Không còn lỗi mức “Chưa đạt” trong các mục chức năng, giao diện và chất lượng mã nguồn.
- Các mục “Cần cải thiện” đã được kiểm thử hoặc có chấp thuận rõ ràng về phạm vi chưa thực hiện.
- Có minh chứng chạy thử trên môi trường mục tiêu và cập nhật trạng thái báo cáo theo kết quả thực tế.