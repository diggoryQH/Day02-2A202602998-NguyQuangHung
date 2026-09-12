# 03 — Individual Reflection

> Viết bằng lời của bạn (Phase 7 trong `01-worksheet.md`). Có thể dùng AI gợi ý câu hỏi tự soi, không dùng AI viết thay. 8-12 câu, có chuyện cụ thể.

## Thông tin cá nhân

- Họ và tên: Ngụy Quang Hùng
- Mã học viên: 2A202602998
- Nhóm: Nhóm C1
- Candidate problem nhóm chọn: Tìm kiếm lại video TikTok đã tim để gửi cho bạn bè.

---

## 1. Tôi đã tham gia vào phần nào?

Ghi việc cụ thể + kết quả cụ thể. Không ghi chung chung kiểu "tham gia thảo luận".

| Hoạt động | Tôi đã làm gì? (việc cụ thể) | Kết quả / ảnh hưởng tới nhóm |
|---|---|---|
| Scan cá nhân | Tự suy nghĩ và liệt kê ra 8 problem, trong đó mình đào sâu vào những bực bội hằng ngày khi học và code. | Đem đến cho nhóm 3 candidate khá thực tế (xoay quanh debug, tìm docs, và quản lý deadline), góp vào tổng số 15 ý tưởng để nhóm chọn lọc. |
| Pitch Problem Card | Thuyết trình và bảo vệ bài "Lọc thông báo deadline, lịch họp vào Notion". | Bài của mình được mọi người vote vào top 3 shortlist do đánh trúng cái khó chịu mà sinh viên nào cũng bị, và metric đo lường rất dễ. |
| Challenge bài của bạn khác | Lúc Dũng trình bày bài tìm video TikTok, mình có đặt câu hỏi xoáy sâu vào kỹ thuật: "TikTok nó đóng API thì lấy data bằng cách nào?". | Câu hỏi này làm nhóm chững lại một chút, nhưng nhờ vậy mà mọi người nhận ra rủi ro kỹ thuật từ sớm và chuyển sang hướng an toàn hơn là dùng tính năng Data Export. |
| Gom trùng / cluster | Hỗ trợ nhóm trưởng sắp xếp lại 15 ý tưởng lộn xộn ban đầu thành 4 nhóm cụ thể: Dev, Teamwork, Học tập, Tiêu dùng. | Mọi thứ rõ ràng hơn hẳn, nhóm đỡ bị rối khi phải review lại toàn bộ và rút ngắn thời gian chọn lọc ý tưởng. |
| Chọn candidate problem | Sau khi cân nhắc, mình vote 5 sao cho bài TikTok của Dũng và 4 sao cho bài Deadline của mình. | Bài TikTok thực sự quá hấp dẫn, phần vote của mình góp phần giúp bài này chiến thắng luôn vì sau khi điều chỉnh lại ranh giới, nó hoàn toàn khả thi. |
| Validation / research | Nhận nhiệm vụ đi tìm hiểu thực tế: vọc thử tính năng Collections, TikTok Search, Data Download và đọc tài liệu của Twelve Labs API. | Cứu nhóm một bàn thua vì ban đầu tính làm Agent đi cào dữ liệu. Nhờ research, mình chỉ ra pattern an toàn nhất là kết hợp "Data Export + Text Embedding và Whisper". |
| Workflow nhóm | Ngồi vẽ và vạch ra chi tiết bước số 2 (Extract & Embed) và lên kịch bản cho bước Fallback (nếu AI làm sai thì xử lý sao). | Giúp sơ đồ workflow thực tế hơn hẳn, không bị mang hơi hướm "bỏ vào AI là xong" mà thấy rõ từng luồng xử lý kỹ thuật bên dưới. |
| Problem Statement | Nhận viết và chốt lại phần Boundary (Làm gì và Không làm gì). | Đặt ra giới hạn an toàn: hệ thống tuyệt đối không tải raw video (phòng rủi ro chi phí server) và không scraping để tránh bị block. |
| Rule / Workflow / Agent | Tranh luận với nhóm để chọn kiến trúc Workflow lai Rule, thay vì cố đấm ăn xôi dùng Agent. | Nhóm đồng tình và bảo vệ được quyết định cuối cùng: không cần dùng công nghệ đao to búa lớn, cứ áp dụng workflow là hiệu quả và dễ demo nhất. |
| Decision | Lên phương án thiết kế một bản Pilot nhỏ nhất, cốt lõi nhất. | Cung cấp một hướng dẫn thực hành thực sự làm được trong quy mô lab, chạy tay qua ChromaDB và Whisper để ra ngay kết quả. |

**Dấu tay rõ nhất của tôi trong artifact cuối (1-2 câu):**

```text
Dấu ấn đậm nét nhất của mình nằm ở phần "Research giải pháp đã có" và việc thiết lập ranh giới (boundary) kỹ thuật cho bài toán. Bằng dữ liệu research thực tế, mình đã "kéo" cả nhóm từ chỗ mơ mộng dùng Agent đi cào video trên app về phương án dùng Workflow an toàn với file JSON export của TikTok.
```

---

## 2. Bảng dùng AI (mỗi dòng 1 phase có dùng AI — 2 cột cuối bắt buộc)

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai / hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| Scan | Mở ChatGPT lên nhờ gợi ý xem sinh viên IT thường tốn thời gian vào những việc "vô tri" nào. | Nhờ gợi ý mà nhớ ra mấy cái lắt nhắt như nộp CV, lọc email nhắc việc, đi lục tìm tài liệu cũ. | AI đưa ra mấy ý như "Hệ thống tự động học bài hộ" nghe rất chung chung và viển vông. | Mình gạt bỏ hết mấy ý xa rời thực tế, chỉ viết lại những pain point bản thân đã trải qua và có thể đo lường thời gian lãng phí cụ thể. |
| Problem Card | Nhờ Claude đọc thử và phản biện draft Card (bài lỗi Debug) của mình. | Cảnh báo một ý khá hay là nếu dùng AI tự sửa code, nó có thể sinh ra code bịa (hallucination) làm hỏng cả project. | AI gợi ý luôn việc làm một con "Agent tự động đọc và sửa mã nguồn" - hơi quá sức so với thời gian làm lab. | Mình điều chỉnh lại giới hạn ở mức Workflow, và đưa thêm boundary bắt buộc phải có con người (dev) review lại đoạn code do AI sinh ra. |
| Workflow | Lúc làm báo cáo, quăng ý tưởng nhờ AI sinh ra cú pháp Mermaid để vẽ sơ đồ cho lẹ. | Viết cấu trúc Graph TD cực nhanh và đều, copy paste vào là ra sơ đồ ngay. | AI không có tư duy chia cụm cái nào là hệ thống hiện tại (Current), cái nào là tương lai (Future). | Mình phải tự sửa code Mermaid, đóng khung 2 cụm subgraph lại và bôi màu đỏ cho các nút đang bị thắt cổ chai để dễ nhìn. |
| Research | Dùng Perplexity (công cụ tìm kiếm) để dò xem thị trường đang có mô hình Video Understanding nào hiệu quả. | Tìm đúng cái nền tảng Twelve Labs chuyên mảng video, có luôn tài liệu tham khảo rất sát. | AI chỉ liệt kê tính năng mà không phân tích tiền bạc (cost) và độ trễ (latency) nếu lôi toàn bộ frame video ra phân tích. | Mình tự tính toán rủi ro và chốt phương án lai: chỉ tách âm thanh (Whisper) để giảm thiểu chi phí tính toán mà vẫn đủ thông tin text để search. |
| Problem Statement | Không dùng | X | X | Mình tự ngồi viết tay phần này bám sát template và những gì nhóm đã chốt, vì AI không nắm được bối cảnh nội bộ của nhóm. |
| Rule / Workflow / Agent | Không dùng | X | X | Cả nhóm gọi điện phân tích dựa vào các tiêu chí trong bài giảng để chốt Workflow. Phần này tranh luận logic nên AI không can thiệp. |
| Decision | Không dùng | X | X | Quyết định đi tiếp (Go) hoàn toàn dựa vào bằng chứng team đã research và các metric thực tế. |

> Nếu phase nào không dùng AI, ghi `Không dùng` và vì sao tự làm.

---

## 3. Reflection câu hỏi mở

Chọn 3-4 câu trong 6 câu dưới để viết thành đoạn 8-12 câu (không trả lời bullet 1 dòng):
- Tôi học được gì khi nghe top 3 problems của các bạn khác?
- Nhóm có lúc nào bị solution-first, đòi làm Agent cho ngầu không?
- Tôi có thay đổi ý kiến sau khi bị challenge không, vì sao đổi?
- Tôi đóng góp gì thật sự vào artifact cuối, phần nào có dấu tay của tôi?
- Điều khó nhất khi viết Problem Statement là gì, metric hay boundary?
- Nếu làm lại, tôi sẽ challenge nhóm mạnh hơn ở điểm nào?

**Reflection:**

```text
Qua đợt làm bài tập nhóm vừa rồi, mình nhận ra một bài học rất thấm về ranh giới giữa một vấn đề "mình thấy hay" và một vấn đề "ai cũng thấy đau". Lúc đầu, mình cứ đinh ninh cái bài lọc deadline của mình là ổn nhất vì quy trình rất rõ ràng và dễ đo lường thành công. Nhưng đến khi nghe Dũng pitch cái ý tưởng "Tìm lại video TikTok đã thả tim", mình và cả nhóm gần như "đứng hình" vài giây rồi gật gù vì đúng là ai hay lướt TikTok cũng bực mình chuyện này mà chả mấy ai nghĩ đến việc giải quyết bằng AI. Cái buồn cười nhất là lúc bắt đầu bàn giải pháp, cả nhóm hăng máu quá nên suýt nữa sập bẫy "solution-first". Mọi người cứ đòi làm hẳn một con Agent cho nó ngầu, cho nó tự động mở app TikTok trên điện thoại rồi lướt lấy dữ liệu. Vì ôm phần research, mình phải vội "kéo" cả đám xuống mặt đất ngay lập tức. Mình phản biện gắt ý tưởng đó, phân tích rõ là API của TikTok đóng chặt, mà xử lý ảnh/video liên tục bằng AI thì tiền server chịu sao nổi, tốc độ lại rùa bò thà tự tìm tay còn hơn. Nghe phân tích hợp lý, cả nhóm mới bẻ lái sang tận dụng Data Export của TikTok và kết hợp Semantic Search. Nhìn lại toàn bộ báo cáo, mình tâm đắc nhất là phần ranh giới (boundary) do mình chốt hạ, vì nó giữ cho cả team không bị "ảo tưởng AI", đảm bảo sản phẩm giải quyết đúng chuyện cần giải quyết với chi phí khả thi. Nếu có cơ hội làm lại, mình sẽ còn "soi" kỹ hơn về cấu trúc file JSON trả về của TikTok để dự phòng trường hợp format bị thay đổi đột ngột.
```

---

## 4. Tự kiểm cuối bài (check trước khi nộp repo)

- [x] [12đ] Cá nhân có 5+ problems + top 3 Problem Cards
- [x] [12đ] Tôi đã pitch rõ + challenge nhóm đúng trọng tâm (ghi ở bảng mục 1)
- [x] Nhóm có nhật ký hội tụ từ candidates về 1 bài
- [x] [15đ] Nhóm có workflow trước/sau
- [x] [20đ] Nhóm có PS v0/v1 với metric + boundary rõ
- [x] [15đ] Nhóm có so sánh No AI / Rule / Workflow / Agent
- [x] [10đ] Nhóm có Go / Not Yet / No-Go + lý do rõ
- [x] [10đ] Reflection này có vai trò thật + AI giúp/sai ở đâu + điều học được + nếu làm lại đổi gì
- [x] [6đ] Tôi tự giải thích được mạch problem → workflow → metric → boundary → độ phù hợp AI
