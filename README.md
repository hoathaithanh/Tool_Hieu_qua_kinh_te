# Công Cụ Đánh Giá Hiệu Quả Kinh Tế (Economic Viability Tool)

[![Live Demo](https://img.shields.io/badge/Live-Demo-success.svg?style=for-the-badge)](https://hoathaithanh.github.io/Tool_Hieu_qua_kinh_te/)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Glossary/HTML5)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

Chào mừng bạn đến với **Công cụ Đánh giá Hiệu quả Kinh tế** dành cho các dự án tiết kiệm năng lượng và năng lượng tái tạo. Dự án này chuyển đổi mô hình tính toán tài chính truyền thống trên Excel thành một ứng dụng Web (One-page Application) tinh gọn, trực quan và tiện lợi.

## 🌟 Tính Năng Nổi Bật

- **Tính toán thời gian thực (Real-time):** Gõ số liệu tới đâu, các chỉ số tài chính và biểu đồ cập nhật ngay tới đó.
- **Độ chính xác chuẩn tài chính:** Tính toán đầy đủ Giá trị hiện tại ròng (NPV), Thời gian hoàn vốn tĩnh & hoàn vốn động dựa trên dòng tiền chiết khấu.
- **Đa tham số dòng tiền:** Hỗ trợ tính toán tỷ lệ lạm phát (trượt giá) và độ hao hụt thiết bị riêng biệt cho TỪNG hạng mục chi phí/lợi ích.
- **Biểu đồ trực quan:** Tự động vẽ biểu đồ dòng tiền tích lũy lũy kế có chiết khấu bằng thư viện `Chart.js`. Điểm hòa vốn được thể hiện qua sự thay đổi màu sắc (Đỏ = Lỗ, Xanh = Lãi).
- **Siêu nhẹ & Độc lập:** Không cần cài đặt phần mềm, framework hay cơ sở dữ liệu. Toàn bộ tính toán được xử lý ở phía trình duyệt (Client-side) trong một tệp `index.html` duy nhất.

---

## 🚀 Hướng Dẫn Sử Dụng Nhanh

Bạn có thể sử dụng công cụ bằng 2 cách:

1. **Sử dụng trực tiếp trên Web (Khuyên dùng):** 
   Truy cập vào link [Live Demo](https://hoathaithanh.github.io/Tool_Hieu_qua_kinh_te/).

2. **Chạy ở máy tính cá nhân (Offline):**
   - Clone kho lưu trữ này về máy: `git clone https://github.com/hoathaithanh/Tool_Hieu_qua_kinh_te.git`
   - Nhấp đúp chuột để mở tệp `index.html` bằng bất kỳ trình duyệt nào (Chrome, Edge, Safari...).

---

## 📘 Hướng Dẫn Nhập Liệu

### 1. Cài Đặt Tham Số Chung
- **Tiền tệ:** Gõ ký hiệu tiền tệ ở góc phải (VNĐ, USD, EUR...). Hệ thống sẽ tự động format toàn bộ giao diện theo đồng tiền đó.
- **Lãi suất (%):** Chi phí vốn hay lãi suất chiết khấu kỳ vọng của doanh nghiệp.
- **Tuổi thọ dự kiến (năm):** Vòng đời hoạt động của hệ thống (VD: Hệ thống điện mặt trời thường là 20-25 năm).

### 2. Chi Phí Đầu Tư Ban Đầu (Năm 0)
Đây là toàn bộ chi phí hình thành tài sản ban đầu (Thiết bị, nhân công lắp đặt, tư vấn,...).
- Bấm **"+ Thêm chi phí đầu tư"** để tạo nhiều hạng mục.
- Nhập số lượng và đơn giá, hệ thống sẽ tự tính tổng đầu tư (Dòng tiền xuất của năm 0).

### 3. Chi Phí Vận Hành Hàng Năm
Các chi phí duy trì hệ thống mỗi năm (bảo trì, điện năng tiêu thụ cho bơm nhiệt,...).
- **Trượt giá (%/năm):** Tỷ lệ lạm phát của chi phí (VD: Giá điện tăng 5%/năm).
- **Hao hụt (%/năm):** Để `0`.

### 4. Lợi Ích & Tiết Kiệm Hàng Năm
Các khoản thu hoặc chi phí tránh được (tiết kiệm than, điện, khí LPG,...).
- **Trượt giá (%/năm):** Tỷ lệ tăng giá trị của năng lượng tiết kiệm được.
- **Hao hụt (%/năm):** Mức suy giảm hiệu suất của thiết bị qua các năm. **Lưu ý: Phải nhập số âm** (VD: Pin mặt trời suy giảm 1% mỗi năm, hãy nhập `-1`).

---

## 📈 Đọc Báo Cáo Hiệu Quả

Sau khi nhập thông số, công cụ sẽ ngay lập tức trả về 3 chỉ số chính trên cùng:
* 🟢 **Màu Xanh:** Dự án khả thi, đã thu hồi được vốn trong tuổi thọ dự kiến.
* 🟠 **Màu Cam/Đỏ:** Dự án rủi ro, NPV âm hoặc chưa kịp thu hồi vốn.

- **Giá trị hiện tại ròng (NPV):** Mức lợi nhuận thực tế dự án mang lại sau khi đã tính tới giá trị thời gian của tiền tệ. `NPV > 0` nghĩa là dự án đáng để đầu tư.
- **Hoàn vốn tĩnh:** Tính bằng công thức `Tổng đầu tư / Lợi ích ròng hàng năm năm 0`.
- **Hoàn vốn động:** Thời gian thực tế để dòng tiền lũy kế (đã chiết khấu) vượt mốc số 0.

---

## 🤝 Giấy Phép & Đóng Góp
Mã nguồn mở và hoàn toàn miễn phí. Mọi ý kiến đóng góp, báo lỗi (Issue) hoặc yêu cầu Pull Request (PR) đều được hoan nghênh để làm cho công cụ ngày càng hoàn thiện hơn.
