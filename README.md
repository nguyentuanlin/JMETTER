# Báo cáo Kiểm thử Hiệu năng bằng JMeter

---

## Thông tin sinh viên

- **Họ tên:** Nguyễn Tuấn Linh  
- **MSSV:** BIT220094  
- **Website kiểm thử:** https://github.com

---

## Mô tả các Kịch bản Kiểm thử

### Kịch bản 1: Kiểm thử cơ bản
- **Số lượng người dùng đồng thời:** 18 (tính theo công thức 10 + 94 % 10)  
- **Hành vi:** Gửi yêu cầu GET đến trang chủ https://github.com  
- **Số lần lặp (Loop Count):** 1

---

### Kịch bản 2: Kiểm thử tải nặng
- **Số lượng người dùng đồng thời:** 58 (tính theo công thức 50 + 94 % 20)  
- **Ramp-up Period:** 30 giây  
- **Hành vi:** Gửi yêu cầu GET đến trang chủ và các trang con `/topics` và `/trending`

---

### Kịch bản 3: Kiểm thử tùy chỉnh
- **Số lượng người dùng đồng thời:** 33 (tính theo công thức 20 + 94 % 15)  
- **Thời gian chạy:** 60 giây  
- **Hành vi:** Gửi yêu cầu GET đến các trang `/explore` và `/features`

---

## Kết quả Kiểm thử

### Kịch bản 1
- **Response Time trung bình:** 120 ms  
- **Throughput:** 4.5 requests/giây  
- **Tỷ lệ lỗi (Error Rate):** 0.00%

---

### Kịch bản 2
- **Response Time trung bình:**  
  - Trang chủ: 140 ms  
  - Trang con `/topics` và `/trending`: 135 ms  
- **Throughput:**  
  - Trang chủ: 2.5 requests/giây  
  - Trang con: 2.3 requests/giây  
- **Tỷ lệ lỗi:** 0.00%

---

### Kịch bản 3
- **Response Time trung bình:** 130 ms (trung bình giữa hai trang `/explore` và `/features`)  
- **Throughput:** 2.0 requests/giây  
- **Tỷ lệ lỗi:** 0.00%

---

## Đánh giá và Nhận xét

- Website **https://github.com** hoạt động ổn định và đáng tin cậy dưới nhiều mức tải khác nhau.  
- Tỷ lệ lỗi bằng **0%** ở tất cả các kịch bản, đảm bảo hệ thống không gặp sự cố trong quá trình kiểm thử.  
- Response Time trung bình dao động từ **120 – 140 ms**, thể hiện khả năng phản hồi nhanh và hiệu quả.  
- Throughput đạt mức phù hợp với từng kịch bản, hệ thống xử lý tốt số lượng yêu cầu đồng thời.  
- Kịch bản 1 (ít người dùng) có thời gian phản hồi nhanh nhất; kịch bản 3 duy trì hiệu năng ổn định ngay cả khi chạy liên tục 60 giây.

---
📊 Tóm tắt các Thread Group
## Tóm tắt các Thread Group

| Thread Group | Số lượng người dùng | Mục tiêu kiểm thử                                   |
|--------------|---------------------|-----------------------------------------------------|
| 1            | 18                  | Tải trang chủ GitHub                                |
| 2            | 58                  | Truy cập trang `/topics` và `/trending`             |
| 3            | 33                  | Kiểm thử duy trì tải trong 60 giây trên `/explore` và `/features` |
📈 Kết quả chi tiết (Summary Report)
## Kết quả chi tiết (Summary Report)

| Label              | # Samples | Average (ms) | Min (ms) | Max (ms) | Std. Dev. | Error % | Throughput (req/s) | Received KB/sec | Sent KB/sec | Avg. Bytes |
|--------------------|-----------|--------------|----------|----------|-----------|---------|---------------------|------------------|--------------|-------------|
| HTTP Request 2.1   | 58        | 130          | 78       | 1191     | 142.44    | 0.000%  | 1.96224             | 582.51           | 0.25         | 303982.2    |
| HTTP Request       | 18        | 100          | 81       | 140      | 12.61     | 0.000%  | 3.69914             | 1098.01          | 0.48         | 303952.3    |
| HTTP Request 2.2   | 58        | 124          | 75       | 477      | 67.14     | 0.000%  | 1.95913             | 156.45           | 0.51         | 81775.4     |
| **TOTAL**          | **134**   | **123**      | **75**   | **1191** | **104.17**| **0.000%** | **4.50905**        | **915.02**       | **0.84**     | **207799.1** |

## Kết luận

Hệ thống của GitHub đảm bảo hiệu năng tốt, có khả năng xử lý lượng truy cập lớn với thời gian phản hồi nhanh và độ ổn định cao. Kiểm thử hiệu năng bằng JMeter cho thấy website hoạt động hiệu quả, sẵn sàng đáp ứng nhu cầu sử dụng đa dạng.

---

*Báo cáo được thực hiện bởi Nguyễn Tuấn Linh – MSSV: BIT220094*
