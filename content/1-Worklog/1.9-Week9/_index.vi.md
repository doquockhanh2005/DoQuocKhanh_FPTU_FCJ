---
title: "Worklog Tuần 9"
date: 2025-11-09


weight: 1
chapter: false
pre: " <b> 1.9. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 9:

* Chuyển đổi tư duy từ "ClickOps" (dùng chuột) sang "IaC" (dùng code).
* Sử dụng AWS CDK để định nghĩa hạ tầng.
### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Tìm hiểu khái niệm IaC (Infrastructure as Code) <br> - Giới thiệu CloudFormation và AWS CDK (Cloud Development Kit)    | 03/11/2025   | 03/11/2025      |
| 3   | - **Thực hành:** Cài đặt AWS CDK, khởi tạo project CDK (TypeScript/Python) <br> - Tìm hiểu cấu trúc App, Stack, Construct                                            | 04/11/2025   | 04/11/2025      | 
| 4   | - **Thực hành:** Viết code CDK để tạo một S3 Bucket và DynamoDB Table <br> - Lệnh `cdk synth` và `cdk deploy`  | 05/11/2025   | 05/11/2025      | 
| 5   | - **Thực hành nâng cao:** Viết code CDK để dựng lại VPC (như tuần 2) <br> - Quản lý sự phụ thuộc giữa các resource trong code                  | 06/11/2025   | 06/11/2025      | 
| 6   | - Thực hiện `cdk destroy` để dọn dẹp tài nguyên. Hiểu về Drift detection.| 07/11/2025   | 07/11/2025      |  |


### Kết quả đạt được tuần 9:

* Hiểu lợi ích của IaC trong việc quản lý version và tái sử dụng hạ tầng.

* Có khả năng dùng ngôn ngữ lập trình để tự động hóa việc tạo tài nguyên AWS thay vì làm thủ công.