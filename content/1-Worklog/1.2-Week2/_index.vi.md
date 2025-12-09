---
title: "Worklog Tuần 2"
date: 2024-09-15


weight: 1
chapter: false
pre: " <b> 1.2. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 2:

* Hiểu sâu về kiến trúc mạng trong AWS: VPC, Subnet, Route Table.
* Nắm vững các cơ chế bảo mật mạng: Security Group và NACL.
* **Thực hành:** Tự xây dựng một hệ thống mạng (Custom VPC) hoàn chỉnh thay vì dùng Default VPC.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Tìm hiểu lý thuyết về Amazon VPC, Region, Availability Zones (AZ) <br> - Hiểu về CIDR Blocks và cách chia dải IP    | 15/09/2025   | 15/09/2025      | <https://cloudjourney.awsstudygroup.com/> |
| 3   | - Tìm hiểu các thành phần: Subnet (Public/Private), Route Tables, Internet Gateway (IGW) <br> - Tìm hiểu về NAT Gateway (để Private subnet ra internet)                                            | 16/09/2025   | 16/09/2025      | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - **Thực hành:** Tạo Custom VPC, chia 2 Subnet (1 Public, 1 Private), gắn Internet Gateway  | 17/09/2025   | 17/09/2025      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Phân biệt Security Group (Stateful) và Network ACL (Stateless) <br> - Cấu hình Inbound/Outbound rules cơ bản (SSH, HTTP)                  | 18/09/2025   | 18/09/2025      | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - **Thực hành:** Hoàn thiện mô hình VPC 2 lớp. Kiểm tra kết nối mạng giữa các subnet và ra internet.| 19/09/2025   | 19/09/2025      | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 2:

* Đã hiểu rõ luồng đi của gói tin trong VPC (Traffic flow).

* Tự tay dựng được một kiến trúc VPC an toàn bao gồm: Public Subnet (cho Web Server) và Private Subnet (cho Database sau này).
  
* Biết cách cấu hình Security Group để chỉ mở các port cần thiết (Least Privilege).

