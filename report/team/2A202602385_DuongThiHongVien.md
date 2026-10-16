# Báo cáo cá nhân · Lab Day 13

- Họ tên: Dương Thị Hồng Viên
- Mã sinh viên: 2A202602385
- Nhóm: Neiv
- Khóa học: VinUni AI Thực Chiến – Cohort IV
- Đề: 1 · SổSạch

## Phần việc và bằng chứng

| Phần việc | Nội dung | Bằng chứng trong `Neiv_CS13.xlsx` |
|---|---|---|
| CP1 | Đọc 6 mục hồ sơ, viết giả thuyết và ngưỡng cho đủ 6 việc | `0_Đầu vào!B5:B10`, `1_Danh sách việc!B5:E10` |
| CP2 | Chấm 7 đầu vào ưu tiên, quyết định tự làm/mua/chờ/không làm và giải thích | `1_Danh sách việc!F5:Q10` |
| CP3 | Phân vai AI/người, đặt cổng, cỡ mẫu và tính kinh tế | `2_Mức tự động!C5:M8` |
| CP4 | Hoàn thiện 3 tầng lộ trình và lịch xem xét theo thời gian/sự kiện | `3_Bảng lộ trình!B5:D12`, `4_Rà soát!B5:D10` |
| CP5 | Viết 5 thông điệp dưới 60 chữ/ô và chuyển thành 1 slide | `5_Slide lãnh đạo!B4:D8`, `Neiv_CS13_Slide.pptx` |

## Quyết định và điều rút ra

Nhập tệp gốc đứng đầu điểm ưu tiên (9,75) nhưng lựa chọn là tận dụng chức năng có sẵn, không tự xây lại. Gắn cờ (8,55) và đối chiếu mã số thuế (7,40) là phần bảo vệ chất lượng trước khi tăng quyền tự nhập. Đọc ảnh (2,84) vẫn có trong tầng Bây giờ vì trực tiếp phục vụ mục tiêu giảm giờ nhập. Điểm thấp hơn không đồng nghĩa không làm nếu đó là phần thiết yếu của kết quả mong muốn.

Mức 1 có chi phí 704 đồng/việc, biên gộp 68,79% theo dữ liệu đề. Nếu tỷ lệ duyệt tăng từ 20% lên 40%, chi phí thành 954 đồng, biên còn 57,71%. Vì vậy phải đo tỷ lệ cờ thật và chi phí duyệt, không hạ tiêu chuẩn an toàn để giữ biên.

40 doanh nghiệp của văn phòng thử nghiệm không đồng nghĩa 40 văn phòng khách hàng. Điều kiện dừng doanh thu cần ít nhất 10 văn phòng trong 2 tháng, nên chưa đủ mẫu thì giữ thử nghiệm, không tuyên bố đã vượt kiểm tra kinh doanh. 12.000 hóa đơn/tháng mô tả văn phòng thử nghiệm; 1.760 việc/khách/tháng là giả định kinh tế, hai số không được tráo đổi.

## Tự đánh giá và giới hạn

Nội dung cần hiểu và giải thích được là quan hệ giữa dữ liệu, cổng, quyền tự động và chi phí. Không thấy lỗi trên 40 ca không chứng minh tỷ lệ lỗi thật bằng 0. Cổng bổ sung 300 ca và 1.000 ca là đề xuất, chưa chạy thử. Chưa có báo giá tích hợp, lịch giờ Tùng hoặc dữ liệu hạch toán nên phải xác nhận trước triển khai.

Bài được xây dựng với hỗ trợ AI trong phiên làm việc, dựa trên hồ sơ giả định. [Ghi nhận phân tích AI](AI_REVIEW.md) trình bày nhận định về rủi ro bị mô hình miễn phí làm thay. Các điểm số là phán đoán cho bài lab, không phải bằng chứng thị trường đã kiểm chứng.

## Nguồn

- `docs/CS13_HoSoTinhHuong.pdf`, Đề 1, trang 2–3.
- `docs/CS13_SlideLop_AIRoadmap.pdf`, slide 74, 81–85.
- `src/CS13_Roadmap_De1.xlsx`, mẫu biểu và công thức gốc.
- `CHECKPOINTS.md`, `RUBRIC.md`, `SUBMISSION.md`.
