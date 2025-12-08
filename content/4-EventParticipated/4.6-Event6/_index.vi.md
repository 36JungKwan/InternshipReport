---
title: "Sự Kiện 6"
date: 2025-09-09
weight: 6
chapter: false
pre: " <b> 4.6. </b> "
---

# Báo Cáo Tóm Tắt: "Workshop Trụ Cột Bảo Mật AWS Well-Architected"

### Tổng Quan Sự Kiện

- **Tên Sự Kiện:** AWS Well-Architected Security Pillar Workshop  
- **Ngày:** 29 tháng 11, 2025  
- **Vai Trò:** Người tham dự  
- **Hình Thức:** Workshop tại chỗ  
- **Thời Lượng:** Workshop trọn ngày (9:15 AM – 11:50 AM+)
- **Địa Điểm:** Tầng 26, Tòa nhà Bitexco Financial Tower, Quận 1, Thành phố Hồ Chí Minh, Việt Nam

Workshop toàn diện này tập trung độc quyền vào trụ cột Security của AWS Well-Architected Framework. Sự kiện cung cấp coverage kỹ thuật sâu về security best practices, công cụ, và patterns để xây dựng các workloads an toàn trên AWS. Mỗi phiên xây dựng dựa trên các khái niệm trước đó, tạo ra bức tranh hoàn chỉnh về bảo mật AWS.

### Chương Trình Workshop

#### Phiên 1: Identity & Access Management (9:15 – 9:45 AM)
**Diễn Giả:** Huynh Hoang Long, Dinh Le Hoang Anh

##### Nền Tảng IAM
- **IAM là gì?**: Hiểu Identity và Access Management
- **IAM Quản Lý**:
  - Users: Tài khoản cá nhân cho người và ứng dụng
  - Groups: Tập hợp users với permissions được chia sẻ
  - Roles: Credentials tạm thời cho services và users
  - Policies: Documents định nghĩa permissions
- **IAM Đảm Bảo**:
  - Authentication: Xác minh danh tính
  - Authorization: Kiểm soát truy cập tài nguyên
  - Auditability: Theo dõi ai đã làm gì và khi nào

##### IAM Best Practices

**Nguyên Tắc Least Privilege**
- Chỉ cấp permissions tối thiểu cần thiết
- Bắt đầu với không có permissions và chỉ thêm những gì cần
- Review và loại bỏ permissions không cần thiết thường xuyên
- Sử dụng IAM Access Analyzer để xác định policies quá permissive

**Bảo Mật Tài Khoản Root**
- **Không bao giờ sử dụng root access keys**: Root credentials cung cấp truy cập không giới hạn
- **Xóa root access keys**: Loại bỏ bất kỳ root access keys hiện có nào
- **Bật MFA cho root**: Multi-factor authentication như một lớp bảo mật bổ sung
- **Chỉ sử dụng root cho quản lý tài khoản**: Giới hạn sử dụng root cho các tác vụ cần thiết

**Quản Lý Policy**
- **Sử dụng managed policies**: Tận dụng AWS-managed policies khi có thể
- **Tạo custom policies**: Khi AWS-managed policies không phù hợp
- **Tránh wildcards ("*")**: Cụ thể về các actions và resources được phép
- **Policy versioning**: Quản lý thay đổi policy theo thời gian
- **Policy testing**: Sử dụng IAM policy simulator

**Truy Cập Dựa Trên Role**
- **Sử dụng roles thay vì users cho ứng dụng**: Roles cung cấp credentials tạm thời
- **Assume roles**: Sử dụng role assumption cho cross-account và service access
- **Role chaining**: Hiểu giới hạn role assumption
- **Session duration**: Thiết lập session timeouts phù hợp

**Best Practices Đăng Nhập AWS**
- **Sử dụng AWS SSO hoặc IAM Identity Center**: Quản lý danh tính tập trung
- **Tránh long-lived access keys**: Ưu tiên credentials tạm thời
- **Rotate credentials thường xuyên**: Thay đổi access keys định kỳ
- **Sử dụng AWS CLI với profiles**: Quản lý nhiều credentials một cách an toàn

**Multi-Factor Authentication (MFA)**
- **MFA cho tất cả users**: Yêu cầu MFA cho human users
- **TOTP (Time-based One-Time Password)**: Sử dụng authenticator apps
- **FIDO2**: Hardware security keys cho xác thực mạnh hơn
- **MFA cho root**: Quan trọng cho bảo vệ root account
- **MFA cho operations đặc quyền**: Yêu cầu MFA cho các actions nhạy cảm

**Credential Rotation**
- **Rotation thường xuyên**: Thay đổi credentials theo lịch trình
- **AWS Secrets Manager**: Rotation tự động cho database credentials, API keys, v.v.
- **Chiến lược rotation**: Các cách tiếp cận khác nhau cho các loại credentials khác nhau
- **Giám sát rotation**: Đảm bảo rotation xảy ra thành công

##### Single Sign-On (SSO) / IAM Identity Center

**Khái Niệm SSO**
- **Single sign-on**: Đăng nhập một lần để truy cập nhiều services
- **Quản lý danh tính tập trung**: Một nơi để quản lý tất cả identities
- **Tích hợp đa tài khoản**: Sử dụng SSO trên AWS Organizations
- **Nhiều roles**: Users có thể có roles khác nhau cho các accounts khác nhau

**Tính Năng IAM Identity Center**
- **Quản lý user và group**: Quản trị user tập trung
- **Gán ứng dụng**: Gán truy cập cho AWS và ứng dụng bên thứ ba
- **Permission sets**: Tập hợp permissions có thể tái sử dụng
- **Quản lý session**: Kiểm soát thời lượng session và policies

**Tích Hợp AWS Organizations**
- **SSO toàn tổ chức**: SSO hoạt động trên tất cả accounts trong một organization
- **Quản lý tài khoản**: Đơn giản hóa truy cập vào nhiều accounts
- **Quản trị tập trung**: Quản lý truy cập từ một nơi

##### Service Control Policies (SCPs)

**Tổng Quan SCP**
- **Maximum permissions**: Thiết lập maximum permissions cho accounts trong một organization
- **Không cấp permissions**: SCPs lọc permissions nhưng không cấp chúng
- **Deny by default**: Hiểu cách SCPs hoạt động với logic allow/deny
- **Kiểm soát cấp tổ chức**: Áp dụng policies ở cấp organization

**Use Cases SCP**
- **Ngăn chặn các actions nhất định**: Chặn các operations rủi ro trên tất cả accounts
- **Thực thi tuân thủ**: Đảm bảo tất cả accounts đáp ứng yêu cầu tuân thủ
- **Kiểm soát chi phí**: Ngăn chặn các operations đắt đỏ
- **Security guardrails**: Thực thi security policies toàn tổ chức

##### Permission Boundaries

**Khái Niệm Permission Boundary**
- **Maximum permissions cho policies**: Thiết lập giới hạn về những gì policies có thể cấp
- **Áp dụng cho roles hoặc users**: Sử dụng permission boundaries để hạn chế truy cập
- **Không cấp permissions**: Giống như SCPs, chúng lọc thay vì cấp
- **Kiểm soát chi tiết**: Chi tiết hơn SCPs

**Use Cases**
- **Ủy quyền tạo policy**: Cho phép teams tạo policies trong giới hạn
- **Ngăn chặn privilege escalation**: Đảm bảo users không thể tự cấp thêm truy cập
- **Tuân thủ**: Đáp ứng yêu cầu quy định cho kiểm soát truy cập

##### Mối Quan Hệ Giữa IAM, SCPs, và Permission Boundaries
- **IAM Policies**: Cấp permissions cho users, groups, và roles
- **Permission Boundaries**: Giới hạn những gì IAM policies có thể cấp
- **SCPs**: Giới hạn những gì có thể ở cấp organization
- **Thứ tự đánh giá**: Hiểu cách chúng hoạt động cùng nhau
- **Effective permissions**: Tính toán những gì user thực sự có thể làm

##### Phổ Credentials

**Credentials Dài Hạn**
- **IAM user access keys**: Credentials vĩnh viễn không có expiration
- **Rủi ro**: Nếu bị xâm phạm, vẫn hợp lệ cho đến khi được rotate thủ công
- **Use cases**: Các tình huống hạn chế nơi credentials dài hạn là cần thiết
- **Best practice**: Tránh khi có thể

**Credentials Ngắn Hạn**
- **AWS Security Token Service (STS)**: Credentials tạm thời
- **Lợi ích**: Expiration tự động, giảm rủi ro nếu bị xâm phạm
- **Session tokens**: Truy cập giới hạn thời gian
- **Best practice**: Sử dụng credentials ngắn hạn bất cứ khi nào có thể

##### IAM Access Analyzer
- **Phát hiện lỗ hổng bảo mật**: Xác định các vấn đề bảo mật dựa trên logic
- **Phân tích truy cập bên ngoài**: Tìm resources có thể truy cập từ bên ngoài tài khoản của bạn
- **Phân tích policy**: Xác định các policies quá permissive
- **Giám sát liên tục**: Phân tích liên tục cấu hình IAM của bạn

#### Phiên 2: Detection & Continuous Monitoring (9:50 – 10:20 AM)
**Diễn Giả:** Tran Duc Anh, Nguyen Tuan Thinh, Nguyen Do Thanh Dat

##### AWS CloudTrail

**Tầm Nhìn Bảo Mật Đa Lớp**
- **Ghi log API calls**: Ghi lại tất cả API calls được thực hiện trong tài khoản AWS của bạn
- **Ai, cái gì, khi nào, ở đâu**: Audit trail toàn diện
- **Management events**: Các actions quản trị
- **Data events**: Các operations cấp resource (truy cập S3 object, Lambda invocation)
- **CloudTrail logs**: Được lưu trong S3 với integrity validation

**Cảnh Báo & Tự Động Hóa với EventBridge**
- **Tích hợp EventBridge**: Tự động phản hồi các events CloudTrail
- **Tạo rules**: Định nghĩa patterns để khớp
- **Target actions**: Kích hoạt phản hồi (Lambda, SNS, v.v.)
- **Giám sát real-time**: Thông báo ngay lập tức về security events
- **Remediation tự động**: Tự động sửa các issues

**Detection as Code**
- **Infrastructure as Code cho monitoring**: Định nghĩa detection rules trong code
- **Version control**: Theo dõi thay đổi detection logic
- **Reproducibility**: Detection nhất quán trên các môi trường
- **Testing**: Xác thực detection rules trước khi triển khai

##### Amazon GuardDuty

**Điểm Đau Kinh Doanh**
- **Phát hiện mối đe dọa**: Xác định hoạt động độc hại và hành vi trái phép
- **Quy mô**: Giám sát lượng dữ liệu lớn
- **Chuyên môn**: Yêu cầu chuyên môn bảo mật để xác định mối đe dọa
- **False positives**: Giảm tiếng ồn từ các hoạt động hợp pháp

**Tổng Quan GuardDuty**
- **Managed threat detection**: Giám sát liên tục cho hoạt động độc hại
- **Machine learning**: Sử dụng ML để xác định mối đe dọa
- **Threat intelligence**: Tận dụng AWS và threat feeds bên thứ ba
- **Không quản lý infrastructure**: Dịch vụ được quản lý hoàn toàn

**Nguồn Dữ Liệu**
- **VPC Flow Logs**: Phân tích network traffic
- **CloudTrail event logs**: Phân tích API calls
- **DNS logs**: Phân tích domain name resolution
- **Malware protection**: Bảo vệ runtime EKS
- **S3 protection**: Phát hiện mối đe dọa cấp object

**GuardDuty Giám Sát**
- **API calls trái phép**: Hoạt động API đáng ngờ
- **Instances bị xâm phạm**: EC2 instances giao tiếp với IPs độc hại
- **Account bị xâm phạm**: Hoạt động tài khoản bất thường
- **Instance bị xâm phạm**: Malware và hành vi đáng ngờ
- **Mối đe dọa container**: Các vấn đề bảo mật EKS cluster

**Kế Hoạch Bảo Vệ Nâng Cao**
- **S3 Protection**: Giám sát S3 data events cho mối đe dọa
- **Kubernetes Protection**: Phát hiện mối đe dọa runtime EKS
- **Malware Protection**: Quét EC2 và ECS workloads
- **RDS Protection**: Phát hiện mối đe dọa database
- **Lambda Protection**: Giám sát serverless function

**GuardDuty Agent**
- **Bảo vệ on-premises**: Mở rộng GuardDuty đến môi trường on-premises
- **Triển khai agent**: Cài đặt agents trên servers
- **Phát hiện mối đe dọa**: Giám sát workloads on-premises
- **Góc nhìn thống nhất**: Single pane of glass cho cloud và on-premises

**GuardDuty Cảnh Báo & Tự Động Hóa với EventBridge**
- **Thông báo findings**: Cảnh báo về security findings
- **Mức độ nghiêm trọng**: Critical, high, medium, low
- **Phản hồi tự động**: Kích hoạt remediation workflows
- **Tích hợp**: Làm việc với các dịch vụ AWS khác

**GuardDuty Detection as Code**
- **Detection rules dựa trên code**: Định nghĩa detection logic tùy chỉnh
- **Suppression rules**: Lọc false positives
- **Version control**: Quản lý detection rules trong Git
- **Testing**: Xác thực detection rules

##### AWS Security Hub

**CSPM (Cloud Security Posture Management)**
- **Đánh giá security posture**: Đánh giá security posture tổng thể
- **Kiểm tra tuân thủ**: Xác minh tuân thủ với các tiêu chuẩn
- **Inventory tài nguyên**: Hiểu những gì bạn có
- **Đánh giá rủi ro**: Xác định rủi ro bảo mật

**Cảnh Báo Tập Trung & Chuẩn Hóa**
- **ASFF (AWS Security Finding Format)**: Định dạng finding chuẩn hóa
- **Tập hợp**: Thu thập findings từ nhiều nguồn
- **Chuẩn hóa**: Chuyển đổi findings sang định dạng chung
- **Deduplication**: Loại bỏ findings trùng lặp
- **Ưu tiên hóa**: Xếp hạng findings theo mức độ nghiêm trọng

**Tính Năng Security Hub**
- **Kiểm tra bảo mật tự động**: Giám sát tuân thủ liên tục
- **Security insights**: Hiểu xu hướng bảo mật
- **Custom insights**: Tạo phân tích tùy chỉnh
- **Tích hợp**: Làm việc với công cụ bảo mật đối tác
- **Remediation**: Tùy chọn remediation tự động và thủ công

**Tiêu Chuẩn Tuân Thủ**
- **AWS Foundational Security Best Practices**: Thực hành bảo mật được AWS khuyến nghị
- **CIS AWS Foundations Benchmark**: Security controls tiêu chuẩn ngành
- **PCI DSS**: Tuân thủ ngành thẻ thanh toán
- **Custom frameworks**: Định nghĩa tiêu chuẩn tuân thủ của riêng bạn

**Detection as Code**
- **Tuân thủ dựa trên code**: Định nghĩa compliance rules trong code
- **Custom insights**: Tạo phân tích bảo mật tùy chỉnh
- **Tự động hóa**: Tự động hóa kiểm tra tuân thủ
- **Báo cáo**: Tạo compliance reports

#### Phiên 3: Network & Workload Security (10:30 – 11:10 AM)
**Diễn Giả:** Nguyen Van Hoang Kha

##### Nền Tảng Network Security

**Luồng Traffic Tốt**
- **Hiểu patterns traffic bình thường**: Baseline để phát hiện bất thường
- **East-west traffic**: Traffic trong network
- **North-south traffic**: Traffic vào/ra network
- **Phân đoạn traffic**: Cô lập các loại traffic khác nhau

**Vectơ Tấn Công Network**
- **Tấn công DDoS**: Distributed denial of service
- **Man-in-the-middle**: Chặn giao tiếp
- **Port scanning**: Thăm dò các cổng mở
- **Tấn công DNS**: DNS spoofing và hijacking
- **Rò rỉ dữ liệu**: Loại bỏ dữ liệu trái phép

**Giải Phẫu Một Exploit - Mélofee**
- **Nghiên cứu tình huống**: Phân tích tấn công thực tế
- **Tiến trình tấn công**: Cách các cuộc tấn công diễn ra
- **Khai thác lỗ hổng**: Hiểu kỹ thuật exploit
- **Chiến lược phòng thủ**: Cách ngăn chặn các cuộc tấn công tương tự

**Use Cases Bảo Vệ Network**
- **Bảo vệ inbound**: Bảo vệ chống lại mối đe dọa bên ngoài
- **Bảo vệ outbound**: Ngăn chặn rò rỉ dữ liệu
- **Bảo vệ east-west**: Bảo mật traffic nội bộ
- **Bảo vệ kết hợp**: Cách tiếp cận bảo mật phân lớp

##### Bảo Mật Phân Lớp AWS

**AWS Firewall Manager**
- **Quản lý firewall tập trung**: Quản lý firewalls trên các accounts
- **Thực thi policy**: Đảm bảo security policies nhất quán
- **Tuân thủ**: Đáp ứng yêu cầu bảo mật toàn tổ chức

**AWS Network Firewall**
- **Managed network firewall**: Firewall kiểm tra stateful
- **Lọc traffic**: Kiểm soát network traffic
- **Ngăn chặn xâm nhập**: Phát hiện và chặn mối đe dọa
- **Tích hợp**: Làm việc với VPCs và Transit Gateway

**DNS Firewall**
- **Route 53 Resolver DNS Firewall**: Lọc DNS queries
- **Lọc domain**: Chặn các domains độc hại
- **Threat intelligence**: Sử dụng threat feeds
- **Ghi log**: Theo dõi DNS queries

**AWS WAF**
- **Web Application Firewall**: Bảo vệ web applications
- **Lọc dựa trên rules**: Custom và managed rules
- **Giới hạn tốc độ**: Ngăn chặn lạm dụng
- **Bảo vệ bot**: Chặn bots độc hại

**VPC Flow Logs**
- **Ghi log network traffic**: Ghi lại network flows
- **Phân tích traffic**: Hiểu hành vi network
- **Giám sát bảo mật**: Phát hiện traffic đáng ngờ
- **Troubleshooting**: Chẩn đoán network issues

**Traffic Mirroring**
- **Sao chép network traffic**: Để phân tích và giám sát
- **Công cụ bảo mật**: Cung cấp traffic cho security appliances
- **Tuân thủ**: Đáp ứng yêu cầu giám sát

##### VPC Security Groups

**Cơ Bản Security Group**
- **Firewall cấp instance**: Kiểm soát traffic đến EC2 instances
- **Firewall stateful**: Tự động cho phép return traffic
- **Deny mặc định**: Chỉ traffic được phép rõ ràng mới được phép
- **Chỉ rules allow**: Không thể tạo explicit deny rules

**Security Group Best Practices**
- **Least privilege**: Chỉ cho phép traffic cần thiết
- **Ports và protocols cụ thể**: Cụ thể về traffic được phép
- **Hạn chế nguồn**: Giới hạn source IPs khi có thể
- **Review thường xuyên**: Kiểm tra security group rules

**VPC Peering & Transit Gateway**
- **VPC peering**: Kết nối VPCs một cách an toàn
- **Transit Gateway**: Hub network tập trung
- **Quản lý route**: Kiểm soát traffic routing
- **Cân nhắc bảo mật**: Bảo mật inter-VPC traffic

**Chia Sẻ Security Group**
- **Chia sẻ cross-account**: Chia sẻ security groups trên các accounts
- **Use cases**: Quản lý security group tập trung
- **Best practices**: Khi nào và cách chia sẻ security groups

**Tham Chiếu Security Group**
- **Tham chiếu security groups khác**: Cho phép traffic từ các security groups cụ thể
- **Rules động**: Rules thích ứng với membership group
- **Use cases**: Đơn giản hóa quản lý security group

##### Network ACLs (NACLs)

**Cơ Bản NACL**
- **Firewall cấp subnet**: Kiểm soát traffic ở cấp subnet
- **Stateless**: Phải cho phép return traffic một cách rõ ràng
- **Allow và deny rules**: Có thể tạo cả allow và deny rules
- **Đánh giá rules**: Rules được đánh giá theo thứ tự

**NACL vs Security Groups**
- **Khi nào sử dụng NACLs**: Kiểm soát cấp subnet
- **Khi nào sử dụng Security Groups**: Kiểm soát cấp instance
- **Sử dụng kết hợp**: Sử dụng cả hai cho defense in depth

**Security Groups & NACLs Chống Vectơ Tấn Công**
- **Bảo vệ DDoS**: Giới hạn tốc độ và lọc
- **Port scanning**: Chặn các cổng không cần thiết
- **Rò rỉ dữ liệu**: Giám sát và chặn outbound traffic
- **Phòng thủ phân lớp**: Nhiều lớp bảo vệ

##### Route 53 VPC DNS Resolver

**Phân Giải DNS**
- **Private DNS**: Phân giải DNS queries trong VPC
- **Lọc DNS**: Chặn các domains độc hại
- **Ghi log DNS**: Theo dõi DNS queries
- **Hybrid DNS**: Phân giải on-premises và cloud resources

##### Tính Năng Route 53 DNS Firewall

**Khả Năng DNS Firewall**
- **Lọc domain**: Chặn truy cập vào các domains độc hại
- **Threat intelligence**: Sử dụng AWS và custom threat lists
- **Custom rules**: Tạo domain allow/deny lists
- **Ghi log**: Ghi lại DNS queries để phân tích

**SG, NACL, DNS Firewall Chống Vectơ Tấn Công**
- **Bảo vệ toàn diện**: Nhiều lớp bảo mật network
- **Ngăn chặn tấn công**: Chặn tấn công trước khi chúng đến resources
- **Tầm nhìn**: Hiểu patterns network traffic

##### Inter-VPC và On-Premises qua Transit Gateway

**Transit Gateway**
- **Kết nối tập trung**: Hub cho VPC và on-premises connectivity
- **Quản lý route**: Kiểm soát traffic routing
- **Bảo mật**: Áp dụng security policies tại transit gateway
- **Khả năng mở rộng**: Hỗ trợ networks quy mô lớn

##### AWS Network Firewall

**Hành Vi Firewall**
- **Kiểm tra stateful**: Hiểu connection state
- **Lọc traffic**: Cho phép hoặc từ chối traffic dựa trên rules
- **Ngăn chặn xâm nhập**: Phát hiện và chặn mối đe dọa
- **Kiểm tra SSL/TLS**: Giải mã và kiểm tra encrypted traffic

**Rules Network Firewall**
- **Stateless rules**: Allow/deny đơn giản dựa trên header fields
- **Stateful rules**: Hiểu connection context
- **Rule groups**: Tổ chức và tái sử dụng rules
- **Suricata rules**: Sử dụng rules tương thích Suricata

**Nhiều VPC Endpoints**
- **Tích hợp VPC endpoint**: Làm việc với VPC endpoints
- **Kiểm tra traffic**: Kiểm tra traffic đến dịch vụ AWS
- **Bảo mật**: Đảm bảo truy cập an toàn đến dịch vụ AWS

**Danh Sách Domain Tự Động**
- **Threat intelligence feeds**: Tự động cập nhật threat lists
- **Custom lists**: Thêm domain lists của riêng bạn
- **Bảo trì**: Giảm quản lý list thủ công

**Tích Hợp Transit Gateway Gốc**
- **Tích hợp liền mạch**: Làm việc trực tiếp với Transit Gateway
- **Route propagation**: Quản lý route tự động
- **Khả năng mở rộng**: Xử lý deployments quy mô lớn

**Bảo Mật Đa Lớp Chống Vectơ Tấn Công**
- **Defense in depth**: Nhiều lớp bảo mật
- **Bảo vệ toàn diện**: Bao phủ tất cả vectơ tấn công
- **Tầm nhìn**: Hiểu mối đe dọa trên các lớp

#### Phiên 4: AWS Data Protection (11:15 – 11:45 AM)
**Diễn Giả:** Thinh Lam, Viet Nguyen

##### AWS Key Management Service (KMS)

**Workflow KMS**
- **Tạo key**: Tạo và quản lý encryption keys
- **Sử dụng key**: Sử dụng keys để mã hóa và giải mã dữ liệu
- **Rotation key**: Tự động rotate keys
- **Kiểm soát truy cập**: Kiểm soát ai có thể sử dụng keys

**Policies KMS**
- **Key policies**: Định nghĩa ai có thể sử dụng keys
- **IAM policies**: Kiểm soát truy cập bổ sung
- **Best practices**: Quản lý key an toàn

**Tính Năng KMS**

**Customer Master Keys (CMKs)**
- **Symmetric keys**: Mã hóa AES-256
- **Asymmetric keys**: RSA và ECC keys
- **Key material**: AWS-managed vs customer-managed
- **Key aliases**: Tên key dễ đọc

**Quản Lý Key**
- **Rotation key**: Rotation tự động và thủ công
- **Xóa key**: Xóa key an toàn
- **Import key**: Mang keys của riêng bạn
- **Multi-Region keys**: Replicate keys qua các regions

##### Phân Loại Dữ Liệu

**Phân Loại Với Dịch Vụ ML**
- **Phân loại tự động**: Sử dụng ML để phân loại dữ liệu
- **Mức độ nhạy cảm**: Xác định độ nhạy cảm dữ liệu
- **Tuân thủ**: Đáp ứng yêu cầu phân loại dữ liệu
- **Tagging**: Áp dụng classification tags

##### Guardrails Truy Cập
- **Kiểm soát truy cập**: Đảm bảo chỉ truy cập được ủy quyền
- **Audit trails**: Theo dõi truy cập dữ liệu
- **Tuân thủ**: Đáp ứng yêu cầu quy định

##### Mã Hóa Trong Quá Trình Truyền

**Dịch Vụ Dựa Trên API (S3 & DynamoDB)**
- **TLS/SSL**: Mã hóa dữ liệu trong quá trình truyền
- **HTTPS**: Giao tiếp API an toàn
- **Mã hóa phía client**: Mã hóa trước khi truyền

**Dịch Vụ Database (Amazon RDS)**
- **Kết nối TLS**: Mã hóa kết nối database
- **SSL certificates**: Quản lý SSL certificates
- **Kết nối được mã hóa**: Đảm bảo tất cả kết nối được mã hóa

**Lớp Infrastructure (EBS & Nitro)**
- **Mã hóa EBS**: Mã hóa EBS volumes
- **Hệ thống Nitro**: Mã hóa dựa trên phần cứng
- **Hiệu suất**: Mã hóa không ảnh hưởng hiệu suất

**Quản Lý Secrets - ACM**
- **AWS Certificate Manager**: Quản lý SSL/TLS certificates
- **Tự động hóa certificate**: Renewal certificate tự động
- **Private CA**: Tạo private certificate authorities

##### AWS Secrets Manager & Rotation

**Tổng Quan Secrets Manager**
- **Secrets tập trung**: Lưu trữ secrets một cách an toàn
- **Rotation tự động**: Tự động rotate secrets
- **Kiểm soát truy cập**: Kiểm soát ai có thể truy cập secrets
- **Audit logging**: Theo dõi truy cập secret

**Chiến Lược Rotation**
- **Database credentials**: Rotate database passwords
- **API keys**: Rotate API keys
- **Rotation tùy chỉnh**: Tạo rotation logic tùy chỉnh
- **Lịch trình rotation**: Thiết lập tần suất rotation

#### Phiên 5: Incident Response (11:50 AM+)
**Diễn Giả:** Tinh Truong, Mendel Grabski (Long)

##### Hiểu Về Incidents

**Các Loại Incidents**
- **Breach**: Truy cập trái phép vào dữ liệu hoặc hệ thống
- **Hacking**: Xâm nhập độc hại vào hệ thống
- **Downtime**: Không khả dụng dịch vụ
- **Hư hỏng dữ liệu**: Mất mát hoặc hư hỏng dữ liệu
- **Các sự kiện bảo mật khác**: Các incidents liên quan đến bảo mật khác nhau

##### Security Incident Response Cho Cloud Hiện Đại

**Cân Nhắc Cụ Thể Cloud**
- **Trách nhiệm chia sẻ**: Hiểu trách nhiệm AWS và khách hàng
- **Công cụ cloud-native**: Sử dụng dịch vụ AWS cho incident response
- **Tự động hóa**: Tự động hóa incident response
- **Khả năng mở rộng**: Xử lý incidents ở quy mô cloud

##### Incident Controls - Nền Tảng Bảo Mật

**Controls Phòng Ngừa**
- **Security controls**: Ngăn chặn incidents xảy ra
- **Best practices**: Triển khai security best practices
- **Tuân thủ**: Đáp ứng yêu cầu bảo mật

##### Phòng Ngừa - Không Ai Có Thời Gian Cho Incidents

**Chiến Lược Phòng Ngừa Chính**

**Loại Bỏ Credentials Dài Hạn**
- **Loại bỏ permanent credentials**: Loại bỏ long-term access keys
- **Sử dụng temporary credentials**: Ưu tiên STS tokens
- **Rotation thường xuyên**: Rotate bất kỳ credentials còn lại nào

**Không Bao Giờ Expose S3 Buckets Trực Tiếp**
- **Private theo mặc định**: Giữ buckets ở chế độ riêng tư
- **Kiểm soát truy cập**: Sử dụng IAM và bucket policies
- **Truy cập công khai**: Chỉ khi thực sự cần thiết với controls phù hợp

**Không Có Gì Internet-Facing Không Nên**
- **Giảm thiểu attack surface**: Giảm resources có thể truy cập công khai
- **Phân đoạn network**: Cô lập resources
- **Security groups**: Hạn chế truy cập

**Mọi Thứ Qua Infrastructure as Code**
- **Version control**: Theo dõi tất cả thay đổi infrastructure
- **Auditability**: Biết những gì đã thay đổi và khi nào
- **Reproducibility**: Infrastructure nhất quán
- **Quy trình review**: Code review cho thay đổi infrastructure

**Double-Gate Cho Thay Đổi Rủi Ro Cao**
- **Quy trình phê duyệt**: Yêu cầu nhiều phê duyệt cho thay đổi rủi ro
- **Quản lý thay đổi**: Quy trình thay đổi chính thức
- **Testing**: Testing thay đổi trước production

##### Hướng Dẫn Ngủ Tốt Hơn
- **Tự tin về bảo mật**: Biết bảo mật của bạn vững chắc
- **Giám sát**: Giám sát bảo mật liên tục
- **Tự động hóa**: Phản hồi bảo mật tự động
- **Best practices**: Tuân theo security best practices

##### Quy Trình Incident Response

**Phát Hiện**
- **Xác định incidents**: Nhận ra security events
- **Cảnh báo**: Nhận thông báo về incidents
- **Triage**: Ưu tiên hóa incidents

**Ngăn Chặn**
- **Cô lập mối đe dọa**: Ngăn chặn lây lan
- **Bảo tồn bằng chứng**: Duy trì bằng chứng để phân tích
- **Giao tiếp**: Thông báo cho các bên liên quan

**Loại Bỏ**
- **Loại bỏ mối đe dọa**: Loại bỏ nguyên nhân
- **Sửa lỗ hổng**: Sửa các vấn đề bảo mật
- **Dọn dẹp**: Loại bỏ resources bị xâm phạm

**Phục Hồi**
- **Khôi phục dịch vụ**: Quay lại hoạt động bình thường
- **Xác minh**: Đảm bảo mối đe dọa đã biến mất
- **Giám sát**: Tăng giám sát sau incident

**Bài Học**
- **Review sau incident**: Phân tích những gì đã xảy ra
- **Cải thiện**: Xác định các lĩnh vực cần cải thiện
- **Tài liệu**: Ghi lại bài học

### Kiến Thức Kỹ Thuật Quan Trọng

#### Bảo Mật Là Đa Lớp
- Bảo mật yêu cầu defense in depth với nhiều lớp
- Mỗi lớp giải quyết các vectơ tấn công khác nhau
- Không có một security control đơn lẻ nào là đủ

#### Identity Là Nền Tảng
- Quản lý danh tính và truy cập mạnh mẽ là quan trọng
- Least privilege là cần thiết
- Credentials tạm thời giảm rủi ro

#### Giám Sát Liên Tục Là Cần Thiết
- Bạn không thể bảo vệ những gì bạn không thể thấy
- Logging và giám sát toàn diện cho phép phát hiện
- Tự động hóa giúp phản hồi mối đe dọa nhanh chóng

#### Bảo Mật Network Là Quan Trọng
- Network controls là tuyến phòng thủ đầu tiên
- Nhiều lớp bảo mật network cung cấp bảo vệ tốt hơn
- Hiểu traffic flows giúp phát hiện bất thường

#### Bảo Vệ Dữ Liệu Là Bắt Buộc
- Mã hóa at rest và in transit là cần thiết
- Quản lý key phù hợp là quan trọng
- Secrets phải được quản lý một cách an toàn

#### Incident Response Phải Được Chuẩn Bị
- Phòng ngừa là tốt nhất, nhưng incidents sẽ xảy ra
- Có kế hoạch và thực hành nó là cần thiết
- Tự động hóa có thể tăng tốc phản hồi

### Bài Học Cá Nhân

#### Tư Duy Bảo Mật
- Tôi học được cách bảo mật phân lớp trên AWS hoạt động trong thực tế
- Tôi hiểu cách kết hợp IAM, logging, network controls, và encryption
- Tôi thấy bảo mật như một quy trình liên tục, không phải thiết lập một lần

#### Kỹ Năng Thực Tế
- Tôi có thể thiết kế kiến trúc an toàn sử dụng dịch vụ bảo mật AWS
- Tôi hiểu cách triển khai defense in depth
- Tôi biết cách giám sát và phản hồi security events

#### Best Practices
- Tầm quan trọng của least privilege và temporary credentials
- Cách sử dụng nhiều lớp bảo mật hiệu quả
- Giá trị của tự động hóa trong bảo mật

#### Phát Triển Sự Nghiệp
- Workshop này đã làm sâu sắc đáng kể hiểu biết của tôi về bảo mật AWS
- Tôi thấy bảo mật như một kỹ năng quan trọng cho bất kỳ chuyên gia cloud nào
- Tôi có động lực tiếp tục học về các chủ đề bảo mật nâng cao

### Trải Nghiệm Sự Kiện

Workshop này cực kỳ toàn diện và thực tế. Độ sâu coverage trên mỗi chủ đề, kết hợp với examples thực tế và best practices, làm cho các khái niệm bảo mật phức tạp trở nên dễ tiếp cận.

Sự tiến triển từ quản lý danh tính qua phát hiện, bảo mật network, bảo vệ dữ liệu, và incident response đã tạo ra bức tranh hoàn chỉnh về bảo mật AWS. Mỗi phiên xây dựng dựa trên các khái niệm trước đó, củng cố việc học.

Các diễn giả có kiến thức và cung cấp insights thực tế vượt ra ngoài chỉ mô tả tính năng. Các examples thực tế và case studies giúp tôi hiểu cách áp dụng các thực hành bảo mật này trong thực tế.

Workshop này đã cải thiện đáng kể hiểu biết của tôi về cách xây dựng các workloads an toàn trên AWS, và tôi tự tin có thể áp dụng những bài học này để thiết kế và triển khai các kiến trúc an toàn.

### Ảnh Sự Kiện

![Enter image alt description](/images/4-Event/event6_img1.jpg)
![Enter image alt description](/images/4-Event/event6_img2.jpg)

