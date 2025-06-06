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








