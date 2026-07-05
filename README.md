Lab 1a-1 

Overview

This lab was to set up a linux environment using virtualization software. The main goal was to install and configure a virtual machine running Ubuntu linux and to understand the basics of virtualisation, installation steps and network configuration.

Tools that were used:
VMware Workstation (VirtualBox was attempted at first), Ubuntu Desktop ISO, Git and GitHub


Steps Completed

I first downloaded and installed VirtualBox and tried to set up a virtual machine with Ubuntu. However, Ubuntu was having booting and loading issues on VirtualBox and could not run properly. It seemed like it was a hypervisor-related compatibility issue with my computer hence why it was having a lot of issue with trying to run Ubuntu in VirtualBox. It had caused the virtual machine to freeze during the boot process for a very long time. I eventually was advised to switch to VMware Workstation which helped me resolved the problem, indicating that the issue was related to the virtualization platform rather than the Ubuntu installation itself.

<img width="500" height="350" alt="photo_6217736004970418368_w (1)" src="https://github.com/user-attachments/assets/f56308b1-2810-4f46-87bb-6224d1c30ff1" />
<img width="500" height="350" alt="photo_6217736004970418369_w (1)" src="https://github.com/user-attachments/assets/2cc78636-86b4-4f9f-8f01-805c5647ea16" />


Because of this technical issues, i switched to VMware Workstation. 
By using VMware, I successfully created a new virtual machine and installed Ubuntu without issues. After installation, I configured the network settings using NAT so the VM could access the internet.

<img width="500" height="350" alt="Screenshot From 2026-07-04 18-42-35" src="https://github.com/user-attachments/assets/06025fe0-8f96-406d-ba06-e6bccfa24dd3" />


Once Ubuntu was running properly, i installed Git inside the system. I then created a GitHub repository and cloned it into the Linux environment for documentation purposes. 

<img width="500" height="400" alt="photo_6219962228253855846_w" src="https://github.com/user-attachments/assets/f36aee01-5e95-48b0-8377-77d75c6eb454" />


Challenges Faced

I ran into issues with Ubuntu not booting properly on VirtualBox, including freezing and long loading times. I also had some confusion at the start with VM settings and network configuration. These issues were eventually solved by switching to VMware which worked more smoothly and was way more stable.


What I Learned

From this lab, i learned how virtualization allows multiple operating systems to run on one physical machine. I also understood the differences between VirtualBox and VMware especially in terms of stability and performance.
In addition, i gained hands-on experience setting up a linux environment, configuring basic network settings and using Git and GitHub for version control. It was not easy but i think it helped me to gain a better understanding on downloading stuff.


Reflection

This lab helped me to become more confident in using Ubuntu and working with virtual machines. Even though I faced technical problems during setup, troubleshooting them helped me understand virtualization better.
It also gave me a clearer idea of how linux is used in real IT environments like system administration and software development. If i were to do this lab again, i would double-check the VM settings and system requirements before starting to avoid installation issues.


Conclusion

Overall, I was able to successfully install and configure an Ubuntu virtual machine using VMware. This lab gave me a solid introduction to linux environments, virtualization and basic system setup which will be useful for future labs and IT work.
