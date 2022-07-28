# Full Setup Stake Wars III - A New Validator

<p align-"center">
<img src="https://user-images.githubusercontent.com/78410824/181486582-f9bb7df1-7045-49b5-b15f-9b7354f97100.jpg" width="900px"/>
</p>

## Recommended Hardware Requirements

- 4x CPUs ( Faster Clock speed is better )
- 8GB Memory RAM
- 500GB of storage ( SSD or NVME )
- Permanent Internet connection ( traffic will be during devnet; 10Mbps will be plenty - for production at leas 100Mbps is expected )

## GCP Setup

Before you scrolling down, please make sure that you already have GCP ( Google Cloud Platform ) account, if you don't you can [register here](https://console.cloud.google.com)

1. Create VM ( Virtual Machine )

    This is the GCP Home Page
    
    <img width="1000" alt="1" src="https://user-images.githubusercontent.com/78410824/181489895-e0be57f0-8588-449d-b714-592dc1c98ec0.png">

    Look at the top right corner, drag your cursos to the 3 lines then click it

    <img width="400" alt="2" src="https://user-images.githubusercontent.com/78410824/181484402-88e037d3-85f3-41e5-b589-31753119dc3f.png">
    
    Now, drag your cursor to `Compute Engine` and select `VM Instance`

    <img width="800" alt="3" src="https://user-images.githubusercontent.com/78410824/181484417-f51c414a-3df0-406e-afd6-0096d2c9ec84.png">
    
    Select `Create Instance`

    <img width="1000" alt="4" src="https://user-images.githubusercontent.com/78410824/181484424-bc8f4aa1-4442-4759-85d6-bd0ab9781553.png">
    
2. Name the VM, choose the regional and specification 

    <i>It's highly recommended to choose the type as shown in the picture or at least according to the recommendations</i>    
    
    <img width="1000" alt="5" src="https://user-images.githubusercontent.com/78410824/181484430-d635457b-ec5f-4d03-a23e-da25edf7e5d7.png">
    

3. Set your storage

    On `Boot Disk`, go to `Change`

    <img width="800" alt="6" src="https://user-images.githubusercontent.com/78410824/181484435-59825085-4b3d-47ef-81c0-0fa80175ce0e.png">
    
    Change the OS to Ubuntu 20.04 LTS ( x86/x64 ) and input the storage value ( 500GB; recommended ) then click `Select` button

    <img width="800" alt="7" src="https://user-images.githubusercontent.com/78410824/181484440-e4ca705f-5063-4cc7-bf44-80fc1171b69f.png">
   
   
4. Check your `Boot Disk` and your `Monthly Estimation`

    Make sure everything is correct

    <img width="1000" alt="8" src="https://user-images.githubusercontent.com/78410824/181484444-74f850be-13cf-4f94-acd3-0e6c7792d486.png">
    
5. Checklist All Firewall then `Create`    

    <img width="400" alt="9" src="https://user-images.githubusercontent.com/78410824/181484449-bc2810ad-6a87-4354-916d-f87550638cc5.png">
    
6. How to use the VM

    After VM is ready, drag your cursor to the `Down Arrow` and click it, look at the picture bellow in the Red Box if you didn't notice

    <img width="1000" alt="10" src="https://user-images.githubusercontent.com/78410824/181484453-c4b3310b-296c-4c17-9f1c-4a73e4e9d331.png">
    
    Select `Open in browser window`

    <img width="400" alt="11" src="https://user-images.githubusercontent.com/78410824/181484460-f0c68e88-15f5-4086-90ff-50b22e3b14c7.png">

7. VPS is ready to use

    <img width="1000" alt="12" src="https://user-images.githubusercontent.com/78410824/181484466-caac9977-a58b-459b-867d-502c7aaac5ff.png">
    
    ##### For prevent any trouble in the future, please always use these command to your VPS every before use
    
    ```bash
    sudo su
    ```
  
    ```bash
    cd
    ```
    
    `sudo su` = change user to root, this is very important for any kind of command that requires permission
    
    `cd` = change current directory to root directory
    
    
After that, you only can access the VPS on GCP website with your browser


## Challenge

