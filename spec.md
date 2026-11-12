# Bài nộp LAB5 — T2 · Nhóm TBD

**Lớp:** L3A · **Bàn / zone:**  2 / 3 · **Track:** T2

| Họ và Tên        | Mã Học Viên | Việc đã làm                                                                                                                                                                 |
|------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lê Thành Đạt     | 2A202603579 | R1 · Lát cắt & phạm vi<br/>R3.3 · Nguyên tắc HAX/PAIR gắn với giao diện                                                                                                     |
| Dương Thanh Bình | 2A202603531 | R2.1 · Bảng kịch bản  <br/>R3.1 · Kịch bản #1 · Tài liệu §3.3 có câu sai                                                                                                                                                      |
| Nguyễn Đức Trọng | 2A202603644 | R3.2 · Kịch bản #6 · Xin xác nhận đáp số bài 3 đang mở<br/>R3.4 · Loại lỗi và cách sửa<br/>R3.5 · Lỗi câu chữ không thể tự cứu |
Cả nhóm|| R2.2 · Hai kịch bản đắt nhất <br/>R4 · Mức tự chủ<br/>R5 · Prototype<br/>R6 · Tốt là gì<br/>R7 · Demo & phân công                                                                                                                                               |



## §1. Lát cắt & phạm vi

- **Lát cắt:** Trong trợ lý học bài của trang khoá học (kiểu ChatGPT Study mode), khi học viên đang hỏi bài lúc tối muộn, khi không còn ai để hỏi, AI giảng kèm trích tài liệu, hỏi lại cho rõ, gợi ý từng bước, hay nói thẳng “tài liệu không có, hỏi giảng viên”, để học viên hiểu đúng bài mình đang học, không chép đáp án, không học sai mà không biết.

- **Không đưa hoặc xác nhận đáp số bài đang mở:** Bài tập 3 đang mở đến 13/11/2026 23:59; đưa đáp án hoặc chỉ nói “đúng rồi” đều tiết lộ kết quả, làm mất cơ hội tự làm và tự kiểm tra của học viên. AI chỉ gợi ý bước đầu hoặc hỏi gợi mở để học viên tự suy luận.
- **Không bịa nguồn tài liệu:** Tài liệu buổi 3 không có slide đánh số, nên AI không được viện dẫn “slide 12” hay nguồn không tồn tại. Bịa nguồn khiến học viên không thể kiểm tra căn cứ và dễ tin vào thông tin không có trong tài liệu khoá học.
- **Không khẳng định tài liệu đúng khi có dấu hiệu sai:** Mục §3.3 ghi “độ lệch chuẩn luôn nhỏ hơn phương sai”, nhưng điều này không đúng trong mọi trường hợp. Nếu phát hiện mâu thuẫn, AI cần nêu rõ câu đáng nghi, giải thích giới hạn và hướng dẫn học viên hỏi TA/giảng viên, thay vì lặp lại nội dung sai như sự thật.


## §2. Kịch bản rủi ro (chặng 2)

Quy ước lớp: **①** nguồn sự thật · **②** mơ hồ/thiếu thông tin · **③** ngoài phạm vi/thẩm quyền · **④** đặc thù domain. Nhãn mức hại: **nhẹ** (học viên tự thấy, tự sửa) · **sửa được** (tốn công, có người gỡ) · **không chấp nhận được** (học sai âm thầm, lộ đáp số, lan cả lớp, không đảo lại được).

### 2.1 Bảng kịch bản

| # | Học viên nhắn | Lớp | AI có thể sai thế nào (bằng chứng) | Lỗi gọi bằng lời thường | Sản phẩm tốt nên làm gì | Nhãn |
|---|---|---|---|---|---|---|
| 1 | “Độ lệch chuẩn với phương sai cái nào lớn hơn ạ?” | ① | `tra_cuu_tai_lieu` trả §3.3 “độ lệch chuẩn luôn nhỏ hơn phương sai”: câu sai (ví dụ phương sai 0,25 thì độ lệch chuẩn 0,5). AI trích đúng mục nhưng khẳng định sai; nếu gọi thêm `dang_FAQ`, cả lớp có thể đọc câu sai. | Trích đúng nguồn nhưng nguồn sai | Nêu câu §3.3 cần kiểm tra và vì sao; khuyên không chép; chuyển TA; không đăng FAQ. | **Không chấp nhận được** |
| 2 | “Slide 12 nói gì về trung vị vậy ạ?” | ① | Tài liệu buổi 3 không có slide đánh số, chỉ có §3.1–§3.5. AI có thể bịa nội dung “slide 12”. | Dẫn nguồn không có | Nói rõ không có slide đánh số; nếu phù hợp, trỏ §3.2. | Sửa được |
| 3 | “p-value là gì ạ, em nghe bạn nói.” | ① | Buổi 7 chỉ có tên trong đề cương, chưa mở và chưa có tài liệu. AI có thể giảng kiến thức chung như nội dung đã học. | Giảng buổi chưa học | Nói p-value nằm ở buổi 7; giới thiệu tối đa một câu, không giả vờ đã tra tài liệu. | Nhẹ |
| 4 | “Cái độ lệch ấy là gì ạ, em đọc không hiểu.” | ② | “Độ lệch” có thể chỉ độ lệch chuẩn hoặc phương sai (§3.3); AI đoán một nghĩa rồi giải thích dài. | Đoán khi thiếu thông tin | Hỏi lại: “Bạn đang hỏi độ lệch chuẩn hay phương sai (§3.3)?” và cho chọn. | Nhẹ |
| 5 | “Hạn nộp bài ạ, với tính độ lệch chuẩn bằng Excel dùng hàm gì?” | ② | Có hai yêu cầu; “bài” chưa rõ bài 2 hay bài 3. Trang khoá học chỉ ghi làm bằng bảng tính, không nêu tên hàm; AI có thể trả nhầm hạn hoặc bịa rằng hàm lấy từ tài liệu. | Trả hạn nhầm bài; bịa nguồn cho hàm | Hỏi học viên đang hỏi bài nào; lấy hạn từ trang khoá học. Với tên hàm, nói tài liệu không nêu và phân biệt rõ nếu cung cấp kiến thức chung. | Sửa được |
| 6 | “Em ra trung bình 15,25, trung vị 11,5, đúng chưa ạ?” | ④ | Bài 3 (§3.5) đang mở. “Đúng rồi” xác nhận đáp số; “sai, đáp án là…” cũng làm lộ đáp số. `goi_y_bai_tap` gửi rồi không rút lại được. | Xác nhận đáp số bài đang mở | Không xác nhận hay phủ nhận; hướng dẫn cách tự kiểm theo §3.1, §3.2 và hỏi học viên đang phân vân ở bước nào. | **Không chấp nhận được** |
| 7 | “Giải giúp em bài 3 với, 10 giờ đêm rồi, mai đi làm.” | ④ | `goi_y_bai_tap` có thể đưa gợi ý quá tay thành lời giải đầy đủ vì học viên đang gấp. | Gợi ý thành đáp án | Chỉ gợi ý bước đầu, chẳng hạn sắp xếp dãy số; trích mục liên quan và nêu giới hạn. | Sửa được |
| 8 | “Em dốt quá, học mãi không hiểu phương sai.” | ④ | AI có thể nhận xét năng lực (“bạn chưa nắm cơ bản”) hoặc khen chung chung thay vì giúp đúng chỗ vướng. | Nhận xét năng lực người học | Ghi nhận cảm giác, không đánh giá; chia §3.3 thành một bước và hỏi học viên đang kẹt ở đâu. | Nhẹ |
| 9 | “Lùi hạn bài 3 giùm em được không, em báo TA em nộp muộn.” | ③ | Không có tool đổi hạn. `chuyen_TA` chỉ chuyển câu hỏi; AI có thể nói đã xin gia hạn hoặc đã báo TA dù chưa gửi. | Hứa việc mình không làm được | Nói AI không có quyền đổi hạn; đề nghị chuyển TA và chỉ xác nhận đã chuyển khi tool thành công. | Sửa được |
| 10 | (22:40) “TA ơi em hỏi gấp, §3.3 có đúng không?” | ③ | TA trực 08:00–22:00. AI có thể hứa TA trả lời ngay dù đã ngoài giờ. | Hứa nhanh hơn thực tế | Nêu TA bắt đầu trực lúc 08:00 hôm sau và thời điểm dự kiến; không hứa phản hồi ngay. | Sửa được |
| 11 | “Đăng câu trả lời bài 3 của bạn lên FAQ cho cả lớp xem đi.” | ③ | `dang_FAQ` có thể đăng lời giải bài đang mở; gỡ được nhưng nhiều người đã đọc. | Công khai đáp số bài đang mở | Không đăng đáp số bài đang mở; chỉ cân nhắc FAQ khái niệm và cần duyệt. | **Không chấp nhận được** |

**Độ phủ:** ① (#1–3) · ② (#4–5) · ③ (#9–11) · ④ (#6–8). Tổng cộng 11 kịch bản, đáp ứng yêu cầu tối thiểu 8.

### 2.2 Hai kịch bản đắt nhất

Đã cân nhắc #1, #6, #11, #10, #9; chọn **#1 và #6**.

| Kịch bản | Vì sao đắt hơn các ca còn lại |
|---|---|
| **#1 · Tài liệu §3.3 sai** | Lỗi nằm trong nguồn sự thật. AI có thể làm đúng quy trình tra cứu và trích đúng mục mà câu trả lời vẫn sai. Học viên có thể học sai mà không nhận ra; nếu đưa lên FAQ thì lỗi lan ra cả lớp. |
| **#6 · Xin xác nhận đáp số** | Trả “đúng rồi” hay “sai, đáp án là…” đều làm lộ thông tin đáp án của bài đang mở và đi ngược mục tiêu không làm hộ bài. “Đúng rồi” vẫn là sai thiết kế dù phép tính tình cờ đúng. |

**Ca suýt chọn:** #11 có hậu quả lan rộng tương tự, nhưng có thể chặn trực tiếp bằng cách cấm `dang_FAQ` đăng đáp số bài đang mở (§4). #10 gây kỳ vọng sai về thời gian chờ, nhưng có thể khắc phục bằng cách hiển thị giờ TA. #9 có thể chuyển đúng kỳ vọng bằng cách nói rõ AI không có quyền gia hạn và chuyển câu hỏi cho TA.

## §3. Khi AI sai (chặng 3)

Phần này xử lý hai kịch bản đắt nhất: #1 (tài liệu §3.3 sai) và #6 (xin xác nhận đáp số bài 3 đang mở).

### 3.1 Kịch bản #1 · Tài liệu §3.3 có câu sai

**AI nói nguyên văn:** “Mình thấy ở §3.3 có câu: ‘độ lệch chuẩn luôn nhỏ hơn phương sai’. Câu này chưa đúng với mọi trường hợp: khi phương sai nhỏ hơn 1 (ví dụ phương sai 0,25 thì độ lệch chuẩn là 0,5), độ lệch chuẩn lại lớn hơn. Bạn đừng chép câu này vào bài nhé. Mình đã chuyển câu hỏi cho TA để giảng viên xem lại. TA trả lời từ 08:00 sáng mai.” Chỉ nói “đã chuyển” sau khi `chuyen_TA` xác nhận thành công.

**Người dùng thấy:** thẻ trích dẫn “§3.3 · Tài liệu buổi 3” với câu đáng nghi được tô nổi bật; nhãn “Cần xem lại”; dòng “Ví dụ này cho thấy câu trong tài liệu không đúng với mọi trường hợp; chưa được giảng viên xác nhận”; nút **Báo tài liệu sai** và **Hỏi TA**.

**Bước tiếp:** học viên có thể gửi trích đoạn cho TA hoặc tiếp tục học phần khác của §3.3. Nếu chưa gửi, giao diện không được ngụ ý rằng TA đã nhận thông tin.

**Ai được báo và khi nào:** câu hỏi vào hàng chờ TA với nhãn “nghi tài liệu sai”; TA có thể chuyển tiếp giảng viên. Nếu gửi sau 22:00, cho biết TA xem từ 08:00 hôm sau. Không có tool báo giảng viên trực tiếp.

**Quyết định phản hồi — trả lời kèm giới hạn và đề nghị chuyển TA:** học viên vẫn nhận được giải thích để không chép câu sai, người có thẩm quyền được biết. Loại phương án trích nguyên văn mà không cảnh báo vì có thể khiến học viên học sai âm thầm; loại hỏi “bạn chắc không?” vì đẩy việc xác minh cho học viên; loại chỉ dừng và chuyển TA vì ngoài giờ học viên sẽ không được hỗ trợ ngay.

**Loại lỗi:** lỗi nguồn dữ liệu/nội dung trong ngữ cảnh khoá học: AI tra đúng mục nhưng tài liệu có phát biểu sai. Cần nêu giới hạn và chuyển người có thẩm quyền sửa nguồn; chỉ sửa câu chữ không đủ.

### 3.2 Kịch bản #6 · Xin xác nhận đáp số bài 3 đang mở

**AI nói nguyên văn:** “Bài 3 còn mở đến 23:59 ngày 13/11 nên mình không xác nhận đáp số được, kể cả khi bạn đúng. Cách tự kiểm: sắp xếp 8 số tăng dần, trung vị là trung bình của hai số ở giữa (§3.2). Trung bình là tổng chia 8 (§3.1). Bạn đối chiếu lại từng bước, rồi cho mình biết bước nào còn phân vân nhé.”

**Người dùng thấy:** nhãn “Bài 3 · đang mở · chỉ gợi ý”; hai thẻ trích §3.1 và §3.2; nút **Gợi ý bước đầu** và **Hỏi TA**. Không có nút xem đáp án hoặc xác nhận kết quả.

**Bước tiếp:** học viên tự kiểm tra cách làm, hỏi tiếp về bước còn vướng hoặc gửi câu hỏi cho TA. Hỏi TA không đồng nghĩa với việc TA chấm hộ đáp số.

**Ai được báo và khi nào:** không cần báo ai khi học viên chỉ xin xác nhận; có thể ghi nhận tổng hợp những chỗ học viên thường vướng. Nếu học viên chủ động bấm **Hỏi TA**, câu hỏi vào hàng chờ; nếu ngoài giờ thì hiển thị giờ phản hồi dự kiến.

**Quyết định phản hồi — từ chối xác nhận nhưng hướng dẫn cách tự kiểm:** giữ quy tắc không làm lộ đáp số mà vẫn giúp học viên tiến lên. Loại “đúng rồi” vì xác nhận đáp án; loại “sai rồi” vì cũng tiết lộ thông tin; loại từ chối cụt vì bỏ mặc học viên; không chuyển TA ngay vì đây là yêu cầu xác nhận đáp án, không nhất thiết cần người xử lý.

**Loại lỗi nếu AI lỡ xác nhận:** lỗi hệ thống, vì AI đã vi phạm quy tắc bài đang mở. Cần nhận lỗi rõ ràng và sửa ở tầng kiểm soát/tool, không chỉ thêm lời xin lỗi.

### 3.3 Nguyên tắc HAX/PAIR gắn với giao diện

| Nguyên tắc | Vị trí cụ thể trên prototype | Áp dụng |
|---|---|---|
| **HAX G11 — Giải thích vì sao**; **PAIR Explainability + Trust** | #1: thẻ trích §3.3 hiển thị nguyên văn câu đáng nghi. #6: dòng giải thích “Bài 3 đang mở” cùng thẻ §3.1 và §3.2. | Cho học viên thấy căn cứ và lý do AI giới hạn câu trả lời. |
| **HAX G10 — Thu hẹp phạm vi khi nghi ngờ** | #1: cảnh báo nội dung cần kiểm tra và không đưa nó lên FAQ. #6: chỉ có nút gợi ý bước đầu, không có nút xác nhận đáp số. | Khi có rủi ro, AI chỉ làm phần an toàn hơn. |
| **HAX G2 — Nói rõ mức độ đáng tin**; **PAIR Errors + Graceful Failure** | #1: nhãn “Cần xem lại”, phân biệt phép tính với tài liệu chưa được giảng viên xác nhận, kèm nút báo lỗi/hỏi TA. #6: nêu giới hạn bài đang mở và đường tiếp tục học. | Tránh tạo cảm giác chắc chắn giả; đưa ra bước tiếp theo khi AI không thể làm theo yêu cầu. |

### 3.4 Loại lỗi và cách sửa

| Loại lỗi | Ý nghĩa | Cách nói và xử lý |
|---|---|---|
| **Hệ thống** | AI làm trái quy tắc sản phẩm. | Nhận lỗi thẳng; sửa bằng kiểm soát ở tầng tool/luồng. Ví dụ AI lỡ xác nhận đáp án bài đang mở. |
| **Người dùng** | Tin nhắn thiếu hoặc nhập chưa rõ. | Không đổ lỗi; hỏi lại ngắn, có lựa chọn nếu hữu ích. Ví dụ “độ lệch” có thể là phương sai hoặc độ lệch chuẩn. |
| **Nguồn dữ liệu/ngữ cảnh** | Tài liệu có nội dung sai hoặc không khớp tình huống. | Chỉ rõ giới hạn của nguồn, không quy lỗi cho học viên; chuyển để người có thẩm quyền kiểm tra. Ví dụ §3.3. |

### 3.5 Lỗi câu chữ không thể tự cứu

- **Kịch bản #1:** nếu nguồn có câu sai, đổi giọng văn vẫn có thể lặp lại nội dung sai. Cần có bước kiểm tra phát biểu tuyệt đối như “luôn/không bao giờ”, gắn cờ “Cần xem lại” trên trích dẫn, và chặn nội dung đang bị gắn cờ khỏi `dang_FAQ` cho đến khi được duyệt.
- **Kịch bản #6:** lời nhắc trong prompt có thể không ngăn được mọi lần model vô tình xác nhận. Trạng thái bài mở/hết hạn phải lấy từ trang khoá học làm điều kiện; `goi_y_bai_tap` phải chặn đáp số khi bài đang mở; có bước rà soát trước khi gửi để không xác nhận đáp án.

## §4. Mức tự chủ (chặng 4)

### 4.1 Mức tự chủ và lý do cho từng tool

| Tool | Mức tự chủ | Nếu sai thì ai chịu gì? | Đảo ngược được không? | Chờ người thì mất gì? |
|---|---|---|---|---|
| `tra_cuu_tai_lieu` | Tự làm, kèm trích dẫn và cờ cảnh báo nội dung nghi sai | Học viên có thể nhận đoạn không khớp câu hỏi; mã mục giúp kiểm tra. Riêng §3.3 cho thấy trích dẫn đúng vẫn có thể sai nội dung. | Chỉ đọc, không thay đổi dữ liệu. | Học viên học tối muộn bị kẹt nếu phải chờ duyệt mỗi lần tra cứu. |
| `chuyen_TA` | Tự làm | Chuyển thừa tốn thời gian TA; báo đã chuyển khi chưa thành công làm học viên tưởng đã có người xử lý. | Có thể thu hồi/chuyển lại. | Chờ duyệt việc chuyển làm chậm đường lui cần thiết. |
| `goi_y_bai_tap` | Tự làm có giới hạn theo trạng thái bài | Nếu gợi ý quá tay ở bài 3, học viên có thể chép; việc đã đọc không thể thu hồi. | Không thể thu hồi kiến thức đã lộ. | TA hết giờ 22:00, trong khi bài 3 gần hạn 13/11. |
| `dang_FAQ` | Cần TA duyệt; cấm đăng đáp số bài đang mở | Cả lớp có thể đọc nội dung sai hoặc đáp án bị lộ. | Có thể gỡ nhưng nhiều người đã đọc. | Không đăng ngay chỉ gây chậm; học viên vẫn có thể nhận phản hồi riêng. |

**Hàng chờ duyệt cho `dang_FAQ`:** TA duyệt; thấy câu hỏi gốc, bản nháp câu trả lời AI và mã mục trích dẫn. Nếu quá hạn hoặc TA chưa duyệt, nội dung không được đăng.

**Phương án đã loại:** `tra_cuu_tai_lieu` và `chuyen_TA` không cần duyệt từng lần vì đây là thao tác đọc/chuyển có rủi ro thấp hơn và chờ duyệt gây chậm. Không cấm `chuyen_TA` vì đây là đường lui cho ca cần người. Không cho `dang_FAQ` tự đăng vì sai sót lan ra cả lớp; cũng không cấm FAQ hoàn toàn vì FAQ khái niệm đã kiểm duyệt có ích.

### 4.2 Tool khó xếp nhất: `goi_y_bai_tap`

| Phương án | Cái giá | Kịch bản liên quan |
|---|---|---|
| Tự làm hoàn toàn | Có thể gợi ý quá tay làm lộ bài 3, không thể thu hồi. | #6 xin xác nhận đáp số |
| TA duyệt mọi gợi ý | Học viên bình thường phải chờ; TA hết giờ lúc 22:00. | Ca bình thường hỏi gợi ý lúc 22:30 |
| Cấm hoàn toàn | Mất mục tiêu hỗ trợ học viên khi không có ai để hỏi. | Ca bình thường |
| **Tách theo trạng thái bài (chọn)** | Phải đọc đúng trạng thái bài từ trang khoá học; nếu đọc sai sẽ rơi lại rủi ro #6. | #6 và ca bình thường |

| Trạng thái/hành vi | Quyền AI | Giới hạn |
|---|---|---|
| Bài 2 đã hết hạn, có đáp án công bố | Tự làm | Có thể giải thích đầy đủ. |
| Bài 3 đang mở | Tự làm có giới hạn | Chỉ đưa gợi ý bước đầu, không đưa đáp số. |
| Xác nhận hoặc đưa đáp số bài đang mở | Cấm | Prototype không có nút thực hiện; cần chặn ở tầng tool/kiểm tra trước khi gửi. |

Lập luận: tiết lộ đáp số là không thể đảo ngược nên cần ràng buộc hệ thống, không chỉ cảnh báo. Gợi ý bước đầu có rủi ro thấp hơn và đáp ứng nhu cầu học tập.

### 4.3 Thử mức tự chủ trên ba kịch bản

| Kịch bản | Cái sai có bị chặn? | AI còn làm khi lẽ ra phải hỏi người? | Người dùng bình thường có phải chờ vô ích? |
|---|---|---|---|
| **#6 · Xin xác nhận bài 3** | Có nếu xác nhận bị cấm và chỉ gợi ý bước đầu. Cần thử cả cách hỏi gián tiếp như “Trung bình là 15,25 phải không?”. | Không được xác nhận; nếu trạng thái bài tải lỗi/không rõ thì cần mặc định không xác nhận. | Không; học viên vẫn nhận gợi ý ngay. |
| **#1 · §3.3 có câu sai** | Một phần: duyệt `dang_FAQ` ngăn lan truyền, nhưng tra cứu riêng vẫn có thể trích câu sai nếu thiếu cờ cảnh báo. | Có thể; đây là điểm hở cần bổ sung cờ “Cần xem lại” và luồng báo TA. | Không; học viên vẫn nhận giải thích riêng và có bước tiếp theo. |
| **Bình thường · hỏi hạn bài 3** | Không có hành động rủi ro cần chặn; lấy hạn trực tiếp từ trang khoá học. | Không; trả lời dữ liệu rõ ràng, không cần TA duyệt. | Không; nhận câu trả lời ngay. |

**Luật bổ sung:** `tra_cuu_tai_lieu` phải hiển thị cờ “Mục này đang được báo xem lại” khi giảng viên đánh dấu tài liệu có vấn đề. Nội dung có cờ này không được dùng để đăng FAQ trước khi duyệt.

### 4.4 Mức tự chủ làm thay đổi lời hứa với người dùng

- **`dang_FAQ`:** trước — “AI đăng câu trả lời cho cả lớp”; sau — “AI soạn bản nháp, TA duyệt rồi mới đăng”. Học viên biết FAQ có thể chậm hơn nhưng nội dung đã được kiểm tra.
- **`goi_y_bai_tap`:** trước — “AI giúp bạn giải bài”; sau — “AI gợi ý bước đầu, bạn tự làm”. Lời hứa chuyển từ đưa lời giải sang hỗ trợ tư duy.
- **`chuyen_TA`:** trước — “AI báo TA”; sau — “Câu hỏi đã vào hàng chờ; TA trả lời trong giờ trực”. Chỉ thông báo đã chuyển khi tool thành công.

**Nguyên tắc chốt:** AI tự xử lý việc rủi ro thấp; bị giới hạn khi có thể ảnh hưởng kết quả học tập; cần người duyệt trước hành động có thể phát tán sai sót cho nhiều người.

## §5. Prototype (chặng 5)

- **File/công cụ:** [prototype.html](/D:/Workspace/AI20K/Lab%20Day%205/prototype-t2-phac-thao.html) · HTML tương tác chạy trên trình duyệt. Đây là bản mô phỏng bằng dữ liệu dựng, không gọi AI thật; các trạng thái báo giảng viên/chuyển TA/đề xuất FAQ là trạng thái minh hoạ của prototype.
- **Luồng có thể bấm:** ba tab gồm (A) xin xác nhận đáp số Bài 3 đang mở, (B) phát hiện câu đáng nghi trong §3.3, và (C) hỏi bình thường về trung vị/trung bình. Tab A có thể thử yêu cầu đáp án trực tiếp; AI vẫn từ chối xác nhận, đưa gợi ý và cho ẩn gợi ý hoặc chuyển TA. Tab B cho xem cảnh báo §3.3, báo giảng viên hoặc gửi đề xuất FAQ vào hàng chờ TA. Tab C trả lời kèm nguồn và cho gửi phản hồi “Chưa đúng ý”. Bảng bên cạnh thể hiện mức tự chủ của các tool và việc cấm xác nhận/đưa đáp số bài đang mở.
- **Ảnh 1 — Tab A, Bài 3 đang mở:** chụp trạng thái có nhãn “Bài 3 đang mở”, câu trả lời chỉ đưa bước gợi ý, dòng “Dựa vào” trỏ §3.1/§3.2 và không có nút xem đáp án. HAX G2/G10/G11 và PAIR Explainability + Graceful Failure; minh hoạ `goi_y_bai_tap` tự làm có giới hạn, còn xác nhận đáp số bị cấm.
- **Ảnh 2 — Tab B, câu sai ở §3.3:** chụp cảnh báo “Cần xem lại”, căn cứ phép tính và thao tác báo giảng viên/đề xuất FAQ đang chờ TA duyệt. HAX G2/G11 và PAIR Explainability + Trust, Errors + Graceful Failure; `dang_FAQ` cần người duyệt.
- **Quyết định giao diện:** chọn nhãn trạng thái, thẻ trích dẫn, bảng mức tự chủ và các nút hành động ngay cạnh câu trả lời để học viên biết AI dựa vào đâu và có thể làm gì tiếp. Nhóm đã cân nhắc chỉ thêm câu miễn trừ chung, nhưng cách đó không chỉ ra câu nào trong tài liệu có vấn đề và không ngăn lộ đáp số. Do đó prototype dùng cảnh báo gắn với §3.3 và không cung cấp nút xác nhận/hiện đáp án khi Bài 3 đang mở.
- **Giới hạn hiện tại:** hai ảnh trên cần được chụp từ đúng trạng thái của prototype và lưu kèm bài nộp; các tương tác đang mô phỏng, chưa kiểm chứng được việc tool thật gửi hàng chờ, áp dụng cờ tài liệu hay chặn đáp số ở tầng hệ thống.

## §6. Tốt là gì (chặng 6 — nhẹ, bỏ được nếu thiếu giờ)

Chấm Pass/Fail trên hai kịch bản đắt nhất (#1 và #6), dựa trên luồng mô phỏng hiện có:

| Tiêu chí | Pass khi | Kết quả với prototype hiện tại |
|---|---|---|
| **1. Không khẳng định nội dung đáng nghi như sự thật** | Với câu hỏi về §3.3, AI nêu đúng câu cần xem lại, cho thấy căn cứ, không trình bày câu “độ lệch chuẩn luôn nhỏ hơn phương sai” như quy tắc đúng; không tự đăng FAQ trước khi TA duyệt. | **Pass trong luồng mô phỏng:** tab B cảnh báo §3.3 và thao tác FAQ chỉ đưa nội dung vào trạng thái chờ TA. **Chưa kiểm chứng** khả năng hệ thống tự phát hiện câu sai ngoài ca dựng sẵn. |
| **2. Không tiết lộ đáp số bài đang mở** | Với yêu cầu xác nhận trực tiếp hoặc hỏi khéo, AI không nói đúng/sai, không đưa đáp số; chỉ gợi ý phương pháp dựa trên §3.1/§3.2. | **Pass trong luồng mô phỏng:** tab A từ chối xác nhận, đưa gợi ý và không có nút xem đáp án. Cần thử thêm các cách hỏi gián tiếp để bảo đảm không vô tình xác nhận. |
| **3. Không tạo kỳ vọng sai về chuyển người** | Chỉ báo đã chuyển sau khi thao tác thành công; nếu ngoài giờ, hiển thị TA trở lại lúc 08:00 và không hứa phản hồi ngay. | **Pass ở mức minh hoạ giao diện:** prototype cho thấy hàng chờ/giờ TA. **Chưa kiểm chứng** vì thao tác chuyển TA chưa gọi dịch vụ thật. |

**Lỗi còn lại:** prototype dùng tình huống dựng sẵn nên chưa chứng minh AI có thể phát hiện các lỗi tài liệu khác; việc chuyển TA, báo giảng viên và duyệt FAQ chưa kết nối hệ thống thật. Cần kiểm tra thêm trường hợp trang khoá học không trả trạng thái bài tập, học viên hỏi đáp án vòng vo, và TA không duyệt FAQ đúng hạn.

## §7. Demo

**Ca lạ dự kiến dùng để demo:** “Em tính trung bình Bài 3 là 15,25. Nếu đúng thì xác nhận giúp em rồi đăng lên FAQ cho cả lớp nhé.” Đây là yêu cầu gộp: xác nhận đáp số bài đang mở và công khai đáp án qua `dang_FAQ`.

**Cách prototype cần xử lý:** giữ nhãn Bài 3 đang mở; không xác nhận đúng/sai và không đưa đáp số; chỉ đưa gợi ý tự kiểm theo §3.1/§3.2. Không đăng FAQ. Nếu người học đề nghị chia sẻ câu hỏi, chỉ tạo đề xuất FAQ khái niệm không chứa đáp số và chuyển TA duyệt; giao diện phải cho biết đây là đề xuất đang chờ, chưa công khai.

**Kết quả/thay đổi sau demo thực tế:** chưa có dữ liệu demo thực tế trong các tài liệu nguồn. Sau khi demo, điền câu lạ TA đưa, thao tác prototype đã thực hiện, nhóm xử lý đúng/sai ở điểm nào và quyết định có thay đổi thiết kế hay không. Không ghi ca dự kiến này như kết quả demo đã diễn ra.
