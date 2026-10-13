# SỬA LỖI BÁO CÁO VELOCITY VÀ BURNDOWN CHART CỦA SPRINT 4 (RikkeiGo)

**Vai trò:** Lan (Scrum Master) rà soát báo cáo cuối Sprint của Tú
**Sprint 4:** 10 ngày | **Sprint Goal:** "Giúp khách thanh toán chuyến đi bằng ví RikkeiPay mà không cần tiền mặt."

**Dữ liệu cần đối chiếu:**
- Tổng SP ban đầu (ngày 0) = 8 + 5 + 5 + 3 + 2 = **23 SP**, khớp với Burndown ngày 0.
- PBI Done: Hủy chuyến (5) + Đánh giá tài xế (5) + Lưu địa chỉ yêu thích (3) + Đổi ảnh đại diện (2) = **15 SP**.
- PBI chưa Done: Thanh toán ví RikkeiPay (8 SP, chưa qua Integration Test) và Hiển thị mã khuyến mãi (3 SP, chưa làm) = **11 SP**.
- Ngày 3: Đức thêm PBI 3 SP vào Sprint nên Burndown tăng 21 → 24.

---

## Phần 1 – Phân tích

| Nhận định | Đúng / Sai | Căn cứ trong dữ liệu | Hậu quả nếu giữ nguyên |
|-----------|------------|----------------------|-------------------------|
| **BC1.** Velocity = 21 SP (15 SP Done + 6 SP cho PBI ví đã làm 75%) | **Sai** | Velocity chỉ tính SP của PBI đạt DoD, PBI chưa Done tính 0 SP. PBI ví RikkeiPay chưa qua Integration Test nên chưa Done, không được cộng 6 SP theo phần trăm. Velocity đúng là 15 SP. | Velocity bị thổi phồng 6 SP (40%). Sprint sau đội cam kết quá sức, dự báo tiến độ và quản lý bị sai lệch, ảo tưởng rằng Sprint Goal gần đạt. |
| **BC2.** Ngày 1 → 2 đường nằm ngang (21 → 21), tại Daily Scrum đội hỏi nhau có Task quá lớn hoặc làm dở quá nhiều việc cùng lúc | **Đúng** | Burndown đi ngang là tín hiệu cần tìm nguyên nhân, không phải kết luận về năng suất. Việc dùng Daily Scrum để kiểm tra Task quá lớn hoặc quá nhiều việc dở dang là cách xử lý phù hợp. **Giữ nguyên.** | Không có hậu quả xấu, đây là hành động đúng. |
| **BC3.** Ngày 3 đường tăng 21 → 24 chứng tỏ Developers làm việc chậm | **Sai** | Mức tăng 3 SP đúng bằng PBI "Hiển thị mã khuyến mãi trên hóa đơn" (3 SP) mà Đức thương lượng với Developers và thêm vào ngày 3. Đường tăng do phạm vi tăng, không phải do năng suất. | Kết luận oan cho Developers, che mất nguyên nhân thật là thay đổi phạm vi giữa Sprint (thêm PBI 3 SP mà không bỏ bớt việc), nên đội không rút kinh nghiệm đúng cách. |
| **BC4.** Ngày 10 sửa số còn lại từ 11 về 0 để Actual Line chạm Ideal Line | **Sai** | Actual Line phải phản ánh đúng công việc còn lại. Cuối Sprint còn 8 SP (ví RikkeiPay) + 3 SP (khuyến mãi) = 11 SP chưa Done, nên ngày 10 phải là 11, không phải 0. Ideal Line chỉ để tham chiếu. | Số liệu bị làm đẹp, quản lý tưởng Sprint hoàn thành toàn bộ và Sprint Goal đạt. Mất tính minh bạch, đội không phát hiện vấn đề để cải tiến ở Retrospective. |
| **BC5.** PBI ví chỉ thiếu Integration Test nên tự động chuyển sang Sprint 5 với 2 SP còn lại | **Sai** | PBI chưa Done thì quay lại Product Backlog để Product Owner xem xét thứ tự, không tự động chuyển sang Sprint sau. Không có căn cứ để cắt còn 2 SP: PBI chưa đạt DoD vẫn tính nguyên 8 SP, "gần xong" chưa phải Done. | Bỏ qua vai trò sắp xếp thứ tự ưu tiên của Product Owner, và con số 2 SP làm Sprint 5 đánh giá thấp khối lượng thực tế, gây overcommit. |

---

## Phần 2 – Vá lỗi

**Velocity Sprint 4 (tính lại):**

Velocity = 5 (Hủy chuyến) + 5 (Đánh giá tài xế) + 3 (Lưu địa chỉ yêu thích) + 2 (Đổi ảnh đại diện) = **15 SP**

PBI ví RikkeiPay (8 SP) và PBI khuyến mãi (3 SP) chưa Done nên tính 0 SP.

**Số SP còn lại đúng của ngày 10:**

8 (ví RikkeiPay) + 3 (khuyến mãi trên hóa đơn) = **11 SP** (không phải 0).

**Cách xử lý PBI ví RikkeiPay:**

PBI này chưa đạt DoD nên không được tính SP vào Velocity và không tự động chuyển sang Sprint 5, mà quay lại Product Backlog để Đức (Product Owner) xem xét thứ tự ưu tiên. Nếu được ưu tiên đưa vào Sprint 5, Developers ước lượng lại SP cho phần việc còn lại (kể cả Integration Test) bằng Planning Poker, không gán sẵn 2 SP.
