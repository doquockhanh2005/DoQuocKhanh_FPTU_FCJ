---
title: "Event AWS Cloud Mastery Series #3"
date: 2025-11-29


weight: 1
chapter: false
pre: " <b> 4.4. </b> "
---
# Báo cáo Tổng hợp: “Identity & Access Management”
## Mục tiêu Sự kiện
* Hiểu rõ về IAM, quản lý thông tin xác thực và cấu trúc AWS Organization.
* Làm chủ hệ thống phát hiện mối đe dọa với GuardDuty và tư duy Detection-as-Code.
* Thiết kế kiến trúc bảo mật mạng phân lớp (Layered Security) và triển khai Network Firewall tối ưu.
* Hiểu sâu về cơ chế mã hóa dữ liệu với AWS KMS (Key Management Service): Sự khác biệt giữa AWS Managed Key và Customer Managed Key (CMK).
* Áp dụng chiến lược lọc traffic tự động (Automated Domain Lists) để chặn các mối đe dọa mới.
## Speakers
* **FCJ members**
## Điểm nhấn Chính
### Quản lý Danh tính & Truy cập (IAM)
* Nguyên tắc: Loại bỏ Access Keys dài hạn, sử dụng Short-term credentials qua IAM Identity Center.
* Kiểm soát: Kết hợp SCP (chặn quyền mức tổ chức) và Permission Boundaries (giới hạn quyền mức user).
* Tự động hóa: Xoay vòng mật khẩu DB tự động với Secrets Manager.
### Phát hiện & Phản ứng (Detection & Response)
* GuardDuty: Giám sát thời gian thực (Runtime Monitoring) để phát hiện hành vi bất thường sâu trong OS (process, file access).
* Detection-as-Code: Quản lý quy tắc phát hiện dưới dạng mã nguồn (CloudFormation/Terraform) để đảm bảo tính nhất quán và tuân thủ (Compliance).
### An ninh Mạng (Network Security)
* Bảo mật đa lớp: Kết hợp WAF (Layer 7) -> Network Firewall (Layer 3-7) -> NACL (Subnet) -> Security Group (Instance).
* Network Firewall:
  * Sử dụng Active Threat Defense để tự động cập nhật rules chặn các mối đe dọa mới nhất từ AWS Threat Intelligence.
  * Tính năng Automated Domain Lists: Tự động phân tích traffic HTTP/HTTPS để tạo rule chặn hoặc cho phép dựa trên tên miền (FQDN) mà không cần quản lý IP thủ công.
### Bảo vệ Dữ liệu (Data Protection)
* Cơ chế KMS:
  * KMS quản lý Master Key (không bao giờ rời khỏi KMS).
  * Master Key dùng để mã hóa Data Key.
  * Data Key (dạng plaintext) mới thực sự được dùng để mã hóa dữ liệu người dùng.
* Phân loại Key:
  * AWS Managed Key: Miễn phí, do AWS quản lý, user không thể xoay vòng (rotate) thủ công hay thay đổi policy.
  * Customer Managed Key (CMK): Có phí, user toàn quyền kiểm soát (xoay vòng, phân quyền, xóa), bắt buộc dùng cho các yêu cầu tuân thủ cao.
  * Mã hóa EBS: Quy trình mã hóa ổ cứng EBS bao gồm việc tạo Data Key, mã hóa volume bằng Data Key đó và lưu trữ Data Key đã mã hóa kèm theo volume.
## Bài học Chính (Key Takeaways)
### Chiến lược Bảo vệ Dữ liệu
* Sử dụng CMK cho dữ liệu nhạy cảm: Mặc dù AWS Managed Key tiện lợi, nhưng CMK cho phép kiểm soát chặt chẽ hơn về việc ai được phép dùng key để giải mã (thông qua Key Policy).
* Key Rotation: Bật tính năng tự động xoay vòng key mỗi năm (đối với CMK) để đảm bảo an toàn nếu key cũ bị lộ.
### Kiến trúc Kỹ thuật
* Tối ưu chi phí Network: Sử dụng mô hình Multiple VPC Endpoints cho Network Firewall để giảm chi phí vận hành và đơn giản hóa kiến trúc mạng.
* Security Group Reference: Thay vì whitelist IP cứng trong Security Group, hãy tham chiếu đến SG ID của các tier khác (ví dụ: SG-App chỉ cho phép traffic từ SG-Web) để linh hoạt hơn.
## Ứng dụng vào Project
#### Cải thiện Quản lý Danh tính (IAM)
* Audit & Clean-up: Rà soát lại toàn bộ IAM User trong dự án, xóa các Access Key cũ/không sử dụng. Bắt buộc kích hoạt MFA (ưu tiên FIDO2/YubiKey) cho tất cả tài khoản.
* Implement Secrets Manager: Thay thế các biến môi trường chứa password DB trong code (ví dụ Spring Boot/Node.js) bằng code gọi API lấy secret từ AWS Secrets Manager.
#### Tăng cường An ninh Mạng
* Chặn luồng ra (Egress Filtering): Triển khai AWS Network Firewall hoặc DNS Firewall để kiểm soát traffic từ server ra Internet, ngăn chặn kết nối đến các domain lạ hoặc C2 server.
* Review Security Groups: Chuyển đổi các rule đang dùng IP tĩnh sang dùng Security Group Referencing để hỗ trợ tốt hơn cho Auto Scaling.
#### Giám sát & Phản ứng Tự động
* Kích hoạt GuardDuty: Bật GuardDuty trên môi trường Production để phát hiện ngay các hành vi bất thường (như đào tiền ảo, port scanning).
* Automated Remediation: Viết một Lambda function đơn giản và kết nối với EventBridge: Khi GuardDuty báo mức độ "High", tự động thu hồi session token hoặc chặn Security Group của instance đó.
## Trải nghiệm Sự kiện
Tham gia chuyên đề “AWS Mastery #3” đã giúp tôi hệ thống hóa lại toàn bộ các lớp bảo mật trên AWS.Là một lập trình viên thường tập trung vào code hơn là hạ tầng, sự kiện này đã thực sự thay đổi tư duy của tôi về trách nhiệm bảo mật:
#### Thay đổi tư duy về "Code sạch"
* Trước đây, tôi nghĩ không hardcode password là đủ. Nhưng khi thấy demo về IAM Access Analyzer, tôi nhận ra việc viết Infrastructure-as-Code (Terraform/CloudFormation) cũng cần phải được "lint" (kiểm tra lỗi) về logic bảo mật. Một dòng Principal: * vô tình trong code có thể mở toang cửa cho hacker, và công cụ này hoạt động như một "Unit Test" cho policy vậy.
#### Phân tích mã độc Mélofee
* Nhìn thấy dòng lệnh wget http://173.209... kết nối trực tiếp đến IP thay vì domain đã làm tôi "tỉnh ngộ". Tôi từng nghĩ chỉ cần chặn DNS là an toàn, nhưng malware thực tế khôn ngoan hơn nhiều. Điều này chứng minh tại sao Network Firewall (chặn IP egress) lại quan trọng đến thế đối với các server backend.
### Bài học "xương máu" về chi phí
* Một chi tiết nhỏ nhưng đắt giá mà diễn giả chia sẻ: Tài khoản Free Tier sẽ mất hiệu lực ngay lập tức khi tham gia AWS Organization. Đây là thông tin cực kỳ hữu ích cho các anh em Dev hay dùng tài khoản cá nhân để vọc vạch, giúp tránh được những hóa đơn "từ trên trời rơi xuống".
  
