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
- Then we selet the AMI (OS). Select the Amazon Linux because its `Free tier eligible`
![image](https://github.com/user-attachments/assets/dab4060c-3b75-47fb-a0b9-858bd87b0489)
- Then select the `instance type` which is `free tier`
- To connect with this `instance` we are provided with `Key pair` so we can `create key pair`. After creating new key pair we a file will be downloaded
![image](https://github.com/user-attachments/assets/21599c5a-569a-42bf-9e69-4051e16624d6)
- After we can set the network through `Network settings`. We can control the service we need or allowed in the server we can control it.
- So in Firewall, we check `Allow SSH traffic from Anywhere`. It means the server can be accessed using the SSH from any `source IP`.
- Also check `Allow HTTP traffic from the internet`. So we can install the web server here and for that we need HTTP
![image](https://github.com/user-attachments/assets/cae15261-615b-4916-982d-978bc05ceb04)
- In `Configure Storage` we are allowed 30GB `free tier` but 8 GB is enough for starting
- We can select the `Intance no` in `Number of instances`

### Using Userdata
- We can provide some `Advanced details` its optional but if we want to run someting with the instance starts we can provide in `User data - optional` we can provide a script there
![image](https://github.com/user-attachments/assets/d81a0cd6-3300-48bb-9c7b-f03e0b38e225)
**Important**: The `Auto-assign public IP` needs to be `Enable` in `Network settings`
- At the end click on `Launch Instance`
- After the instance creating if you go to EC2 the `Intances running` will be 1
![image](https://github.com/user-attachments/assets/234dde98-1e74-4871-9068-3e6bf4791ddd)
- Click on the `Instance Id` to get more details
![image](https://github.com/user-attachments/assets/0f2ed226-8e2f-4226-b145-18f20851fd14)
- By pasting the public IP in new tab we can see the `script` we provided in the `Advance details`

## Overview of Security Groups
- Security Groups: Network firewall rules that control `inbound` and `outbound traffic for instances`.
![image](https://github.com/user-attachments/assets/12b5781c-0688-4829-a4f4-f6958e5e994e)
- EC2 Dashboard --> Instance running --> Instance Id --> scroll down --> Security -->Security Groups
- Inbound rules: In our sever a website is deployed, so we request our web server (EC2 intance) that the website need to be accessed. It means in our server a request will came from outside / from a browser it is controlled by `inbound rules`
- In inbound rules: `port 80` -> HTTP service and `port 22` -> SSH
- We can change it through `Security Groups` --> `Edit inbound rules`
![image](https://github.com/user-attachments/assets/46abc71b-f19a-4034-a2a3-606d0cce4e74)

### Important points about security groups:
- Region specific
- Only `Allow` rule (but no deny rule)
- All inbound traffic blocked and outbound allowed by default
- You define rules for specific:
  - Protocols (like HTTP, HTTPS, SSH, etc)
  - Port numbers (allow traffic only from a specific IP or range of IPs).
  - IP addresses or ranges (allow traffic only from a specific IP or range of IPs)
 
- If you allow incoming traffic on a specific port (port 80 for HTTP), the outgoing response traffic is automatically allowed without an explicit outbound rule

## Some ports you should be aware of
- HTTP (port 80)- Unencrypted web traffic
- HTTPS (port 443)- Encrypted web traffic (SSL/TLS)
- SSH (port 22) - secure remote access to servers (Linux/Unix)
- FTP (port 21) - File Transfer protocol (unsecured)
- SFTP (port 22) - Secure File Transfer Protocol
- SMTP (port 25) - Simple Mail Transfer Protocol (email sending)
- RDP (port 3389) - Remote Desktop Protocol (Windows remote access)
- MySQL (Port 3306) - MySQL database connections
- PostgreSQL (Port 5432) - PostgreSQL databse connections
- DNS (port 53) - Domain Name System (converts domain names to IP address)

## Create our own Security Group:
- Go to the left side --> Scroll down --> Network & Security --> Security Groups --> Create security group
![image](https://github.com/user-attachments/assets/ccf5d814-eab4-45f6-bf73-3fb773fb2996)
- When we create our instance we can use our old `Security Group` there
- Go to Instance --> Click on Actions drop down --> Security --> Change security groups --> Select security groups --> Add security group --> save

## Accessing Our EC2 Instance
**How to SSH into EC2 instance**
- SSH allows you to control/access a remote machine
![image](https://github.com/user-attachments/assets/173188a0-4cf3-4abd-9d75-7e0e772a1186)
- In instance there will be a `connect` button
![image](https://github.com/user-attachments/assets/8f106b1c-6b80-44a3-9d2f-0741760b03ec)
- EC2 Instance Connect --> Username (ec2-user) --> Connect
![image](https://github.com/user-attachments/assets/ddb11419-2ee4-44d4-9e62-4bb5aa8001dd)
![image](https://github.com/user-attachments/assets/918fdb35-ec4e-4d48-aced-ba715100316c)
- New window will be opened
![image](https://github.com/user-attachments/assets/019ef58c-778d-41a5-bdc4-10285d83ded0)
- Here we can run anything
- We add a script when we create the connection we can check the file name
![image](https://github.com/user-attachments/assets/087e3881-f28c-4c7d-b882-275b52214ef5)
- We can change inside that script
![image](https://github.com/user-attachments/assets/4d9798b9-9824-400e-b642-8f25fe2c7482)
![image](https://github.com/user-attachments/assets/ba9bba69-f2d9-474a-b3ad-6e2b8a674bea)
- after that we save the file useing `:wq` Enter
- check the html we use `cat index.html`
![image](https://github.com/user-attachments/assets/b6c437cb-4b85-4e56-a04c-a1a1c4140513)
- Check the OS `cat /etc/os-release`
![image](https://github.com/user-attachments/assets/81c83847-e3c9-4334-b469-ded698c7a0fc)
- Check the memory by using `free`
- Check the memory `df -h`

**SSH EC2 From Windows/Laptop**:
- Click on `SSH client
![image](https://github.com/user-attachments/assets/ea5ba3f9-1a32-4e62-ac64-3e9ac8d957c9)
- For `SSH client` we can use `putty` --> Download Putty
- We need the file which was downloaded when we created the instance `mywebserver-key.pem`. Now we need to change the format. For that we can use `PuTTYgen` --> Load the file using `Load` --> Save private file --> .ppk format
![image](https://github.com/user-attachments/assets/3da2c810-3e2b-4f75-91e4-93f9dddd359a)
- Now open the PuTTy give the IP address from the Public IP in `EC2 intance connection`
![image](https://github.com/user-attachments/assets/30f5dd20-a3b3-4d84-a6fc-9c7823bd2214)
- Then go to `SSH in left` --> `Auth` --> `Credentails` --> Load the `.ppk` file
![image](https://github.com/user-attachments/assets/6e7ca329-2e4e-4a39-8d23-ce9e91b5c06b)
- Then go to `session` we can save it also by given a name and press the save button
![image](https://github.com/user-attachments/assets/55ce246e-9555-473a-bb3b-ef698985f2b0)
- Select the name press open --> Accept --> loging asL ec2-user
![image](https://github.com/user-attachments/assets/c84ce816-aaac-4a7c-aee0-637e2f907175)
- We don't need password because it key based authentication
- If we don't want to give the user name again and again then we can change the Host name little and save it
![image](https://github.com/user-attachments/assets/a6bab7f1-ba22-4731-8ce0-2aa287b11988)

## Teminate the EC2 because we have limited time access in Free
- Click on `Instance state` --> `Stop instance` / `Terminate (delete) instance`
![image](https://github.com/user-attachments/assets/c9382d67-969a-4b92-aad0-a52e81502111)

## Instance Type:
- General Purpose
- Compute Optimized
- Memory Optimized
- Accelerated Computing
- Storage Optimized

### Use case:
- Case 1: Small Website or Blog
  - Suitable Type: t3.micro or t3.small(General purpose)

- Case 2: E-Commerce Application
  - Suitable Type: m5.large or m4.xlarge (General Purpose)
 
- Case 3: Real-Time video Rendering and Streaming (Accelerated Computing)
  - Instance Type: g5.12xlarge or g5.24xlarge
 
- Case 4: In-Memory Database for Real-Time Analytics (Memory Optimized)
  - r6g.16xlarge or x2idn.32large(Memory Optimized)
 
### Purchasing Options
- On-Demand: Short-term, unpredictable workloads
- Reserved Instances: Long-term, stready workloads (1-3 years)
- Spot Instances: Fault-tolerant, flexible, batch jobs, big data, CI/CD, distributed computing
- Saving plans: Consistent workloads but needing more flexibility than Reserved Instances
- Dedicated Hosts : Workloads requiring complete hardware control (compliance, software licensing)
- Dedicated Instances: Workloads needing physical isolation without full control over the hardware
![image](https://github.com/user-attachments/assets/50c887b0-eeca-4b23-85da-90054fffc996)
![image](https://github.com/user-attachments/assets/fc1f298e-f681-49eb-90a2-9275c6b70e3e)
![image](https://github.com/user-attachments/assets/f5548874-cd07-48e9-9933-6f5958d15e5c)









