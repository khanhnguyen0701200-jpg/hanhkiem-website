# Website Quản lý điểm hạnh kiểm

Mở `index.html` trực tiếp bằng trình duyệt.

## Tài khoản mặc định
- Admin: `admin` / `admin123`

## Tính năng chính
- Quản lý học sinh, giữ nguyên thứ tự nhập.
- Import `.xlsx`, `.csv` và dán dữ liệu từ Excel.
- Cấu trúc Excel ưu tiên: cột 1 **Lớp**, cột 2 **Họ và tên**; vẫn nhận tiêu đề `Họ tên thí sinh`.
- Điểm học sinh luôn được giới hạn 0–10; điểm khởi đầu cố định 10.
- Quản lý giáo viên và lớp phụ trách.
- Admin quản lý quy định chung.
- Giáo viên có 2 mục riêng: **Vi phạm lớp tôi** và **Khen thưởng lớp tôi**, tự tạo/sửa/xóa quy định cho từng lớp mình được phân công.
- Giáo viên có mục **Tài khoản** để đổi họ tên, mật khẩu và **ảnh đại diện**; ảnh được nén và lưu trong localStorage.
- Quy định riêng của giáo viên chỉ áp dụng đúng lớp đó và chỉ tài khoản giáo viên đó sử dụng được.
- Khi ghi vi phạm/khen thưởng, giáo viên thấy cả quy định chung của Admin và quy định riêng của mình cho lớp đang chọn.
- Lịch sử, tìm kiếm, xóa/hoàn tác bất kỳ vi phạm hoặc khen thưởng trong phạm vi được phép; luôn hỏi xác nhận trước khi xóa.
- Khi xóa một bản ghi cũ, điểm hiện tại và các mốc điểm phía sau của học sinh được tính lại theo các thao tác còn hiệu lực. Hệ thống tạo thêm một bản ghi **Đã xóa lịch sử** để lưu dấu vết và không cho xóa bản ghi nhật ký này.
- Sao lưu/khôi phục JSON và lưu dữ liệu bằng `localStorage`.
- Xuất dữ liệu ra file `.xlsx` ngay trong trình duyệt: học sinh, lịch sử, quy định, tổng quan; Admin có thêm danh sách giáo viên. Giáo viên chỉ xuất được dữ liệu thuộc các lớp mình được phân công.

## Gợi ý cấu trúc Excel
| Lớp | Họ tên thí sinh |
|---|---|
| 12A2 | Nguyễn Văn A |
| 12A2 | Trần Thị B |
| 12A3 | Lê Văn C |
