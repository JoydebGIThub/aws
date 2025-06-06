# What is Virtualization?

## Why we need Virtual Machine?
- Let assume we work on a windows systeam and develope a application then the application is only work for windows.
- But if we want to use the app on `linux and windows both` then before publishing we need to test the application for the `linux` also
- So, for all that we need linux based system.
- But we can use Virtualisation to use any other OS over our basic `os`.
- Like if we need `Linus OS` then we can add `Virtualization` over the `Windows` and then add `Linux OS` over it. Also we can set up more than one `opperating system` over virtualization.

## How to setup Virtualization?
- The `virtualization` layer is called `Hypervisor`.
- **Hypervisor**: It is software that creates and runs virtual machines (VMs).
- We need `Hypervior` over our main machine to set up, maintain, and make `virtual machines`.
- One of the Hypervisor is `VirtualBox`

## How Hypervisor works?
- Virtual box share hardware resources from `Host OS`.
- Separate set of `virtual CPU`, `RAM`, `storage` etc.
- VMs are fully isolated(independent of hosted OS).
- Let assume we have `8GB RAM and 100GB HDD` with the helo of the `software` we divide the ram and HDD and create 2 separte `Virtual Machine`-> V1(2GB RAM 20GB HDD), V2(2GB RAM 10GB HDD). Over that `Virtual machine` we set up some `os` called `Linux` and `MAC`

![image](https://github.com/user-attachments/assets/ee77aea2-c08c-41bd-92cf-ef84f5ace0ac)

## Benefits of VMs
- We don't need new resources to use different OS.
- No risk of any issues with the primary OS. (All the vms are work in isolated environment).
- Testing any app on different OS

## Types of Hypervisor
1. Bare Metal
2. Hosted

## Bare Metal
- It will be directly `install` in any `harware` and it has no `host os`
- This type of `Hypervisor` works as `mini os`.
- So, basic os is present in it for set up in the `hardware`
- Example like `cloud provider` and `enterprise servers`.

![image](https://github.com/user-attachments/assets/cc83002e-ee63-4a05-9e9b-bfda6f1d4756)

### Hosted:
- Here will have a `HOST OS` and over that we use `Hypervisor`
- It called hosted because it's present over the `host or primary os`

![image](https://github.com/user-attachments/assets/f30ab0e8-66dc-439c-9159-a0d475978b72)

## Why companies use Virtualization?
- Cheap
- Reduces Workload, Space, Energy
- Easy backup using snapshot
- Easy recovery.

-------------------------------------------------------------------------------------------------------------
# What is Cloud Computing?
- On-demand delivery of IT resources over the Internet with `pay-as-you-go` pricing..
- Access `computing resoures` (like servers, storage, database and software) over the internet, rather than owning and maintaining physical hardware.
**Cloud Service Provider**:
1. Amazon Web Service(AWS).
2. Microsoft Azure
3. Google Cloud Platform(GCP).
4. IBM Cloud
5. Oracle Cloud
6. Alibaba Cloud
7. DigitalOcean
8. Salesforce
9. VMware CLoud
10. Rackspace Cloud.

- In this provider has there own big large physical servers.
- And they use Virtualization (is the process of creating multiple simulated environments or virtual machines from a single physical hardware system, enabling more efficient resource use.) and serve multiple user or organization `through cloud`.

## Use case of Cloud platform
- Let assume we want to do a business and you create an website
- And now you want to publish/live/deploye then we need to consider some points like (active 24/7, secure network for (ecomarch service), fast, backups, handle multiple users).
- Then for all this we can by many servers but then the maintainens, security, etc then its become complecated and costly.
- So, we have an better options called `rent`, we can rent a service like servers, storage etc from any Service Provider. And all the other necessary things will be handled by the provider we don't need to think about it.
- And we only pay for the part we use

![image](https://github.com/user-attachments/assets/bfd5bf55-bce6-40c6-8aaa-ce2f8a4b7c45)

## Types of cloud computing
1. IaaS
2. PaaS
3. SaaS

### IaaS (Infrastructure as a Service)
- IaaS contains the basic building blocks for cloud IT. It typically provides `access to networking features`, `computers` (virtual or on dedicated hardware), and `data storage space`.
- IaaS gives you IT resoures. It is most similar to the `existing IT resource` with which many IT departments and developers are familiar.

### PaaS (Platform as a Service)
- PaaS `removes` the need for you to `manage underlying infrastructure` (usually hardware and operating systems), and allows you to `focus of the deployment` and `management of your application`.
- This helps you be more efficient as you don't need to worry about the resource procurement, capacity planning, software maintenance, patching, or any of the other undifferentiated heavy lifting invloved in running your application.

### SaaS (Software as a Service)
- SaaS provides you with a complete product that is run and managed by the `service provider`. In most cases, people referring to SaaS are refering to `end-user applications` (such as web-based email). With a SaaS offering, you don't have to think about how the service is maintained or how the underlying infrastructure is managed. You only need to think about how you will use that particular software.
- We don't need to download it, we directly use it through internet.
- `Google sheet` is the best example we don't need to install it like `word excel` to use it we can use it in online.

## Different types of cloud deployments:
1. Public Cloud
2. Private Cloud
3. Hybrid Cloud

### Public Cloud
- A shared cloud environment where multiple users can access services over the internet, like `AWS` or `Azure`.

### Private Cloud
- A dedicated cloud environment for one organization, offering more control and privacy.

### Hybrid Cloud
- A mix of public and private clouds, allowing data and applications to move between them for flexibility.

## Few features commonly offered by cloud providers:
1. Compute Services
2. Storage Services
3. Database Services
4. Networking Services
5. Container Services
6. Serverless Computing
7. Machine Learning Services
8. Identity and Access Management (IAM)
9. Monitoring and Logging
10. Content Delivery Network(CDN)
11. Backup and Disaster Recovery
12. Security and Compliance Tools
13. Virtual Private Cloud (VPC)
14. Data Analytics Services
15. API Management










