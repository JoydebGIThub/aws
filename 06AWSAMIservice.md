# AMI Service
- Amazom Machine Image
- An `Amanzon Machine Image` (AMI) is a pre-configured template the provides the necessary information to launch an EC2 instance in AWS.
- It includes:
  - Operating System (Linux, Windows)
  - Application server (Apache, Nginx)
  - Pre-installed software and configurations.
 
- Its not only an operating system, its kind of `Image` that we can say `template` or `blue print`. All the necessary packages, software etc everything already present there so our time is safe.

## Process
- 1st we create an EC2 instance
- 2nd HTTP / Apache server installed
- 3rd set up a customize wesite there

![image](https://github.com/user-attachments/assets/25236565-0612-4459-a1c4-1e7a4c57cb38)

- Let assume the 1st created instance was for a `texting environment` so now we want to deply it in production
- For production we need OS, Apache web server version, web server configuration so all of this need to be same or consistant.
- So, for this we can directly go to **Actions --> Image and templates --> create image**

![image](https://github.com/user-attachments/assets/e3e277bb-3734-4fa9-829d-46942e41e733)

- Give a `image name` with a version so that in future we can create more image version of it, unselect the `Reboot instance`, create Image

![image](https://github.com/user-attachments/assets/5f5ba88f-f0d2-494d-a509-97bfa83bd643)

- After that in the left side of the page we get `Images --> AMIs` there i can find the created image

![image](https://github.com/user-attachments/assets/981eb944-a79f-488b-8592-07ed10db2b80)

- Now we select the image --> `Launch instance from AMI`

![image](https://github.com/user-attachments/assets/30a99471-afda-4f3b-b162-ed1fa0dfc43e)

- Give the name of the new instance, we can change the `Instance Type` for higher version (t3-micro) for production, select the `key pair name`.
- We need to access the wesite so `Allow HTTP traffic from the internet` --> Launch Instance

![image](https://github.com/user-attachments/assets/4b324552-eba3-48f8-99e1-476efe8f5efe)
![image](https://github.com/user-attachments/assets/bd08a132-5cdb-48ae-a69c-3202dc5a57e0)
![image](https://github.com/user-attachments/assets/0d83da20-7947-41b6-b378-45e46f08e8a2)
![image](https://github.com/user-attachments/assets/a294fc83-bf35-4171-938c-c5fb30740a1d)

- Select the new instance and copy the public Ip then run it

![image](https://github.com/user-attachments/assets/81c8ee4a-e24f-4d0a-9dda-4aa424d5fa0d)

- With an AMI, you can launch new EC2 intances with a consistent, predefined configuration. You can also create custom AMIs to include specific software or settings, allowing for quick replication of environments.

## Types of AWS AMIs
- `public AMIs`: Available to all AWS users. Useful for basic use cases like popular operating systems (ubantu, CentOS)
- `private AMIs`: Created by a user and only available within that account or shared with specific accounts.
- `Paid AMIs/ Marketplace AMIs`: Provided by third parties through AWS Marketplace, offering software like databases, web servers, or pre-configured environments
- We can check through AMI catelog

![image](https://github.com/user-attachments/assets/6e2a1ab9-db82-4fcd-b5f1-4ed2114986d4)

### UseCase of Paid AMIs:
- `Rapid Deployment`: The LAMP stack is pre-configured, eliminating the need to manually install and configure Apache, MySQL, and PHP
- `Scalability and Load Balancing`: Running on AWS enables quick scaling to match website traffic, while Elastic Load Balancer helps in distributing requests.
- `Cost Efficiency`: You only pay for the infrastructure and the software according to your usage.

![image](https://github.com/user-attachments/assets/c06ca1c7-6f89-4afd-a5f1-060406de48bc)
![image](https://github.com/user-attachments/assets/7bd4c31c-1c06-4ee0-8af1-24d679e27491)

## Run Cleanup Script:
- In testing invironment we give access to multiple user and they can access but we need to avoid this in `prod` so for this we need to clean up

![image](https://github.com/user-attachments/assets/45f82f3d-abf5-498c-bc1f-b741999759b5)

## Create Lanuch Template VS Create Image:
- Template means the configuration of `EC2 instance` that will come
- Select the instance --> Actions --> Image and templates --> Create template from instance

![image](https://github.com/user-attachments/assets/88cba82a-ae57-4fd7-a614-753a1cb4dc0e)

- Give the templete name
- Select the AMIs --> My AMIs (webserver-v1)
- Select the `Instance type`
- Key pair name
- Create Launch templete
- After the instance create Go to Instances --> Launch Templetes

![image](https://github.com/user-attachments/assets/f7f580ad-4365-4be8-b9ff-c16eea53f9d0)

The benifies of it is that we don't need to configure the same type of instance again and again we can select the `Launch Templete` --> `Actions` --> `Launch instance from templete`

![image](https://github.com/user-attachments/assets/c868c2f9-970b-495e-8eff-d0a3123dea10)
![image](https://github.com/user-attachments/assets/3fda687d-4e06-4a2d-988a-24b1c49d0f14)

### Key Difference
![image](https://github.com/user-attachments/assets/032497dc-52af-440b-aa3b-d92d65f47d61)

## Summary
![image](https://github.com/user-attachments/assets/5b8ac09a-6578-42c8-9aff-205aae4e8e0d)

## EC2 Image Builder
In Left side Images --> AMIs --> EC2 Image Builder

![image](https://github.com/user-attachments/assets/9442d4ab-0c48-47c4-a6cd-da6547d8ecad)

When we can manually create the image then what it do:
- Automate VM or Image Creation
  - creation, testing, and deployment of AMIs
 
- Can be configured to run at regular intervals
  - (daily, weekly or monthly)
 
- Free

![image](https://github.com/user-attachments/assets/3bf7c009-f26b-4afa-94d0-adf92b351cc9)



