---
title: "Worklog Tuần 8"
date: 2025-11-02


weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 8:

* Hiểu về Containerization trên AWS.
* Deploy ứng dụng Docker lên AWS ECS Fargate.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Ôn tập Docker: Dockerfile, Image, Container <br> - Tìm hiểu Amazon ECR (Elastic Container Registry)    | 27/10/2025   | 27/10/2025      |
| 3   | - **Thực hành:** Build Docker Image cho một app NodeJS đơn giản <br> - Push Image lên ECR repository                                            | 28/10/2025   | 28/10/2025      |
| 4   | - Tìm hiểu Amazon ECS (Elastic Container Service) <br> - Phân biệt EC2 Launch Type và Fargate (Serverless compute for containers)  | 29/10/2025   | 29/10/2025      | 
| 5   | - **Thực hành:** Tạo ECS Cluster, Task Definition và Service <br> - Deploy container chạy trên nền tảng Fargate                  | 30/10/2025   | 30/10/2025      |
| 6   | - Kiểm tra ứng dụng chạy, xem logs container trên AWS.| 31/10/2025   | 31/10/2025      | 


### Kết quả đạt được tuần 8:

* Biết cách đóng gói ứng dụng và quản lý Docker Images trên ECR.

* Đã deploy ứng dụng container hóa lên môi trường production-ready sử dụng ECS Fargate mà không cần quản lý server vật lý.