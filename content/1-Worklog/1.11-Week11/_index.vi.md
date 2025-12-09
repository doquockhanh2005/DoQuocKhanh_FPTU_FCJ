---
title: "Worklog Tuần 11"
date: 2025-11-23


weight: 2
chapter: false
pre: " <b> 1.11. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 11:

* Giám sát sức khỏe hệ thống và xử lý sự cố.
* Kiểm toán các hoạt động trên tài khoản AWS.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Tìm hiểu Amazon CloudWatch: Metrics, Logs, Alarms <br> - Các metric chuẩn của EC2 (CPU, Network...)    | 17/11/2025   | 17/11/2025      |
| 3   | - **Thực hành:** Tạo CloudWatch Alarm gửi email qua SNS khi CPU EC2 > 80% <br> - Cài CloudWatch Agent để lấy thông số RAM (Memory usage)                                            | 18/11/2025   | 18/11/2025      |
| 4   | - Tìm hiểu AWS CloudTrail (Audit log) <br> - Tìm hiểu AWS X-Ray (Tracing cho microservices)  | 19/11/2025   | 19/11/2025      |
| 5   | - **Thực hành:** Tạo Dashboard trên CloudWatch để quan sát tổng quan hệ thống <br> - Kiểm tra CloudTrail để xem ai đã xóa resource                  | 20/11/2025   | 20/11/2025      |
| 6   | - Review CouldTrail và CouldWatch                                                                                         | 15/08/2025   | 15/08/2025      | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 11:

* Có khả năng giám sát hệ thống thời gian thực.

* Thiết lập được hệ thống cảnh báo sớm sự cố.

* Biết cách truy vết (audit) các hành động nhạy cảm trên tài khoản AWS.
