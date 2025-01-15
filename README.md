# Hybrid-secure-s3-access-vpc
Hybrid Secure Access to S3 using VPC Endpoints

# Introduction
VPC endpoints are virtual devices. They are horizontally scaled, redundant, and highly available VPC components. They allow communication between your compute resources and AWS services without imposing availability risks.

# We will explore two primary endpoint types:
Gateway Endpoints: For communication between compute resources within a VPC and S3.
Interface Endpoints: For both VPC and on-premises resources to access S3.

"VPC Cloud" is for cloud resources such as a Gateway endpoint and an EC2 instance to test with. "VPC On-Prem" simulates an on-premises environment such as a factory or corporate datacenter. An EC2 instance running strongSwan VPN software has been deployed in "VPC On-prem" and automatically configured to establish a Site-to-Site VPN tunnel with AWS Transit Gateway. This VPN simulates connectivity from an on-premises location to the AWS cloud.



![Blank diagram](https://github.com/user-attachments/assets/9e161804-dbcd-4348-94bf-1da91b7385ac)


# Key Concepts:
VPC Endpoints: Virtual devices within a VPC that enable private and secure communication with supported AWS services.
PrivateLink: A service that enables you to privately connect your VPC to other AWS services, such as S3, without exposing your traffic to the public internet.
Site-to-Site VPN: A secure connection between your on-premises network and an AWS VPC, allowing for private communication between the two.

# Architecture:

# Two VPCs:
"VPC Cloud": Hosts a Gateway Endpoint and an EC2 instance for testing S3 access within the VPC.

"VPC On-Prem": Simulates an on-premises environment. Contains an EC2 instance running strongSwan VPN software to establish a Site-to-Site VPN connection with AWS Transit Gateway.

AWS Transit Gateway: Facilitates connectivity between "VPC Cloud" and "VPC On-Prem" via the Site-to-Site VPN.

# Objectives:
Learn about the benefits of using VPC Endpoints for S3 access.
Explore the differences between Gateway and Interface Endpoints.
Implement and test secure S3 access using VPC Endpoints from both within the VPC and from the simulated on-premises environment.
