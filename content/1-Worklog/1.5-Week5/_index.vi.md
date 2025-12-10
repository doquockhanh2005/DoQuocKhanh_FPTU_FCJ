---
title: "Worklog Tuần 5"
date: 2025-10-12


weight: 1
chapter: false
pre: " <b> 1.5. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 5:

* Phân biệt và sử dụng được RDS (SQL) và DynamoDB (NoSQL).
* Hiểu về kiến trúc Multi-AZ cho Database.
* **Thực hành:** Kết nối ứng dụng với Database.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Tìm hiểu Amazon RDS, các engine hỗ trợ (MySQL, Postgres...) <br> - Khái niệm Multi-AZ và Read Replicas    | 06/10/2025   | 06/10/2025      |  |
| 3   | - **Thực hành:** Tạo RDS Instance (MySQL) trong Private Subnet <br> - Cấu hình Security Group cho phép EC2 kết nối tới RDS                                            | 07/10/2025   | 07/10/2025      |  |
| 4   | - Tìm hiểu Amazon DynamoDB (NoSQL): Table, Item, Partition Key, Sort Key <br> - Các chế độ Capacity (Provisioned vs On-demand)  | 08/10/2025   | 08/10/2025      |  |
| 5   | - **Thực hành:** Tạo bảng DynamoDB, thêm/sửa/xóa item qua AWS Console và AWS CLI <br> - Tìm hiểu ElastiCache (Redis) cơ bản                  | 09/10/2025   | 09/10/2025      |  |
| 6   | - **Thực hành:** Viết script nhỏ (Python/NodeJS) trên EC2 để query dữ liệu từ RDS và DynamoDB.| 10/10/2025   | 10/10/2025      |  |

### Kết quả đạt được tuần 5:

* Đã tạo và cấu hình thành công RDS MySQL an toàn trong Private Subnet.
  
* Hiểu cách thiết kế bảng cơ bản với DynamoDB.

* Thực hiện kết nối thành công từ Web Server vào Database Server.

