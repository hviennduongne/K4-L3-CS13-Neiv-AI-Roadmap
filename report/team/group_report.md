# Báo cáo nhóm · Lab Day 13

## Thông tin

- Nhóm: Neiv
- Thành viên: Dương Thị Hồng Viên
- Mã sinh viên: 2A202602385
- Khóa học: VinUni AI Thực Chiến – Cohort IV
- Đề: 1 · SổSạch
- Sản phẩm chính: [Excel](../../Neiv_CS13.xlsx) và [1 slide lãnh đạo](../../Neiv_CS13_Slide.pptx).

## Mục tiêu và căn cứ

1 việc là 1 hóa đơn được đọc, đối chiếu và nhập vào phần mềm kế toán. Mục tiêu là giảm 50% giờ nhập hóa đơn ảnh mà vẫn chặn sai mã số thuế/tiền. Bộ đề có 40 hóa đơn thuộc 4 tầng; tỷ trọng thực tế Thường 65%, Khó 25%, Nguy hiểm 7%, Ngoài phạm vi 3%. Phải quy kết quả theo tỷ trọng thực tế, không tự suy số ca từng tầng bằng cách nhân rồi làm tròn 40 ca.

Hồ sơ cho phép phát hành bản 2 với tỷ lệ đạt 97,3%, 0 lỗi nghiêm trọng, 0 tầng tụt và kappa 0,90. Đây là dữ liệu đề cho sẵn, không phải thí nghiệm đã chạy trong bài. Cổng bổ sung trên hóa đơn thật chỉ là kế hoạch kiểm chứng.

## Ưu tiên và giải pháp

| Việc | Điểm | Quyết định và căn cứ |
|---|---:|---|
| Nhập tệp gốc | 9,75 | Mua/tận dụng tính năng phần mềm có sẵn, không tự xây lại |
| Gắn cờ | 8,55 | Tự làm quy tắc và hàng đợi phù hợp quy trình, ưu tiên an toàn/chi phí |
| Đối chiếu MST | 7,40 | Mua dịch vụ, tích hợp chặn ngoại lệ trước khi tăng tự nhập |
| Đọc ảnh | 2,84 | Tự làm quy trình hai bước, đo giảm giờ trên cùng bộ ảnh |
| Gợi ý hạch toán | 0,63 | Chờ dữ liệu khách hàng và bộ đề riêng, xem lại tháng 6/9 |
| Hỏi đáp thuế chung | 0,34 | Không làm, thiếu bộ đề và rủi ro công cụ chung làm thay cao |

Nhập tệp gốc đứng đầu nhưng ưu tiên tự xây tập trung vào gắn cờ/đọc ảnh, vì chức năng nhập tệp đã tồn tại. Tra cứu MST là phụ thuộc an toàn. Điểm không thay thế quan hệ phụ thuộc. Bảy đầu vào và lý do cụ thể được ghi ở trang 1, không nhận điểm của bản mẫu làm mặc định. [Phân tích AI](AI_REVIEW.md) hỗ trợ cột L, chưa phải kiểm chứng thị trường.

## Mức tự động, cổng và nguồn lực

Mức 0 duyệt 100%, dùng khi cần quay lui. Mức 1 dự kiến duyệt 20%, gồm mọi cờ và mẫu 10% tổng việc chọn từ phần không cờ. Tuần đầu chị Hạnh kiểm 1% hóa đơn thật, lồng trong mẫu. Mức 2 dự kiến 10% khi cờ ≤5%, gồm mọi cờ cộng mẫu 5% tổng việc không cờ. Mức 3 dự kiến 5% khi cờ ≤2%, gồm mọi cờ cộng mẫu 3% tổng việc không cờ. Nếu tỷ lệ cờ cao hơn, tăng duyệt và tính lại chi phí, không bỏ qua cờ.

Cổng Mức 1 giữ ngưỡng hồ sơ trên 40 ca: ≥95% quy về thực tế, 0 lỗi nghiêm trọng, 0 tầng tụt, kappa ≥0,6; thêm chạy thử 1.000 hóa đơn, kiểm ít nhất 200. Mức 2 giữ cổng hồi quy và cần kiểm độc lập 300 hóa đơn thật đủ tầng, 0 lỗi nghiêm trọng. Mức 3 chưa cam kết, cần kiểm ít nhất 1.000 ca trong ít nhất 4 tuần, 0 lỗi nghiêm trọng. Chị Hạnh xác nhận nghiệp vụ, anh Tùng đối chiếu; lãnh đạo quyết định tăng mức sau kiểm chi phí.

Quy tắc gần đúng 3/n khi quan sát 0 lỗi cho giới hạn trên ở mức tin cậy 95%: 40 ca khoảng 7,5%, 300 ca khoảng 1%, 1.000 ca khoảng 0,3%. Không diễn giải 0 lỗi quan sát thành bảo đảm không có lỗi. Các ca lấy mẫu và ca khó phải ghi tách tầng; tỷ lệ tổng hợp quy theo phân bố thực tế.

Văn phòng thử nghiệm có 12.000 hóa đơn/tháng. Với 1,5 phút/ca, Mức 1 cần khoảng 60 giờ duyệt công ty/tháng, Mức 2 cần 30 giờ, Mức 3 cần 15 giờ, chưa tính các vòng đánh giá bổ sung. Đây là nhân sự vận hành của công ty, không dồn hết cho chuyên gia. Hạnh có tối đa 3 giờ/tuần. Một vòng 40 ca tốn 8,5 giờ nên chia ít nhất 3 tuần và xác nhận giờ hỗ trợ của Tùng. Kiểm 1% thực tế tuần đầu tương đương khoảng 30 ca/tuần nếu phân bố 4 tuần, ít nhất 45 phút rà nhanh; ca tranh luận cần thêm thời gian. Giới hạn 3 giờ vẫn phải bao gồm phần việc của Hạnh trong hồi quy và các ngoại lệ.

## Kinh tế và độ nhạy

Chi phí mỗi việc = 254 + 200 + tỷ lệ duyệt × 1,5 × 50.000 / 60. Biên gộp = 1 − 1.760 × chi phí / 3.970.000. Giữ nguyên số liệu đề.

| Mức | Chi phí/việc | Biên gộp |
|---|---:|---:|
| 0 (100%) | 1.704 đồng | 24,46% |
| 1 (20%) | 704 đồng | 68,79% |
| 2 (10%) | 579 đồng | 74,33% |
| 3 (5%) | 516,5 đồng | 77,10% |

Thử đổi đầu vào tỷ lệ duyệt Mức 1 sang 40% cho ra 954 đồng và biên 57,71%, rồi khôi phục 20%. Mức 1 chỉ còn dư khoảng 198,27 đồng/việc trước khi biên xuống 60%, nếu các đầu vào khác giữ nguyên. Phí tích hợp và dịch vụ mua phải đối chiếu phần chi phí 200 đồng đã có, tránh vừa bỏ sót vừa cộng trùng. Chưa có báo giá nên không khẳng định mô hình kinh tế đã được xác minh.

12.000 việc/tháng là quy mô văn phòng thử nghiệm; 1.760 việc/khách/tháng là giả định bình quân dùng tính kinh tế. Không đổi âm thầm 2 mẫu số này. Nếu khách thử nghiệm chịu cùng doanh thu 3,97 triệu nhưng xử lý toàn bộ 12.000 việc, phải thỏa thuận lại giá/hạn mức hoặc tính riêng trước ký hợp đồng.

## Lộ trình và điều kiện dừng

0–3 tháng tập trung đọc ảnh, gắn cờ, tích hợp công cụ sẵn có và đo hiệu quả ở Mức 1. 3–6 tháng chỉ mở Mức 2 sau cổng. 6–12 tháng khám phá hạch toán và Mức 3 nếu đủ dữ liệu, chuyên gia và kinh phí. Lịch không tự động cấp quyền tăng mức.

- Bất kỳ lúc nào có ít nhất 1 lỗi MST/tiền: dừng tự nhập, lùi Mức 0, điều tra và chạy hồi quy.
- Ngày 30: cờ thừa >10%/1.000 ca hoặc giảm giờ nhập <50%/100 ảnh thì sửa và giữ quy mô.
- Ngày 90: chưa đủ 300 ca kiểm hoặc có lỗi nghiêm trọng thì giữ/lùi mức, không mở Mức 2.
- Doanh thu bình quân <3,71 triệu/văn phòng trong 2 tháng liên tiếp, trên ít nhất 10 văn phòng: dừng mở rộng.
- Thiếu 10 văn phòng thì chưa đủ dữ liệu xét cổng doanh thu. 40 doanh nghiệp của khách thử nghiệm không được tính thành 40 văn phòng.
- Trước tháng 7 cần kiểm khả năng tiền mặt do kịch bản xấu hết tiền tháng 7; thiếu kinh phí thì dừng tuyển mới và xử lý nghĩa vụ hiện có.

Trang 4 ghi quyết định ngày 30/60/90 từ lúc bắt đầu triển khai và các sự kiện đổi mô hình/giá, đối thủ/nền tảng, pháp lý. Phần tuân thủ là công việc cần xác nhận quyền dữ liệu, nhật ký và nghĩa vụ áp dụng trước phát hành, không tự kết luận sản phẩm đã đáp ứng pháp luật.

## Kết quả, hạn chế và đóng góp

Excel được tính lại bằng Microsoft Excel, 8/8 mục trang 6 đạt; 5 ô trang 5 có lần lượt 34, 35, 48, 50 và 51 chữ. Slide có đúng 1 trang, cùng nội dung trang 5. Đã kiểm công thức kinh tế và thay đổi tỷ lệ duyệt. Kết quả tự kiểm tra không phải điểm chấm nội dung.

Chưa có dữ liệu vận hành mới, báo giá dịch vụ, giờ Tùng cam kết, mẫu 10 văn phòng hoặc dữ liệu hạch toán. Vì vậy bài chỉ đề xuất lộ trình có điều kiện. [Thông tin đóng góp](../../team/TEAM.md) và [báo cáo cá nhân](2A202602385_DuongThiHongVien.md) dẫn đến bằng chứng tương ứng.

## Nguồn

1. `docs/CS13_HoSoTinhHuong.pdf`, Đề 1, trang 2–3.
2. `docs/CS13_SlideLop_AIRoadmap.pdf`, slide 74 và 81–85.
3. `src/CS13_Roadmap_De1.xlsx`, công thức và mẫu gốc.
4. `CHECKPOINTS.md`, `RUBRIC.md`, `SUBMISSION.md`, `RULES.md`.
