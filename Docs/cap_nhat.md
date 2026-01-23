# Cập nhật mới của d2ttool

## Phiên bản 1.7.2 (23/01/2026 - Bản hoàn thiện UI)
- **Tình năng mới**: Thêm chức năng MD5.

## Phiên bản 1.6.0 (Mới nhất)
*   **Tính năng mới: Chuyển đổi định dạng ảnh.** Thêm tùy chọn "Chuyển tất cả ảnh sang .jpg".
*   **Tính năng mới: Thay đổi MD5 (Unique File).** Thêm tùy chọn chèn dữ liệu ẩn vào cuối file để thay đổi mã định danh MD5, giúp file trở thành "duy nhất" đối với các hệ thống quét. Chương trình thông minh tự động bỏ qua bước này đối với các file đã được convert JPG để tối ưu tốc độ.
*   **Cải tiến: Xử lý đường dài (Long Path).** Tích hợp sâu hơn cơ chế tiền tố `\\?\` để triệt tiêu hoàn toàn lỗi WinError 3 trên NAS.

## Phiên bản 1.5.0
*   **Giao diện Hiện đại (Modern UI):** Toàn bộ giao diện đã được chuyển sang thư viện `CustomTkinter` với phong cách Dark Mode sang trọng, bo góc các widget và bố cục thông thoáng hơn.
*   **Window Fix:** Cố định kích thước cửa sổ (800x700) và căn giữa màn hình khi khởi chạy, không cho phép thay đổi kích thước để đảm bảo bố cục luôn chuẩn.
*   **Cải tiến Log:** Thêm các icon trạng thái (🔴, 🟠, ⚪) vào phần log giúp dễ dàng nhận biết lỗi và cảnh báo.
*   **Dependency:** Yêu cầu cài đặt thêm thư viện `customtkinter`.

## Phiên bản 1.4.0
*   **Tinh chỉnh tên folder:** Loại bỏ dấu gạch dưới `_` giữa các thành phần tên (Prefix, Suffix, Ngày, Số). Tên sẽ được ghép liền mạch theo ý muốn của người dùng.
*   **Tính năng Tự động Xóa (Auto-Clear):** Sau khi xử lý xong và người dùng xác nhận "OK" trên thông báo, toàn bộ các ô nhập liệu, đường dẫn và log sẽ được xóa trắng để sẵn sàng cho lượt xử lý mới.

## Phiên bản 1.3.0
*   **Tính năng mới: Đánh số thứ tự tăng dần.** Thêm ô "Số bắt đầu" cho phép tự động đánh số thứ tự cho các folder. Hỗ trợ giữ định dạng (Padding) như `01`, `001`.
*   **Cải tiến:** Tên thư mục mới giờ đây bao gồm tùy chọn số thứ tự: `[Tiền tố][Hậu tố][Ngày][Số thứ tự]`.

## Phiên bản 1.2.0
*   **Thay đổi logic đổi tên:** Tên thư mục mới hiện tại sẽ hoàn toàn dựa trên cấu trúc cài đặt (Tiền tố + Hậu tố + Ngày tháng) và không còn giữ lại tên thư mục cũ.
*   **Thêm tùy chọn ngày tháng:** Bổ sung thêm 2 định dạng ngày mới là `MMDD` và `DDMM` bên cạnh `YYYYMMDD`.
*   **Giao diện:** Chuyển từ Checkbox sang Radio buttons để lựa chọn định dạng ngày thuận tiện hơn.

## Phiên bản 1.1.0
*   **Tính năng mới:** Chuyển sang cơ chế di chuyển toàn bộ thư mục thay vì từng file đơn lẻ. Điều này giúp giữ nguyên cấu trúc thư mục con và tăng tốc độ xử lý trên hạ tầng NAS.
*   **Cải tiến:** Tự động chuẩn hóa đường dẫn mạng (UNC) giúp tương thích tốt hơn với các hệ thống Windows/NAS.
*   **Sửa lỗi:** Thêm chế độ lưu báo cáo dự phòng với timestamp khi file `report.xlsx` chính đang bị mở, ngăn chặn lỗi crash ứng dụng.
*   **Sửa lỗi:** Xử lý lỗi "Permission Denied" và thêm kiểm tra trùng lặp thư mục Gốc/Đích.

## Phiên bản 1.0.0
*   Khởi tạo dự án với giao diện GUI Tkinter.
*   Hỗ trợ đổi tên folder với prefix, suffix và date.
*   Hỗ trợ di chuyển file cơ bản.
*   Xuất báo cáo Excel bằng thư viện `openpyxl`.
*   Log tiến trình xử lý.
