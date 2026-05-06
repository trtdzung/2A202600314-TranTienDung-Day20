# 4. dependency_map.md

## External Dependencies & Plan B

**DEPENDENCY 1: OpenAI GPT-4o Vision API (Tier 1 - Critical)**
- **Worst-case:** OpenAI siết rate limit đột ngột hoặc tăng chi phí API 5x, phá vỡ Unit Economics.
- **Plan B:** Xây dựng Abstraction Layer cho LLM ngay từ đầu. Tích hợp sẵn Anthropic Claude 3.5 Sonnet làm mô hình dự phòng. Chỉ cần đổi biến môi trường để switch API trong vòng 2 giờ.
- **Cost:** 1 tuần dev setup multi-LLM architecture.

**DEPENDENCY 2: Nền tảng nhắn tin Zalo/Telegram (Tier 2 - Important)**
- **Worst-case:** Zalo thay đổi chính sách API Webhook, chặn bot trích xuất hình ảnh từ luồng chat riêng tư.
- **Plan B:** Chuyển dịch toàn bộ luồng thu thập sang Telegram Bot. Cung cấp kịch bản copy-paste để PT yêu cầu khách hàng chuyển kênh báo cáo.
- **Cost:** Tổn thất khoảng 15% lượng khách hàng end-user từ chối cài Telegram. 2 ngày setup Telegram Bot pipeline.

**DEPENDENCY 3: Quy định bảo vệ dữ liệu cá nhân (Tier 1 - Critical)**
- **Worst-case:** Bị thanh tra và đình chỉ do lưu trữ hình ảnh sinh hoạt cá nhân của người dùng cuối chưa có sự đồng ý (explicit consent) theo Nghị định 13/CP.
- **Plan B:** Triển khai luồng Onboarding bắt buộc học viên bấm "Đồng ý" trên màn hình Bot trước khi kích hoạt. Thiết lập cron job tự động xóa hình ảnh raw khỏi S3 sau 48h, chỉ lưu trữ text output.
- **Cost:** 3 ngày làm việc với đơn vị tư vấn luật (khoảng 10.000.000 VNĐ) + 1 ngày dev code cron job.

## Critical Path (Quý 1)

**Legal Compliance & Privacy Consent** → **Thiết lập Data Pipeline (Webhook Zalo/Telegram)** → **Tích hợp GPT-4o Vision API & Thuật toán đối chiếu** → **Xây dựng Alert Dashboard & Manual Override UI** → **Beta Launch.**

*Parallel / Buffer Tasks:* UI/UX Polish, Landing page marketing, Documentations.