---
title: "Worklog Tuần 3"
date: 2025-09-28


weight: 1
chapter: false
pre: " <b> 1.3. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 3:

* Học dịch vụ máy chủ ảo EC2 và các loại ổ đĩa EBS.
*  Hiểu về tính sẵn sàng cao (High Availability) và khả năng mở rộng (Scalability).
* **Thực hành:** Deploy web server với Load Balancer và Auto Scaling.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Tìm hiểu các dòng EC2 (Instance types), AMI và Key Pairs <br> - Tìm hiểu về EBS Volumes và Snapshots    | 22/09/2025   | 22/09/2025      |  |
| 3   | - **Thực hành:** Khởi tạo EC2 Linux, SSH vào server, cài đặt Apache/Nginx đơn giản <br> - Gắn thêm EBS Volume vào EC2                                            | 23/09/2025   | 23/09/2025      |  |
| 4   | - Tìm hiểu về Elastic Load Balancer (ALB vs NLB) <br> - Tìm hiểu về Auto Scaling Group (ASG) và Launch Template  | 24/09/2025   | 24/09/2025      |  |
| 5   | - **Thực hành:** Tạo Application Load Balancer trỏ vào EC2 <br> - Cấu hình Target Groups và Health Checks                  | 25/09/2025   | 25/09/2025      |  |
| 6   | - **Thực hành Lab:** Giả lập traffic tăng cao để Auto Scaling tự động tạo thêm server mới.| 26/09/2025   | 26/09/2025      |  |


### Kết quả đạt được tuần 3:

* Đã deploy thành công một Web Server cơ bản trên EC2.
  
* Hiểu và cấu hình được Load Balancer để phân phối tải.

* Thiết lập được Auto Scaling Group để hệ thống tự động co giãn theo nhu cầu thực tế.
