# Audit liên kết nội bộ – 15 bài PR AIO CITY

Ngày rà soát: 12/11/2026  
Phạm vi: nội dung HTML của 15 bài PR có ID 31718–31740.  
Phương pháp: đọc nội dung WordPress ở chế độ edit và trích xuất thẻ liên kết trong body.

## 1. Kết quả tổng quan

- 15/15 bài đã được kiểm tra.
- Các bài đều có liên kết nội bộ; số lượng trong phạm vi kiểm tra dao động khoảng 2–8 link/bài.
- Một số bài có liên kết đến trang trụ cột /du-an/aio-city.html.
- Các trang chuyên đề pháp lý và giá bán tại /gkey-homes/aio-city/ có xuất hiện trong link map.
- Fanpage AIO City Hoa Lâm là liên kết ngoài được dùng ở một số bài; phù hợp ngoại lệ người quản lý đã cho phép.
- Phát hiện một đường dẫn nội bộ sai trong bài ID 31738.
- Hai bài mới đang trỏ đến bài ID 3003, nơi audit đã phát hiện thông tin lịch nội bộ công khai. Cần tạm xem link đích này là rủi ro cho đến khi bài 3003 được xử lý.

## 2. Chi tiết liên kết đã trích xuất

| Post ID | URL nguồn | Số link | Nhận xét |
|---:|---|---:|---|
| 31718 | https://realestateproject.vn/tin-tuc/aio-city-vai-tro-hoa-lam-an-gia-phat-trien-du-an.html | 4 | Link trang dự án, pháp lý, giá bán và fanpage |
| 31721 | https://realestateproject.vn/tin-tuc/vi-tri-aio-city-binh-tan-ket-noi-khu-do-thi-ten-lua.html | 5 | Có link về bài cũ ID 3003; cần xử lý đích trước khi tiếp tục dẫn traffic |
| 31723 | https://realestateproject.vn/tin-tuc/tien-ich-aio-city-binh-tan-danh-gia-chat-luong-song.html | 4 | Link trang dự án, pháp lý, giá bán và fanpage |
| 31725 | https://realestateproject.vn/tin-tuc/quy-hoach-aio-city-cach-doc-mat-bang-ho-so-du-an.html | 5 | Link bài shophouse cũ ID 24817; cần rà soát nội dung đích |
| 31727 | https://realestateproject.vn/tin-tuc/thi-truong-can-ho-binh-tan-goc-nhin-chon-mua-aio-city.html | 5 | Có liên kết chéo đến vị trí và tiện ích |
| 31729 | https://realestateproject.vn/tin-tuc/thiet-ke-can-ho-aio-city-chon-mat-bang-phu-hop.html | 4 | Có link về bài cũ ID 3003; cần xử lý đích trước khi tiếp tục dẫn traffic |
| 31731 | https://realestateproject.vn/tin-tuc/tai-chinh-mua-can-ho-aio-city-lap-ngan-sach-an-toan.html | 4 | Link trang dự án, giá bán, pháp lý và fanpage |
| 31733 | https://realestateproject.vn/phong-thuy/co-nen-mua-aio-city-uu-diem-rui-ro-can-can-nhac.html | 8 | Có nhiều link chéo trong cụm; cần giữ anchor đa dạng |
| 31734 | https://realestateproject.vn/tin-tuc/shophouse-aio-city-vi-tri-va-tiem-nang-khai-thac.html | 3 | Link trang dự án, pháp lý, tài chính |
| 31735 | https://realestateproject.vn/tin-tuc/cac-loai-can-ho-aio-city-chon-dien-tich-theo-nhu-cau.html | 3 | Link tài chính, trang dự án và giá bán |
| 31736 | https://realestateproject.vn/tin-tuc/phap-ly-aio-city-ho-so-nguoi-mua-can-kiem-tra.html | 2 | Link pháp lý và trang dự án |
| 31737 | https://realestateproject.vn/tin-tuc/ha-tang-khu-tay-tphcm-kha-nang-ket-noi-aio-city.html | 2 | Link vị trí và trang dự án |
| 31738 | https://realestateproject.vn/tin-tuc/aio-city-va-du-an-can-ho-binh-tan-so-sanh-the-nao.html | 4 | Một href sai đường dẫn bài ID 31733 |
| 31739 | https://realestateproject.vn/tin-tuc/aio-city-qua-trinh-hinh-thanh-va-phat-trien-du-an.html | 4 | Link vai trò đơn vị, trang dự án, pháp lý và quy hoạch |
| 31740 | https://realestateproject.vn/tin-tuc/tien-ich-aio-city-cho-gia-dinh-danh-gia-nhu-cau.html | 3 | Link tiện ích, thiết kế và trang dự án |

## 3. Lỗi đường dẫn xác định được

Nguồn:
https://realestateproject.vn/tin-tuc/aio-city-va-du-an-can-ho-binh-tan-so-sanh-the-nao.html

Post ID: 31738

Href đang có:
https://realestateproject.vn/tin-tuc/co-nen-mua-aio-city-uu-diem-rui-ro-can-can-nhac.html

URL chuẩn của bài đích ID 31733:
https://realestateproject.vn/phong-thuy/co-nen-mua-aio-city-uu-diem-rui-ro-can-can-nhac.html

Hành động đề xuất: chỉ sửa href của anchor hiện hữu sang URL chuẩn, giữ nguyên anchor text và phần nội dung còn lại. Cần kiểm tra sau khi cập nhật.

## 4. Link đích cần xử lý trước

Bài ID 31721 và 31729 có link đến:
https://realestateproject.vn/tin-tuc/can-ho-aio-city-lua-chon-an-cu-phu-hop-tai-binh-tan.html

Bài đích ID 3003 hiện chứa phần cập nhật có lịch triển khai nội bộ. Không nên tiếp tục dẫn người đọc tới bài này cho đến khi phần thông tin nội bộ được gỡ theo phạm vi đã duyệt.

## 5. Kiểm tra trang trụ cột

URL: https://realestateproject.vn/du-an/aio-city.html

Trang truy cập công khai được kiểm tra ngày 12/11/2026. Nội dung hiển thị có các điểm cần xác minh/cập nhật:

- Trường “Phát triển dự án” đang ghi Công ty TNHH Đầu tư Gkey Homes, không khớp thông tin người quản lý đã xác nhận: An Gia Group là đơn vị phát triển.
- Một số mốc như “thời gian mở bán Quý 3/2026”, giá bán và bàn giao là dữ liệu cũ hoặc cần đối chiếu lại trước khi tiếp tục hiển thị.
- Một số thông tin dự án/địa chỉ và thông số cần đối chiếu hồ sơ hiện hành.
- Không được suy luận pháp nhân đứng tên hồ sơ từ tên đơn vị phát triển.

Đề xuất: tạo một đợt rà soát riêng cho trang trụ cột. Chỉ cập nhật những trường đã có căn cứ và được người quản lý duyệt; giữ nguyên cấu trúc, shortcode và bố cục Flatsome.

## 6. Trạng thái

- Audit nội dung link của 15 bài: hoàn thành.
- Sửa href sai của ID 31738: chưa thực hiện.
- Xử lý link trỏ đến ID 3003: chờ gỡ thông tin nội bộ ở bài đích.
- Rà soát trang trụ cột: cần đối chiếu dữ liệu và được duyệt.
- Kiểm tra HTTP status/canonical tự động cho toàn bộ link: chưa hoàn thành.
