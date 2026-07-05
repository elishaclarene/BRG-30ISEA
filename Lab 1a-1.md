Lab 1a-1 

Overview
This lab was to set up a linux environment using virtualization software. The goal was to successfully install and configure a virtual machine running Ubuntu linux and to understand the basics of virtualisation, installation steps and network configuration.

Tools that I used in the process:
VMware Workstation (VirtualBox was attempted at first), Ubuntu Desktop ISO, Git and GitHub

I first downloaded and installed VirtualBox and tried to set up a virtual machine with Ubuntu. However, Ubuntu was having booting and loading issues on VirtualBox and could not run properly. It seemed like it was a hypervisor-related compatibility issue with my computer hence why it was having a lot of issue with trying to run Ubuntu in VirtualBox. It had caused the virtual machine to freeze during the boot process for a very long time. I eventually was advised to switch to VMware Workstation which helped me resolved the problem, indicating that the issue was related to the virtualization platform rather than the Ubuntu installation itself.

<img width="500" height="350" alt="photo_6217736004970418368_w (1)" src="https://github.com/user-attachments/assets/f56308b1-2810-4f46-87bb-6224d1c30ff1" />
<img width="500" height="350" alt="photo_6217736004970418369_w (1)" src="https://github.com/user-attachments/assets/2cc78636-86b4-4f9f-8f01-805c5647ea16" />


Because of the technical issues i faced, i decided to use VMware Workstation instead. 
By using VMware, I successfully created a new virtual machine and installed Ubuntu without issues. After installation, i configured the network settings using NAT so the VM could access the internet.

<img width="500" height="350" alt="Screenshot From 2026-07-04 18-42-35" src="https://github.com/user-attachments/assets/06025fe0-8f96-406d-ba06-e6bccfa24dd3" />
