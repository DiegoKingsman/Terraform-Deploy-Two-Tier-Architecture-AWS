Terraform: Deploy A Two-Tier Architecture With AWS. 
Configuring a CI/CD Pipeline on Terraform Cloud

In this project, we will leverage the power of Terraform Cloud, AWS, and Github to create a robust CI/CD pipeline. 
Through a step-by-step approach, we will demonstrate how to create Terraform configuration files and implement a highly scalable and available two-tier architecture.

The architecture we will build consists of a public network and a private network, known as the first and second tiers respectively. 
The first tier is the user-facing network, providing access to the web application. On the other hand, the second tier serves as the data center, offering business 
logic back to the web application. By segregating the data center’s information from the client, this architecture helps to keep sensitive information secure.

We will begin by setting up the development environment, configuring Github repositories, and creating IAM roles with the necessary permissions. 
Afterward, we will move on to creating a VPC, subnets, security groups, and NAT gateway. We will then build an RDS instance and connect it to the web application. 
Finally, we will use Terraform Cloud to implement the CI/CD pipeline.

By the end of this project, you will have a deep understanding of how to use Terraform, AWS, and Github to build a highly scalable and available two-tier architecture. 
You will also learn how to automate the deployment process with Terraform Cloud and ensure that changes are rolled out efficiently and reliably. 
Without further ado, let’s dive in and start building!

Project Outline:

Create a custom VPC with:

2 public subnets for the Web Server Tier
2 private subnets for the RDS Tier
A public route table
A private route table
Create an Auto Scaling Group to launch an EC2 Instance with an Apache web server in each public subnet in the web tier. Configure necessary security groups.
Create an Internet-facing Application Load Balancer targeting web servers.
Create an ALB security group with needed permissions and modifications needed.
Create one RDS MySQL Instance (micro) in the private RDS subnets with appropriate security groups.
Deploy the architecture using Terraform Cloud as a CI/CD tool to check the build.

Prerequisites:

An AWS Admin Account with Access Key and Secret Access Key
An AWS Cloud9 Environment
A free Terraform Cloud Account
A Github Account
Familiarity with Linux and Git commands
In your chose IDE (I am using Cloud9) Lets write the code that will launch our infrastructure.
