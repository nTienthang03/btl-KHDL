# Phân tích thực tế về chất lượng không khí tại Hà Nội

## 1. Thông tin sinh viên

* **Sinh viên:** Nguyễn Tiến Thắng
* **MSSV:** K225480106058
* **Lớp:** K58KTP
* **Môn học:** Khoa học dữ liệu
* **Giảng viên hướng dẫn:** Nguyễn Văn Huy
## Link trình bày :

---

## 2. Tên đề tài

**Phân tích thực tế về chất lượng không khí tại Hà Nội**

Đề tài tập trung phân tích chỉ số bụi mịn **PM2.5** tại Hà Nội trong giai đoạn từ **14/02/2024 đến 26/01/2026**. Thông qua dữ liệu thực tế, đề tài thực hiện xử lý dữ liệu, tính toán thống kê, trực quan hóa kết quả, phân tích xu hướng, dự đoán PM2.5 và phân nhóm mức độ ô nhiễm.

---

## 3. Mục tiêu đề tài

* Phân tích chất lượng không khí tại Hà Nội thông qua chỉ số PM2.5.
* Xác định số ngày có PM2.5 trung bình vượt ngưỡng.
* Tìm khung giờ trong ngày thường có PM2.5 cao nhất.
* Phân tích điều kiện thời tiết khi PM2.5 vượt ngưỡng.
* Đánh giá sự thay đổi PM2.5 theo mùa.
* Xem xét xu hướng PM2.5 trong giai đoạn 2024–2026.
* Dự đoán PM2.5 trung bình cho 06 tháng cuối năm 2026.
* Phân nhóm PM2.5 thành 03 mức: thấp, trung bình và cao.

---

## 4. Dữ liệu sử dụng

File dữ liệu sử dụng trong đề tài:

```text
hanoi_aqi_ml_ready_fixed.csv
```

Các trường dữ liệu chính:

| STT | Tên trường           | Ý nghĩa                    |
| --: | -------------------- | -------------------------- |
|   1 | datetime             | Thời gian ghi nhận dữ liệu |
|   2 | pm25                 | Nồng độ bụi mịn PM2.5      |
|   3 | temperature          | Nhiệt độ                   |
|   4 | humidity             | Độ ẩm                      |
|   5 | wind_speed           | Tốc độ gió                 |
|   6 | rain / precipitation | Lượng mưa                  |
|   7 | is_raining           | Trạng thái có mưa          |
|   8 | cloud_cover          | Độ che phủ mây             |

Khoảng thời gian phân tích:

```text
14/02/2024 - 26/01/2026
```

---

## 5. Công cụ và thư viện sử dụng

Đề tài được thực hiện bằng **Python** trên môi trường **Jupyter Notebook**.

Các thư viện chính:

* **Pandas:** đọc, xử lý và nhóm dữ liệu.
* **NumPy:** hỗ trợ tính toán dữ liệu số.
* **Matplotlib:** trực quan hóa dữ liệu bằng biểu đồ.
* **Scikit-learn:** hỗ trợ phân tích, dự đoán hoặc phân nhóm dữ liệu.

---

## 6. Các câu hỏi phân tích

Đề tài tập trung trả lời 07 câu hỏi chính:

1. Từ ngày 14/02/2024 đến ngày 26/01/2026, số ngày có PM2.5 vượt ngưỡng là bao nhiêu?
2. Khung giờ nào trong ngày thường có nồng độ PM2.5 cao nhất?
3. Chỉ số PM2.5 trung bình vượt ngưỡng thường xuất hiện trong điều kiện thời tiết nào?
4. Nồng độ PM2.5 tại Hà Nội thay đổi như thế nào theo mùa trong giai đoạn 2024–2026?
5. PM2.5 trong giai đoạn 2024–2026 đang có xu hướng tốt lên hay xấu đi?
6. Dự đoán PM2.5 trung bình của 06 tháng cuối năm 2026 như thế nào?
7. Phân nhóm PM2.5 thành 03 mức thấp, trung bình và cao dựa trên ngưỡng đánh giá như thế nào?

---

## 7. Kết quả chính

### 7.1. Số ngày PM2.5 vượt ngưỡng

* Tổng số ngày phân tích: **641 ngày**
* Số ngày PM2.5 trung bình vượt ngưỡng 50 µg/m3: **100 ngày**
* Tỷ lệ ngày vượt ngưỡng: **15.60%**

### 7.2. Khung giờ PM2.5 cao nhất

* Khung giờ có PM2.5 trung bình cao nhất: **khoảng 18 giờ**

### 7.3. Điều kiện thời tiết khi PM2.5 vượt ngưỡng

Các ngày PM2.5 vượt ngưỡng thường xuất hiện trong điều kiện:

* Ít mưa.
* Tốc độ gió thấp.
* Nhiệt độ thấp hơn.
* Độ ẩm thấp hơn.
* Khả năng khuếch tán không khí kém.

### 7.4. PM2.5 theo mùa

| Mùa  | PM2.5 trung bình | Tỷ lệ ngày vượt ngưỡng |
| ---- | ---------------: | ---------------------: |
| Xuân |      35.59 µg/m3 |                 23.81% |
| Hạ   |      31.28 µg/m3 |                  9.47% |
| Thu  |      27.29 µg/m3 |                  4.47% |
| Đông |      41.11 µg/m3 |                 28.08% |

Nhận xét:

* Mùa đông có PM2.5 trung bình cao nhất.
* Mùa thu có PM2.5 trung bình thấp nhất.
* PM2.5 tại Hà Nội có sự thay đổi rõ rệt theo mùa.

### 7.5. Xu hướng PM2.5

* PM2.5 trung bình 3 tháng đầu kỳ: **25.62 µg/m3**
* PM2.5 trung bình 3 tháng cuối kỳ: **41.21 µg/m3**
* Mức tăng: **15.59 µg/m3**
* Tỷ lệ tăng: **60.85%**

Nhận xét:

PM2.5 có dấu hiệu tăng ở giai đoạn cuối, cho thấy chất lượng không khí có xu hướng xấu hơn. Tuy nhiên, kết quả cần được xem xét cùng yếu tố mùa vì giai đoạn cuối nằm gần mùa đông, thời điểm PM2.5 thường cao hơn.

### 7.6. Phân nhóm PM2.5

| Nhóm               | Điều kiện       |  Số ngày |  Tỷ lệ |
| ------------------ | --------------- | -------: | -----: |
| Ô nhiễm thấp       | PM2.5 ≤ 25      | 241 ngày | 37.60% |
| Ô nhiễm trung bình | 25 < PM2.5 ≤ 50 | 300 ngày | 46.80% |
| Ô nhiễm cao        | PM2.5 > 50      | 100 ngày | 15.60% |

---

## 8. Cấu trúc thư mục dự án

```text
btl-KHDL/
│
├── hanoi_aqi_ml_ready_fixed.csv
├── main.ipynb
├── README.md
│
├── output/
│   ├── bang_01_pm25_trung_binh_theo_ngay.csv
│   ├── bang_03_so_sanh_thoi_tiet_pm25_vuot_nguong.csv
│   ├── bang_06_du_doan_pm25_06_thang_cuoi_2026.csv
│   └── ...
│
└── output/bieu_do/
    ├── bieu_do_01_pm25_trung_binh_theo_ngay.png
    ├── bieu_do_02_pm25_trung_binh_theo_gio.png
    ├── bieu_do_03_so_sanh_thoi_tiet_pm25_vuot_nguong.png
    ├── bieu_do_04_pm25_theo_mua.png
    ├── bieu_do_05_xu_huong_pm25_theo_thang.png
    ├── bieu_do_06_du_doan_pm25_06_thang_cuoi_2026.png
    └── bieu_do_07_phan_nhom_pm25_theo_nguong.png
```

---

## 9. Cách chạy chương trình

### Bước 1. Cài đặt thư viện cần thiết

```bash
pip install pandas numpy matplotlib scikit-learn
```

### Bước 2. Mở Jupyter Notebook

```bash
jupyter notebook
```

### Bước 3. Chạy file notebook

Mở file:

```text
main.ipynb
```

Sau đó chạy lần lượt các cell từ trên xuống dưới để tạo bảng kết quả và biểu đồ.

---

## 10. Kết luận

Đề tài đã thực hiện phân tích dữ liệu PM2.5 tại Hà Nội trong giai đoạn từ ngày 14/02/2024 đến ngày 26/01/2026. Kết quả cho thấy Hà Nội có 100 ngày PM2.5 trung bình vượt ngưỡng 50 µg/m3. PM2.5 có sự thay đổi theo giờ, theo mùa và có xu hướng tăng ở giai đoạn cuối của dữ liệu.

Thông qua đề tài, sinh viên đã vận dụng được kiến thức môn Khoa học dữ liệu vào một bài toán thực tế, bao gồm đọc dữ liệu, xử lý dữ liệu, thống kê, trực quan hóa, dự đoán và phân nhóm dữ liệu.

---

## 11. Hướng phát triển

* Bổ sung dữ liệu trong thời gian dài hơn.
* Kết hợp thêm các chỉ số ô nhiễm khác như PM10, CO, NO2, SO2, O3 hoặc AQI.
* Xây dựng mô hình dự đoán PM2.5 chính xác hơn.
* Phát triển dashboard trực quan hóa dữ liệu.
* Kết nối dữ liệu thời gian thực để theo dõi và cảnh báo chất lượng không khí.

---

## 12. Tài liệu tham khảo

* Kaggle Dataset: Hanoi Air Quality PM2.5 & Weather Data 2024–2026
  https://www.kaggle.com/datasets/diabolicfox/hanoi-air-quality-pm2-5-weather-data-2024-2026

* Python Documentation
  https://docs.python.org/3/

* Pandas Documentation
  https://pandas.pydata.org/docs/

* NumPy Documentation
  https://numpy.org/doc/

* Matplotlib Documentation
  https://matplotlib.org/stable/

* Scikit-learn Documentation
  https://scikit-learn.org/stable/
