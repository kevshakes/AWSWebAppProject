# AWS WEB APPLICATION ARCHITECTURE  
This project is aimed at planning, building and deploying a 3 tier web application while utilizing the AWS cloud architecture.  
The web application architecture will have various layers separated such as the web server,  web application and database instance.  

The main objective is to ensure High Availability, Performance and Scalability of the application. 

## ARCHITECTURE DIAGRAM  

### Solution Requirements  
1. **Functionality** <br>
   Functionality will be implemented by the Cloud9 IDE to host the code and separate the various layers.The application will
   be deployed in a web server where a user can view, add,delete or modify student records.

2. **Load Balanced** <br>
   Distribution of web traffic will be implemented by use of 2 elastic load balancers(Application load balancers). One load
   balancer will distribute traffic to the public subnets with web servers target groups while the 2nd will distribute traffic
   to the orivate subnets with the web app target group.
   
4. **Scalability** <br>
   Scalability will be accomplished by autoscaling groups for the public and public subnets. For each group, the minimum amount
   instances running is 2 and the maximum 4.
   
5. **Availability** <br>
   For availability, we will implement a multi-AZ infrastructure for the subnets and the services in the subnets.We will
   make use of 2 availability zones. For the database, we have two databases, one primary rds database instance and one standby
   rds database instance.
      
7. **Security** <br>
   Security will be implemented by use of private subnets security groups, NACL, secrets manager, systems manager and
   IAM roles.Policies will be implemented in the various infrastructure levels.
    
8. **Cost Optimization** <br>
  For cost optimization, we will use a cost estimation calculator to estiate the cost. We will also use reserved instances to
  have obtain discounts on the EC2 instances.
9. **Performance** <br>
    The performance of the application will be evidenced in using t3.medium instances with 4GB memory.The load balancers and
    autoscaling will also enhance performance.
    
   
