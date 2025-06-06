# What is AWS?
- `AWS` (Amazon Web Services) offers a `vast range of services`, including `computer power`, `storage solutions`, `networking`, `databases` and much more.
- It offers a `pay-as-you-go` model, allowing you to pay only for what you use, which is ideal for optimizing costs.
- `AWS` was `launched in 2006` as the first `public cloud platform`.
- Started with `Amazon S3` for `storage` and `EC2` for `computer power`.
- Now expanded into offering over `200 fully featured services` across various domains like `AI`, `machine learning`, `IoT` and more...
- In real life `AWS services` are used by **Netflix, NASA** etc.

## What makes AWS so special?
- Scalability (If the application needs more resource or less resource so it will be flexible to scale it)
- Global Reach (The application's target reach will be in globally)
- Reliability 
- Security

## Market
- AWS in the Present Market, as per the CRN report:
```
Cloud Market share Q2 2024
AWS: 32 percent
Microsoft: 23 percent
Google Cloud: 12 percent
```

## Popular Services Provided by AWS:
Most popular ones include `EC2` for `scalable compute capacity`, `S3` for highly `reliable storage`, `RDS` for `managed databases`, `Lambda` for `serverless computing`, and `CloudFront` for `content delivery`.

## AWS Global Infrastructure
- 34 launched Regions
- 108 Availability Zones
- 600+ CloudFront POPs

## AWS specific roles:
1. Cloud Engineer
2. Solutions Architect
3. DevOps Engineer
4. Cloud Developer
5. Data Engineer
6. Cloud Security Specialist
7. Machine Learning Engineer
8. Cloud Consultant
9. AWS Support Engineer / Cloud Support Associate
10. Site Reliability Engineer (SRE)

---------------------------------------------------------------------------------------------------
# AWS Account Setup:
- Sign up for Free AWS
- AWS Free Tier
- Create a Free Account
- Email and mobile no verification
- Details of `Credit or Debit card`
- Purpose (Personal use)
- Document type (PAN)
- Document verification
- Basic support - free
- Complete sign up

## After login:
![image](https://github.com/user-attachments/assets/26021abc-0d73-49fc-963c-7ce594c3950f)

![image](https://github.com/user-attachments/assets/4fab2977-c987-4224-b333-634e85aaf77a)

### Location Stockholm
![image](https://github.com/user-attachments/assets/77cbb994-7583-419f-ad5e-9017ede02070)

### Services
![image](https://github.com/user-attachments/assets/43e52d0a-1fae-489f-9626-2e20c409938d)
- we also can click on `view all service` to see all the services

-------------------------------------------------------------------------------------------------
## AWS IAM Services
- AWS Identity & Access Management
- We can manage user by the help of this account
- If we work on an organization then multiple user need access that can be manage, created, permission by the help of `IAM`.

### Defination
- IAM is a service that helps you `securely control access` to AWS resources.
- It allows you to manage users, roles and permissions to define who can access what within your AWS environment

### Note:
- When we create an account there we create an `root` users that is the owner of the account and has all the access

![image](https://github.com/user-attachments/assets/f838b21c-4555-406e-a5ee-834f2b130e55)

### Uses:
- Click on IAM or direct search IAM

![image](https://github.com/user-attachments/assets/d00b6a64-fa7d-45b6-b130-d9a6bc458e57)

- after that we get an `IAM Dashboard` we can monitor here, here we can check the security risks

![image](https://github.com/user-attachments/assets/64fda6ab-8dad-4aa2-a2fb-bc6513aa7851)

- `IAM resouces` we can check the user / resource I created

![image](https://github.com/user-attachments/assets/59e651de-c4f7-4370-adcf-a933234542d0)

#### Note:
- Free Service: IAM is offered at no additional cost
- Global Service (Not reason specific)
![image](https://github.com/user-attachments/assets/7b55b30a-eede-4f29-8bae-4cd661902be6)
- Root account created by default, shouldn't be used or shared because we don't use in any company we used it `over the internet` so we don't used it, we need to create a new user and use thats credencial and use the services

## Create Users:
- You can create individual user accounts for people who need access to your AWS resources.

## Assign Permissions:
- You can assign specific permissions to users, groups or roles to control what actions they can perform on AWS services.

## Create Groups:
- You can group users together and assign permissions to the group, making management easier for multiple users.

![image](https://github.com/user-attachments/assets/b19f0d5f-9f9d-48b5-87c6-7775e51ae917)

### AWS IAM Create User:
- Click on the `user` in the left side:
![image](https://github.com/user-attachments/assets/7fbfd8fe-e8ff-4393-bc4a-502fa871ef34)
- Click on `Create User`
- Give `user name` and `provide access to AWS console` and click on `create IAM user`:
![image](https://github.com/user-attachments/assets/960c5200-ce5c-48ff-b764-414b0677d052)
- Custom the console password:
![image](https://github.com/user-attachments/assets/09deacbe-f23c-479d-b59e-84842a496272)
- In next step we need to give the permission (1. Add user to group, 2. Attach policies directly)
![image](https://github.com/user-attachments/assets/0cefb85e-12d7-42eb-b0d9-ae75dbb2470a)
- Create group by click on the button `Create Group`.
- Give a name to the group and give all the permission it need.
![image](https://github.com/user-attachments/assets/f81b07bb-b19a-462a-9c65-8f755a53a02f)
- Permissions are given in JSON format and the `AdministratorAccess` provide full access of AWS services:
![image](https://github.com/user-attachments/assets/878b8105-4cea-4356-bc25-a28dfb03c0f6)
- We define all the permission inside the JSON
- We give the "Version" then in "Statement" we set the "Effect": `Allow`, in "Action": `*` all the action, in "Resource": `*` all the resource
- We also can create our own policy by click `Create Policy`
![image](https://github.com/user-attachments/assets/0a64fb86-9132-4481-a5ec-1ccc84865a60)
- after give all the permission in the new policy we need to give a name to the policy
![image](https://github.com/user-attachments/assets/f6f36730-befe-4bfb-90ba-e2a86725afc3)
![image](https://github.com/user-attachments/assets/95af0fb6-e4c6-4f51-addf-94dc636d3314)
![image](https://github.com/user-attachments/assets/433e2e05-4641-4b67-b9d3-32fd965d73ff)
- After all done by clicking on the `Create user group` we create the group:
![image](https://github.com/user-attachments/assets/fc5a79b7-90c0-40db-b3d3-69093a511a78)
- After clicking on next then `create user` then we can download the details in .csv file
![image](https://github.com/user-attachments/assets/f8d0a873-e208-460b-98b5-177002961bb3)

### IAM Resources:
![image](https://github.com/user-attachments/assets/30edd7ba-2782-433d-bc59-9dd32105617a)
- We need to add the group to the user also
- So we open the user click on `Add user to groups` check the `admin`
![image](https://github.com/user-attachments/assets/eed9971c-aa9d-4523-928e-cfc6988800e8)

### How to access the user:
- Go to `Security Credentilas`
- Copy the `Console sign-in link`
![image](https://github.com/user-attachments/assets/b547ce72-317c-42aa-a780-ee1538645e48)
- Give the user name and password and sign in
![image](https://github.com/user-attachments/assets/58ec53c2-8f1c-44f6-b2dd-8f2dd3d9e27b)
- Now if we remove the `group` access from the `user` through the `root` then we get an `Access denied` error in `User groups`
![image](https://github.com/user-attachments/assets/10b18c97-2153-47df-953d-e6bddc0cf1ee)
- If we give the permission again then is alex
![image](https://github.com/user-attachments/assets/f61bf140-ec67-42fb-8619-7a51ae692988)

## Create Roles:
- You can create roles to assign temporary permissions to AWS services or users, especially useful for securely managing permissions across different AWS resources.

## Define Policies:
- You can create and attach custome policies to define fine-grained permissions for controlling access to AWS resources.

## Manage Federated Access:
- IAM allows integrating with external identity providers (like Active Directory) for centralized management of user access across AWS.

## AWS IAM MFA
- MFA (Multi-Factor Authentication) is an extra layer of security that requires users to provide `two or more forms of verifications`, like a password and a code from their phone, to access their accounts.
![image](https://github.com/user-attachments/assets/9e08b93a-1706-4f2e-894f-4a243a8ae9f6)
- MFA (username + password + security code)
- Add MFA for `root`
- Select MFA device give a `Device name`
![image](https://github.com/user-attachments/assets/ba83d2cd-61e6-4017-8cf2-a79cfd138857)
- Select the MFA device select the `Authenticator app`
![image](https://github.com/user-attachments/assets/4a35c242-e201-49de-a8de-1bc14cf2f626)
- Next Set Up device
- Install any app mentioned in the 1
![image](https://github.com/user-attachments/assets/25012d08-aab7-4729-aa0d-716743fbfe36)
![image](https://github.com/user-attachments/assets/73c0d7f4-ea22-40f6-bbe5-0260b153b95a)
- Using the add in the app we can `scan` the QR in the 2
- The provide the 1st MFA code 1 then after 30 sec MFA code 2 then Add MFA
![image](https://github.com/user-attachments/assets/8b671dde-aecf-4b51-a941-7f30f277bcf8)

## Ways of accessing AWS
- The `AWS Management Console` provides a graphical, web-based approach. Using the `CloudShell` we don't need the credencial because it only uses after we logged in
![image](https://github.com/user-attachments/assets/c6d2956a-1ac4-4946-9eb1-c114e2ce7d62)
- The `AWS CLI` provides a command-line, scripting approach. In our local system by using only the `terminal` in the bases of `command` perform some action then we use CLI. In the Management Console we need to present to run anything but by the help of CLI we can automate some repetative task, mantain task.
- `AWS SDKs and APIs` offer programmatic, code-based access, allowing users to integrate AWS directly into their applications. 
















