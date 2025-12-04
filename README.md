<div align="center">

# ☸️ **ĐẠI NAM VẠN BẢO** ☸️  

</div>

## 🏯☸️ Nền Tảng Tư Vấn Phong Thủy & Pháp Phẩm Kim Cang Thừa ☸️🏯  
> Website tư vấn phong thủy – kiến trúc An Trạch kết hợp thương mại pháp phẩm Kim Cang Thừa  
> Xây dựng trên WordPress + Plugin PHP/JS + WooCommerce  
> Tích hợp 8 trường phái phong thủy chuyên sâu

[![WordPress](https://img.shields.io/badge/CMS-WordPress-21759B?logo=wordpress)]()
[![PHP](https://img.shields.io/badge/Backend-PHP-777BB4?logo=php)]()
[![JavaScript](https://img.shields.io/badge/Frontend-JavaScript-F7DF1E?logo=javascript)]()
[![WooCommerce](https://img.shields.io/badge/Ecommerce-WooCommerce-96588A?logo=woocommerce)]()
[![MySQL](https://img.shields.io/badge/Database-MySQL-4479A1?logo=mysql)]()

---

## 📞 THÔNG TIN LIÊN HỆ

**Sinh viên thực hiện:**  
- **Họ tên:** Trần Trung Phúc  
- **MSSV:** 110122142  
- **Lớp:** DA22TTB  

**Giảng viên hướng dẫn:**  
- **ThS. Nguyễn Hoàng Duy Thiện**

**Trường:** Đại học Trà Vinh  
**Khoa:** Công nghệ thông tin  
**Thời gian thực hiện:** 03/11/2025 – 28/12/2025  

---

# 📚 MỤC LỤC

1. [Giới thiệu tổng quan](#-giới-thiệu-tổng-quan)  
2. [Phạm vi & Mục tiêu hệ thống](#-phạm-vi--mục-tiêu-hệ-thống)  
3. [Tổng quan chức năng](#-tổng-quan-chức-năng)  
4. [Chi tiết từng chức năng phong thủy](#-chi-tiết-từng-chức-năng-phong-thủy)  
5. [Kiến trúc hệ thống](#-kiến-trúc-hệ-thống)  
6. [Công nghệ sử dụng](#-công-nghệ-sử-dụng)  
7. [Cấu trúc thư mục](#-cấu-trúc-thư-mục)  
8. [Plugin tự phát triển](#-plugin-tự-phát-triển)  
9. [Tính toán phong thủy – Giải thích thuật toán](#-tính-toán-phong-thủy--giải-thích-thuật-toán)  
10. [Cơ sở dữ liệu sử dụng](#-cơ-sở-dữ-liệu-sử-dụng)  
11. [Hướng dẫn cài đặt](#-hướng-dẫn-cài-đặt)  
12. [Hướng dẫn sử dụng](#-hướng-dẫn-sử-dụng)  
13. [Bảo mật hệ thống](#-bảo-mật-hệ-thống)  
14. [Kiểm thử hệ thống](#-kiểm-thử-hệ-thống)  
15. [Tối ưu hiệu năng](#-tối-ưu-hiệu-năng)  
16. [Kết luận & hướng phát triển](#-kết-luận--hướng-phát-triển)

---

# 🎯 GIỚI THIỆU TỔNG QUAN

**AnTrạchHub** là nền tảng tư vấn phong thủy – kiến trúc được xây dựng theo mô hình “Website tích hợp đa chức năng”, với hai mục tiêu chính:

1. **Tự động hóa hệ thống tra cứu – tư vấn phong thủy cổ truyền**  
2. **Kết hợp thương mại điện tử để kinh doanh pháp phẩm Kim Cang Thừa**

Hệ thống được xây dựng dựa trên các trường phái phong thủy kinh điển như:

- Bát Trạch Minh Cảnh  
- Dương Trạch Tam Yếu  
- Huyền Không Phi Tinh  
- Thiên Can – Địa Chi  
- Ngũ Hành – Nạp Âm  
- Lỗ Ban – Dương Trạch & Âm Trạch  
- Loan Đầu – Hình Thế  
- Tứ Trụ Bát Tự (ứng dụng một phần)  

Mọi thuật toán phong thủy được triển khai bằng **PHP + JavaScript**, đóng gói dưới dạng **plugin WordPress** giúp dễ dàng mở rộng, bảo trì và tích hợp vào bất kỳ website nào.

---

# 🧭 PHẠM VI & MỤC TIÊU HỆ THỐNG

## 🎯 **Mục tiêu chính**

- Phát triển website phong thủy toàn diện, có khả năng:
  - Tính toán và phân tích phong thủy một cách tự động  
  - Hiển thị kết quả theo dạng luận giải chi tiết  
  - Hỗ trợ người dùng lựa chọn hướng nhà, hướng bàn thờ, tuổi xây dựng…  
  - Sử dụng thước Lỗ Ban online trực quan  
  - Xem lịch âm – dương theo Can Chi  
  - Dự toán chi phí xây dựng nhà  

- Tích hợp hệ thống bán hàng:
  - WooCommerce làm backend thương mại điện tử
  - Sản phẩm: pháp khí – pháp phẩm Kim Cang Thừa
  - Gợi ý sản phẩm phù hợp theo mệnh/hướng/tuổi  

## 🎯 **Phạm vi đề tài**

Hệ thống gồm hai nhóm chính:

### **1. Nhóm chức năng phong thủy**
Gồm:

- Xem tuổi xây dựng  
- Xem hướng nhà tốt  
- Xem hướng nhà hợp tuổi  
- Xem hướng đặt bàn thờ theo tuổi  
- Tra cứu thước Lỗ Ban  
- Dự toán xây nhà  
- Xem lịch âm dương (Can Chi – giờ hoàng đạo – hắc đạo)  

### **2. Nhóm chức năng thương mại điện tử**
- Danh mục pháp phẩm  
- Giỏ hàng – thanh toán  
- Gợi ý sản phẩm hợp mệnh  
- Quản lý đơn hàng, kho hàng  

---

# 🔥 TỔNG QUAN CHỨC NĂNG

Dưới đây là danh sách đầy đủ **tất cả chức năng chính thức** của Website AnTrạchHub (phiên bản hoàn chỉnh):

| Nhóm chức năng | Tên chức năng | Mô tả |
|----------------|---------------|-------|
| **Phong thủy** | Xem tuổi xây dựng | Dựa trên năm sinh gia chủ và năm xây dựng → Luận Kim Lâu, Hoang Ốc, Tam Tai |
| | Xem hướng nhà tốt | Liệt kê toàn bộ 8 hướng theo Bát Trạch → luận tốt/xấu |
| | Xem hướng nhà hợp tuổi | Dựa vào năm sinh + giới tính → tính cung phi → so sánh hướng nhà |
| | Xem hướng đặt bàn thờ | Dựa trên hướng nhà + cung phi → luận hướng phù hợp |
| | Tra cứu thước Lỗ Ban | Hỗ trợ kéo thước + nhập số đo → tra cung tốt/xấu |
| | Dự toán xây nhà | Tính chi phí dự kiến theo diện tích + vật liệu |
| | Xem lịch âm dương | Ngày âm/dương + Can Chi + giờ hoàng đạo/hắc đạo |
| **Ecommerce** | Danh mục pháp phẩm | Xem sản phẩm Kim Cang Thừa |
| | Gợi ý pháp khí | Dựa vào mệnh/ngày sinh/hướng nhà |
| | Giỏ hàng | WooCommerce |
| | Thanh toán | WooCommerce checkout |

---

# 🔮 CHI TIẾT TỪNG CHỨC NĂNG PHONG THỦY

Dưới đây là mô tả chuyên sâu của từng chức năng, bao gồm input – output – logic – giao diện.

---

# 1️⃣ XEM TUỔI XÂY DỰNG

### 🔍 Mô tả
Chức năng phân tích năm đẹp để xây nhà dựa trên:

- **Năm sinh gia chủ**
- **Giới tính**
- **Năm dự định xây dựng**

Dựa vào 4 yếu tố:

| Yếu tố | Giải thích |
|--------|------------|
| **Tam Tai** | 3 năm hạn theo tuổi |
| **Hoang Ốc** | Cung tốt/xấu liên quan đến sự thịnh suy của nhà |
| **Kim Lâu** | 4 loại tai ương nếu phạm |
| **Trạch Tuổi** | 12 trạch tốt xấu theo năm |

### 🔢 Input

{
"nam_sinh": 1998,
"nam_xay": 2026,
"gioi_tinh": "Nam"
}

markdown
Sao chép mã

### 📤 Output

- Tam tai: phạm / không phạm  
- Kim lâu: phạm / không phạm  
- Hoang Ốc: loại cung + xấu/tốt  
- Trạch Tuổi: luận giải  
- Kết luận chung: năm đó xây được hay không  
- Gợi ý năm đẹp khác  

---

# 2️⃣ XEM HƯỚNG NHÀ TỐT (KHÔNG CẦN NHẬP HƯỚNG)

### 🔍 Mô tả
Tính toán 8 hướng Bát Trạch theo cung mệnh của gia chủ.

### 8 hướng được giải thích đầy đủ:

- Sinh Khí  
- Thiên Y  
- Diên Niên  
- Phục Vị  
- Tuyệt Mệnh  
- Ngũ Quỷ  
- Lục Sát  
- Họa Hại  

Không cần nhập hướng nhà vì hệ thống:

- Tự động đề xuất hướng tốt nhất cho gia chủ  
- Xuất chi tiết từng hướng và ảnh hưởng trong đời sống  

---

# 3️⃣ XEM HƯỚNG NHÀ HỢP TUỔI (Có hướng cụ thể)

### 🔍 Mô tả
Chức năng này **có nhập hướng nhà** để hệ thống:

- Xác định cung phi gia chủ  
- So sánh hướng nhà  
- Luận giải tốt/xấu  
- Gợi ý cải thiện nhà phạm hướng xấu  

### Input

nam_sinh + giới tính + hướng nhà

yaml
Sao chép mã

### Output

- Tên cung (ví dụ: Khảm – Thủy)  
- Nhóm mệnh: Đông Tứ / Tây Tứ  
- Hướng nhà đối chiếu  
- Kết luận: hợp – không hợp  
- Cách hóa giải  

---

# 4️⃣ XEM HƯỚNG ĐẶT BÀN THỜ

### 🔍 Mô tả
Một chức năng rất quan trọng trong phong thủy.

Dựa trên:

- Cung phi gia chủ  
- Hướng nhà  

Hệ thống tự luận ra:

- 4 hướng tốt  
- 4 hướng xấu  
- Hướng đặt bàn thờ tối ưu nhất  
- Hướng kỵ tuyệt đối  
- Vị trí nên tránh trong mặt bằng nhà  

---

# 5️⃣ TRA CỨU THƯỚC LỖ BAN ONLINE

### 🔍 Mô tả

Hỗ trợ 3 loại thước:

| Loại thước | Công dụng |
|------------|-----------|
| 52.2 cm | Dương trạch (nhà cửa) |
| 42.9 cm | Âm phần (mồ mả) |
| 38.8 cm | Nội thất |

### Tính năng nâng cao

- Người dùng **kéo thước bằng chuột hoặc chạm**  
- Nhập giá trị số đo → hệ thống tự xét cung  
- Mỗi cung hiển thị màu:  
  - Xanh: tốt  
  - Vàng: trung tính  
  - Đỏ: xấu  
 
---

# 6️⃣ XEM LỊCH ÂM DƯƠNG (Can Chi – Giờ Hoàng Đạo)

### Tính năng:

- Hiển thị song song lịch âm và dương  
- Ngày âm theo Can Chi:  
  - Ví dụ: “Ngày Kỷ Mùi, Tháng Giáp Thân, Năm Ất Tỵ”  
- Giờ hoàng đạo:  
  - Tý – Sửu – Dần – Mão – Thìn…  
- Giờ hắc đạo  
- Chọn tháng/năm tùy ý  
- Xem trực tiếp Can Chi của ngày  
- Tự động tính Trực ngày  

---

