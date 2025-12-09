---
title: "Worklog Tuần 10"
date: 2025-11-16


weight: 2
chapter: false
pre: " <b> 1.10. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 10:

* Tự động hóa quy trình phát triển phần mềm (DevOps).
* Xây dựng pipeline CI/CD hoàn chỉnh trên AWS.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Tìm hiểu về CI/CD (Continuous Integration / Continuous Delivery) <br> - Giới thiệu bộ công cụ: CodeCommit, CodeBuild, CodeDeploy, CodePipeline    | 10/11/2025   | 10/11/2025      |
| 3   | - **Thực hành:** Tạo Repository (có thể dùng GitHub), kết nối với CodeBuild <br> - Viết file `buildspec.yml` để build code                                            | 11/11/2025   | 11/11/2025      |
| 4   | - Tìm hiểu CodePipeline: Source stage, Build stage, Deploy stage <br> - **Thực hành:** Tạo Pipeline đơn giản deploy file lên S3  | 12/11/2025   | 12/11/2025      |
| 5   | - **Thực hành nâng cao:** Tạo Pipeline deploy ứng dụng lên ECS hoặc Lambda <br> - Thêm bước "Manual Approval" trước khi deploy production                  | 13/11/2025   | 13/11/2025      |
| 6   | - Test luồng: Push code -> Tự động Build -> Tự động Deploy.| 14/11/2025   | 14/11/2025      |


### Kết quả đạt được tuần 10:

* Hiểu quy trình DevOps tiêu chuẩn.

* Đã xây dựng được pipeline tự động hóa: chỉ cần commit code, hệ thống tự động build và deploy phiên bản mới.