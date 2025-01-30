# Phase 2

This phase required me to do the following:

    Task 1: Creating a virtual network
    Create a virtual network to host the web application.

    Task 2: Creating a virtual machine
    Create a virtual machine in the cloud to host the web application.
    
    Task 3: Testing the deployment
    Test the deployment of the web application to ensure it is accessible from the internet and functional. Perform a few tasks, such as viewing, adding, deleting, or modifying records.

## 1. Task 1: Creating a virtual network
- I created a VPC called 'Phase2'.
- For this phase, I deployed my resources in 'Phase2-Public-Subnet' which is in the 'us-east-1a' availability zone.
    ![VPC Resource Map](phase2-vpc.png)
- I then created an Internet Gateway called 'Phase2-igw'
- The route table for 'Phase2' to routes traffic to the internet through the internet gateway. I associated this route table to 'Phase2-Public-Subnet'
    ![Route Table](phase2-rt.png)

## 2. Creating a virtual machine
- Here I created an EC2 instance with the following properties/details:

    - Platform - Ubuntu
    - Instance type - t2.micro
    - VPC - Phase2
    - Subnet - Phase2-Public-Subnet

- Then I uploaded the shell script to install the required web application and database on the virtual machine.
    ![Phase 2 VM](phase2-vm.png)

## Task 3: Testing the deployment
- I opened the public IPv4 address link and was able to see the deployed web application
- Finally I tested the application and was able to add and edit a student record
![Student web page](phase2-webpage.png)