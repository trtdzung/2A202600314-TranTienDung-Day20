# FINAL SUBMISSION PACKAGE: AI PRODUCT STRATEGY & PITCH

## PART 1: PRODUCT STRATEGY & MARKET ANALYSIS (DAY 16 & 17)

### 1. Idea Reframed
**Original idea:** App B2C có chức năng tính lượng calo thông qua ảnh chụp bữa ăn bằng AI.
**Reframed as a product opportunity:** Công cụ tự động hóa quy trình theo dõi, đối chiếu và phân tích sai lệch dinh dưỡng hàng ngày dành cho Huấn luyện viên cá nhân (PT) phân khúc trung-cao cấp. Chuyển đổi mô hình từ B2C sang B2B SaaS tích hợp thẳng vào luồng tin nhắn Zalo/Telegram hiện tại để loại bỏ ma sát nhập liệu và tối ưu hóa thời gian vận hành.

### 2. Customer / Segment Card
*   **Segment name:** Huấn luyện viên cá nhân (PT) tại các chuỗi phòng tập trung-cao cấp.
*   **Operational context:** Quản lý đồng thời 10-25 khách hàng. 
*   **Recurring workflow:** Cấp sẵn thực đơn định mức -> Nhận ảnh chụp bữa ăn thực tế từ khách hàng qua Zalo/Telegram -> Đối chiếu ảnh với thực đơn gốc -> Nhận diện, tính toán lại lượng calo/macro chênh lệch đối với các món ăn bị thay đổi hoặc sai định lượng -> Phản hồi.
*   **Pain moment:** Khách hàng hiếm khi tuân thủ 100% thực đơn. Cuối ngày, PT phải soi từng ảnh, phát hiện các món ngoài luồng và tự ước lượng lại lượng calo chênh lệch cho hàng chục khách hàng. Quá trình đối chiếu thủ công gây kiệt sức, tạo sai số và kìm hãm khả năng nhận thêm khách.
*   **Why now:** Sự trưởng thành của LLM Vision (GPT-4o) đủ khả năng nhận diện hình ảnh món ăn phức tạp. Sự bão hòa của các app B2C đếm calo khiến tỷ lệ churn rate của học viên cực cao, buộc PT phải tìm giải pháp quản trị hệ thống tập trung.
*   **Access path:** Bán trực tiếp (Direct Sales) vào các tổ chức quản lý chuỗi phòng tập hoặc các cộng đồng nhóm kín của Head Coach/PT độc lập chuyên nghiệp.

### 3. Need Map
**Priority Need:**
*   **Statement (JTBD):** When khách hàng báo cáo bằng hình ảnh bữa ăn không tuân thủ chính xác thực đơn đã cấp, I want hệ thống tự động nhận diện món ăn thực tế và tính toán mức chênh lệch calo/macro so với plan gốc, so I can loại bỏ việc rà soát thủ công và nắm bắt chính xác mức độ tuân thủ.
*   **Current workaround:** Dùng mắt đối chiếu để "trừ hao", nhắn tin hỏi ngược lại khách hàng, hoặc chủ động bỏ qua các sai lệch nhỏ vì quá tốn thời gian.
*   **Pain signal:** PT mất 1-2 giờ rà soát tin nhắn mỗi đêm. Khách hàng chững cân do sai lệch calo tích tụ (calorie creep) nhưng không được can thiệp kịp thời.
*   **Why underserved:** Các giải pháp hiện tại là app B2C bắt người dùng cuối tự nhập liệu. Thiếu một Dashboard B2B đóng vai trò CRM dinh dưỡng chuyên biệt cho quy trình của PT.

### 4. Strategy Statement
**For** Huấn luyện viên cá nhân và chuyên gia dinh dưỡng
**who struggle with** việc đối chiếu thủ công và tính toán lượng calo chênh lệch từ những bữa ăn sai kế hoạch của khách hàng,
**our product helps them** tự động hóa việc kiểm soát mức độ tuân thủ và cập nhật chỉ số dinh dưỡng thực tế
**through** hệ thống AI phân tích hình ảnh bữa ăn và tự động so khớp với thực đơn gốc thông qua bot Zalo/Telegram,
**unlike** các ứng dụng đếm calo B2C yêu cầu người dùng cuối tải app và tự nhập liệu,
**because we can leverage** quy trình báo cáo hình ảnh đã có sẵn, thói quen giao tiếp vô thức của khách hàng và năng lực phân tích của LLM Vision.

### 5. Moat Hypothesis
**Moat mechanism:** Workflow embedding và Data compounding.
If we deploy 50 times in các luồng quản lý của PT, the following improve:
1. Hệ thống học được các pattern sai lệch phổ biến của khách hàng địa phương (đổi món, sai định lượng khẩu phần), cải thiện độ chính xác nội bộ vượt trội so với API đại trà.
2. Sản phẩm trở thành "hệ thống kiểm toán tuân thủ". Khi PT đã chuyển toàn bộ dữ liệu thực đơn, lịch sử khách hàng vào hệ thống, chi phí chuyển đổi (switching cost) trở nên quá cao để rời bỏ.

### 6. Ranh giới MVP
*   **In-Scope:** Giao diện Web Dashboard cho PT nhập thực đơn định mức. Bot webhook tích hợp Zalo/Telegram nhận ảnh tự động. Kết nối API GPT-4o trích xuất tên món/định lượng. Thuật toán so khớp tính calo chênh lệch. Gắn cờ (flag) các bữa ăn vi phạm trên Dashboard.
*   **Out-of-Scope:** Tính toán vi lượng chi tiết. Tự động nhắn tin nhắc nhở khách hàng thay PT. AI tự lập thực đơn mới. App Mobile native.
*   **Non-Goals:** Ứng dụng B2C. Tự train LLM Vision từ đầu. Độ chính xác dinh dưỡng 100% chuẩn phòng thí nghiệm (chỉ cần đo lường xu hướng sai lệch).

### 7. PRD Skeleton & PMF Scorecard
*   **Problem:** PT lãng phí hàng giờ mỗi đêm để đối chiếu thủ công ảnh bữa ăn thực tế với thực đơn chuẩn nhằm tìm ra mức chênh lệch calo.
*   **User Story 1:** As a PT, I want hệ thống tự động gắn cờ các bữa ăn sai lệch định mức, so that tôi chỉ rà soát những khách vi phạm.
*   **Fallback UX:** Confidence score < 75% -> Gắn thẻ "Cần Xác Nhận" (viền vàng) -> Yêu cầu PT Manual Override (nhập tay số calo).
*   **Riskiest Assumption:** Biên độ sai số của AI Vision đối với món ăn Việt phức tạp đủ thấp để PT tin tưởng, chi phí thời gian Manual Override không lớn hơn việc nhẩm tính thủ công.
*   **Aha Moment:** Lần đầu tiên PT mở Dashboard cuối ngày và chỉ phải xử lý 3 báo cáo bôi đỏ, bỏ qua 17 báo cáo hợp lệ.
*   **PMF Signal:** >80% retention rate trong việc sử dụng Dashboard 4 ngày/tuần đến tuần thứ 3. Tỷ lệ chấp nhận kết quả AI (không Manual Override) >80%.

---

## PART 2: UNIT ECONOMICS & REVENUE MODEL (DAY 18)

### 1. Revenue Model
*   **Mô hình cốt lõi:** Tiered Subscription Pricing B2B.
*   Thu phí cố định hàng tháng dựa trên Active Seats (Số lượng khách hàng PT đang quản lý).
*   Tích hợp hệ thống tín chỉ (Credit System) cho giới hạn API Call để bảo vệ biên lợi nhuận trước các trường hợp lạm dụng spam ảnh.

### 2. Unit Economics (Base Scenario)
*   **TAM:** 100,000 PT/Coach tại Việt Nam.
*   **ARPU:** 400,000 VND/tháng (Tương đương gói Pro $15-$20/tháng, quản lý 10-25 học viên).
*   **Adoption Rate:** 0.25% TAM/tháng.
*   **API Cost (COGS):** 150,000 VND/khách/tháng.
*   **CAC:** 1,000,000 VND. Duy trì mức thấp nhờ chiến lược bán sỉ trực tiếp (B2B) qua mạng lưới chuỗi phòng tập và cộng đồng Head Coach, triệt tiêu chi phí quảng cáo B2C.

---

## PART 3: INVESTOR PITCH & STAKEHOLDER MAP (DAY 19)

### 1. Stakeholder Map
*   **Lead VC lý tưởng:** Ascend Vietnam Ventures (AVV) / Do Ventures (Khẩu vị B2B SaaS, HealthTech/Fitness chuyển đổi số).
*   **Foundation Model Dependency:** GPT-4o Vision API. Plan B: Claude 3.5 Sonnet. Fallback UX bắt buộc để ngăn chặn rủi ro hallucination.
*   **Early Adopter Community:** Group kín Head Coach tại các chuỗi Elite Fitness/California Fitness, cộng đồng PT độc lập có tệp khách online.

### 2. User Hook (Archetype: The Overloaded)
"Hải (PT Elite) tiết kiệm 1 giờ mỗi đêm: AI quét ảnh Zalo, tự tính chênh lệch calo, báo thẳng 3 học viên vi phạm."

### 3. Pitch Memo (The 1-Pager)
**1. THE PROBLEM**
PT tại các chuỗi trung-cao cấp lãng phí 45-60 phút mỗi đêm rà soát tin nhắn Zalo/Telegram. Họ phải đối chiếu thủ công hình ảnh bữa ăn thực tế của hàng chục học viên với thực đơn định mức để tính toán lượng calo sai lệch, gây kiệt sức và kìm hãm khả năng mở rộng tệp khách hàng.

**2. THE INSIGHT**
Khách hàng B2C không có kỷ luật nhập liệu calo và sẽ luôn nói dối. Luồng báo cáo hình ảnh tự nhiên qua chat là điểm chạm duy nhất giữ được tỷ lệ tuân thủ, và nó cần được số hóa từ phía người quản lý (PT), không phải từ phía người dùng.

**3. THE SOLUTION**
B2B SaaS Dashboard tích hợp bot Zalo/Telegram. AI Vision tự động thu thập ảnh, đối chiếu với thực đơn gốc, đo lường chênh lệch calo và highlight học viên vi phạm. Giữ nguyên thói quen nhắn tin của người dùng cuối, triệt tiêu hoàn toàn ma sát nhập liệu.

**4. WHY NOW**
Năng lực Zero-shot của các mô hình LLM Vision hiện tại đủ sức phân rã kết cấu hình ảnh món ăn phức tạp mà không cần chi phí huấn luyện Data Labeling khổng lồ như trước năm 2023.

**5. TRACTION / PROOF**
TAM nội địa 100,000 PT. ARPU mục tiêu $15-$20/tháng (Biên lợi nhuận gộp 60%). CAC mục tiêu < $40 thông qua kênh phân phối B2B.

**6. THE ASK**
Gọi 100,000 USD Pre-Seed. 40% cho R&D hoàn thiện cơ chế đối chiếu LLM Vision, 60% cho Direct Sales B2B nhằm khóa 500 khách hàng trả phí đầu tiên trong 12 tháng tới.

### 4. The Twitter Pitch (258 ký tự)
PT kiệt sức vì soi hàng trăm ảnh bữa ăn Zalo mỗi đêm? Sản phẩm B2B SaaS của chúng tôi dùng AI tự quét ảnh, đối chiếu thực đơn gốc và báo thẳng mức chênh lệch calo. Cắt giảm 1 giờ rà soát, giúp PT tăng gấp đôi khách hàng. Đã khóa quy trình, sẵn sàng scale.

### 5. VC Critique & Defense (AI Feedback Log)
*   **Threat:** AI Vision không thể đo lường calo tuyệt đối chính xác 100%. (Ảo tưởng độ chính xác).
    *   *Defense (Accepted & Adjusted):* Tái định vị sản phẩm. Đây không phải công cụ phòng thí nghiệm. Đây là "công cụ phát hiện sai lệch xu hướng". Cơ chế Fallback UX buộc PT can thiệp khi AI có confidence < 75% giải quyết triệt để rủi ro sai số.
*   **Threat:** Rào cản công nghệ mỏng. OpenAI có thể ra mắt tính năng tương tự.
    *   *Defense (Accepted & Adjusted):* Lợi thế bảo vệ cốt lõi là Workflow Embedding. Sản phẩm khóa chặt luồng giao tiếp riêng tư trên Zalo/Telegram và lưu trữ lịch sử cấu trúc thực đơn. OpenAI cung cấp trí tuệ thô, chúng tôi cung cấp hệ thống quản trị chuyên ngành.