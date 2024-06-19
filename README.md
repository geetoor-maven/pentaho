<h1 align='center'>Guidebook Pentaho on Ubuntu 22.04</h1>

## 1. install Virtual Box

- install virtual box the latest version according to your operating system : https://www.virtualbox.org/wiki/Download_Old_Builds_7_0
ㅤ
- After being downloaded, You can install Virtual Box with tutorials found on Google : 
- https://data-flair.training/blogs/install-virtualbox/
- https://www.geeksforgeeks.org/how-to-install-virtualbox-on-windows/

- If successful, you can open a virtual box and get a look like this
![virtualbox-1](img/virtualbox/vb1.png)

## 2. Create VM Ubuntu 22.04 in Virtual Box

- install iso ubuntu 22.04 : <a href='https://releases.ubuntu.com/jammy/ubuntu-22.04.4-desktop-amd64.iso' target='_blank'>Download Here</a>

- After you download iso ubuntu 22.04 -> Open your Virtual Box and Create New Virtual Machine.

- Give your virtual machine name with the name ubuntu, and the type is Linux and the version is Ubuntu(64-bit) and click next
![virtualbox-1](img/vm/vm1.png)

- For good performance Adjust RAM to 4GB (4096 MB) or less according to your system configuration.
![virtualbox-2](img/vm/vm2.png)

- Let the "Create a virtual hard disk now" option selected and proceed to the next step

- Select the type of Hard disk. Using VDI type is recommended.

- Either of the Physical Storage types can be selected. Using a Dynamically Allocated Disk is by default recommended.

- Select Disk Size and provide the Destination Folder to install and Allocate about Minimum 30GB of virtual space. and click Create
![virtualbox-2](img/vm/vm3.png)

## 3. Starting Ubuntu Virtual Machines 22.04
