# GDT_TCHD — Phần mềm Tra cứu & Tải Hóa đơn Điện tử (Tổng cục Thuế)
![Version](https://img.shields.io/badge/Phiên_bản-v1.2.0-004f8b?style=flat-square)
![Platform](https://img.shields.io/badge/Nền_tảng-Windows_10_%2F_11_(64--bit)-0078D6?style=flat-square)
![Publisher](https://img.shields.io/badge/Phát_triển_bởi-A.I_Machine-16a34a?style=flat-square)
**GDT_TCHD** là ứng dụng desktop dành cho kế toán, doanh nghiệp và hộ kinh doanh, hỗ trợ tự động hóa quá trình tra cứu, tải tệp hóa đơn gốc (XML, PDF, ZIP) và tổng hợp báo cáo bảng kê Excel từ Cổng thông tin Hóa đơn điện tử của Tổng cục Thuế (`hoadondientu.gdt.gov.vn`).
---
## 1. Tính năng nổi bật
* **Tra cứu & tải hóa đơn hàng loạt:** Hỗ trợ đầy đủ cả hai luồng **Hóa đơn mua vào (Đầu vào)** và **Hóa đơn bán ra (Đầu ra)** theo từng tháng hoặc gộp theo quý.
* **Xuất báo cáo Excel chuẩn hóa (`.xlsx`):** Tự động trích xuất dữ liệu chi tiết từ XML (thông tin người bán/người mua, tên hàng hóa, số lượng, đơn giá, chiết khấu, thuế suất, tổng tiền thanh toán) và gộp bảng kê gọn gàng, chính xác.
* **Tải trọn bộ hồ sơ hóa đơn:** Tùy chọn chỉ xuất bảng kê Excel hoặc tải đồng thời file gốc **XML** và bản thể hiện **PDF** được sắp xếp khoa học theo từng kỳ.
* **Cơ chế Cache thông minh & chống trùng lặp:**
  * Lưu trạng thái các kỳ không phát sinh dữ liệu ngay trong thư mục ứng dụng để bỏ qua ở lần chạy sau, rút ngắn thời gian tra cứu.
  * Tự động cảnh báo khi tệp báo cáo của kỳ tra cứu đã tồn tại và tích hợp nút **Xóa cache** một chạm trên giao diện.
* **Vận hành ngầm ổn định:** Tự động tận dụng trình duyệt Microsoft Edge hoặc Google Chrome có sẵn trên Windows, tối ưu tài nguyên và hạn chế gián đoạn thao tác.
* **Bảo mật & Quản lý bản quyền linh hoạt:**
  * Kiểm tra tính toàn vẹn mã nguồn bằng chữ ký số **RSA-2048** (`manifest.sig`) mỗi khi khởi động.
  * Hỗ trợ kích hoạt nhiều thiết bị trên cùng một mã bản quyền (tùy theo gói) và chuyển đổi thiết bị thuận tiện khi thay máy tính.
---
## 2. Yêu cầu hệ thống
| Thành phần | Yêu cầu tối thiểu |
| :--- | :--- |
| **Hệ điều hành** | Windows 10 hoặc Windows 11 (64-bit) |
| **Trình duyệt** | Microsoft Edge hoặc Google Chrome (bản cập nhật mới) |
| **Bộ nhớ (RAM)** | 4 GB trở lên (khuyến nghị 8 GB khi tải số lượng lớn hóa đơn) |
| **Dung lượng trống** | Tối thiểu 500 MB ổ đĩa |
| **Kết nối mạng** | Internet ổn định để kết nối Cổng Tổng cục Thuế và xác thực bản quyền |
---
## 3. Hướng dẫn tải và cài đặt
1. **Tải bộ cài đặt:**
   * Truy cập https://drive.google.com/file/d/1oRwTnurNevBYxrR8e_91RKQHeXJEtUUh/view?usp=sharing và tải về tệp n **`GDT_TCHD_Setup_v1.2.0.exe`**.
2. **Chạy trình cài đặt:**
   * Mở tệp **`GDT_TCHD_Setup_v1.2.0.exe`**.
   * Nếu Windows hiển thị thông báo bảo vệ **Windows SmartScreen** (*"Windows protected your PC"*):
     1. Bấm vào dòng chữ **More info** (Thông tin thêm).
     2. Bấm nút **Run anyway** (Vẫn chạy) để tiếp tục.
3. **Hoàn tất cài đặt:**
   * Giữ nguyên đường dẫn cài đặt mặc định (`%LOCALAPPDATA%\GDT_TCHD`) để phần mềm có đầy đủ quyền đọc/ghi dữ liệu cấu hình và cache mà không cần quyền Administrator.
   * Bấm **Next → Install → Finish** và mở ứng dụng từ biểu tượng **GDT_TCHD** trên màn hình Desktop.
---
## 4. Hướng dẫn kích hoạt & Sử dụng nhanh
### Bước 1: Kích hoạt bản quyền
1. Mở phần mềm **GDT_TCHD**, chuyển sang tab **Bản quyền**.
2. Nhập mã bản quyền do **A.I Machine** cung cấp (định dạng `AIM-XXXX-XXXX-XXXX`).
3. Nhấn **KÍCH HOẠT**.
   > *Lưu ý: Thời hạn sử dụng của gói bản quyền bắt đầu được tính kể từ ngày bạn kích hoạt thành công lần đầu tiên.*
### Bước 2: Tra cứu và xuất dữ liệu hóa đơn
1. Nhập **Tên đăng nhập** và **Mật khẩu** tài khoản Cổng Hóa đơn điện tử (`hoadondientu.gdt.gov.vn`).
2. Chọn **Loại hóa đơn** (Mua vào / Bán ra), **Kỳ tra cứu** (Tháng / Quý / Năm) và **Chế độ xuất dữ liệu**.
3. Chọn **Thư mục lưu kết quả** trên máy tính.
4. Nhấn **BẮT ĐẦU**, nhập mã **Captcha** khi hộp thoại hiển thị và chờ phần mềm tự động tải, tổng hợp báo cáo.
---
## 5. Câu hỏi thường gặp (FAQ)
<details>
<summary><strong>1. Tại sao Windows hiện cảnh báo "Windows protected your PC" khi mở file cài đặt?</strong></summary>
<br>
Đây là cơ chế SmartScreen mặc định của Windows đối với các phần mềm độc lập mới phát hành chưa mua chứng chỉ EV Code Signing của Microsoft. Bạn chỉ cần chọn <strong>More info → Run anyway</strong> để cài đặt bình thường.
</details>
<details>
<summary><strong>2. Kỳ trước đó không có hóa đơn, nay mới phát sinh hóa đơn bổ sung thì làm thế nào?</strong></summary>
<br>
Phần mềm lưu dấu các kỳ trống trong cache để tăng tốc độ chạy. Khi có hóa đơn phát sinh mới cho kỳ cũ, bạn chỉ cần bấm nút <strong>Xóa cache</strong> ở góc trên khung <strong>Nhật ký</strong> trên giao diện chính rồi chạy lại tra cứu.
</details>
<details>
<summary><strong>3. Phần mềm báo "File tra cứu đã tồn tại" khi bấm Bắt đầu?</strong></summary>
<br>
Thông báo này giúp tránh ghi đè nhầm lên báo cáo Excel bạn đã xuất trước đó trong cùng thư mục lưu. Hãy di chuyển/đổi tên tệp cũ hoặc chọn một thư mục lưu mới trước khi chạy lại.
</details>
<details>
<summary><strong>4. Tôi đổi sang máy tính mới thì chuyển bản quyền như thế nào?</strong></summary>
<br>
Nếu còn truy cập được máy cũ, bạn vào tab <strong>Bản quyền → Hủy kích hoạt thiết bị này</strong>, sau đó nhập lại key trên máy mới. Trường hợp máy cũ hỏng hoặc cài lại Windows, hãy dùng tính năng <strong>Chuyển máy</strong> ngay trên tab Bản quyền hoặc liên hệ bộ phận hỗ trợ.
</details>
<details>
<summary><strong>5. Ứng dụng báo lỗi kiểm tra tính toàn vẹn tệp (manifest.sig)?</strong></summary>
<br>
Một hoặc nhiều tệp trong thư mục cài đặt đã bị thay đổi hoặc thiếu so với bản phát hành gốc. Vui lòng gỡ cài đặt và chạy lại tệp <code>GDT_TCHD_Setup_v1.2.0.exe</code> chính thức.
</details>
---
## 6. Hỗ trợ kỹ thuật & Bản quyền
* **Đơn vị phát triển:** A.I Machine
* **Email hỗ trợ:** `support_aimachine@gmail.com`
*Bản quyền phần mềm thuộc về **A.I Machine**. Nghiêm cấm mọi hành vi dịch ngược, chỉnh sửa mã nguồn hoặc phân phối lại trái phép.*
