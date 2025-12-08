---
title: "Sự Kiện 5"
date: 2025-09-09
weight: 5
chapter: false
pre: " <b> 4.5. </b> "
---

# Báo Cáo Tóm Tắt: "DevOps trên AWS – AWS Cloud Mastery Series #2"

### Tổng Quan Sự Kiện

- **Tên Sự Kiện:** DevOps trên AWS – AWS Cloud Mastery Series #2  
- **Ngày:** 17 tháng 11, 2025  
- **Vai Trò:** Người tham dự  
- **Hình Thức:** Phiên kỹ thuật tại chỗ  
- **Thời Lượng:** Phiên trọn ngày
- **Địa Điểm:** Tầng 26, Tòa nhà Bitexco Financial Tower, Quận 1, Thành phố Hồ Chí Minh, Việt Nam

Phiên này là phần thứ hai của AWS Cloud Mastery Series, tập trung cụ thể vào các nguyên tắc và thực hành DevOps sử dụng dịch vụ AWS. Sự kiện bao gồm cách triển khai workflows DevOps hiện đại, tự động hóa giao phần mềm, và vận hành ứng dụng ở quy mô lớn trên AWS.

### Chương Trình Phiên

#### Giới Thiệu Nguyên Tắc DevOps
- **DevOps là gì?**: Hiểu phong trào văn hóa và kỹ thuật
- **Nguyên Tắc Cốt Lõi**:
  - Hợp tác giữa development và operations
  - Tự động hóa các quy trình thủ công
  - Continuous integration và continuous delivery (CI/CD)
  - Infrastructure as Code (IaC)
  - Monitoring và observability
  - Feedback loops và cải tiến liên tục

#### Infrastructure as Code (IaC)

##### AWS CloudFormation
- **Tổng Quan**: Dịch vụ IaC gốc của AWS
- **Cấu Trúc Template**: Hiểu JSON/YAML CloudFormation templates
- **Resources và Properties**: Định nghĩa AWS resources một cách khai báo
- **Parameters và Mappings**: Làm cho templates có thể tái sử dụng và linh hoạt
- **Outputs**: Expose các giá trị quan trọng từ stacks
- **Quản Lý Stack**: Tạo, cập nhật, và xóa stacks
- **Best Practices**:
  - Tổ chức và modularity của template
  - Version control cho templates
  - Stack policies và change sets
  - Drift detection

##### Terraform trên AWS
- **Tổng Quan Terraform**: Công cụ IaC mã nguồn mở
- **Terraform vs CloudFormation**: Hiểu sự khác biệt
- **Cú Pháp HCL**: Viết Terraform configuration files
- **Quản Lý State**: Hiểu Terraform state
- **Providers**: Sử dụng AWS provider
- **Modules**: Tạo các components infrastructure có thể tái sử dụng
- **Workspaces**: Quản lý nhiều môi trường
- **Best Practices**:
  - Remote state backends
  - Quản lý biến
  - Module design patterns

##### Patterns Infrastructure
- **Quản Lý Đa Môi Trường**: Dev, staging, production
- **Tham Số Hóa**: Làm cho infrastructure có thể cấu hình
- **Khả Năng Tái Sử Dụng**: Nguyên tắc DRY trong infrastructure code
- **Testing Infrastructure**: Xác thực thay đổi infrastructure

#### CI/CD Pipelines

##### AWS CodePipeline
- **Khái Niệm Pipeline**: Hiểu các stages và actions của pipeline
- **Source Stage**: Tích hợp với source control (GitHub, CodeCommit, S3)
- **Build Stage**: Biên dịch và đóng gói ứng dụng
- **Deploy Stage**: Triển khai đến các môi trường khác nhau
- **Approval Actions**: Cổng thủ công cho production deployments
- **Pipeline Triggers**: Tự động hóa thực thi pipeline
- **Pipeline Visualization**: Giám sát thực thi pipeline

##### AWS CodeBuild
- **Build Projects**: Định nghĩa cấu hình build
- **Buildspec Files**: Hướng dẫn build dựa trên YAML
- **Build Environments**: Chọn compute types và images
- **Artifacts**: Quản lý build outputs
- **Caching**: Tăng tốc builds với chiến lược caching
- **Environment Variables**: Quản lý secrets một cách an toàn
- **Build Logs**: Debug các builds thất bại

##### AWS CodeDeploy
- **Khái Niệm Deployment**: Hiểu các chiến lược deployment
- **In-Place Deployments**: Cập nhật các instances hiện có
- **Blue/Green Deployments**: Deployments không downtime
- **Rolling Deployments**: Cập nhật instances dần dần
- **Deployment Groups**: Tổ chức deployment targets
- **AppSpec Files**: Định nghĩa hướng dẫn deployment
- **Deployment Monitoring**: Theo dõi tiến trình deployment

##### Tích Hợp Với Các Dịch Vụ Khác
- **AWS CodeCommit**: Managed Git repositories
- **Tích Hợp GitHub**: Sử dụng GitHub làm source
- **S3 Artifacts**: Lưu trữ build artifacts
- **Lambda Deployments**: Triển khai serverless functions
- **ECS Deployments**: Chiến lược deployment container
- **EC2 Deployments**: Triển khai ứng dụng truyền thống

#### Chiến Lược Deployment Container

##### Amazon ECS Deployment
- **Cập Nhật ECS Service**: Rolling updates cho ECS services
- **Task Definitions**: Định nghĩa cấu hình container
- **Service Auto-scaling**: Tự động điều chỉnh capacity
- **Blue/Green với ECS**: Container deployments không downtime
- **Health Checks**: Đảm bảo độ tin cậy service
- **Load Balancing**: Phân phối traffic trên các tasks

##### Amazon EKS Deployment
- **Kubernetes trên AWS**: Dịch vụ Kubernetes được quản lý
- **Chiến Lược Deployment**: Rolling updates, canary, blue/green
- **Helm Charts**: Quản lý package cho Kubernetes
- **GitOps**: Sử dụng Git làm source of truth cho Kubernetes
- **CI/CD cho Kubernetes**: Tích hợp với CodePipeline

##### Container Best Practices
- **Quản Lý Image**: Chiến lược versioning và tagging
- **Security Scanning**: Quét container images cho vulnerabilities
- **Multi-stage Builds**: Tối ưu kích thước image
- **Quản Lý Registry**: Sử dụng Amazon ECR hiệu quả

#### Serverless Deployment

##### AWS Lambda Deployment
- **Triển Khai Function**: Triển khai Lambda functions
- **Versioning và Aliases**: Quản lý phiên bản function
- **Canary Deployments**: Rollout dần các cập nhật function
- **Lambda Layers**: Chia sẻ mã và dependencies
- **Environment Variables**: Quản lý cấu hình
- **Dead Letter Queues**: Xử lý lỗi

##### Serverless Application Model (SAM)
- **Tổng Quan SAM**: Framework cho ứng dụng serverless
- **SAM Templates**: Định nghĩa serverless resources
- **SAM CLI**: Phát triển và triển khai local
- **SAM Pipeline**: CI/CD cho ứng dụng SAM

##### API Gateway Deployment
- **API Versioning**: Quản lý phiên bản API
- **Quản Lý Stage**: Dev, staging, production stages
- **Canary Releases**: Testing phiên bản API mới
- **Throttling và Caching**: Tối ưu hiệu suất

#### Monitoring và Observability

##### Amazon CloudWatch
- **Metrics**: Thu thập và trực quan hóa metrics
- **Logs**: Quản lý log tập trung
- **Alarms**: Thiết lập cảnh báo tự động
- **Dashboards**: Tạo monitoring dashboards tùy chỉnh
- **Insights**: Phân tích dữ liệu log
- **Composite Alarms**: Logic cảnh báo phức tạp

##### AWS X-Ray
- **Distributed Tracing**: Hiểu request flows
- **Service Maps**: Trực quan hóa kiến trúc ứng dụng
- **Phân Tích Hiệu Suất**: Xác định bottlenecks
- **Error Tracking**: Tìm và sửa issues

##### Công Cụ Observability Bổ Sung
- **CloudWatch Synthetics**: Giám sát tính khả dụng ứng dụng
- **CloudWatch Contributor Insights**: Phân tích dữ liệu high-cardinality
- **CloudWatch Logs Insights**: Truy vấn dữ liệu log
- **Tích Hợp Bên Thứ Ba**: Datadog, New Relic, v.v.

#### Chủ Đề DevOps Nâng Cao

##### Testing Infrastructure
- **Unit Testing**: Testing infrastructure code
- **Integration Testing**: Xác thực thay đổi infrastructure
- **Compliance Testing**: Đảm bảo bảo mật và tuân thủ
- **Công Cụ**: Terratest, Pulumi Testing, v.v.

##### Bảo Mật Trong DevOps
- **Quản Lý Secrets**: AWS Secrets Manager
- **IAM Roles**: Truy cập least privilege
- **Security Scanning**: Kiểm tra bảo mật tự động
- **Tuân Thủ**: Đáp ứng yêu cầu quy định

##### Tối Ưu Chi Phí
- **Resource Tagging**: Theo dõi chi phí
- **Right-sizing**: Chọn instance types phù hợp
- **Reserved Instances**: Chiến lược tiết kiệm chi phí
- **Spot Instances**: Sử dụng Spot để tối ưu chi phí

##### Chiến Lược Đa Tài Khoản
- **AWS Organizations**: Quản lý nhiều tài khoản
- **Cấu Trúc Tài Khoản**: Tổ chức tài khoản theo môi trường/team
- **Cross-Account Deployments**: Triển khai qua các tài khoản
- **Centralized Logging**: Tập hợp logs từ nhiều tài khoản

### Kiến Thức Kỹ Thuật Quan Trọng

#### Văn Hóa và Thực Hành DevOps
- Hiểu DevOps vừa là sự thay đổi văn hóa vừa là một bộ thực hành kỹ thuật
- Tầm quan trọng của tự động hóa trong việc giảm lỗi thủ công và tăng tốc độ
- Cách feedback loops cho phép cải tiến liên tục

#### Infrastructure as Code
- IaC cho phép version control, khả năng lặp lại, và tính nhất quán
- Cả CloudFormation và Terraform đều có điểm mạnh riêng
- Infrastructure code modular, có thể tái sử dụng là cần thiết cho quy mô

#### Triển Khai CI/CD
- CI/CD pipelines tự động hóa quy trình giao phần mềm
- Các chiến lược deployment khác nhau phù hợp với các use case khác nhau
- Testing và validation nên được tích hợp vào pipelines

#### Monitoring và Observability
- Giám sát toàn diện là cần thiết để vận hành ứng dụng
- Logs, metrics, và traces cung cấp insights khác nhau nhưng bổ sung
- Giám sát chủ động giúp ngăn chặn issues trước khi chúng ảnh hưởng đến người dùng

### Bài Học Cá Nhân

#### Kỹ Năng Kỹ Thuật
- Tôi học được cách các thực hành DevOps và công cụ AWS phối hợp với nhau để tự động hóa vòng đời giao phần mềm
- Tôi hiểu cách thiết kế CI/CD pipelines cho các loại ứng dụng khác nhau
- Tôi có được kiến thức thực tế về nguyên tắc và công cụ Infrastructure as Code

#### Best Practices
- Tầm quan trọng của việc bắt đầu với tự động hóa đơn giản và dần tăng độ phức tạp
- Cách cân bằng tốc độ và an toàn trong quy trình deployment
- Giá trị của monitoring và observability toàn diện

#### Ứng Dụng Thực Tế
- Tôi có thể thiết kế CI/CD pipelines cho ứng dụng containerized và serverless
- Tôi hiểu cách sử dụng Infrastructure as Code để quản lý AWS resources
- Tôi biết cách triển khai monitoring và alerting cho ứng dụng

#### Phát Triển Sự Nghiệp
- Sự kiện này củng cố những gì tôi đã học trong các workshop khác về xây dựng và vận hành ứng dụng trên AWS
- Tôi thấy cách kỹ năng DevOps là cần thiết cho phát triển phần mềm hiện đại
- Tôi có động lực tiếp tục học về thực hành và công cụ DevOps nâng cao

### Trải Nghiệm Sự Kiện

Phiên này cung cấp tổng quan toàn diện về DevOps trên AWS, bao gồm mọi thứ từ khái niệm cơ bản đến thực hành nâng cao. Sự kết hợp giữa lý thuyết và examples thực tế làm cho các chủ đề phức tạp trở nên dễ tiếp cận.

Tập trung vào các tình huống thực tế và best practices đặc biệt có giá trị. Hiểu không chỉ cách sử dụng công cụ, mà còn khi nào và tại sao sử dụng chúng, giúp tôi phát triển quan điểm chiến lược hơn về DevOps.

Cấu trúc sự kiện cho phép bao phủ tốt cả khái niệm nền tảng và chủ đề nâng cao, làm cho nó có giá trị cho người tham dự ở các cấp độ kinh nghiệm khác nhau.

### Ảnh Sự Kiện

![Enter image alt description](/images/4-Event/event5_img1.jpg)
![Enter image alt description](/images/4-Event/event5_img2.jpg)
