# Nguồn giftcode Delta Force · đối chiếu 25/10/2026

## Nguyên nhân bỏ sót

Bản 1.2.2 chỉ có XemGì và tin Garena trong danh sách nguồn mặc định. Code Mới nằm ở phần gợi ý thêm nguồn nên người dùng chưa thêm nguồn này sẽ không thấy những mã chỉ có tại đây.

Ngày 25/10, bộ quét XemGì hiện có vẫn đọc được **242 chuỗi ứng viên**, không tăng so với danh sách đi kèm 1.2.2. Code Mới có **41 chuỗi**; 8 chuỗi chưa có trong XemGì. Hợp hai nguồn là **250 ứng viên**. Đây là số chuỗi tìm thấy, không phải số mã chắc chắn nhận quà được.

## Kết quả nguồn

| Nguồn công khai | HTTP / kết quả | Phạm vi trong tiện ích |
|---|---|---|
| [XemGì](https://xemgi.de/codes) | 242 ứng viên từ API + dữ liệu tĩnh | Mặc định |
| [Code Mới](https://codemoi.net/games/delta-force/) | 200; 41 mã trong thẻ `code` | Mặc định từ 1.2.3 |
| [Garena Việt Nam](https://deltaforce.garena.vn/) | API trang chủ/tin hoạt động; 8 bài đã đọc, 0 giftcode chữ nhận dạng được | Mặc định; tối đa 8 bài/lượt |
| [Download.com.vn](https://download.com.vn/code-game-delta-force-195638) | 200; 24 ứng viên, loại tiêu đề bảng và chuỗi thiết lập súng | Gợi ý tùy chọn |
| [Điện máy XANH](https://www.dienmayxanh.com/kinh-nghiem-hay/code-delta-force-garena-moi-nhat-1591472) | 200; 19 ứng viên | Gợi ý tùy chọn |
| FPT Shop `/tin-tuc/danh-gia/code-delta-force-184570` | 404 | Thay gợi ý bằng Download.com.vn |
| FPT Shop `/tin-tuc/giai-tri/code-delta-force-184570` | 404 | Không dùng URL này để thay thế |

Hai nguồn tùy chọn có nhiều mã cũ/trùng; không cộng các số trong bảng để tuyên bố số mã mới. Kết quả chỉ áp dụng nội dung công khai đã lấy ngày 25/10/2026; bài viết có thể thay đổi sau đó.

## Tám ứng viên bổ sung từ Code Mới

```text
SsCkDfxY5AkdZqiJLkXq
POCSEEYOUTMR
POCISHERE
WHOISPOCKING
POCS2S2
HITTHEROADTODFI
DFVNA4T8Z6P3
WELCOMETODF
```

Giữ nguyên chữ hoa/thường. Không bắt buộc mã phải có tiền tố DF. Hiệu lực, khu vực, giới hạn và điều kiện tài khoản do Garena xác nhận; chưa thực hiện đổi quà trên tài khoản thật trong lần kiểm tra này.

## Thay đổi 1.2.3

- Thêm Code Mới mặc định và quyền hẹp `https://codemoi.net/*`. Bản cài cũ tự thêm nguồn một lần, không nhân đôi URL đã có, giữ nguồn từng tắt và không tự khôi phục nguồn đã xóa sau nâng cấp.
- Quét tự lưu mã mới cùng danh sách vừa thêm. Quét lại không nhân đôi; lịch sử mã đã nhận/đã bỏ qua không bị hồi sinh.
- Báo số nguồn hoàn tất/lỗi/đọc một phần; không coi lỗi tải hoặc selector rỗng là đã quét thành công và không có code mới.
- Giải phóng trạng thái quét dang dở khi worker khởi động lại; mã đã lưu vẫn còn.
- Bỏ tiêu đề `Codes` trong bảng dùng ô `td`, tránh đưa tiêu đề vào hàng chờ.
- Danh sách đi kèm được tạo từ báo cáo nguồn và kết quả DOMParser đã kiểm tra; script kiểm tra mạng không ghi đè seed thành dữ liệu chỉ có XemGì.

## Cách kiểm tra

Mã bộ quét/worker thật chạy với HTML công khai đã lưu và API Chrome giả lập. Luồng kiểm tra xác nhận 242 → 250, đủ 8 mã và URL nguồn, lần quét hai thêm 0, giữ kết quả đã nhận và lỗi đã bỏ qua. Ba cấu hình nguồn đọc bằng DOMParser thật, không thực thi JavaScript của nguồn.

Cài trong môi trường content script cô lập, đổi quà tài khoản thật và lịch chạy đủ một ngày: **NOT_RUN**. Code trong ảnh, bình luận, video, livestream hoặc nhóm riêng không thuộc bộ đọc chữ hiện tại.
