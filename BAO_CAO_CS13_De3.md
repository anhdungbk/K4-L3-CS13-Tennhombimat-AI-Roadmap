# Báo cáo CS13 — Lộ trình sản phẩm RaViện

| Thông tin | Nội dung |
|---|---|
| Nhóm | Tennhombimat |
| Học viên | Nguyễn Anh Dũng |
| MSSV | 2A202602554 |
| Phạm vi | Đề 3, toàn bộ CP0–CP5 |
| Repo | [https://github.com/anhdungbk/K4-L3-CS13-Tennhombimat-AI-Roadmap](https://github.com/anhdungbk/K4-L3-CS13-Tennhombimat-AI-Roadmap) |

## 1. Bối cảnh và mục tiêu

RaViện soạn nháp tóm tắt ra viện cho bác sĩ khoa nội. Một việc tương ứng một bản nháp cho một người bệnh. Theo hồ sơ, bác sĩ đang mất 15–20 phút cho mỗi bản; phiên bản mới chưa phát hành vì một lỗi nhầm thời điểm dùng insulin.

Mục tiêu đề xuất là giảm hai phần ba thời gian hoàn tất, tính cả đọc, sửa và ký. Bác sĩ bệnh viện luôn duyệt và ký 100%; sản phẩm không tự gửi nội dung cho người bệnh. Các số liệu đầu vào là dữ liệu giả định của lab. Các ngưỡng bổ sung là mục tiêu kiểm chứng, chưa phải kết quả đã đạt.

## 2. Giả thuyết và ưu tiên

Giả thuyết trọng tâm: đối chiếu thuốc, gắn cờ mâu thuẫn và tạo nháp có dẫn nguồn giúp bác sĩ hoàn tất tóm tắt nhanh hơn mà không để lỗi thuốc lọt tới người bệnh.

Điểm ưu tiên kết hợp RICE, mức sẵn sàng dữ liệu/đánh giá và rủi ro chức năng bị thay thế. Chi tiết đầu vào tại `1_Danh sách việc!F5:L10`.

| Công việc | Điểm | Hạng | Quyết định |
|---|---:|---:|---|
| Đối chiếu thuốc với y lệnh cuối | 6,94 | 1 | Tự làm trước, xử lý lỗi chặn phát hành |
| Gắn cờ hồ sơ mâu thuẫn | 4,82 | 2 | Tự làm |
| Nháp diễn biến và chẩn đoán có nguồn | 3,38 | 3 | Tự làm sau điều kiện an toàn |
| Mã hóa bệnh cho bảo hiểm | 1,44 | 4 | Không tự xây, bệnh viện đã có phần mềm |
| Lời dặn dễ hiểu | 1,20 | 5 | Chờ đánh giá lại ở tháng 6 |
| Tóm tắt chuyển khoa | 0,48 | 6 | Chờ bộ đề riêng, khám phá tháng 6–12 |

Điểm không thay thế quyết định an toàn hoặc điều kiện triển khai. Nhận định về khả năng mô hình miễn phí thay thế chức năng là giả định chiến lược, chưa phải khảo sát thị trường đã kiểm chứng.

## 3. Lộ trình và cổng đánh giá

| Giai đoạn | Mức tự động và điều kiện |
|---|---|
| 0–3 tháng | Thử ngoại tuyến, sửa insulin, thêm 5 ca và đánh giá lại toàn bộ 45 ca. Chỉ vào Mức 1 sau cổng chất lượng; BS và DS kiểm 100% bản thử nghiệm. |
| 3–6 tháng | Duy trì Mức 1 để thu bằng chứng. Xét Mức 2 sau 600 bản và cổng hiệu quả; giảm DS từng bước theo rủi ro, BS vẫn ký 100%. |
| 6–12 tháng | Ổn định tối đa ở Mức 2. Chỉ khám phá chuyển khoa khi có bộ đề và chuyên gia riêng. Không triển khai Mức 3. |

**Cổng Mức 1:** sửa lỗi insulin, thêm 5 ca rồi chạy lại cả 45 ca. Yêu cầu 0 lỗi nghiêm trọng, tỷ lệ đạt quy về thực tế ≥95%, không tầng nào tụt và kappa ≥0,8. BS Phương và DS Hải xác nhận. Năm ca insulin tăng cường kiểm riêng; không cộng thô vào tỷ lệ quy về thực tế. Trọng số bốn tầng phải được chốt theo bộ đánh giá gốc.

**Cổng Mức 2 đề xuất:** 600 bản liên tiếp được DS kiểm 100%, không có lỗi thuốc nghiêm trọng và giữ cổng hồi quy. Đồng thời, trung vị thời gian hoàn tất ≤1/3 nền trên ít nhất 100 bản đo cặp; tỷ lệ sửa nhiều ≤30% trên ít nhất 300 bản trong tháng pilot thứ ba. BS Phương và DS Hải phê duyệt trước khi giảm duyệt. Quy tắc 3/600 ≈0,5% cho thấy 0 lỗi quan sát không chứng minh tỷ lệ lỗi thực bằng 0.

Định nghĩa sửa nhiều: phải sửa thuốc, chẩn đoán, diễn biến chính hoặc viết lại trên 30% nội dung. Định nghĩa và quy trình đo cần thống nhất trước thử nghiệm. DS luôn duyệt mọi cờ/rủi ro thuốc và lấy mẫu ngẫu nhiên phần còn lại. Tổng tỷ lệ 10% chỉ là mục tiêu có điều kiện; không bỏ qua cờ để giữ tỷ lệ này.

## 4. Dữ liệu, hạ tầng và nguồn lực

Dữ liệu cần ẩn danh, y lệnh cuối có phiên bản và liên kết nguồn. Hệ thống cần phân quyền, nhật ký, chặn xuất khi chưa ký và khả năng quay lui. Bệnh viện xác nhận phạm vi, quyền dữ liệu và yêu cầu tuân thủ trước pilot.

Hồ sơ cho biết 40 ca đã cần 20,3 giờ chuyên gia. Dự toán bổ sung của kế hoạch: BS 2 giờ/tuần cho chấm đánh giá, DS 4 giờ/tuần; 5 ca insulin thêm 4 giờ tổng. Tạm dự trù 24,3 giờ cho 45 ca, bố trí ít nhất 5 tuần. Tổng giờ chỉ là dự toán; lịch và phân bổ từng chuyên gia phải xác nhận trước khi thực hiện. Giờ BS chấm đánh giá tách khỏi giờ đọc, sửa và ký trong công việc lâm sàng.

Với 3 phút/bản, DS 4 giờ/tuần kiểm tối đa 80 bản/tuần; 600 bản cần ít nhất 8 tuần. Pilot điều tiết theo năng lực này. Nếu xử lý đủ 1.200 bản/tháng ở Mức 1, phải cấp 60 giờ DS/tháng. Ở Mức 2, tổng DS 10% tương ứng 6 giờ/tháng nếu đủ điều kiện an toàn.

## 5. Kinh tế theo mức tự động

Giữ nguyên đầu vào đề: gọi AI 2.968 đ/bản, hạ tầng/đánh giá/khác 1.200 đ/bản; DS công ty 3 phút/bản, 150.000 đ/giờ; giá 15 triệu đ/khoa/tháng cho 1.200 bản. BS bệnh viện không thuộc chi phí nhà cung cấp.

| Phương án | DS duyệt | Chi phí/bản | Biên gộp | Lãi gộp/khoa/tháng |
|---|---:|---:|---:|---:|
| Mức 1 | 100% | 11.668 đ | 6,656% | 998.400 đ |
| Mức 2 có điều kiện | 10% | 4.918 đ | 60,656% | 9.098.400 đ |

Các giá trị tháng giả định đủ 1.200 bản và thu đủ 15 triệu, chưa trừ chi phí cố định. Chi phí mỗi bản = 4.168 + 7.500 × tỷ lệ DS. Muốn biên ≥60% cần tỷ lệ DS ≤11,0933%. Nếu an toàn đòi tỷ lệ cao hơn, giữ mức duyệt và xem lại giá, phạm vi hoặc ngân sách.

Kịch bản xấu của đề là ký chậm 6 tháng sau thử nghiệm, có thể cạn tiền tháng 9. Rà soát hợp đồng và kế hoạch tiền trước tháng 6. Không suy ra thời gian duy trì mới từ lãi gộp khi thiếu số dư tiền và chi phí cố định.

## 6. Điều kiện dừng và rà soát

- Có 1 lỗi thuốc lọt tới người bệnh ở bất kỳ thời điểm nào: dừng ngay, điều tra và không mở khoa.
- Cuối tháng pilot thứ ba, sửa nhiều >30% trên ít nhất 300 bản: dừng mở rộng. Thiếu mẫu thì chưa đủ căn cứ để mở.
- Phát hiện lỗi thuốc nghiêm trọng trong nháp sau giảm DS: lùi Mức 1 và điều tra. Nếu đã lọt người bệnh thì dừng ngay.
- Tháng 6 chưa có hợp đồng hoặc kinh tế không khả thi ở mức duyệt an toàn: dừng mở rộng, xem lại giá/vốn.

Rà soát ngày 30/60/90 tính từ khởi động; tách riêng cuối tháng pilot thứ ba tính từ ngày pilot được phê duyệt. Rà soát ngay khi đổi mô hình, giá, tính năng nền tảng hoặc quy định áp dụng. Các ngày triển khai cụ thể sẽ xác định sau phê duyệt phạm vi và nguồn lực.

## 7. Kết quả bài làm và giới hạn

Đã hoàn thiện Excel CP0–CP5, một slide lãnh đạo, thông tin thành viên và báo cáo cá nhân. Trang tự kiểm tra đạt 8/8; có đúng hai cổng áp dụng. Năm nội dung slide đều dưới 60 chữ và khớp Excel. Công thức được giữ theo mẫu và tính lại bằng LibreOffice, không có ô lỗi. Chưa xác minh trong Microsoft Excel.

Tự đánh giá theo rubric: 94/100; chi tiết tại [CHAM_THU_CS13.md](CHAM_THU_CS13.md). Đây là điểm tham khảo, không phải điểm giảng viên. Kế hoạch chưa bao gồm thử nghiệm lâm sàng, đo hiệu quả hay hợp đồng thực tế.

## 8. Tài liệu tham khảo

1. [Hồ sơ tình huống](docs/CS13_HoSoTinhHuong.pdf), trang 6–7, Đề 3 RaViện.
2. [Mẫu Excel Đề 3](src/CS13_Roadmap_De3.xlsx), công thức và số liệu kinh tế.
3. [CHECKPOINTS.md](CHECKPOINTS.md), [RUBRIC.md](RUBRIC.md), [RULES.md](RULES.md), [SUBMISSION.md](SUBMISSION.md).
4. [Slide bài học](docs/CS13_SlideLop_AIRoadmap.pdf), phần công thức và thực hành roadmap.
