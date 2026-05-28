# Ngày 1 — Bài Tập & Phản Ánh (Nộp Bài)
## Phần 2 — Bài Tập Mở Rộng (1:00–1:30) — Đáp án

### Bài tập 2.1 — Độ Nhạy Của Temperature
Prompt: "Hãy kể cho tôi một sự thật thú vị về Việt Nam."

- Quan sát: Khi `temperature = 0.0` phản hồi rất quyết định và lặp lại (ít sáng tạo). `temperature = 0.5` cho kết quả cân bằng giữa chính xác và sáng tạo. `temperature = 1.0` bắt đầu có nhiều biến thể, câu chữ phong phú hơn. `temperature = 1.5` cho câu trả lời sáng tạo nhưng có nguy cơ lạc đề hoặc tạo thông tin không chính xác.
- Chọn cho chatbot hỗ trợ khách hàng: Tôi sẽ đặt `temperature` khoảng `0.0–0.3` để ưu tiên tính nhất quán và đúng sự thật — hỗ trợ khách hàng cần câu trả lời ổn định và có thể kiểm tra.

### Bài tập 2.2 — Đánh Đổi Chi Phí
- Giả sử mỗi lần gọi sinh ~350 token đầu ra.
  - Người dùng hoạt động/ngày = 10.000
  - Gọi/người/ngày = 3
  - Token mỗi lần = 350
  - Tổng token/ngày = 10.000 * 3 * 350 = 10.500.000 tokens
  - Tổng (1K token) = 10.500 (vì 10.500.000 / 1000)

- Chi phí ước tính/ngày:
  - GPT-4o: 10.500 * $0.010 = $105.00
  - GPT-4o-mini: 10.500 * $0.0006 = $6.30
  - GPT-4o đắt hơn GPT-4o-mini khoảng 105 / 6.3 ≈ 16.7 lần.

- Khi nào chi phí cao hơn xứng đáng:
  - Trường hợp cần đầu ra chất lượng cao, độ chính xác/độ phức tạp ngôn ngữ, hoặc khi hệ thống phục vụ tác vụ quan trọng (ví dụ: tóm tắt pháp lý, phân tích y tế, soạn thảo văn bản chính thức) — đầu tư vào GPT-4o là hợp lý.
- Khi nào chọn GPT-4o-mini:
  - Ứng dụng có khối lượng cuộc gọi lớn, yêu cầu nhanh và rẻ (FAQ, trả lời truy vấn đơn giản, gợi ý autocompletion), hoặc khi đưa model vào giai đoạn thử nghiệm/prototype.

### Bài tập 2.3 — Trải Nghiệm Người Dùng với Streaming
Streaming quan trọng nhất khi phản hồi dài hoặc khi cảm nhận độ trễ là yếu tố UX chính: ví dụ trò chuyện trực tiếp, viết nội dung dài, hay khi người dùng muốn thấy tiến độ (assistant "typing"). Streaming làm giảm độ trễ cảm nhận và cải thiện tương tác. Non-streaming phù hợp cho tác vụ ngắn, batch processing, hoặc khi cần đảm bảo đầu ra nguyên tử (toàn bộ phản hồi cần có mặt cùng lúc để xử lý tiếp).

---

**Danh sách nộp:**
- [x] Tất cả tests pass: pytest tests/ -v (đã kiểm thử cục bộ)
- [x] `solution/solution.py` — template đã triển khai
- [x] `solution/exercises.md` — phần 2 đã hoàn thiện
