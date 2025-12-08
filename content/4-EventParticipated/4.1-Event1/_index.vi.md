---
title: "Sự Kiện 1"
date: 2025-09-09
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

# Báo Cáo Tóm Tắt: "AWS Cloud Day Vietnam"

### Tổng Quan Sự Kiện

- **Tên Sự Kiện:** AWS Cloud Day Vietnam  
- **Ngày:** 18 tháng 9, 2025  
- **Vai Trò:** Người tham dự  
- **Hình Thức:** Hội nghị đa track, trực tiếp  
- **Địa Điểm:** Tầng 26, Tòa nhà Bitexco Financial Tower, Quận 1, Thành phố Hồ Chí Minh, Việt Nam

AWS Cloud Day Vietnam là một sự kiện trọn ngày toàn diện quy tụ các chuyên gia AWS, đối tác và khách hàng địa phương để chia sẻ best practices, câu chuyện migration thực tế, và những đổi mới mới nhất trong cloud computing. Sự kiện có nhiều track song song bao gồm nền tảng cloud, bảo mật, dữ liệu & phân tích, AI/ML, và các chiến lược hiện đại hóa trên AWS.

### Các Điểm Nổi Bật Trong Chương Trình

#### Bài Phát Biểu Khai Mạc
Sự kiện bắt đầu với một phiên keynote truyền cảm hứng bao gồm:
- Xu hướng áp dụng cloud và chuyển đổi số tại Việt Nam
- Hạ tầng toàn cầu của AWS và cách nó hỗ trợ doanh nghiệp trên toàn thế giới
- Câu chuyện thành công từ các doanh nghiệp Việt Nam đã chuyển đổi hoạt động của họ bằng AWS
- Tương lai của cloud computing và các công nghệ mới nổi

#### Track 1: Kiến Trúc Cloud-Native & Hiện Đại Hóa
Track này tập trung vào xây dựng ứng dụng có khả năng mở rộng và khả năng phục hồi trên AWS:
- **Thiết kế kiến trúc cloud-native**: Best practices để thiết kế ứng dụng tận dụng các dịch vụ được quản lý của AWS
- **Microservices và serverless patterns**: Khi nào và cách sử dụng containers (ECS, EKS) so với serverless (Lambda, Fargate)
- **Chiến lược hiện đại hóa ứng dụng**: Khung 7Rs (Rehost, Replatform, Refactor, Rearchitect, v.v.)
- **Tối ưu chi phí**: Right-sizing tài nguyên, sử dụng Reserved Instances, và triển khai auto-scaling

#### Track 2: Bảo Mật & Quản Trị
Đi sâu vào bảo mật môi trường AWS:
- **Chiến lược multi-account**: Sử dụng AWS Organizations để tách biệt môi trường (dev, staging, prod)
- **IAM best practices**: Truy cập least privilege, role-based access control, và permission boundaries
- **Security monitoring**: Sử dụng AWS Security Hub, GuardDuty, và CloudTrail để giám sát liên tục
- **Tuân thủ và quản trị**: Đáp ứng yêu cầu quy định và triển khai khung quản trị

#### Track 3: Dữ Liệu & Phân Tích
Xây dựng data lakes và giải pháp phân tích:
- **Kiến trúc data lake**: Sử dụng Amazon S3 làm nền tảng cho data lakes
- **ETL và xử lý dữ liệu**: AWS Glue cho ETL serverless, Amazon Athena cho truy vấn tương tác
- **Data warehousing**: Amazon Redshift cho analytics workloads
- **Real-time analytics**: Amazon Kinesis cho xử lý streaming data
- **Trực quan hóa dữ liệu**: Xây dựng dashboards và báo cáo

#### Track 4: AI/ML trên AWS
Triển khai AI/ML thực tế:
- **Amazon SageMaker**: Quy trình ML end-to-end từ chuẩn bị dữ liệu đến triển khai model
- **Amazon Bedrock**: Sử dụng foundation models cho ứng dụng generative AI
- **Dịch vụ AI**: Các dịch vụ AI được xây dựng sẵn như Rekognition, Comprehend, và Translate
- **MLOps**: Vận hành hóa các mô hình machine learning trong production

#### Nghiên Cứu Tình Huống Khách Hàng
Một số công ty Việt Nam đã chia sẻ hành trình AWS của họ:
- Các nền tảng thương mại điện tử đã mở rộng quy mô trong mùa cao điểm
- Các công ty dịch vụ tài chính đã cải thiện bảo mật và tuân thủ
- Các startup đã tăng tốc time-to-market bằng kiến trúc serverless
- Các doanh nghiệp đã giảm chi phí trong khi cải thiện hiệu suất

### Kiến Thức Kỹ Thuật Quan Trọng

#### Các Pattern Kiến Trúc
- **Well-Architected Framework**: Hiểu năm trụ cột (Operational Excellence, Security, Reliability, Performance Efficiency, Cost Optimization)
- **Kiến trúc đa tầng**: Web, application, và database tiers với sự tách biệt phù hợp
- **High availability**: Thiết kế cho 99.99% uptime sử dụng nhiều Availability Zones
- **Disaster recovery**: Chiến lược backup và lập kế hoạch disaster recovery

#### Security Best Practices
- **Defense in depth**: Cách tiếp cận bảo mật phân lớp sử dụng nhiều dịch vụ bảo mật AWS
- **Network security**: Thiết kế VPC, security groups, NACLs, và AWS WAF
- **Mã hóa dữ liệu**: Mã hóa at rest và in transit sử dụng AWS KMS
- **Quản lý danh tính**: SSO, MFA, và chiến lược credential rotation

#### Insights Dữ Liệu & Phân Tích
- **Data lake vs data warehouse**: Khi nào sử dụng mỗi cách tiếp cận
- **Schema-on-read**: Lợi ích của việc lưu trữ dữ liệu ở định dạng thô và áp dụng schema khi truy vấn
- **Phân tích hiệu quả về chi phí**: Sử dụng đúng dịch vụ cho đúng workload (Athena cho truy vấn ad-hoc, Redshift cho phân tích phức tạp)
- **Quản trị dữ liệu**: Triển khai chất lượng dữ liệu, cataloging, và access controls

#### Kiến Thức Thực Tế AI/ML
- **Managed vs custom models**: Khi nào sử dụng dịch vụ AI được xây dựng sẵn so với xây dựng custom models
- **Model training**: Sử dụng SageMaker cho distributed training và hyperparameter tuning
- **Model deployment**: Các pattern inference real-time và batch
- **Tối ưu chi phí**: Sử dụng Spot Instances cho training và right-sizing inference endpoints

### Bài Học Cá Nhân

#### Phát Triển Kỹ Thuật
- Tôi có được hiểu biết toàn diện về cách các dịch vụ AWS khác nhau hoạt động cùng nhau trong các tình huống thực tế, không chỉ riêng lẻ
- Sự kiện giúp tôi kết nối kiến thức lý thuyết từ thực tập với ứng dụng kinh doanh thực tế
- Tôi học được về các pattern kiến trúc và best practices mà tôi có thể áp dụng cho các dự án tương lai

#### Insights Ngành
- Hiểu cách các công ty Việt Nam đang áp dụng công nghệ cloud và những thách thức họ phải đối mặt
- Tìm hiểu về hệ sinh thái cloud tại Việt Nam, bao gồm các đối tác AWS và nhà cung cấp dịch vụ
- Có được insights về con đường sự nghiệp trong cloud computing, từ solutions architect đến DevOps engineer đến data engineer

#### Networking & Cộng Đồng
- Kết nối với các chuyên gia AWS, solution architects, và các chuyên gia khác trong lĩnh vực cloud
- Thảo luận về các thách thức kỹ thuật và giải pháp với các đồng nghiệp đang làm việc trên các dự án tương tự
- Xây dựng các mối quan hệ có thể có giá trị cho hợp tác và học tập trong tương lai

#### Ứng Dụng Thực Tế
- Tôi có thể thiết kế kiến trúc tốt hơn tuân theo AWS best practices
- Tôi hiểu cách cân bằng chi phí, hiệu suất và bảo mật trong các tình huống thực tế
- Tôi có bức tranh rõ ràng hơn về dịch vụ AWS nào sử dụng cho các use case khác nhau

### Trải Nghiệm Sự Kiện

Tham dự AWS Cloud Day Vietnam là một trải nghiệm phong phú cung cấp cả chiều sâu kỹ thuật và insights chiến lược. Sự kết hợp giữa các phiên do chuyên gia dẫn dắt, câu chuyện khách hàng thực tế, và các demo thực hành đã cho tôi cái nhìn toàn diện về cách AWS đang chuyển đổi doanh nghiệp tại Việt Nam.

Sự kiện củng cố sự quan tâm của tôi về cloud computing và AI/ML, và cho tôi tự tin rằng các kỹ năng tôi đang phát triển trong thời gian thực tập phù hợp với nhu cầu ngành. Cơ hội networking đặc biệt có giá trị, vì tôi có thể học hỏi từ các chuyên gia có kinh nghiệm và hiểu các quan điểm khác nhau về việc áp dụng cloud.

### Ảnh Sự Kiện

![Enter image alt description](/images/4-Event/event1_img1.jpg)
![Enter image alt description](/images/4-Event/event1_img2.jpeg)
