---
title: "Event CloudDay"
date: 2025-09-18


weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---


# Bài thu hoạch “Building a Unified Data Foundation on AWS for AI and Analytics Workloads”

### Mục Đích Của Sự Kiện

- Chia sẻ chiến lược và các phương pháp tối ưu (best practices) để xây dựng một nền tảng dữ liệu hợp nhất, có khả năng mở rộng.
- Tùy chỉnh hạ tầng dữ liệu để hỗ trợ các khối lượng công việc (workloads) về AI và phân tích.
- Tận dụng các dịch vụ của AWS để tạo ra một môi trường vững chắc cho các ứng dụng hiện đại.
- Bao quát các thành phần then chốt bao gồm: thu thập (ingestion), lưu trữ, xử lý và quản trị dữ liệu.
- Kích hoạt khả năng quản lý dữ liệu hiệu quả phục vụ cho các sáng kiến phân tích nâng cao và AI.

### Danh Sách Diễn Giả

- **Kien Nguyen** - Solutions Architect (Kiến trúc sư Giải pháp), AWS
  
### Nội Dung Nổi Bật

#### Sự trỗi dậy của Agentic AI

- Chuyển dịch từ Chatbot -> Hệ thống Agentic (tự chủ, đa tác nhân, mô phỏng logic con người).
- Dự báo đến năm 2028, 15% các quyết định công việc hàng ngày sẽ được thực hiện tự động bởi AI.

#### Amazon Bedrock AgentCore

- **Security** Triển khai các agent an toàn ở quy mô lớn với các kiểm soát cấp doanh nghiệp.
- **Capabilities** Tăng cường sức mạnh cho agent bằng các Công cụ (Tools/APIs) để thực hiện hành động và Bộ nhớ (Memory) để lưu giữ ngữ cảnh khách hàng.
- **Observability:** Tầm nhìn toàn diện để giám sát quá trình suy luận và hành động của agent.
  
#### Bài học Cốt lõi

#### Tư duy Chiến lược

- **Phương pháp 4 bước**: Xác định domain events → sắp xếp timeline → identify actors → xác định bounded contexts
- **Case study bookstore**: Minh họa cách áp dụng DDD thực tế
- **Context mapping**: 7 patterns tích hợp bounded contexts

#### Event-Driven Architecture

- **Tự chủ hơn là Tự động hóa**: Mục tiêu là xây dựng các hệ thống có thể độc lập đạt được mục tiêu, thay vì chỉ tự động hóa các tác vụ lặp lại đơn thuần.
- **Nhận thức Rủi ro**: Đổi mới sáng tạo phải đi đôi với các kiểm soát rủi ro và xác định rõ giá trị kinh doanh.

#### Kiến Trúc Kỹ Thuật

- **Vector Search (Tìm kiếm Vector)**: Là xương sống của bộ nhớ AI; thành phần thiết yếu cho các quy trình RAG (Retrieval-Augmented Generation)
- **Hệ thống Đa tác nhân (Multi-Agent Systems)**: Tương lai nằm ở sự phối hợp giữa các agent chuyên biệt (ví dụ: Agent Giám sát kết hợp với Agent trả lời câu hỏi thường gặp - FAQ).

### Ứng Dụng Vào Công Việc

- **Đánh giá độ sẵn sàng của Dữ liệu** Kiểm tra khả năng tương thích của các cơ sở dữ liệu hiện tại với Vector Search để hỗ trợ bộ nhớ cho AI
- **Xác định Kiểm soát Rủi ro**: Thiết lập các chính sách quản trị cho các câu lệnh (prompts) và phản hồi của AI trước khi mở rộng quy mô
- **Thử nghiệm Bedrock**: Bắt đầu thử nghiệm với AgentCore để xây dựng một bản mẫu (prototype) tích hợp các công cụ đơn giản.

### Trải nghiệm trong event

Tham gia workshop **“Building a Unified Data Foundation on AWS for AI and Analytics Workloads”** là một trải nghiệm rất bổ ích, giúp tôi có cái nhìn toàn diện về cách hiện đại hóa ứng dụng và cơ sở dữ liệu bằng các phương pháp và công cụ hiện đại. Một số trải nghiệm nổi bật:

#### Học hỏi từ thị trường
- Hiểu rõ **tính cấp thiết** của việc áp dụng công nghệ: Dự báo 33% phần mềm sẽ sử dụng Agentic AI vào năm 2028
- Nắm bắt lý do tại sao 40% các dự án có thể thất bại (do chi phí, kiểm soát rủi ro kém) và cách phòng tránh những cạm bẫy này.

#### Trực quan hóa kỹ thuật
- Hình dung được kiến trúc của **Hệ thống Agentic**: Cách các agent nhận thức, suy luận và hành động tự chủ.
- Thấy rõ mối liên kết trực tiếp giữa **Chiến lược Dữ liệu** (Cơ sở dữ liệu Vector) và **Năng lực của Agent** (Bộ nhớ).

