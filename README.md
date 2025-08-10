<!--
![Image Alt]()

-->
# Clean Works...!!!
#  Deploying Website with the help AWS 

This project demonstrates that  how to set up an AWS system to run websites that is secure, fast, and always available. It has separate public and private networks, balances traffic between servers, automatically adds or removes servers when needed, stores data in a secure database, monitors performance, sends alerts, and connects a custom domain to the site.

---

##  Tables Contents  

- [Project Overview](#project-overview)
- [Technologies Used](#technologies-used)
- [Outputs](#outputs)
- [Conclusion](#conclusion)

---

##  Project Overview

The project involves creating a custom AWS environment to host secure, scalable, and highly available 
applications. It begins with setting up a custom VPC containing public and private subnets, connected via an 
Internet Gateway and NAT Gateway for controlled internet access. Route tables are configured to manage 
traffic flow, and security groups are defined to allow SSH (22) and HTTP (80) access. High availability and 
scalability are achieved by creating an Application Load Balancer (ALB) linked to a target group and 
managed via an Auto Scaling Group. SNS topics are set for notifications, while CloudWatch alarms and 
dashboards are implemented for real-time monitoring of CPU utilization. A domain is attached to the ALB’s 
DNS for seamless access, and a database server is securely deployed in the private subnet for backend data 
storage.

---

##  Technologies Used

- AWS VPC – Custom Virtual Private Cloud with public and private subnets

- AWS Internet Gateway (IGW) – Public internet access for ALB and NAT Gateway

- AWS NAT Gateway – Outbound internet for private subnet resources

- AWS Route Tables – Public and private routing configuration

- AWS Security Groups – Fine-grained inbound/outbound traffic control

- AWS Application Load Balancer (ALB) – High availability & traffic distribution

- AWS Auto Scaling Group (ASG) – Automatic scaling of EC2 instances

- Amazon EC2 – Compute instances for hosting application backend

- Amazon RDS – Managed database in private subnet (Multi-AZ for HA)

- Amazon Route 53 – Domain and DNS routing to ALB

- Amazon Simple Notification Service (SNS) – Event and alarm notifications

- Amazon CloudWatch – Real-time monitoring, alarms, and dashboards

- AWS IAM – Identity & Access Management for secure roles and policies

- TLS/SSL (ACM) – HTTPS encryption via AWS Certificate Manager

- Linux (Amazon Linux/Ubuntu) – Application OS environment

---

##  Output's 

<div align="center">
  
  
  <p><strong>Home page – </strong></p>
  
![Image Alt](https://github.com/20Dartside/Website-Deployment-on-AWS/blob/main/output_img/img1.png?raw=true)
  


<p><strong> About page – </strong></p>

  ![Image Alt](https://github.com/20Dartside/Website-Deployment-on-AWS/blob/main/output_img/img3.png?raw=true)
  

 <p><strong> Contact page - </strong></p>

  ![Image Alt](https://github.com/20Dartside/Website-Deployment-on-AWS/blob/main/output_img/img4.png?raw=true)
 
 <p><strong>Service List page - </strong></p>
 
  ![Image Alt](https://github.com/20Dartside/Website-Deployment-on-AWS/blob/main/output_img/img5.png?raw=true)
 

 <p><strong>Best Offer  page - </strong></p>
 
![Image Alt](https://github.com/20Dartside/Website-Deployment-on-AWS/blob/main/output_img/img6.png?raw=true)


<p><strong>Happy Customer page - </strong></p>
 
![Image Alt](https://github.com/20Dartside/Website-Deployment-on-AWS/blob/main/output_img/img7.png?raw=true)
 
 <p><strong>Website Deployment Architecture Diagram</strong></p>
 
  ![Image Alt](https://github.com/20Dartside/Website-Deployment-on-AWS/blob/main/output_img/img8.png?raw=true)

 
</div>

---

##  Conclusion

- ✅ Create VPC with 2+ AZs and subnet plan (public/private per AZ).
- ✅ Create IGW + public route table.
- ✅Security groups & NACL defaults.
- ✅Launch ALB in public subnets + target group + health checks.
- ✅Create Launch Template/User Data for app instances.
- ✅Create ASG with proper scaling policies (target/step/CPU-based).
- ✅Provision RDS (Multi-AZ, encryption, subnet group) in private subnets.
- ✅Route53 record for domain → ALB.
- ✅CloudWatch metrics/alarms + SNS topic subscriptions.
- ✅IAM roles and SSM agent setup for secure access.
- ✅Backup/DR (RDS snapshots, AMIs) and logging (CloudWatch Logs + S3).
- ✅Test failover & scale-in/scale-out scenarios.


