# Đưa website lên Internet

Website này là static HTML/CSS/JavaScript nên không cần Node.js, PHP hay database để chạy bản hiện tại.

## Cách 1 — GitHub Pages

1. Đăng nhập GitHub.
2. Tạo repository mới, ví dụ `hanhkiem-website`.
3. Upload toàn bộ nội dung của thư mục này lên repository, trong đó `index.html` phải nằm ở thư mục gốc.
4. Vào **Settings → Pages**.
5. Nếu dùng workflow có sẵn trong `.github/workflows/pages.yml`, chọn **GitHub Actions** làm nguồn triển khai.
6. Push/commit lên nhánh `main`. GitHub Actions sẽ tự triển khai.
7. URL thường có dạng `https://TEN-GITHUB.github.io/hanhkiem-website/`.

## Cách 2 — Netlify

### Nhanh nhất
1. Đăng nhập Netlify.
2. Chọn **Add new project → Deploy manually** hoặc khu vực Netlify Drop.
3. Kéo thả **thư mục đã giải nén** này vào vùng deploy.
4. Netlify sẽ cấp một địa chỉ dạng `https://ten-site.netlify.app`.

### Qua GitHub
1. Đưa thư mục này lên GitHub.
2. Trong Netlify chọn **Add new project → Import an existing project**.
3. Chọn GitHub và repository.
4. Publish directory để `.` (thư mục gốc); không cần build command.

## Cách 3 — Vercel

1. Đưa thư mục này lên GitHub.
2. Đăng nhập Vercel.
3. Chọn **Add New → Project**.
4. Import repository GitHub.
5. Với website này, không cần build command; output/publish directory là thư mục gốc.
6. Deploy.

## Lưu ý quan trọng

- Dữ liệu hiện tại được lưu bằng `localStorage` của từng trình duyệt. Nếu mở website trên máy/điện thoại khác thì dữ liệu không tự đồng bộ.
- Tài khoản `admin / admin123` là tài khoản mặc định phía giao diện; không nên coi đây là hệ thống xác thực bảo mật cho môi trường thật.
- Nếu cần nhiều giáo viên cùng dùng chung dữ liệu, cần thêm backend + database + xác thực người dùng.
