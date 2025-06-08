## AWS EBS
- Elastic Block Store
- Here we see how we can add storage, increase the size of the storage, add additional disk, back up the disk, retrive, snapshort transfer from one region to another in EC2 instance
- When we create the EC2 instance there we attache a storage through `Configure storage` that will be in the form of `Elastic Block Store`. To see that we can click on the right of the `Configure storage` as `Advance`. Then we will find `EBS Vloumes`

### Defination:
`AWS EBS` is a cloud-based storage service that provides durable, high-performance block storage for use with `Amazon EC2 instances`. It works like a virtual hard drive, allowing you to store and access data even when your EC2 instances are stopped or terminated.
![image](https://github.com/user-attachments/assets/8aab25f8-ac2c-4da1-a34e-b64f6bf61984)
![image](https://github.com/user-attachments/assets/e951bf11-3fb7-4633-a505-2b1f845eade1)
![image](https://github.com/user-attachments/assets/afb29cc6-c6e5-4380-b568-ee18989862a1)

#### UseCase
- For Example, if you're hosting a MySQL or PostgreSQL database, you need reliable, high-performance storage to handle frequent read/write operations.
- EBS provides persistent, fast storage that ensures you data is saved even if the `EC2 instance` is stopped or restarted, making it ideal for database workloads

## Important Points about EBS:
- Region & AZ (aviablity Zone) specific. Let assume in mumbai there is 3 datacenter (a, b, c). So you create EBS2 in the `a aviablity zone`, then if you again create your EC2 instance in `b zone` then the `EC2 instance` will not use the `EBS2`
- Build-in Redundancy
  - EBS volumes are automatically replicated (data safe) within the same Availability Zone to prevent data loss due to hardware failure. If something happend in the `a zone` particular block then also the data will be safe but if the whole zone is destroied then data will also destroied 
 
- Different Volume Types
  - gp2/3, io1/2, st1, sc1

![image](https://github.com/user-attachments/assets/69cabfd8-47d8-460e-a3b4-4315a3dd29e1) 

- Allow Encryption & Snapshot for backup

![image](https://github.com/user-attachments/assets/b34c723b-1b65-4628-9d01-36d4015ab4e8)
- Scalable (Volume can be resizeable)
  - No data loss will occure during resizing
  - No need to restart the EC2 instance during the process

## Practical
- After createing the intance we go to the left side and `Elastic Block Store` --> Vloumes
![image](https://github.com/user-attachments/assets/def936bb-04f3-42fb-af8e-e2bbc1818111)
![image](https://github.com/user-attachments/assets/6dcfae41-baa9-4223-ad07-d7ca5fcca75d)

### Termination on Delete
- If we go to the instance --> select it --> click on storage --> at the right corner we get a `column` called `Delete on termination` it will be Yes.
- It means if the instance is terminated then the EBS will be also terminated its by default
![image](https://github.com/user-attachments/assets/5723cb30-1a6e-4f97-9516-6c7f27e15e2e)
- To make it `no` when we `Launch instance` --> In `Configure storage` --> `Advance` --> expand the `volume` --> There will be a option called `Delete on termination` -->No
![image](https://github.com/user-attachments/assets/bdff5063-e8b8-4fe3-b45b-b066448a0f90)

## Create & Attach EBS
- Go to `Elastic Block store` --> `vloumes` --> `Create volume`
![image](https://github.com/user-attachments/assets/65d29ce6-15ec-49ac-afc2-31a53f6bc5a7)
- Create the volume in the same zone
![image](https://github.com/user-attachments/assets/4a640fcd-2113-4d5b-bbbf-21fc9a0ec501)
- By selecting the `volume` we can click on the `Action` --> `Attach volume`
![image](https://github.com/user-attachments/assets/e384edfd-c50d-4b2a-aa8d-23f9f047c76b)
![image](https://github.com/user-attachments/assets/a81a7088-a639-4ed6-b0d1-1a64ae8900d0)
- New we can check the storage through instance -> storage / through terminal
![image](https://github.com/user-attachments/assets/b31632c1-96cb-44f3-a13f-e49e1eae526d)
![image](https://github.com/user-attachments/assets/60e168fa-c4d2-4870-8f40-dcd5b2257b6e)
- To use it we need to `mount` it

## Modify Size EBS Volume
- Select the `volume` --> `action` --> `modify volume`
![image](https://github.com/user-attachments/assets/0ebe852f-8a84-41f2-b74f-5736f1b12413)
- We only `increase` the size of the `volumne`
![image](https://github.com/user-attachments/assets/08bdabf3-fba7-4886-a337-5465068c15dd)

## Detach or delete EBS
- First we need to detach the volume then we can delete it
![image](https://github.com/user-attachments/assets/70f34ee6-889a-497a-86b3-ed8004b1a62f)
![image](https://github.com/user-attachments/assets/cd75f20a-04cf-4207-aa25-eca7f3a5a2db)

## EBS Snapshot











































