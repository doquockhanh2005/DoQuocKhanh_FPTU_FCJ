---
title: "Event AWS Cloud Mastery Series #2"
date: 2025-11-17


weight: 1
chapter: false
pre: " <b> 4.3. </b> "
---
## Báo cáo tổng hợp: “DevOps on AWS”
## Mục tiêu Sự kiện
* Phân tích sự chuyển dịch từ thao tác thủ công (ClickOps) sang tự động hóa hạ tầng (IaC) để loại bỏ sai sót con người và sự thiếu nhất quán.
* Nắm vững cơ chế hoạt động của AWS CloudFormation trong việc định nghĩa và quản lý vòng đời tài nguyên đám mây .
* Làm chủ AWS CDK (Cloud Development Kit) để xây dựng hạ tầng bằng ngôn ngữ lập trình bậc cao thông qua các cấp độ Construct .
* Hiểu sâu về công nghệ Docker, quy trình đóng gói ứng dụng và quản lý image với Amazon ECR.
* So sánh và lựa chọn giải pháp điều phối Container phù hợp giữa Amazon ECS, Amazon EKS và AWS App Runner.
## Speakers
* **FCJ members**

## Điểm nhấn Chính
### Tư duy Hạ tầng & Quản trị Cấu hình

* Hạn chế của ClickOps: Thao tác trên giao diện điều khiển (Console) gây ra rủi ro cao về lỗi con người, tốc độ chậm và khó khăn trong cộng tác.
* CloudFormation Stack: Quản lý tập hợp các tài nguyên như một đơn vị duy nhất, cho phép tạo, cập nhật hoặc xóa toàn bộ hạ tầng một cách đồng bộ.
* Phát hiện sai lệch (Drift Detection): Cơ chế quan trọng giúp nhận diện khi cấu hình thực tế của tài nguyên bị thay đổi thủ công và không còn khớp với template định nghĩa ban đầu.
## Lập trình Hạ tầng với AWS CDK
* Đa ngôn ngữ: Hỗ trợ định nghĩa hạ tầng bằng TypeScript, JavaScript, Python, Java, C#/.NET và Go.
* Hệ thống Constructs (Cấu trúc):
  * L1 Constructs: Ánh xạ 1:1 với tài nguyên CloudFormation (Cfn), yêu cầu cấu hình chi tiết.
  * L2 Constructs: Cung cấp các thiết lập mặc định (defaults) và các phương thức hỗ trợ (helper methods) tối ưu.
  * L3 Constructs (Patterns): Các mẫu kiến trúc hoàn chỉnh, kết hợp nhiều tài nguyên để giải quyết một bài toán cụ thể.
* Quy trình làm việc (Workflow): Từ khởi tạo (cdk init), tổng hợp template (cdk synth), đến triển khai (cdk deploy) và hủy bỏ (cdk destroy).

### Hệ sinh thái Container & Điều phối

* Docker Fundamentals: Phân biệt Container (nhẹ, chia sẻ kernel) với Virtual Machine (nặng, có Guest OS) và quy trình Build - Push - Pull - Run.
* Amazon ECR: Kho lưu trữ container image bảo mật, hỗ trợ quét lỗ hổng (scanning) và các chính sách vòng đời (lifecycle policies).
* Các mô hình điều phối (Orchestration):
  * Amazon ECS: Giải pháp native của AWS, đơn giản, tích hợp sâu, hỗ trợ chạy trên EC2 hoặc Fargate (Serverless).
  * Amazon EKS: Dịch vụ Kubernetes được quản lý, cung cấp sự linh hoạt và chuẩn hóa mã nguồn mở nhưng phức tạp hơn trong vận hành.
  * AWS App Runner: Giải pháp PaaS giúp triển khai nhanh ứng dụng web trực tiếp từ mã nguồn hoặc image mà không cần quản lý hạ tầng .

## Bài học Chính 
### Chiến lược IaC

* Code thay vì Clicks: Chuyển đổi hoàn toàn sang mô hình "No More ClickOps" để đảm bảo tính nhất quán và khả năng mở rộng.
* Kiểm soát phiên bản: Sử dụng template (YAML/JSON) hoặc mã nguồn CDK đóng vai trò là bản thiết kế (blueprint) duy nhất cho hạ tầng.
* Quản lý sự thay đổi: Thường xuyên sử dụng cdk diff và Drift Detection để kiểm soát sự khác biệt giữa mã nguồn và thực tế trước khi triển khai.

### Kiến trúc Kỹ thuật
* Tính bất biến (Immutability): Docker Image và Container giúp đảm bảo ứng dụng chạy nhất quán trên mọi môi trường ("It works on my machine" -> "Ship your machine").
* Lựa chọn Compute: Sử dụng AWS Fargate để loại bỏ gánh nặng quản lý máy chủ (Serverless), hoặc EC2 khi cần kiểm soát sâu và tối ưu chi phí cho các tác vụ dài hạn.
* Phân cấp trừu tượng: Tận dụng L2/L3 Constructs trong CDK để giảm lượng code phải viết và thừa hưởng các best practices có sẵn.
  
## Ứng dụng vào project
* Triển khai App Runner: Sử dụng cho các ứng dụng web hoặc API cần triển khai nhanh (prototypes) mà không muốn quản lý server.
* Tối ưu hóa ECS: Áp dụng mô hình ECS kết hợp với Application Load Balancer (ALB) cho các kiến trúc microservices tiêu chuẩn như trong bài demo "Cats vs Dogs".
* Chuyển đổi sang CDK: Bắt đầu viết hạ tầng bằng TypeScript/Python thay vì CloudFormation thuần để tăng tốc độ phát triển và khả năng tái sử dụng mã.
## Trải nghiệm Sự kiện
Tham gia chuyên đề “AWS Mastery #2” đã cung cấp một góc nhìn sâu sắc về việc hiện đại hóa quy trình vận hành thông qua mã hóa hạ tầng và container. Những trải nghiệm thực tế bao gồm:
### Học hỏi từ chuyên gia
* Hiểu rõ sự khác biệt cốt lõi giữa Terraform (đa nền tảng, dùng HCL) và AWS CDK/CloudFormation (tối ưu cho AWS, dùng ngôn ngữ lập trình) để đưa ra lựa chọn công cụ phù hợp.
* Nắm bắt được cấu trúc cây (Construct Tree) của một ứng dụng CDK, từ App đến Stack và các Resources.
## Bài học rút ra
* Lựa chọn công cụ: ECS hoặc App Runner là lựa chọn tốt nhất cho các đội ngũ muốn giảm tải vận hành (lower ops overhead), trong khi EKS dành cho các yêu cầu phức tạp và tính di động cao (portability).
* Tự động hóa là bắt buộc: Việc tích hợp CI/CD với CodePipeline và CodeBuild là chìa khóa để duy trì sự ổn định khi triển khai các kiến trúc container phân tán.
* Tiêu chuẩn hóa: Sử dụng Dockerfile và ECR giúp chuẩn hóa môi trường runtime, loại bỏ hoàn toàn các lỗi do sự khác biệt môi trường gây ra.

