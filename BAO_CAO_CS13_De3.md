# Báo cáo lab CS13 — Đề 3: RaViện

- Tên nhóm: Tennhombimat
- Quy mô: 1 thành viên
- Họ tên: Nguyễn Anh Dũng
- MSSV: 2A202602554
- Phụ trách: toàn bộ CP0–CP5, có AI hỗ trợ.
- Repo bài làm:
- Ngày khởi động dự án:
- Ngày bắt đầu pilot sau phê duyệt:

## Kết quả bàn giao

Đã hoàn thiện nội dung CP1–CP5 trong `Tennhombimat_CS13.xlsx` và một slide chỉnh sửa được trong `Tennhombimat_CS13_Slide.pptx`. Lộ trình bao quát đủ 0–3, 3–6 và 6–12 tháng. Có 6 việc được chấm điểm, hai cổng tăng mức áp dụng, điều kiện dừng, rà soát theo lịch và sự kiện, cùng năm ô nội dung lãnh đạo dưới 60 chữ/ô.

Đây là phương án AI hỗ trợ soạn để nhóm đọc, phản biện và xác nhận. Không có thử nghiệm lâm sàng hoặc chạy mô hình thực tế trong công việc này. Đầu vào ghi nhận hồ sơ được rà soát có AI hỗ trợ. Không khẳng định đã thử nghiệm thực tế hoặc hoàn thành nộp bài. Quy định lab yêu cầu nhóm hiểu và giải thích quyết định; người nộp cần tự rà soát và tuân thủ hướng dẫn của giảng viên về sử dụng AI.

## Kết luận đề xuất

Giữ trạng thái **chưa phát hành** hiện tại. Sửa lỗi nhầm thời điểm insulin, thêm 5 ca insulin vào bộ 40 ca và chạy lại cả 45 ca trước khi xét pilot một khoa. Bác sĩ bệnh viện luôn đọc, sửa và ký 100% bản nháp. Máy không tự gửi cho người bệnh. Mức 3 không làm trong lộ trình này.

Ưu tiên theo điểm tính từ giả định đề xuất:

| Việc | Điểm AI | Hạng | Quyết định |
|---|---:|---:|---|
| Đối chiếu thuốc | 6,94 | 1 | Tự làm trước để xử lý lỗi đang chặn phát hành |
| Gắn cờ hồ sơ mâu thuẫn | 4,82 | 2 | Tự làm |
| Nháp diễn biến và chẩn đoán | 3,38 | 3 | Tự làm sau điều kiện an toàn |
| Mã hoá bảo hiểm | 1,44 | 4 | Không tự làm vì bệnh viện đã có phần mềm chuyên dụng |
| Lời dặn dễ hiểu | 1,20 | 5 | Chờ, xem lại tháng 6 |
| Chuyển khoa | 0,48 | 6 | Chờ, chỉ khám phá tháng 6–12 với bộ đề riêng |

Điểm là công cụ so sánh, không ghi đè điều kiện an toàn hoặc lý do loại công việc trùng phần mềm sẵn có. Các hệ số đã được giải thích tại cột Q. Nhận định AI về khả năng mô hình miễn phí làm thay là dự báo để thảo luận, không phải kết quả khảo sát thị trường. Bài không dựa vào tuyên bố cập nhật nào về sản phẩm miễn phí cụ thể.

## Cổng đánh giá và lịch

**Mức 1:** sau sửa lỗi, chạy đủ 45 ca với 0 lỗi nghiêm trọng, tỷ lệ đạt quy về thực tế ≥95%, không tầng nào tụt, kappa ≥0,8. BS Phương và DS Hải xác nhận. Năm ca tăng cường insulin phải được kiểm riêng; không cộng thô vào tỷ lệ thực tế làm sai trọng số. Tỷ trọng bốn tầng của RaViện chưa được đề cung cấp cụ thể nên phải dùng/chốt trọng số của bộ đánh giá gốc khi thực hiện.

**Mức 2:** đề xuất chỉ xem xét sau 600 bản liên tiếp ở Mức 1 được DS kiểm 100%, không có lỗi thuốc nghiêm trọng, giữ cổng hồi quy và đạt hiệu quả tháng pilot 3. Mục tiêu thời gian hoàn tất ≤1/3 nền trên ít nhất 100 bản đo cặp; tỷ lệ sửa nhiều ≤30% trên ít nhất 300 bản trong tháng pilot 3. Các ngưỡng/cỡ mẫu bổ sung là đề xuất chưa được chuyên gia duyệt. Quy tắc 3/600 ≈0,5% cho thấy 0 lỗi quan sát không chứng minh tỷ lệ lỗi thực bằng 0 và không tự đủ để giảm duyệt.

“Sửa nhiều” được đề xuất là phải sửa thuốc, chẩn đoán, diễn biến chính hoặc viết lại trên 30% nội dung; nhóm cần chốt định nghĩa trước khi đo. Khi giảm DS, mọi cờ/rủi ro thuốc vẫn phải được duyệt, đồng thời lấy mẫu ngẫu nhiên phần còn lại. Tổng 10% là giả định kinh tế có điều kiện, không phải hạn mức để bỏ qua cờ. Bác sĩ vẫn ký 100%.

Rà soát ngày 30/60/90 từ khởi động; tách riêng cuối tháng pilot 3 tính từ ngày pilot được duyệt. Nếu thiếu mẫu hoặc chưa đủ lịch chuyên gia, hoãn mở rộng. Rà soát ngay khi đổi mô hình, giá, tính năng nền tảng hoặc quy định áp dụng.

## Kinh tế và nguồn lực

Giữ nguyên số liệu của đề: gọi AI 2.968 đ/bản, hạ tầng/đánh giá/khác 1.200 đ/bản; DS công ty 3 phút/bản ở 150.000 đ/giờ; giá 15 triệu đ/khoa/tháng, 1.200 bản. Bác sĩ bệnh viện không tính vào chi phí nhà cung cấp.

| Phương án | DS công ty duyệt | Chi phí/bản | Biên gộp | Lãi gộp/khoa/tháng |
|---|---:|---:|---:|---:|
| Mức 1 | 100% | 11.668 đ | 6,656% | 998.400 đ |
| Mức 2, có điều kiện | 10% | 4.918 đ | 60,656% | 9.098.400 đ |

Tính trên đúng giá và sản lượng giả định, chưa trừ chi phí cố định. Chi phí DS khi duyệt một bản là 3 × 150.000 / 60 = 7.500 đ. Chi phí tổng = 4.168 + 7.500 × tỷ lệ DS. Muốn biên ≥60%, chi phí không quá 5.000 đ/bản, do đó tổng tỷ lệ DS không quá 11,0933%. Nếu an toàn đòi tỷ lệ cao hơn, phải giữ an toàn và xét giá/phạm vi/vốn; không giảm duyệt để đạt con số.

Một vòng 40 hồ sơ đã tốn 20,3 giờ chuyên gia. Đề không cho giờ/tuần của BS Phương hay DS Hải, cũng không cho thời gian chấm 5 ca mới; các thông tin đó chưa có xác nhận thực tế; dự toán được bổ sung và ghi rõ là giả định ở dưới. Cổng 600 bản cần ít nhất 600 × 3/60 = 30 giờ DS theo giả định 3 phút, chưa tính giờ BS, phân xử và kiểm tra hiệu quả. Không dùng 20,3 giờ để khẳng định toàn bộ 45 ca hay 600 bản đã đủ nguồn lực.

Kịch bản đề: ký chậm 6 tháng sau thử nghiệm có thể cạn tiền tháng 9. Lãnh đạo cần xem hợp đồng và kế hoạch tiền trước tháng 6. Không có số dư tiền hoặc chi phí cố định để tính một runway mới.

## Điều kiện dừng

- Có 1 lỗi thuốc lọt tới người bệnh ở bất kỳ thời điểm nào: dừng ngay, điều tra và không mở khoa.
- Cuối tháng pilot 3, sửa nhiều trên 30% trên ít nhất 300 bản: dừng, không mở sang khoa khác.
- Chưa đủ 300 bản: chưa có bằng chứng đủ để mở rộng.
- Phát hiện lỗi thuốc nghiêm trọng trong nháp sau giảm DS: lùi Mức 1 và điều tra; nếu đã lọt người bệnh thì dừng ngay.
- Tháng 6 chưa có hợp đồng hoặc tỷ lệ DS cần thiết khiến kinh tế không đạt: dừng mở rộng, trình phương án giá/vốn cho lãnh đạo.

## Kiểm tra file

File đã được tính lại bằng LibreOffice và kiểm tra lại giá trị lưu. Trang `6_Tự kiểm tra` có 8/8 mục Đạt. Đây là kiểm tra mức điền, không phải điểm 100 hay xác nhận an toàn. Bộ kiểm tra đếm đúng hai cổng áp dụng (Mức 1 và 2). Mức 3 không triển khai và không được tính cổng.

Giữ nguyên công thức, dữ liệu kinh tế, danh sách thả xuống và bảo vệ của mẫu. Chỉ điền nội dung ô vàng; tăng chiều cao các hàng liên quan để đọc được. Kiểm tra độ nhạy tỷ lệ DS 10% thành 100% cho kết quả lần lượt 60,656% và 6,656%, rồi khôi phục 10%. Không có ô lỗi công thức trong bản cuối. Đã kiểm tra bản xem trước của các vùng thay đổi. Chưa kiểm tra trong Microsoft Excel hay xác nhận vận hành thực tế.

## Thông tin hoàn thiện và chấm thử

Đã điền Nguyễn Anh Dũng, MSSV 2A202602554, nhóm Tennhombimat. Thành viên duy nhất phụ trách CP0–CP5 với AI hỗ trợ. Đã hoàn thiện TEAM.md và báo cáo cá nhân. Sáu mục hồ sơ được rà soát và ghi Có kèm nhãn AI hỗ trợ. Tự chấm tham khảo **94/100**, gồm 19 + 19 + 23 + 14 + 19; chi tiết tại CHAM_THU_CS13.md. Điểm trang 7 ghi rõ là tự chấm, không phải điểm giảng viên.

Dự toán lab: BS có 2 giờ/tuần cho chấm đánh giá, DS có 4 giờ/tuần; 5 ca insulin dự trù thêm 4 giờ tổng, nên tạm tính 24,3 giờ cho 45 ca và bố trí ít nhất 5 tuần. Đây là ngân sách dự kiến, chưa có phân bổ đủ chi tiết từng người để xác nhận lịch. Giờ BS chấm đánh giá không thay giờ đọc/sửa/ký trong công việc lâm sàng thường ngày.

DS 4 giờ/tuần ở 3 phút/bản kiểm được tối đa 80 bản/tuần, nên 600 bản cần ít nhất 8 tuần. Pilot điều tiết theo năng lực, không mặc định sản lượng thương mại 1.200 bản/tháng. Nếu Mức 1 vận hành đủ 1.200 bản/tháng thì cần 60 giờ DS/tháng và phải cấp thêm nguồn lực. DS 10% ở Mức 2 tương đương 6 giờ/tháng nếu đủ điều kiện an toàn và tổng cờ/mẫu cho phép.

Thông tin ngoài hệ thống còn để trống: link repo, số nhóm do lớp cấp nếu yêu cầu, xác nhận đã gửi VLearn. Ngày pilot và lịch thực tế là điều kiện tương lai, không ghi thành phê duyệt đã có.

Theo SUBMISSION.md của lớp, hạn bản CP1–CP4 là trước 18:00 ngày 16/10/2026; bản hoàn thiện CP5 trước 23:59 ngày 19/10/2026, giờ Việt Nam. Cách nộp của lớp qua repo GitHub được dùng thay chỉ dẫn nộp file trực tiếp trong PDF cũ.

## Nguồn sử dụng

1. `K4-L3-CS13-AI-Roadmap/docs/CS13_HoSoTinhHuong.pdf`, trang 6–7, Đề 3 RaViện.
2. `K4-L3-CS13-AI-Roadmap/src/CS13_Roadmap_De3.xlsx`, mẫu và công thức.
3. `K4-L3-CS13-AI-Roadmap/README.md`, `CHECKPOINTS.md`, `RULES.md`, `RUBRIC.md`, `SUBMISSION.md`, các mẫu nhóm/báo cáo.
4. `day28 - ai produc roadmap .pdf`, các trang 74 và 80–86, công thức và hướng dẫn thực hành.

Các mục tuân thủ là công việc phải kiểm tra với đầu mối bệnh viện trước thử nghiệm. Bài không khẳng định tính đúng/hiện hành của số hiệu hay phân loại pháp lý trong slide gốc và không đưa ra hướng dẫn điều trị.
