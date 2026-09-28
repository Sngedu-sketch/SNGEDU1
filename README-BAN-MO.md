# Bản mở — không đăng nhập, không giới hạn lượt

## Đã sửa
- quiz-dynamic / quiz-exam / quiz-tinhtoan / mon-hoc: bỏ bắt buộc đăng nhập, bỏ giới hạn lượt/ngày.
- frontend/usage-limits.js: luôn cho phép, không ghi log. index.js: không tab nào yêu cầu đăng nhập.
- Đọc tài liệu (chi-tiet.html, doc-preview-viewer.html): xem toàn bộ trang, không cần đăng nhập/Pro.
- Admin: chỉ đăng nhập được bằng tài khoản `admin` / mật khẩu `adminsngedu23/9/2026`.

## Cần làm thêm
1. Deploy lại Edge Function: `supabase functions deploy doc-pages` (đã bỏ kiểm tra Pro).
2. Để admin LƯU được dữ liệu: tạo user Supabase email `admin@sngedu.vn`, mật khẩu `adminsngedu23/9/2026`,
   rồi đặt `profiles.role = 'admin'` cho user đó (RLS vẫn kiểm tra ở server).

## Lưu ý bảo mật
Tài khoản/mật khẩu nằm trong admin.js nên ai xem source cũng thấy. Quyền ghi thật sự do Supabase RLS quyết định.
