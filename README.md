# Giờ thứ 5

> Bốn giờ đầu, bạn làm ra tiền lương của mình. Từ giờ thứ năm, bạn làm ra giá trị thặng dư.

Trang web học tập tương tác môn **Kinh tế chính trị Mác – Lênin (MLN122)**, bám theo giáo trình của Bộ GD&ĐT (NXB Chính trị quốc gia Sự thật, 2021):

| Trang | Nội dung |
|---|---|
| Tổng quan | Sơ đồ tổng thể: sức lao động → c + v + m → tiền lương, lợi nhuận → Nhà nước điều hòa |
| Chương 3 · Mục I.1 | Nguồn gốc của giá trị thặng dư |
| Chương 3 · Mục I.2 – II | Sản xuất giá trị thặng dư và tích lũy tư bản |
| Chương 5 · Mục III | Các quan hệ lợi ích kinh tế ở Việt Nam |
| Trò chơi | Liên kết tới game [24h Đi Làm: Đêm Không Bao Giờ Tắt](https://mellow-phoenix-bbd3b8.netlify.app) |

## Chạy thử

Mở `index.html` bằng trình duyệt. Trang chỉ gồm một file HTML, không cần cài đặt.

## Công nghệ

HTML, CSS, JavaScript thuần; font từ Google Fonts.

## Giao diện và điện thoại

- Nút tròn ở góc dưới bên phải đổi giao diện: đang sáng hiện **mặt trăng** để chuyển sang tối; đang tối hiện **mặt trời** để chuyển sang sáng. Nút nằm ngoài header, không chiếm chỗ hoặc che thanh chuyển trang.
- Khi chưa chọn giao diện, trang theo hệ điều hành. Sau khi bấm nút, trang ghi nhớ lựa chọn sáng/tối.
- Lựa chọn giao diện lưu trong `localStorage` với khóa `MLN122_WEB_THEME` và được áp dụng ngay khi tải trang. Nếu trình duyệt chặn lưu trữ, vẫn đổi được giao diện trong trang hiện tại.
- Trên điện thoại, vuốt thanh menu ngang để chuyển phần học; các sơ đồ rộng có thể cuộn ngang trong khung riêng. Thanh ngày lao động và đồng hồ xếp thành một cột.
- Chạm thẻ rồi chạm ô để phân loại. Có thể cuộn dọc từ vùng thẻ; kéo ngang để di chuyển thẻ, hoặc dùng chuột trên máy tính.

## Deploy lên Netlify

Repo là website tĩnh, không có bước cài dependencies hay build. File `netlify.toml` đặt publish directory là thư mục gốc (`.`) và build command rỗng. Khi kết nối GitHub, chọn nhánh cần deploy; có thể dùng Deploy Preview cho PR nếu đã bật trên Netlify.

Các đường dẫn bài học dùng hash (`#chuong-3-1`...), không cần SPA rewrite. Game vẫn ở tên miền riêng, được mở bằng liên kết hiện có.

## Dữ liệu trò chơi

Repo này chỉ chứa web **Giờ thứ 5**, không chứa source game **24h Đi Làm**. Website học chưa lưu lịch sử học hoặc kết quả quiz.

Mã `game.js` trên bản game công khai tại thời điểm kiểm tra 08/11/2026 dùng `localStorage` để lưu ván chơi (gồm nhật ký và lựa chọn), kết cục đã mở, cài đặt và các câu thoại đã đọc. Dữ liệu thuộc trình duyệt/profile và origin của game, không tự đồng bộ giữa thiết bị hoặc chuyển sang một domain Netlify/local khác. Cập nhật trên cùng origin vẫn dùng được dữ liệu đã lưu nếu định dạng save còn tương thích. Xóa dữ liệu trang hoặc kết thúc phiên riêng tư có thể làm mất save.
