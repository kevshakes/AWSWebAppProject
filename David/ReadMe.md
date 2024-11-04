# BUILDING A HIGHLY AVAILABLE, SCALABLE WEB APP
### MY Architecture diagram
- 
![image](https://github.com/user-attachments/assets/7a90dea2-2495-41b3-892b-a37fb59f3f7d)

### Summary
- Auto Scaling group - maintaining application performance and availability while optimizing costs in AWS
- Key Features.
- Dynamic scaling
- Scheduled scaling
- Security group - Virtual firewall that Control inbound and outbound traffic
   It is stateless, i.e., when you allow incoming traffic from a specific IP, the response is auto-allowed regardless of the outbound rule.
- NACL- control security at subnet level - acts as a firewall to control traffic in one or more subnet levels
- Secretes manager- To store credentials, and API keys
- NAT - Perform network address translation, translate private IP to public IP and vice versa
