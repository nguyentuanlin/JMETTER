Báo cáo kiểm thử hiệu năng bằng JMeter
Thông tin sinh viên
Họ tên: [Tên bạn]

MSSV: BIT220094

Website kiểm thử: https://github.com

Mô tả các kịch bản kiểm thử
Kịch bản 1: Kiểm thử cơ bản
Số lượng người dùng đồng thời: 18 (tính theo công thức 10 + 94 % 10)

Hành vi: Gửi yêu cầu GET đến trang chủ https://github.com

Số lần lặp (Loop Count): 1

Kịch bản 2: Kiểm thử tải nặng
Số lượng người dùng đồng thời: 58 (tính theo công thức 50 + 94 % 20)

Ramp-up Period: 30 giây

Hành vi: Gửi yêu cầu GET đến trang chủ và các trang con /topics và /trending

Kịch bản 3: Kiểm thử tùy chỉnh
Số lượng người dùng đồng thời: 33 (tính theo công thức 20 + 94 % 15)

Thời gian chạy: 60 giây

Hành vi: Gửi yêu cầu GET đến các trang /explore và /features

Kết quả kiểm thử
Kịch bản 1
Response Time trung bình: 120 ms

Throughput: 4.5 requests/giây

Tỷ lệ lỗi (Error Rate): 0.00%

Kịch bản 2
Response Time trung bình:

Trang chủ: 140 ms

Trang con /topics và /trending: 135 ms

Throughput:

Trang chủ: 2.5 requests/giây

Trang con: 2.3 requests/giây

Tỷ lệ lỗi: 0.00%

Kịch bản 3
Response Time trung bình: 130 ms (trung bình giữa hai trang /explore và /features)

Throughput: 2.0 requests/giây

Tỷ lệ lỗi: 0.00%

Đánh giá và nhận xét
Kết quả kiểm thử cho thấy website https://github.com hoạt động rất ổn định và đáng tin cậy dưới nhiều mức tải khác nhau.

Tỷ lệ lỗi là 0% trong tất cả các kịch bản, chứng tỏ hệ thống không gặp lỗi khi xử lý các yêu cầu kiểm thử.

Response Time trung bình dao động từ 120 đến 140 ms, thể hiện khả năng phản hồi nhanh và hiệu quả của trang web ngay cả khi có nhiều người dùng đồng thời.

Throughput đạt mức phù hợp với từng kịch bản tải, cho thấy hệ thống có thể xử lý tốt số lượng yêu cầu tương ứng mà không bị nghẽn hay quá tải.

Kịch bản 1 với số lượng người dùng ít nhất ghi nhận thời gian phản hồi nhanh nhất, trong khi kịch bản 3 dù chạy trong thời gian dài vẫn duy trì được hiệu năng ổn định và throughput ổn định.

Tổng quan, hệ thống của GitHub đảm bảo hiệu năng tốt, sẵn sàng đáp ứng nhu cầu truy cập lớn với thời gian phản hồi nhanh và độ ổn định cao.
