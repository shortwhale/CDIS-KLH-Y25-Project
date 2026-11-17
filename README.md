# Cloud-Based Student Attendance and Academic Monitoring System

## Project Overview

The Cloud-Based Student Attendance and Academic Monitoring System is a web application designed to simplify attendance management and academic performance tracking in educational institutions.

The system allows faculty to record attendance and marks, students to monitor their attendance percentages and academic performance, and administrators to manage users and generate reports.

The project is designed around AWS cloud services to provide scalability, security, reliability, and high availability.

## Problem Statement

Traditional attendance management systems involve manual work, which can lead to errors, delays, and inefficient record management.

Students may not receive timely information about attendance shortages, while faculty and administrators face difficulties managing large amounts of academic data.

This project aims to solve these problems through a centralized, cloud-based platform.

## Objectives

- Automate student attendance management.
- Provide subject-wise attendance tracking.
- Allow faculty to manage attendance and marks.
- Generate academic reports efficiently.
- Provide low-attendance warnings.
- Ensure secure access through role-based authentication.
- Improve scalability and availability using AWS cloud infrastructure.

## Key Features

### Faculty Module
- Secure login
- Mark and update attendance
- View class-wise attendance records
- Enter student marks

### Student Module
- View overall attendance percentage
- Track subject-wise attendance
- Receive low-attendance warnings
- View marks and academic performance

### Admin Module
- Manage students, faculty, and courses
- Generate attendance and academic reports
- Download reports in CSV or PDF format
- Monitor system status

## Technologies and AWS Services

| Technology / Service | Purpose |
|---|---|
| Docker | Containerize the web application |
| Amazon EC2 | Host application containers |
| Auto Scaling Group | Automatically adjust EC2 instances based on demand |
| Application Load Balancer | Distribute incoming traffic |
| Amazon VPC | Provide isolated cloud networking |
| Public and Private Subnets | Separate network resources |
| NAT Gateway | Support outbound access from private subnets |
| Amazon ECR | Store Docker images |
| Amazon RDS (Multi-AZ) | Store attendance and academic records |
| Amazon S3 / EFS | Store reports and backups |
| Amazon CloudWatch | Monitor performance, logs, and resource usage |
| IAM and Security Groups | Manage permissions and network access |

## Proposed System Architecture

The application is designed to run inside Docker containers hosted on Amazon EC2 instances.

An Application Load Balancer distributes incoming requests across instances managed by an Auto Scaling Group.

Amazon RDS stores attendance and academic information in private subnets.

Amazon CloudWatch monitors system performance, while IAM and Security Groups help secure access.

### Architecture Flow

```text
          Students / Faculty / Admin
                     |
                     v
          Application Load Balancer
                     |
                     v
              Auto Scaling Group
                     |
              EC2 Instances
             (Docker Containers)
                     |
                     v
              Amazon RDS
          (Private Database)
                     
       CloudWatch -> Monitoring
       S3 / EFS   -> Reports & Backups
       IAM        -> Access Control
```

## Working of the System

1. Users log in according to their assigned roles.
2. Faculty members record attendance and enter marks.
3. Attendance information is stored in the database.
4. Students access their attendance percentages and academic records.
5. The system displays warnings for low attendance.
6. Administrators manage records and generate reports.
7. AWS services support load balancing, scaling, security, and monitoring.

## Expected Benefits

- Reduced manual attendance work
- Improved accuracy of academic records
- Easy access to attendance information
- Better academic monitoring
- Secure and centralized data management
- Improved application availability
- Efficient resource utilization

## Future Enhancements

- Email and SMS alerts for attendance shortages
- Advanced academic analytics dashboard
- Additional performance monitoring features

## Project Team

| Name | Student ID |
|---|---|
| Vineetha | 2520030149 |
| Mahitha | 2520030469 |
| Thanvi | 2520030057 |

## Conclusion

The Cloud-Based Student Attendance and Academic Monitoring System aims to provide a centralized solution for managing attendance and academic records.

By using AWS services such as EC2, RDS, Auto Scaling, Load Balancer, and CloudWatch, the proposed system is designed to support secure, scalable, and reliable academic monitoring.
