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

