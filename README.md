<div align="center">

#  **ĐẠI NAM VẠN BẢO**   

</div>

##  Nền Tảng Tư Vấn Phong Thủy & Pháp Phẩm Kim Cang Thừa  
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


# 🎯 GIỚI THIỆU TỔNG QUAN

**Đại Nam Vạn Bảo** là nền tảng tư vấn phong thủy – kiến trúc được xây dựng theo mô hình “Website tích hợp đa chức năng”, với hai mục tiêu chính:

| Nhóm chức năng | Tên chức năng | Mô tả |
|----------------|---------------|-------|
| **Phong thủy** | Xem tuổi xây dựng | Dựa trên năm sinh gia chủ và năm xây dựng → Luận Kim Lâu, Hoang Ốc, Tam Tai |
| | Xem hướng nhà tốt | Liệt kê toàn bộ 8 hướng theo Bát Trạch → luận tốt/xấu |
| | Xem hướng nhà hợp tuổi | Dựa vào năm sinh + giới tính → tính cung phi → so sánh hướng nhà |
| | Xem hướng đặt bàn thờ | Dựa trên hướng nhà + cung phi → luận hướng phù hợp |
| | Tra cứu thước Lỗ Ban | Hỗ trợ kéo thước + nhập số đo → tra cung tốt/xấu |
| | Xem lịch âm dương | Ngày âm/dương + Can Chi + giờ hoàng đạo/hắc đạo |
| **Ecommerce** | Danh mục pháp phẩm | Xem sản phẩm Kim Cang Thừa |
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

# 🏗️ KIẾN TRÚC HỆ THỐNG

Hệ thống được xây dựng theo mô hình Client-Server với WordPress làm nền tảng chính. Phía Client là trình duyệt web nơi người dùng tương tác. Phía Server bao gồm WordPress Core xử lý các yêu cầu, các plugin tự phát triển cho tính toán phong thủy, WooCommerce cho thương mại điện tử, và cơ sở dữ liệu MySQL lưu trữ dữ liệu.

Luồng xử lý: Người dùng gửi yêu cầu từ trình duyệt → WordPress tiếp nhận → plugin phong thủy hoặc WooCommerce xử lý nghiệp vụ → truy vấn cơ sở dữ liệu khi cần → trả kết quả về hiển thị trên trình duyệt.

# 🛠️ CÔNG NGHỆ SỬ DỤNG

- WordPress 6.4+: Nền tảng quản lý nội dung chính
- PHP 7.4+: Ngôn ngữ xử lý backend và phát triển plugin
- JavaScript (ES6+): Xử lý tương tác frontend
- MySQL 5.7+: Hệ quản trị cơ sở dữ liệu
- WooCommerce 8.0+: Hệ thống thương mại điện tử
- jQuery 3.6+: Hỗ trợ tương thích và hiệu ứng
- HTML5/CSS3: Xây dựng giao diện responsive
- XAMPP 8.2+: Môi trường phát triển cục bộ

# 🧩 PLUGIN TỰ PHÁT TRIỂN

Đã phát triển 6 plugin chuyên biệt cho các chức năng phong thủy:

- Plugin Xem tuổi xây dựng: Tính toán Kim Lâu, Hoang Ốc, Tam Tai
- Plugin Xem hướng nhà: Tính cung phi, đối chiếu Bát Trạch, luận hướng tốt/xấu
- Plugin Xem hướng đặt bàn thờ: Đề xuất hướng đặt bàn thờ tối ưu
- Plugin Tra cứu thước Lỗ Ban: Hỗ trợ kéo thước ảo, nhập số đo, luận giải cung
- Plugin Lịch âm dương: Hiển thị lịch Can Chi, giờ hoàng đạo
- Plugin Tư vấn màu sắc: Gợi ý màu nội thất theo Ngũ hành bản mệnh

Mỗi plugin có cấu trúc độc lập: file chính đăng ký plugin, thư mục includes chứa logic xử lý, thư mục assets chứa tài nguyên, thư mục templates chứa giao diện hiển thị.

# 🧮 TÍNH TOÁN PHONG THỦY - GIẢI THÍCH THUẬT TOÁN

Tính cung phi (Bát trạch): Dựa trên năm sinh âm lịch và giới tính. Tính tổng các chữ số năm sinh, rút gọn đến 1 chữ số, tra bảng quy đổi để ra cung mệnh.

Tính Kim Lâu: Tuổi âm lịch = Năm hiện tại - Năm sinh + 1. Chia tuổi cho 9, nếu dư 1, 3, 6, 8 thì phạm Kim Lâu.

Tính Hoang Ốc: Chia tuổi âm lịch cho 6, dựa vào số dư để xác định cung tốt/xấu (6 cung: Nhất Cát, Nhị Nghi, Tam Địa Sát, Tứ Tấn Tài, Ngũ Thọ Tử, Lục Hoang Ốc).

Tính Tam Tai: Xác định nhóm tam hợp của tuổi, từ đó suy ra 3 năm hạn liên tiếp.

Tính Bát Trạch: Dựa vào cung phi để xác định 8 hướng (Sinh Khí, Thiên Y, Diên Niên, Phục Vị, Tuyệt Mệnh, Ngũ Quỷ, Lục Sát, Họa Hại) và ý nghĩa từng hướng.

Tính thước Lỗ Ban: Số đo nhập vào được chia lấy dư theo chu kỳ thước (52.2cm, 42.9cm, 38.8cm tùy loại), kết quả dư được tra bảng để xác định cung và ý nghĩa.

# 🗄️ CƠ SỞ DỮ LIỆU SỬ DỤNG

Hệ thống sử dụng MySQL với 89 bảng, bao gồm:

- 12 bảng chính của WordPress: wp_posts, wp_postmeta, wp_users, wp_usermeta, wp_terms, wp_term_relationships, wp_comments, wp_commentmeta...
- Các bảng của WooCommerce: wp_woocommerce_order_items, wp_woocommerce_order_itemmeta...
- Các bảng tự tạo cho plugin phong thủy: wp_dnvb_canchi (lưu dữ liệu 60 hoa giáp), wp_dnvb_nguhanh (Ngũ hành), wp_dnvb_battrach (Bát trạch), wp_dnvb_loban (thước Lỗ Ban), wp_dnvb_tra_cuu (lịch sử tra cứu).

Dữ liệu phong thủy được chuẩn hóa và lưu trữ có cấu trúc, cho phép truy vấn nhanh và chính xác.

# ⚙️ HƯỚNG DẪN CÀI ĐẶT

Yêu cầu hệ thống: PHP 7.4+, MySQL 5.7+, WordPress 6.4+, WooCommerce 8.0+.

Các bước cài đặt:

1. Cài đặt XAMPP/WAMP/MAMP và khởi động Apache, MySQL
2. Tạo database mới trong phpMyAdmin
3. Cài đặt WordPress vào thư mục htdocs
4. Cấu hình WordPress với database đã tạo
5. Cài đặt các plugin cần thiết (WooCommerce, Elementor, Contact Form 7...)
6. Upload và kích hoạt các plugin phong thủy tự phát triển
7. Cấu hình WooCommerce (tiền tệ, vận chuyển, thanh toán)
8. Nhập dữ liệu phong thủy gốc qua menu quản trị
9. Thiết lập giao diện và menu

Trên hosting thật: Quy trình tương tự nhưng upload file qua FTP, tạo database trong control panel, cập nhật wp-config.php với thông tin database mới.

# 📘 HƯỚNG DẪN SỬ DỤNG

Cho người dùng:

- Tra cứu phong thủy: Vào menu "Tra cứu phong thủy", chọn chức năng, nhập thông tin (năm sinh, giới tính, hướng nhà...), nhấn "Xem kết quả" để nhận tư vấn.
- Mua sắm: Vào "Cửa hàng", duyệt sản phẩm, thêm vào giỏ hàng, thanh toán qua COD hoặc chuyển khoản.

Cho quản trị viên:

- Quản lý nội dung phong thủy: Vào menu "Phong thủy" để nhập, chỉnh sửa dữ liệu gốc (Can Chi, Ngũ hành, Bát trạch, thước Lỗ Ban).
- Quản lý sản phẩm: Vào "Sản phẩm" để thêm, sửa, xóa sản phẩm, quản lý danh mục và kho hàng.
- Quản lý đơn hàng: Vào "WooCommerce > Đơn hàng" để xử lý đơn hàng, cập nhật trạng thái.
- Quản lý người dùng: Vào "Người dùng" để phân quyền, xem lịch sử hoạt động.

# 🔐 BẢO MẬT HỆ THỐNG

Các biện pháp đã triển khai:

- Sử dụng plugin bảo mật (Wordfence Security) để giám sát và bảo vệ
- Giới hạn số lần đăng nhập sai để chống brute force
- Ẩn thông tin phiên bản WordPress
- Mã hóa mật khẩu người dùng bằng bcrypt
- Validate và escape dữ liệu đầu vào/đầu ra để chống XSS, SQL injection
- Sử dụng nonce cho các form quan trọng
- Triển khai SSL (HTTPS) cho toàn site
- Cập nhật thường xuyên WordPress core, theme và plugin

# 🧪 KIỂM THỬ HỆ THỐNG

Phương pháp kiểm thử:

- Kiểm thử chức năng: Kiểm tra từng chức năng phong thủy với nhiều bộ dữ liệu đầu vào, so sánh kết quả với tính toán thủ công để đảm bảo chính xác.
- Kiểm thử giao diện: Kiểm tra hiển thị trên nhiều trình duyệt (Chrome, Firefox, Safari) và thiết bị (desktop, tablet, mobile).
- Kiểm thử hiệu năng: Đo tốc độ tải trang bằng GTmetrix, PageSpeed Insights.
- Kiểm thử tích hợp: Kiểm tra luồng mua hàng từ thêm giỏ hàng đến thanh toán.

Kết quả kiểm thử:

- Các chức năng phong thủy cho kết quả chính xác 100% so với tra cứu thủ công
- Giao diện hiển thị tốt trên tất cả trình duyệt và thiết bị
- Thời gian tải trang dưới 3 giây cho trang chủ, dưới 2 giây cho trang tra cứu
- Luồng mua hàng hoạt động trơn tru

# 🚀 TỐI ƯU HIỆU NĂNG

Các biện pháp tối ưu:

- Tối ưu database: Đánh index cho các trường thường xuyên query, sử dụng caching query
- Tối ưu frontend: Minify CSS và JavaScript, nén ảnh định dạng WebP, sử dụng CDN cho static files
- Tối ưu WordPress: Sử dụng caching plugin (W3 Total Cache), giới hạn post revision, tắt tính năng không cần thiết
- Tối ưu code: Viết code hiệu quả, giảm số lượng database query, sử dụng lazy loading cho hình ảnh

Kết quả tối ưu:

- Điểm PageSpeed: 85+ trên desktop, 75+ trên mobile
- Thời gian phản hồi server dưới 500ms
- Số lượng HTTP request dưới 50 request/trang

# 🏁 KẾT LUẬN & HƯỚNG PHÁT TRIỂN

Kết luận:  
Dự án "Đại Nam Vạn Bảo" đã thành công trong việc xây dựng website tích hợp tư vấn phong thủy kiến trúc An Trạch và kinh doanh pháp phẩm Kim Cang Thừa. Hệ thống đã hiện thực hóa 6 công cụ tra cứu phong thủy tự động, chính xác, tích hợp hệ thống thương mại điện tử đầy đủ, với giao diện thân thiện và hiệu năng tốt. Dự án chứng minh tính khả thi của việc ứng dụng công nghệ thông tin vào việc số hóa và phổ biến tri thức phong thủy truyền thống.

Hướng phát triển:

- Phát triển ứng dụng di động: Xây dựng app iOS và Android để tăng tính tiện lợi
- Tích hợp AI Chatbot: Phát triển chatbot sử dụng AI để tư vấn phong thủy tự nhiên hơn
- Mở rộng dữ liệu phong thủy: Bổ sung thêm các trường phái phong thủy khác (Huyền không, Phi tinh...)
- Tích hợp thanh toán trực tuyến: Thêm các cổng thanh toán phổ biến (VNPay, Momo, Zalopay)
- Hệ thống đặt lịch tư vấn: Cho phép đặt lịch tư vấn trực tiếp với chuyên gia phong thủy
- Phân tích dữ liệu người dùng: Thu thập và phân tích dữ liệu tra cứu để cải thiện dịch vụ
- Cộng đồng người dùng: Xây dựng diễn đàn trao đổi về phong thủy và trải nghiệm sản phẩm

Dự án mở ra hướng phát triển mới cho việc kết hợp tri thức truyền thống với công nghệ hiện đại, góp phần bảo tồn và phổ biến văn hóa phong thủy Việt Nam trong thời đại số.
