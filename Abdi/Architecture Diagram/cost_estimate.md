# Services Used (us-east-1)
### Estimate Budget

1. Internet Gateway - provides connectivity between the VPC and the internet allowing public resources within the VPC

2. Application Load Balancer (ALB) - Will handle user requests, ensuring they are evenly distributed across the application tier instances. This improves responsivenenss during peak periods by reducing the load on any single server.

3. EC2 Instances - EC2 instances host the web and application layers of the student records system. They process incoming requests, serve content, and manage business logic, ensuring that the application remains responsive under heavy traffic.

4. NAT Gateway - The NAT Gateway enables private instances (such as application or database servers) to access the internet for updates and patches without exposing them to direct public internet access, thereby enhancing security.

5. Amazon RDS - RDS hosts the database for student records, ensuring reliable and performant data storage and retrieval. The Multi-AZ deployment option increases database availability and resilience, especially during peak admissions periods.

6. Amazon Secrets Manager -Secrets Manager stores the database credentials for the RDS instance, ensuring that these credentials are protected and managed securely without hard-coding them in the application code.

7. AWS Shield -  AWS Shield protects the web application from DDoS attacks, helping maintain availability and performance, especially during high-traffic times like admissions, when malicious traffic could disrupt access

8. Cloud9 - Cloud9 provides a convenient development environment for making quick changes, troubleshooting, and debugging the application code in real time, especially during testing and POC stages

9. IAM Role - IAM Roles are used to grant EC2 instances, Lambda functions, or other AWS resources permissions to interact with services like RDS or Secrets Manager. For example, an IAM role could allow an EC2 instance running the application to access the RDS database securely.

10. 