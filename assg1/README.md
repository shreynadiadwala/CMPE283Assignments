# CMPE 283 Assignment 1 Documentation

1. I worked on this assignment myself, without any other team member. First created the ideal environment in my PC - downloaded VMware Workstation 16 Player to create a Ubuntu 20.04 OS workstation, downloaded cmpe283-1.c file and make file from sjsu canvas. 

2. Forked the repo -> https://github.com/torvalds/linux , as instructed. 

3. Installed additional dependencies required to build a kernel using command ***sudo apt-get install libncurses-dev gawk flex bison openssl libssl-dev dkms libelf-dev libudev-dev libpci-dev libiberty-dev autoconf***. Ref - https://wiki.ubuntu.com/Kernel/BuildYourOwnKernel

4. Created structs of different MSRs in cmpe283-1.c file by referring to Intel SDM vol 3 and vol 3c. 
   Pinbased Controls referred from SDM vol 3, section 24.6.1
   Exit Controls referred from SDM vol 3c, section 24.7.1
   Entry Controls referred from SDM vol 3c, section 24.8.1
   Procbased Primary Controls referred from SDM vol 3c, section 24.6.2
   Procbased Secondary Controls referred from SDM vol 3, section 24.6.2
   
5. Executed the code module using ***make*** command. Then inserted module using ***sudo insmod cmpe283-1.ko*** command. Checked the output using ***sudo dmesg*** command.Initially encountered error beacuse the VTX was not enabled on VMware homescreen on my workstation, but it was resolved after enabling it.

## Steps to execute and check the output:

1. Download VMware workstation from the VMware website

2. Create Ubuntu virtual machine with 20.04 OS version. Enable VTX feature from VMware settings on its home screen.

3. Install git by executing "sudo apt install git". Clone the repo "https://github.com/torvalds/linux" by executing ***git clone https://github.com/torvalds/linux.git***

4. Download cmpe283-1.c file and make file from canvas. Download these files in previous step's cloned repo's folder (create a folder with your desired name in repo folder and download these files from canvas in it).

5. Execute ***sudo apt-get install libncurses-dev gawk flex bison openssl libssl-dev dkms libelf-dev libudev-dev libpci-dev libiberty-dev autoconf*** to install additional dependencies required to build a kernel. 

6. Build the module by executing ***make***. Insert or load the module by executing ***insmod cmpe283-1.ko***. Then see the output by ***sudo dmesg***. 

7. Unload the module using ***sudo rmmod cmpe283-1.ko***. Clean make file using ***make clean***. 

## Outputs 

### Pinbased Controls
![assg1 -pinbased](https://user-images.githubusercontent.com/89545745/200206798-a65f99e5-d005-420c-bb09-5215e5e5d35c.png)

### Entry Controls
![assg1-entry](https://user-images.githubusercontent.com/89545745/200206897-43f13a1e-da75-40f7-90e3-14dcd4edcae1.png)

### Exit Controls
![assg1-exit](https://user-images.githubusercontent.com/89545745/200206907-3de15918-e27c-499c-8557-d359f45b739a.png)

### Procbased Primary Controls
![assg1-procbased primary](https://user-images.githubusercontent.com/89545745/200206919-077a8735-84d8-4363-bf8d-665e6badbddc.png)

### Procbased Secondary Controls
![assg1-procbased secondary](https://user-images.githubusercontent.com/89545745/200206933-1a59264e-781e-439f-a8ba-5ff0c530eb3d.png)

