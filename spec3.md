# R4 · Mức tự chủ
# 4.1. Mức tự chủ và lý do lựa chọn cho từng Tool

| Tool | Mức tự chủ | Sai thì ai chịu gì? | Đảo ngược được không? | Chờ người thì mất gì? |
|---|---|---|---|---|
| `tra_cuu_tai_lieu` | Tự làm | Học viên nhận đoạn không khớp câu hỏi, nhưng có mã mục (§3.2...) nên tự kiểm được. | Chỉ đọc, không đổi gì. | Học viên 10 giờ tối bị kẹt một chữ là bỏ, đúng nỗi đau của lát cắt. |
| `chuyen_TA` | Tự làm | Chuyển thừa thì TA tốn vài phút. Chuyển mà không ghi nhận thật thì học viên tin đã có người lo. | Đảo được. | Chờ ai duyệt việc chuyển thì chính việc chuyển bị chậm, vô nghĩa. |
| `goi_y_bai_tap` | Tự làm có giới hạn, tách theo trạng thái bài (xem mục 2). | Học viên chép đáp án Bài 3, không học được gì. | Không: đã chép thì không rút lại được. | TA hết giờ 22:00, chờ đến sáng thì Bài 3 sát hạn 13/11. |
| `dang_FAQ` | Cần người duyệt (TA). | Cả lớp đọc nội dung sai (Ca B: câu sai §3.3 bị đăng như thể đúng). | Gỡ được nhưng nhiều người đã đọc. | Không đăng ngay chỉ mất một chút thời gian, học viên vẫn có câu trả lời riêng. |

## 4.1.1. Các phương án đã loại

Mỗi tool cần có lý do rõ ràng cho các mức tự chủ bị loại:

- **`tra_cuu_tai_lieu`:** Loại mức "Cần duyệt", vì không có gì để duyệt trên một thao tác chỉ đọc mà người duyệt lại offline lúc tối.
- **`chuyen_TA`:** Loại mức "Cần duyệt", vì lý do tương tự. Loại mức "Cấm", vì đây là đường lui an toàn duy nhất của sản phẩm; cấm nó đồng nghĩa với việc mất lối thoát.
- **`dang_FAQ`:** Loại mức "Tự làm", vì lỗi có thể lan ra cả lớp và là kiểu lỗi âm thầm mà đề đã cảnh báo. Loại mức "Cấm", vì câu hỏi nhiều người cùng thắc mắc đăng lên FAQ là giá trị thực sự của sản phẩm.

## 4.1.2. Hàng chờ duyệt (Approval Queue)

Với tool cần duyệt, rubric yêu cầu làm rõ ba yếu tố:

1. **Ai duyệt?** TA.
2. **Người duyệt thấy gì?** Câu hỏi gốc, câu trả lời AI và mã mục trích dẫn.
3. **Nếu quá hạn thì sao?** 

Đối với `dang_FAQ`, nếu quá hạn thì nội dung không được đăng. Đây là cơ chế mặc định an toàn, học viên không bị ảnh hưởng bởi một nội dung chưa được kiểm chứng.

---

# 4.2. Tool khó xếp nhất: `goi_y_bai_tap`

Đây là tool khó phân quyền nhất vì mỗi mức tự chủ đều có một cái giá riêng. Đây cũng là phần cần phân tích sâu để thể hiện khả năng đánh giá rủi ro và thiết kế quyền tự chủ của AI.

## 4.2.1. So sánh các phương án

| Phương án | Cái giá | Trỏ về kịch bản §2 |
|---|---|---|
| Tự làm hoàn toàn | AI gợi ý quá tay, học viên chép đáp án Bài 3, không đảo ngược được. | Ca A (xin xác nhận đáp số bài đang mở). |
| Cần TA duyệt mọi gợi ý | Học viên bình thường phải chờ TA, trong khi TA hết giờ 22:00. | Kịch bản bình thường: hỏi gợi ý bước đầu lúc 22:30. |
| Cấm hoàn toàn | Lát cắt mất lý do tồn tại, vì học viên bị kẹt và không ai gợi ý. | Kịch bản bình thường. |
| **Tách theo trạng thái bài (chọn)** | Cần AI đọc đúng trạng thái bài từ trang khóa học. Nếu đọc sai thì rơi lại rủi ro Ca A. | Ca A và kịch bản bình thường. |

## 4.2.2. Cách chốt mức tự chủ

Tách `goi_y_bai_tap` thành ba hành vi cụ thể:

| Trạng thái / Hành vi | Quyền của AI | Phạm vi thực hiện |
|---|---|---|
| Bài đã hết hạn và có đáp án (Bài 2) | Tự làm | Được giải thích đầy đủ. |
| Bài đang mở (Bài 3) | Tự làm có giới hạn | Chỉ cung cấp bước đầu, không cung cấp số liệu kết quả. |
| Xác nhận hoặc đưa đáp số bài đang mở | Cấm | Prototype không cung cấp nút thực hiện hành vi này. |

**Lập luận chính:**

Rủi ro học viên sao chép đáp án là rủi ro không thể đảo ngược, do đó phải được kiểm soát bằng thiết kế hệ thống thay vì chỉ dựa vào cảnh báo.

Ngược lại, việc cung cấp gợi ý bước đầu có chi phí rủi ro thấp và phù hợp với mục tiêu hỗ trợ học tập.

Mức "Cấm" cũng tạo ra một ví dụ cụ thể cho nguyên tắc: **Hành vi bị cấm phải không có nút thực hiện trong prototype (R5).**

---

# 4.3. Thử nghiệm mức tự chủ trên 3 kịch bản

Đánh giá mức tự chủ đã chọn thông qua ba câu hỏi:

1. Cái sai có bị chặn không?
2. AI có còn thực hiện khi lẽ ra phải hỏi người không?
3. Người dùng bình thường có phải chờ đợi vô ích không?

## 4.3.1. Bảng đánh giá

| Kịch bản | Cái sai có bị chặn? | Còn làm khi lẽ ra phải hỏi? | Người dùng bình thường chờ vô ích? |
|---|---|---|---|
| **Ca A** (xác nhận đáp số Bài 3) | Có. Xác nhận đáp số thuộc mức cấm, AI chỉ cung cấp bước đầu. | Không còn, nhưng cần kiểm tra thêm: nếu học viên hỏi khéo ("Trung bình là 15,25 phải không?"), AI có vô tình xác nhận không? | Không. Học viên vẫn nhận được bước đầu ngay lập tức. |
| **Ca B** (§3.3 có câu sai) | Một phần. `dang_FAQ` cần duyệt nên nội dung sai không lan ra cả lớp. Tuy nhiên, câu trả lời riêng vẫn trích §3.3, nên AI cần có cờ cảnh báo. | Có thể. `tra_cuu_tai_lieu` ở mức tự làm vẫn trả về đoạn sai mà không cảnh báo. Đây là điểm còn hở. | Không. Học viên vẫn được trả lời và có nút báo lỗi. |
| **Bình thường** (hạn nộp Bài 3? Hàm Excel tính độ lệch chuẩn?) | Không có gì cần chặn. | Không. | Không. Hạn nộp được lấy từ trang khóa học, tra cứu tự làm nên học viên nhận được câu trả lời ngay. |

## 4.3.2. Điểm hở phát hiện được và đề xuất bổ sung

Điểm hở ở Ca B chính là giá trị của việc thử nghiệm: nó cho thấy mức tự chủ hiện tại chưa kiểm soát được rủi ro **trích dẫn nguồn sai**.

Có thể ghi nhận trực tiếp điểm yếu này và đề xuất bổ sung một luật:

> **Luật bổ sung:** Tool `tra_cuu_tai_lieu` phải kèm cờ cảnh báo "Mục này đang được báo xem lại" khi giảng viên đánh dấu tài liệu có vấn đề.

Luật này giúp AI không tiếp tục trình bày một đoạn tài liệu đang bị nghi ngờ như một nguồn thông tin đáng tin cậy.

Đây cũng là một ví dụ phù hợp với phần **"Tốt khi"** trong yêu cầu thiết kế hệ thống.

---

# 4.4. Một mức tự chủ đã thay đổi lời hứa nào với người dùng?

Chọn một thay đổi và làm rõ hai trạng thái: **Trước và Sau**.

## 4.4.1. Phương án 1: `dang_FAQ` ở mức Cần duyệt

- **Trước:** "AI đăng câu trả lời cho cả lớp".
- **Sau:** "AI soạn sẵn, TA duyệt rồi mới đăng".

Học viên không còn kỳ vọng câu trả lời xuất hiện ngay lập tức trên FAQ. Thay vào đó, nội dung chỉ được công khai sau khi có sự xác nhận của TA.

## 4.4.2. Phương án 2: `goi_y_bai_tap` có giới hạn

- **Trước:** "AI giúp bạn giải bài".
- **Sau:** "AI gợi ý bước đầu, bạn tự làm".

Lời hứa chuyển từ việc cung cấp lời giải sang hỗ trợ quá trình tư duy, giúp học viên tự hoàn thành bài tập thay vì phụ thuộc vào đáp án.

## 4.4.3. Phương án 3: `chuyen_TA` chỉ thông báo khi tool thành công

- **Trước:** "AI báo TA".
- **Sau:** "AI đưa câu hỏi vào hàng chờ, TA trả lời sau 08:00".

Lời hứa mới phản ánh chính xác hơn trạng thái thực tế của hệ thống. AI chỉ thông báo đã chuyển khi câu hỏi thực sự được ghi nhận vào hàng chờ, thay vì tạo cảm giác TA đã nhận và đang xử lý câu hỏi ngay lập tức.

---

# 4.5. Kết luận

Thiết kế mức tự chủ không đơn thuần là quyết định AI được phép làm gì, mà phải cân bằng giữa ba yếu tố:

- **An toàn:** Ngăn chặn những hành vi có thể gây hậu quả khó đảo ngược.
- **Tính tự chủ:** Cho phép AI xử lý các tác vụ rủi ro thấp mà không cần con người can thiệp.
- **Trải nghiệm người dùng:** Tránh bắt người dùng chờ đợi khi việc duyệt thủ công không thực sự cần thiết.

Nguyên tắc thiết kế được lựa chọn là:

> **AI tự xử lý những hành vi rủi ro thấp, bị giới hạn ở những hành vi có thể ảnh hưởng đến kết quả học tập và phải có con người phê duyệt trước những hành vi có khả năng lan truyền sai sót đến nhiều người.**