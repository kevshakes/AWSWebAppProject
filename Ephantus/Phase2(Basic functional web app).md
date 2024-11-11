# Project Setup and Testing

### 1. VPC and Subnet Creation
- **Created a VPC**: Set up a custom Virtual Private Cloud (VPC) to host the application infrastructure.
- **Configured Subnets**: Added a subnet within the VPC to manage IP allocation.
- **Updated Security Group**: Modified the security group settings to allow HTTP and SSH traffic(from my IP addrress) for the web instance.

### 2. EC2 Instance Launch
- **Uploaded User Data Script**: During the EC2 instance launch, the `userdata.sh` file was uploaded to automate the initial setup.

### 3. Website Testing
- **Tested Functionality**: Successfully tested the deployed web application by adding more entries to the list.
  http://ec2-54-211-136-132.compute-1.amazonaws.com/students

![Website Test Screenshot](https://github.com/user-attachments/assets/9d2fe759-f79d-4045-a5e5-bbe4ed4809f7)

### 4. Database Verification
- **SSH Access to EC2**: Connected to the EC2 instance via SSH using:
  ```bash
  ssh -i web.pem ubuntu@<EC2_PUBLIC_IP>

# MySQL Command:
  ```bash
mysql -u nodeapp -p


# Database Query:
  ```bash
SELECT * FROM students;
 ```

![Screenshot from 2024-11-11 17-38-12](https://github.com/user-attachments/assets/4c6cb4bb-0585-4b60-a45f-b2c67d8f8763)
