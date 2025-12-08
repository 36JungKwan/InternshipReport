---
title: "Sự Kiện 3"
date: 2025-09-09
weight: 3
chapter: false
pre: " <b> 4.3. </b> "
---

# Báo Cáo Tóm Tắt: "Workshop – Data Science trên AWS"

### Tổng Quan Sự Kiện

- **Tên Sự Kiện:** Workshop – Data Science trên AWS  
- **Ngày:** 16 tháng 10, 2025  
- **Vai Trò:** Người tham dự  
- **Hình Thức:** Workshop thực hành với labs có hướng dẫn  
- **Địa Điểm:** Đại học FPT, Thủ Đức, Thành phố Hồ Chí Minh, Việt Nam

Workshop toàn diện này cung cấp một walkthrough hoàn chỉnh về quy trình data science end-to-end trên AWS, từ ingestion và chuẩn bị dữ liệu ban đầu qua training, đánh giá, và triển khai model. Định dạng kết hợp các bài giảng tập trung với các labs thực hành có hướng dẫn, cho phép người tham dự thử nghiệm trực tiếp trong môi trường AWS và có được kinh nghiệm thực tế với các dịch vụ thực.

### Cấu Trúc Workshop

Workshop được chia thành nhiều modules, mỗi module xây dựng dựa trên module trước:

#### Module 1: Ingestion và Lưu Trữ Dữ Liệu
- **Amazon S3 như nền tảng data lake**: Hiểu vai trò của S3 như lưu trữ trung tâm cho các dự án data science
- **Tổ chức dữ liệu**: Best practices để tổ chức dữ liệu trong S3 (raw, processed, curated layers)
- **Định dạng dữ liệu**: Chọn giữa CSV, Parquet, JSON, và các định dạng khác cho các use case khác nhau
- **Tính năng S3 cho data science**: Versioning, lifecycle policies, và access controls
- **Lab thực hành**: Thiết lập cấu trúc S3 bucket và upload sample datasets

#### Module 2: Chuẩn Bị Dữ Liệu và ETL
- **Tổng quan AWS Glue**: Dịch vụ ETL serverless cho chuyển đổi dữ liệu
- **Glue Data Catalog**: Kho metadata tập trung cho data discovery
- **AWS Glue DataBrew**: Công cụ chuẩn bị dữ liệu trực quan để làm sạch và chuyển đổi dữ liệu
- **ETL workflows**: Xây dựng data transformation pipelines
- **Chất lượng dữ liệu**: Xác định và xử lý missing values, duplicates, và outliers
- **Lab thực hành**: Tạo Glue job để chuyển đổi raw data thành định dạng processed

#### Module 3: Khám Phá và Phân Tích Dữ Liệu
- **Amazon Athena**: Dịch vụ truy vấn tương tác serverless cho dữ liệu S3
- **SQL queries trên S3**: Viết SQL queries chống lại dữ liệu được lưu trong S3
- **Tối ưu truy vấn**: Chiến lược phân vùng và tối ưu chi phí
- **Amazon Redshift**: Data warehousing cho analytics workloads
- **Redshift Spectrum**: Truy vấn dữ liệu S3 trực tiếp từ Redshift
- **Lab thực hành**: Chạy exploratory queries trên datasets sử dụng Athena

#### Module 4: Phát Triển Model với Amazon SageMaker
- **SageMaker Studio**: Môi trường phát triển tích hợp cho ML
- **SageMaker Notebooks**: Jupyter notebooks với môi trường được cấu hình sẵn
- **Built-in algorithms**: Sử dụng các algorithms được xây dựng sẵn của SageMaker cho các ML tasks phổ biến
- **Custom model training**: Training models sử dụng custom code và frameworks
- **Hyperparameter tuning**: Sử dụng automatic model tuning của SageMaker
- **Experiment tracking**: Quản lý và so sánh các experiments model khác nhau
- **Lab thực hành**: Xây dựng và training một machine learning model sử dụng SageMaker

#### Module 5: Triển Khai và Giám Sát Model
- **Triển khai model**: Triển khai models như real-time endpoints
- **Batch inference**: Chạy predictions trên large datasets
- **A/B testing**: Testing nhiều phiên bản model trong production
- **Giám sát model**: Theo dõi hiệu suất model và data drift
- **Tối ưu chi phí**: Right-sizing endpoints và sử dụng Spot Instances
- **Lab thực hành**: Triển khai một trained model và thực hiện predictions

### Nội Dung Kỹ Thuật Chi Tiết

#### Kiến Trúc Data Lake
Workshop nhấn mạnh tầm quan trọng của một data lake được thiết kế tốt:
- **Raw layer**: Lưu trữ dữ liệu chính xác như nhận được từ source systems
- **Processed layer**: Dữ liệu đã làm sạch và chuyển đổi sẵn sàng cho phân tích
- **Curated layer**: Datasets sẵn sàng cho business được tối ưu cho các use case cụ thể
- **Lợi ích**: Data lineage, reproducibility, và tính linh hoạt cho các nhu cầu analytics khác nhau

#### AWS Glue Deep Dive
- **Crawlers**: Tự động phát hiện schema và tạo table definitions
- **ETL jobs**: Viết transformation logic trong Python hoặc Scala
- **Job scheduling**: Sử dụng EventBridge để trigger ETL jobs
- **Tối ưu chi phí**: Hiểu pricing của Glue và tối ưu job execution

#### Khả Năng SageMaker
- **Managed infrastructure**: Không cần provision hoặc quản lý servers
- **Auto-scaling**: Tự động scaling training và inference resources
- **Spot Instances**: Sử dụng Spot Instances cho training hiệu quả về chi phí
- **Model registry**: Versioning và quản lý model artifacts
- **Pipelines**: Xây dựng ML pipelines cho automated workflows

#### Patterns Tích Hợp
- **End-to-end pipeline**: Kết nối S3 → Glue → Athena → SageMaker
- **Event-driven workflows**: Sử dụng EventBridge để orchestrate data science workflows
- **CI/CD cho ML**: Tích hợp ML workflows vào thực hành DevOps
- **Monitoring và alerting**: Sử dụng CloudWatch để giám sát ML workloads

### Bài Học Quan Trọng

#### Quy Trình Data Science trên AWS
- Hiểu cách các dịch vụ AWS khác nhau phù hợp với nhau trong một dự án data science hoàn chỉnh
- Tầm quan trọng của tổ chức và quản trị dữ liệu ngay từ đầu
- Cách managed services giảm overhead quản lý infrastructure

#### Best Practices
- **Tổ chức dữ liệu**: Tách biệt raw, processed, và curated data layers
- **Reproducibility**: Sử dụng versioning và experiment tracking
- **Tối ưu chi phí**: Right-sizing resources và sử dụng instance types phù hợp
- **Bảo mật**: Triển khai access controls và encryption phù hợp

#### Kỹ Năng Thực Tế
- Thiết lập kiến trúc data lake trên S3
- Tạo ETL jobs với AWS Glue
- Truy vấn dữ liệu với Athena
- Training models với SageMaker
- Triển khai và giám sát models trong production

### Bài Học Cá Nhân

#### Hiểu Biết Kỹ Thuật
- Tôi có được hiểu biết toàn diện về một data science pipeline hoàn chỉnh trên AWS trông như thế nào trong thực tế
- Các labs thực hành giúp tôi tự tin sử dụng các dịch vụ như S3, Glue, Athena, và SageMaker cùng nhau
- Tôi hiểu cách thiết kế data architectures hỗ trợ cả analytics và machine learning

#### Insights Quy Trình
- Tầm quan trọng của việc suy nghĩ về toàn bộ pipeline, không chỉ model training
- Cách chuẩn bị dữ liệu thường mất nhiều thời gian hơn phát triển model
- Giá trị của managed services trong việc cho phép data scientists tập trung vào phân tích thay vì infrastructure

#### Ứng Dụng Tương Lai
- Workshop này truyền cảm hứng cho tôi suy nghĩ về cách thiết kế experiments có thể tái tạo
- Tôi học được cách tốt hơn để tổ chức datasets cho các dự án tương lai
- Tôi hiểu cách cấu trúc data science projects cho khả năng mở rộng và khả năng bảo trì

#### Phát Triển Sự Nghiệp
- Workshop củng cố sự quan tâm của tôi về data science và ML trên AWS
- Tôi thấy cách kỹ năng data engineering và ML engineering bổ sung cho nhau
- Tôi có động lực tiếp tục học về các tính năng SageMaker nâng cao và thực hành MLOps

### Kinh Nghiệm Thực Hành

Định dạng thực hành của workshop đặc biệt có giá trị. Làm việc qua các labs thực tế giúp tôi:
- Hiểu các bước thực tế liên quan trong mỗi giai đoạn của một dự án data science
- Xem cách các dịch vụ tích hợp và hoạt động cùng nhau
- Xây dựng tự tin trong việc sử dụng AWS console và dịch vụ
- Học từ sai lầm trong môi trường an toàn, có hướng dẫn

Sự kết hợp giữa lý thuyết và thực hành làm cho các khái niệm cụ thể và dễ nhớ hơn nhiều so với các phiên chỉ có bài giảng.

### Trải Nghiệm Sự Kiện

Workshop này là một trong những sự kiện thực tế và thực hành nhất mà tôi đã tham dự. Cách tiếp cận từng bước, kết hợp với các dịch vụ AWS thực tế và datasets thực tế, làm cho nó cảm thấy như làm việc trên một dự án thực tế thay vì chỉ học lý thuyết.

Các giảng viên có kiến thức và hữu ích, cung cấp hướng dẫn khi chúng tôi gặp vấn đề và giải thích "tại sao" đằng sau best practices, không chỉ "cách làm".

Workshop này đã cải thiện đáng kể hiểu biết của tôi về cách xây dựng các giải pháp data science sẵn sàng cho production trên AWS, và tôi rất vui mừng áp dụng những bài học này cho các dự án tương lai.

### Ảnh Sự Kiện

![Enter image alt description](/images/4-Event/event3_img1.jpg)
![Enter image alt description](/images/4-Event/event3_img2.jpg)
