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
- Take backup of the storage so that if the data is deleted or correpted some how then we can retrive it from the backup

### What if we want to copy our data to
- New AZ
- New Region

## Example:
- If I want to copy the EBS1 from `a zone` to `c zone`
- 1st take a snapshot of `EBS1` then create a `EBS` with that in `C Zone`
![image](https://github.com/user-attachments/assets/b88ca079-2307-4166-a026-a9f4c5632d1a)
- Open the console create a folder save a file with some text
![image](https://github.com/user-attachments/assets/a21eeb5d-41f9-496b-8920-a34fbc1e4ec9)
- This will act as our data, Check the `Monitoring` in volumes
- Now for creating the `snapshot` --> Select the `volume` --> `Action` --> `Create snapshot`
![image](https://github.com/user-attachments/assets/ced7db4a-45c7-4d3b-af84-0dcdb46ce8cd)
- Give the description --> `Create a snapshot`
![image](https://github.com/user-attachments/assets/f721daea-1f7c-4659-ae55-8c6e2846b301)
- Now check the `snapshot` in the left side `Elastic Block Store` --> `Snapshots`
![image](https://github.com/user-attachments/assets/688da8af-7bcc-4f03-b781-73ff0684b491)
- Before use it the status of the `Snapshot status` should be `Completed`
![image](https://github.com/user-attachments/assets/922e58a9-7852-4acb-95ae-aa66b597a0e2)
- Now select the `snapshot`--> `Actions` --> `Create volume from snapshot`
![image](https://github.com/user-attachments/assets/4cb09264-f67b-43cc-9dc1-ea47389a3316)
- Here we can change the `Zone`
![image](https://github.com/user-attachments/assets/a2894f88-ea63-4b16-a558-804155ed2d39)
![image](https://github.com/user-attachments/assets/22ada172-ff05-4270-b24b-a5f4c8f12d31)
- Now we can create a new instance --> Change the `zone` through `Network settings` --> `Edit` --> and change the `Subnet` in your perticular `Zone`
![image](https://github.com/user-attachments/assets/f7cb8dde-9956-4a6b-8b7c-0f05c4975886)
![image](https://github.com/user-attachments/assets/c0518aa8-e10a-47c0-91c8-735df06704ef)
- now we can go to volume as the previous we can add the snamshot volume with the instance
- now for accessing the backup data we need to type `sudo file -s /dev/nvmelnlpl`
- now mount the storage with a point or directory `sudo mkdir /mnt/mybackup`
- So next where to mount `sudo mount -o nouuid /dev/nvmelnlpl /mnt/mybackup`
![image](https://github.com/user-attachments/assets/bfe1f4cb-428a-4c1c-9b84-1dc254588e44)
![image](https://github.com/user-attachments/assets/f502b307-e1be-4bd0-a3c8-ac5b5540b43e)
- check `df -h`
- then we can read the old data
![image](https://github.com/user-attachments/assets/bccf52c5-dce1-437d-9c87-1943544168a0)

## Unmount EBS
- After backup we can `unmount` it by using `sudo unmount /mnt/mybackup`
- If the target it busy then `sudo unmount -l /mnt/mybackup`
- Then check `df -l`
![image](https://github.com/user-attachments/assets/ce722cf9-36d0-47ee-8b55-0eef1fb5c687)
- Detach volume
![image](https://github.com/user-attachments/assets/88e1c79f-1538-4f47-a384-640d58172e2c)
- then delete volume
![image](https://github.com/user-attachments/assets/accc29be-619f-4975-8d86-534bd4aec550)
- also we can delete the instance also

## EBS Snapshot copy to other region
- Now I want to use the snapshot in another region
- Action --> Copy snapshot
![image](https://github.com/user-attachments/assets/5c2f5113-f549-437f-8e5a-e6534053c2cb)
- change the region
![image](https://github.com/user-attachments/assets/dc2dc37d-eff7-4cae-ab87-2358853feefc)
- For checking we can change the region then we can see the copied snapshot

## EBS encryption
When you create an encrypted EBS volume and attach it to a supported instance type, the following types of data are encrypted
- Data at rest inside the volume
- All data moving between the volume and the instance
- All snapshot created from the volume
- All volumes created from those snapshots

































