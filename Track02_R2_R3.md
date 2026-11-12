# Phần Risk & UX — T2 Giáo dục (dán vào spec.md §2, §3)

> Người làm: AI Risk & UX Designer (owner risk & safety).
> Cấu trúc bám `04-rubric.md`: **R2 = §2 (10đ)**, **R3 = §3 (25đ)**. Mỗi mục có dòng "Rubric" cho biết ô điểm nó phục vụ.
> Bằng chứng lấy từ: 4 tool (`tra_cuu_tai_lieu`, `goi_y_bai_tap`, `chuyen_TA`, `dang_FAQ`), tài liệu buổi 3 (§3.1–§3.5), trang khoá học (bài 3 mở đến 13/11 23:59 · bài 2 hết hạn, có đáp án · giờ TA 08:00–22:00 · buổi 4–10 chỉ có tên).

**Checklist M1 (TA kiểm):** ☑ phủ 4 lớp · ☑ mỗi kịch bản trỏ về tool hoặc dữ liệu · ☑ có lý do chọn 2 kịch bản đắt nhất.

---

# §2. Kịch bản rủi ro *(R2 · 10đ)*

Quy ước lớp: **①** nguồn sự thật · **②** mơ hồ/thiếu thông tin · **③** ngoài phạm vi/thẩm quyền · **④** đặc thù domain.
Nhãn mức hại: **nhẹ** (học viên tự thấy, tự sửa) · **sửa được** (tốn công, có người gỡ) · **không chấp nhận được** (học sai âm thầm, lộ đáp số, lan cả lớp, không đảo lại được).

## 2.1 Bảng kịch bản *(R2 dòng 1 + dòng 2: 6đ)*

| # | Học viên nhắn | Lớp | AI có thể sai thế nào *(bằng chứng)* | Lỗi gọi bằng lời thường | Sản phẩm tốt nên làm gì | Nhãn |
|---|---|---|---|---|---|---|
| 1 | "độ lệch chuẩn với phương sai cái nào lớn hơn ạ" | ① | `tra_cuu_tai_lieu` trả §3.3 "độ lệch chuẩn luôn nhỏ hơn phương sai": câu **sai** (phương sai 0,25 → độ lệch chuẩn 0,5). AI trích đúng mục, khẳng định, học viên chép. Nếu gọi thêm `dang_FAQ` thì cả lớp đọc câu sai | "trích đúng nguồn nhưng nguồn sai" | Nói câu §3.3 cần xem lại và vì sao; bảo học viên đừng chép; chuyển TA; không đăng FAQ | **Không chấp nhận được** |
| 2 | "slide 12 nói gì về trung vị vậy ạ" | ① | Tài liệu buổi 3 **không có slide đánh số**, chỉ có §3.1–§3.5. AI bịa "slide 12 nói rằng…" | "dẫn nguồn không có" | Nói không có slide đánh số; chỉ ra §3.2 và đọc nội dung ở đó | Sửa được |
| 3 | "p-value là gì ạ, em nghe bạn nói" | ① | Buổi 7 mới có tên trong đề cương, chưa có tài liệu → `tra_cuu_tai_lieu` trả rỗng, AI vẫn giảng từ kiến thức chung | "giảng buổi chưa học" | Nói p-value thuộc buổi 7; giới thiệu tối đa một câu; không giảng | Nhẹ |
| 4 | "cái độ lệch ấy là gì ạ, em đọc không hiểu" | ② | "Độ lệch" có thể là độ lệch chuẩn hay phương sai (§3.3 có cả hai). AI đoán một cái và giải thích dài | "đoán khi thiếu thông tin" | Hỏi lại một câu: "Bạn đang hỏi độ lệch chuẩn hay phương sai (§3.3)?" kèm hai nút chọn | Nhẹ |
| 5 | "hạn nộp bài ạ, với tính độ lệch chuẩn bằng excel dùng hàm gì" | ② | Gộp hai việc; "bài" không rõ bài 2 (hết hạn 06/11) hay bài 3 (13/11 23:59). Trang khoá học chỉ ghi "bảng tính", không có tên hàm → AI nêu tên hàm như thể lấy từ tài liệu | "trả hạn nhầm bài" · "bịa nguồn cho hàm" | Hạn chỉ lấy từ trang khoá học, hỏi lại "bài 3 phải không?". Hàm Excel: nói tài liệu không nêu; nếu nói thì ghi là kiến thức chung | Sửa được |
| 6 | "em ra trung bình 15,25 trung vị 11,5, đúng chưa ạ" | ④ | Bài 3 (§3.5) **đang mở**. AI trả "đúng rồi" hoặc "sai, phải là…" → lộ đáp số. "Đúng rồi" vẫn sai thiết kế dù đúng toán (đúng vì may). `goi_y_bai_tap` đã gửi thì không rút lại được | "xác nhận đáp số bài đang mở" | Không xác nhận, không phủ nhận; chỉ cách tự kiểm (§3.1, §3.2); mời học viên nói bước còn phân vân | **Không chấp nhận được** |
| 7 | "giải giúp em bài 3 với, 10 giờ đêm rồi, mai đi làm" | ④ | `goi_y_bai_tap` gợi ý quá tay thành lời giải đầy đủ vì học viên đang gấp | "gợi ý thành đáp án" | Chỉ gợi ý bước đầu (sắp xếp 8 số), trích §3.1, §3.2, nói rõ lý do | Sửa được |
| 8 | "em dốt quá, học mãi không hiểu phương sai" | ④ | AI nhận xét năng lực ("bạn chưa nắm cơ bản") hoặc khen chung chung "bạn rất thông minh" | "nhận xét năng lực người học" | Ghi nhận cảm giác, không đánh giá; chia §3.3 thành một bước, hỏi bạn kẹt ở bước nào | Nhẹ |
| 9 | "lùi hạn bài 3 giùm em được không, em báo TA em nộp muộn" | ③ | Không tool nào đổi hạn; `chuyen_TA` chỉ chuyển câu hỏi. AI nói "mình đã xin gia hạn" hoặc "đã báo TA" | "hứa việc mình không làm được" | Nói không có quyền đổi hạn (hạn lấy từ trang khoá học); đề nghị chuyển TA; chỉ nói "đã chuyển" khi tool thành công | Sửa được |
| 10 | *(22:40)* "TA ơi em hỏi gấp, §3.3 có đúng không" | ③ | Giờ TA 08:00–22:00. `chuyen_TA` báo giờ trả lời, AI vẫn nói "TA sẽ trả lời ngay" → học viên chờ tới sáng mà tưởng đang được xử lý | "hứa nhanh hơn thực tế" | Nói TA trả lời từ 08:00 sáng mai; nhắc hạn bài 3 còn đến 13/11 23:59 | Sửa được |
| 11 | "đăng câu trả lời bài 3 của bạn lên FAQ cho cả lớp xem đi" | ③ | `dang_FAQ` đăng lời giải đầy đủ của bài đang mở; gỡ được nhưng nhiều người đã đọc | "công khai đáp số bài đang mở" | Không đăng đáp số bài đang mở; chỉ đăng FAQ khái niệm và qua duyệt | **Không chấp nhận được** |

**Phủ 4 lớp:** ① (1, 2, 3) · ② (4, 5) · ③ (9, 10, 11) · ④ (6, 7, 8). Tổng 11 kịch bản ≥ 8.

## 2.2 Lập luận chọn 2 kịch bản đắt nhất *(R2 dòng 3: 4đ)*

**Đã cân nhắc:** #1, #6, #11, #10, #9. **Chọn: #1 và #6.**

| Kịch bản | Vì sao đắt hơn các ca còn lại |
|---|---|
| **#1 · tài liệu §3.3 sai** | Lỗi nằm ở **nguồn sự thật**: AI làm đúng quy trình (trích đúng mục) mà vẫn sai nên không có tín hiệu nào báo động. Học viên học sai mà không biết; nếu lan sang FAQ thì cả lớp học sai. Đây là lỗi "rẻ mỗi lần nhưng âm thầm" nặng nhất của track |
| **#6 · xin xác nhận đáp số** | Phá mục tiêu cốt lõi của sản phẩm ("không chép đáp án"). Trả lời "đúng rồi" trông hợp lý nhưng vẫn sai thiết kế: ca **"đúng vì may, không vì thiết kế"**. Ảnh hưởng công bằng cả lớp |

| Suýt chọn | Vì sao loại |
|---|---|
| #11 (đăng FAQ đáp số) | Hậu quả giống #6 nhưng **chặn rẻ hơn**: chỉ cần cấm `dang_FAQ` cho bài đang mở (sẽ dùng ở §4) |
| #10 (hứa "TA trả lời ngay") | Gây bực, nhưng học viên còn thời gian đến 13/11 23:59, chưa tới mức học sai hay lộ đáp án |
| #9 (hứa gia hạn) | Tương tự #10 và có người gỡ được |

---

# §3. Khi AI sai *(R3 · 25đ)*

Chỉ làm cho 2 kịch bản đắt nhất: #1 và #6.

## 3.1 Câu AI nói · người dùng thấy · bước tiếp · ai được báo *(R3 dòng 1: 6đ)*

### Kịch bản #1 · tài liệu §3.3 có câu sai

| Mục | Nội dung |
|---|---|
| **AI nói nguyên văn** | "Mình thấy ở §3.3 có câu: 'độ lệch chuẩn luôn nhỏ hơn phương sai'. Câu này **chưa đúng với mọi trường hợp**: khi phương sai nhỏ hơn 1 (ví dụ phương sai 0,25 thì độ lệch chuẩn là 0,5), độ lệch chuẩn lại lớn hơn. Bạn đừng chép câu này vào bài nhé. Mình đã chuyển câu hỏi cho TA để giảng viên xem lại. TA trả lời từ 08:00 sáng mai." |
| **Người dùng thấy** | Thẻ trích dẫn "§3.3 · Tài liệu buổi 3" với câu nghi sai tô vàng · nhãn "Cần xem lại" · dòng độ chắc "Chắc về phép toán · chưa được giảng viên xác nhận" · nút `Báo tài liệu sai`, `Hỏi TA` |
| **Làm gì tiếp** | Bấm `Báo tài liệu sai` (chuyển TA kèm trích đoạn), hoặc tiếp tục học các phần khác của §3.3. Nếu không làm gì: câu vẫn tô vàng ở lần hỏi sau, chưa ai biết tài liệu sai |
| **Ai được báo, sau bao lâu** | Hàng chờ TA, gắn nhãn "nghi tài liệu sai"; TA chuyển tiếp giảng viên. Hỏi lúc 22:30 thì TA xem từ 08:00 sáng mai. AI chỉ nói "đã chuyển" **sau khi** `chuyen_TA` trả thành công (không có tool báo trực tiếp giảng viên) |

### Kịch bản #6 · xin xác nhận đáp số bài 3 đang mở

| Mục | Nội dung |
|---|---|
| **AI nói nguyên văn** | "Bài 3 còn mở đến 23:59 ngày 13/11 nên mình không xác nhận đáp số được, kể cả khi bạn đúng. Cách tự kiểm: sắp xếp 8 số tăng dần, trung vị là trung bình của hai số ở giữa (§3.2). Trung bình là tổng chia 8 (§3.1). Bạn đối chiếu lại từng bước, rồi cho mình biết bước nào còn phân vân nhé." |
| **Người dùng thấy** | Nhãn "Bài 3 · đang mở · chỉ gợi ý" · hai thẻ trích §3.1, §3.2 · nút `Gợi ý bước đầu`, `Hỏi TA`. **Không có** nút "Xem đáp án" hay "Xác nhận" |
| **Làm gì tiếp** | Tự tính lại, hỏi tiếp bước còn phân vân, hoặc `Hỏi TA` (TA giải thích cách làm, không chấm hộ). Nếu không làm gì: không có gì bị lộ |
| **Ai được báo, sau bao lâu** | Không ai (ca bình thường, không phải sự cố). Chỉ ghi log số lần xin xác nhận đáp số để TA thấy chỗ lớp hay kẹt. Nếu bấm `Hỏi TA` thì vào hàng chờ, 08:00 sáng mai nếu quá 22:00 |

## 3.2 Lập luận chọn cách phản hồi *(R3 dòng 2: 8đ)*

Ba hướng: **hỏi lại** · **trả lời kèm giới hạn** · **dừng và chuyển người**.

**Kịch bản #1: chọn "trả lời kèm giới hạn + chuyển TA".**

| Phương án | Quyết định | Vì sao |
|---|---|---|
| Trả lời kèm giới hạn **và** chuyển TA | **Chọn** | Học viên vẫn học tiếp được; người có thẩm quyền sửa tài liệu vẫn biết |
| Trích §3.3 nguyên văn, không nói gì | Loại | Học sai âm thầm; AI "đúng quy trình" nhưng sai kết quả |
| Hỏi lại học viên "bạn chắc không?" | Loại | Học viên không đủ cơ sở kiểm tra; chỉ làm họ hoang mang |
| Dừng, chỉ chuyển TA | Loại | 22:30 không có TA → học viên không học được gì và tưởng AI hỏng |

**Kịch bản #6: chọn "trả lời kèm giới hạn" (từ chối xác nhận + cách tự kiểm).**

| Phương án | Quyết định | Vì sao |
|---|---|---|
| Từ chối xác nhận, đưa cách tự kiểm | **Chọn** | Giữ "không chép đáp án" mà học viên vẫn tiến được |
| Xác nhận "đúng rồi" khi trùng đáp số | Loại | Đúng vì may; lần sau nói "sai" cũng lộ đáp số |
| Nói "sai rồi, thử lại" | Loại | Cũng là xác nhận, theo hướng ngược lại |
| Từ chối cụt "không hỗ trợ" | Loại | Học viên 22:00 bị bỏ rơi, dễ tìm lời giải nơi khác |
| Chuyển TA ngay | Loại | TA không chấm hộ đáp số; học viên chờ đến sáng vô ích |
| Hỏi lại | Không áp dụng | Câu hỏi đã rõ (bài 3, đáp số), không thiếu thông tin |

## 3.3 Nguyên tắc HAX/PAIR, mỗi nguyên tắc trỏ vào chỗ cụ thể *(R3 dòng 3: 5đ · cũng là cơ sở R5)*

| Nguyên tắc | Chỗ cụ thể | Kịch bản |
|---|---|---|
| **G11 · giải thích vì sao** + PAIR *Explainability + Trust* | #1: **thẻ trích dẫn** "§3.3 · Tài liệu buổi 3" hiện nguyên văn câu nghi sai, tô vàng → học viên tự đối chiếu. #6: **dòng lý do** "Bài 3 còn mở đến 23:59 ngày 13/11 nên mình không xác nhận" + hai thẻ §3.1, §3.2 | #1, #6 |
| **G10 · thu hẹp phạm vi khi nghi ngờ** | #1: câu "chưa đúng với mọi trường hợp, đừng chép". #6: **nút `Gợi ý bước đầu` là nút duy nhất**, không có nút "Xác nhận" → thu hẹp được thể hiện bằng việc *thiếu nút* | #1, #6 |
| **PAIR · Errors + Graceful Failure** (+ **G2** cho #1) | #1: nút `Báo tài liệu sai`, `Hỏi TA` và dòng độ chắc "Chắc về phép toán · chưa được giảng viên xác nhận" (G2). #6: nút `Hỏi TA` + dòng "TA trả lời từ 08:00 sáng mai" khi ngoài giờ | #1, #6 |

> Ở chặng 5, mỗi chỗ trên bảng phải có mặt trên prototype, chụp ảnh đánh số 1, 2, 3 và ghi nguyên tắc nào. Chỗ nào không dựng được thì bỏ nguyên tắc đó.

## 3.4 Phân loại lỗi · cách nói · cách sửa *(R3 dòng 4: 3đ)*

| Loại lỗi | Là gì | Cách nói | Cách sửa |
|---|---|---|---|
| **Hệ thống** | AI làm sai quy tắc nó phải theo | Nhận lỗi thẳng: "Mình vừa nói quá, đáng lẽ không được xác nhận…" | Sửa ở tầng thiết kế/tool |
| **Người dùng** | Người dùng nhập sai/hiểu nhầm | Không đổ lỗi; hỏi lại nhẹ nhàng | Hướng dẫn nhập lại, có nút chọn |
| **Ngữ cảnh** | Hệ thống chạy đúng thiết kế nhưng sai với tình huống | Không xin lỗi kiểu "mình nhầm"; nói rõ giới hạn của tình huống | Sửa **thiết kế**, không chỉ câu chữ |

| Kịch bản | Loại lỗi | Vì sao nói và sửa theo loại đó |
|---|---|---|
| **#1** | **Ngữ cảnh** | AI trích đúng mục đúng quy trình, nhưng tài liệu sai. Nên nói "chưa đúng với mọi trường hợp, đừng chép", không xin lỗi vì AI không nhầm. Sửa bằng kiểm chéo + cờ "Cần xem lại" (xem 3.5) |
| **#6** | **Hệ thống** (khi AI lỡ xác nhận) | Quy tắc "không xác nhận bài đang mở" là của hệ thống. Nếu AI lỡ nói "đúng rồi" thì phải nhận lỗi thẳng và rút lại. Sửa bằng chặn ở tầng tool (xem 3.5), không nhờ AI "cố gắng hơn" |
| *(đối chiếu)* #4 | **Người dùng** | "Cái độ lệch ấy" thiếu rõ ràng; AI không đoán mà hỏi lại bằng hai nút chọn, không trách học viên |

## 3.5 Lỗi sửa câu chữ không cứu được *(R3 dòng 5: 3đ)*

**#1: AI trích mục đúng nhưng nội dung mục sai.** Sửa lời nói thì AI vẫn không biết mục sai nếu không có bước kiểm. Thiết kế cứu bằng:
1. Bước kiểm chéo: câu khẳng định tuyệt đối ("luôn", "không bao giờ") thì AI thử một ví dụ số trước khi trích.
2. Cờ "Cần xem lại" trên thẻ trích dẫn.
3. Chặn `dang_FAQ` cho nội dung đang bị cờ.

**#6: model có thể lỡ xác nhận dù prompt đã cấm.** Thiết kế cứu bằng:
1. Trạng thái bài (mở/hết hạn) lấy từ trang khoá học làm điều kiện cứng, không để model tự phán.
2. Chặn ở tầng tool: `goi_y_bai_tap` không trả đáp số cho bài đang mở.
3. Bước lọc trước khi gửi: nếu câu trả lời chứa số khớp đáp số bài mở thì thay bằng câu từ chối.

---

## Bàn giao cho đồng đội (§4, §5)
- **§4:** `tra_cuu_tai_lieu` gợi ý tự làm (chỉ đọc) · `goi_y_bai_tap` là tool khó xếp nhất (quá tay thì học viên đã chép, bắt duyệt thì học viên 22:00 chờ vô ích; gợi ý tách "gợi ý bước đầu" và "gợi ý chi tiết") · `chuyen_TA` tự làm, chỉ nói "đã chuyển" sau khi thành công · `dang_FAQ` cần duyệt, cấm với bài đang mở (#11). Đây là gợi ý, nhóm chốt.
- **§5:** dựng ca #1 hoặc #6 với: thẻ trích dẫn tô vàng, dòng độ chắc, nhãn "Bài 3 · đang mở", nút `Gợi ý bước đầu`, `Hỏi TA`, `Báo tài liệu sai`.
