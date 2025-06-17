# AWS ELB
- ELastic Load Balancing (ELB)
- Auto Scaling Groups (ASG)

## Scalability
- Scalability means the ability to grow your system's resources when your application or website gets more `traffic or more users`.

### Virtical Scalability (Scaling up)
- Vertical Scalability means adding more power (CPU, RAM) to your existing server
- t2.micro to m5.large

### Horizotal Scalability (Scaling Out)
- Horizontal Scalability means adding more instances (servers) to distribute the load
- You can add more EC2 instances behind a load balancer

## High Availability (HA)
- High Avalability (HA) means keeping your service up and running with `minimal downtime`, so it's always accessible to users.
- Ex: running resources in multiple AZs (avalability Zone)

## Elasticity
- Elasticity means the ability to automatically adjust resources as the demand changes- adding more when needed and removing when it's no longer necessary.
- ASG (Auto Scaling Group)

## Load Balancing:
![image](https://github.com/user-attachments/assets/422b6ee7-7128-462a-910f-066d0e704ec7)

- If we have `multiple instance` then which instance the request needs to forworded that will be decided by **Load Balancer**
- `Load Balancer` is like an addintional server which work is to set in the front and accept the request and distribute it to different instances.
- We also create the instances in different Zones

![image](https://github.com/user-attachments/assets/8579b4c9-b106-4bc4-80cb-e1fc065e7b34)

- The advantages is Load will distributed properly and we also get High Availability. If any instance has error then other instance will be work properly

![image](https://github.com/user-attachments/assets/9ca112b9-0b00-4f01-bd84-52c352abe839)
