---
title : "Giới thiệu"
date: 2025-09-09
weight : 1
chapter : false
pre : " <b> 5.1. </b> "

---

#### Về MapVibe

**MapVibe** là một nền tảng khám phá địa điểm được hỗ trợ bởi AI, giúp người dùng tìm các địa điểm ăn uống và hoạt động tại Thành phố Hồ Chí Minh bằng cách sử dụng truy vấn ngôn ngữ tự nhiên. Thay vì tìm kiếm từ khóa truyền thống, người dùng có thể diễn đạt nhu cầu của họ bằng ngôn ngữ hội thoại, chẳng hạn như "Hôm nay tôi đang buồn, có quán đồ uống nào giúp tôi giải tỏa nỗi buồn không?"

Nền tảng tận dụng các dịch vụ AI của AWS bao gồm:
- **AWS Bedrock** - Để xử lý ngôn ngữ tự nhiên sử dụng mô hình Titan embedding và Claude LLM
- **Amazon Rekognition** - Để kiểm duyệt nội dung cho hình ảnh do người dùng tải lên
- **Amazon Textract** - Để trích xuất văn bản từ hình ảnh menu và biển hiệu

#### Tổng quan về workshop

Trong workshop này, bạn sẽ học cách xây dựng và triển khai MapVibe, một ứng dụng full-stack sử dụng:

- **Kiến trúc Monorepo** - Sử dụng TurboRepo và Bun để phát triển hiệu quả
- **Ứng dụng Frontend**:
  - `apps/web` - Ứng dụng web chính dành cho người dùng (React 19, Vite, TailwindCSS)
  - `apps/admin` - Bảng điều khiển quản trị để quản lý nội dung
- **Dịch vụ Backend**:
  - `apps/api` - Hàm Lambda API chính xử lý các REST endpoints
  - Nhiều hàm Lambda chuyên biệt cho embeddings, RAG, OCR, Rekognition và tổng hợp đánh giá
- **Hạ tầng**:
  - Các module Terraform cho các dịch vụ AWS (VPC, RDS, Lambda, API Gateway, CloudFront, Cognito, v.v.)
  - Phương pháp Infrastructure as Code để triển khai có thể tái tạo

#### Tổng quan Kiến trúc

Kiến trúc MapVibe tuân theo phương pháp serverless-first:

1. **Frontend**: Ứng dụng React được triển khai lên S3 và phục vụ qua CloudFront CDN
2. **Lớp API**: API Gateway định tuyến yêu cầu đến các hàm Lambda
3. **Lớp Dữ liệu**: Cơ sở dữ liệu PostgreSQL RDS để lưu trữ dữ liệu có cấu trúc
4. **Dịch vụ AI**: Bedrock cho embeddings và LLM, Rekognition để phân tích hình ảnh
5. **Lưu trữ**: S3 buckets cho ảnh và tài sản tĩnh
6. **Xác thực**: AWS Cognito để quản lý người dùng
7. **Bảo mật**: WAF để bảo vệ, Route53 và ACM cho tên miền tùy chỉnh

---
title : "Introduction"
date: 2025-09-09
weight : 1
chapter : false
pre : " <b> 5.1. </b> "

---

#### About MapVibe

**MapVibe** is an AI-powered location discovery platform that helps users find dining and activity locations in Ho Chi Minh City using natural language queries. Instead of traditional keyword searches, users can express their needs in conversational language, such as "I'm feeling sad today, is there any drink place that can help me relieve my sadness?"

The platform leverages AWS AI services including:
- **AWS Bedrock** - For natural language processing using Titan embedding model and Claude LLM
- **Amazon Rekognition** - For content moderation of user-uploaded images
- **Amazon Textract** - For extracting text from menu images and signs

#### Workshop overview

In this workshop, you will learn how to build and deploy MapVibe, a full-stack application using:

- **Monorepo Architecture** - Using TurboRepo and Bun for efficient development
- **Frontend Applications**:
  - `apps/web` - Main user-facing web application (React 19, Vite, TailwindCSS)
  - `apps/admin` - Admin dashboard for content management
- **Backend Services**:
  - `apps/api` - Main API Lambda function handling REST endpoints
  - Multiple specialized Lambda functions for embeddings, RAG, OCR, Rekognition, and review aggregation
- **Infrastructure**:
  - Terraform modules for AWS services (VPC, RDS, Lambda, API Gateway, CloudFront, Cognito, etc.)
  - Infrastructure as Code approach for reproducible deployments

#### Architecture Overview

The MapVibe architecture follows a serverless-first approach:

1. **Frontend**: React applications deployed to S3 and served via CloudFront CDN
2. **API Layer**: API Gateway routes requests to Lambda functions
3. **Data Layer**: PostgreSQL RDS database for structured data storage
4. **AI Services**: Bedrock for embeddings and LLM, Rekognition for image analysis
5. **Storage**: S3 buckets for photos and static assets
6. **Authentication**: AWS Cognito for user management
7. **Security**: WAF for protection, Route53 and ACM for custom domains

![overview](/images/5-Workshop/4N1D-Architechture.drawio.png)
