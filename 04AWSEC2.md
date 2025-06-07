## AWS EC2 Service
- EC2 (Elastic Cloud Compute)
- AWS EC2 (Amazon Elastic Compute Cloud) is a cloud service that provides `resizable virtual servers`, called `instances`, which you can use to run application
- Imagine you're running a business and need a server to host your website or application.
- Instead of buying and managing physical servers `AWS EC2` lets you rent virtual servers in the cloud. These virtual servers are called instances.
- You can configure several options like (OS, RAM, CPU, Disk Space, Network/Firewall, How to access the machine)

## The tearms we see when we configure the AWS
- Instance Type: Select the hardware capacity(CPU, memory).
- AMI (Amazon Machine Image): Choose the `operating system` and software (linux, mac, windows).
- Storage: Configure the type and size of storage (EBS volume).
- Security Groups: Set up firewall rules to control inbound/outbound traffic
- Key Pair: Create or use an existing key pair for SSH access.
- Network Settings: Configure VPC, subnet, and assign public or private IP address.
- IAM Role: Attach an IAM role for permissions to access other AWS resources.
- Use Data: Add scripts to be executed when the instance starts.
- Elastic IP: Optionally associate a static IP address for consistent public access

## Creating First EC2 Instance
- Type `EC2` in the search box
- Select the `EC2`(virtual server in the cloud)
- Then we find the `EC2 Dashboard`
![image](https://github.com/user-attachments/assets/16d608de-53f8-4278-946b-1af019804449)
- `EC2` is region specific. And which region select in the `Stockholm` the server will be present there
- To create the instance we click on `Launch Instance` then give a name
![image](https://github.com/user-attachments/assets/af1c17a9-e633-46ed-aca8-da9cc7a653be)
- Then we selet the AMI (OS)


