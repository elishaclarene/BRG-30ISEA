## Lab 1a-2 

The objective of this lab was to get familiar with the Ubuntu operating system by using both the graphical user interface (GUI) and the command-line interface (CLI). Throughout the lab, I learned how to perform basic file operations, understand user permissions, use simple networking and system information commands and install software using different methods.


For Part 1 

I explored the Ubuntu desktop environment by opening firefox as well downloading LibreOffice Writer to create a document, navigating folders with the files application and accessing the Ubuntu App Center. This helped me become familiar with the Ubuntu graphical interface and its built-in applications.

In this photo is me downloading an application on Ubuntu (LibreOffice) 

<img width="500" height="350" alt="Screenshot From 2026-07-05 15-09-22" src="https://github.com/user-attachments/assets/3716b701-0518-4238-8a0d-979d0ef735a8" />

In the photo shown here is me trying to make a document in LibreOffice Writer using Ubuntu.

<img width="500" height="350" alt="Screenshot From 2026-07-05 15-21-32" src="https://github.com/user-attachments/assets/7b12961a-31fe-4e74-9002-2e0bbe428004" />


For Part 2 

I got to try out different linux commands and became more familiar with using the terminal. I used commands like "pwd" and the different "ls" commands to see where I was and viewed the files in a directory. I also used "p -e" and "top" to check the processes running on the system. Other than that, i created a text file with "touch" edited it using "nano" and viewed it with "cat" and "less". These activities gave me more confidence in navigating the Linux file system and using basic command-line commands.

This picture is me using the "top" command 

<img width="500" height="350" alt="Screenshot From 2026-07-05 15-26-19" src="https://github.com/user-attachments/assets/6d00128f-5911-4180-8dc4-b687a5d4f37a" />

This picture is me using commands like "nano" / "ls" and "cat"

<img width="500" height="350" alt="Screenshot From 2026-07-05 15-27-54" src="https://github.com/user-attachments/assets/54234346-2089-4886-a0fa-3900442a5aa6" />


For Part 3

In this part of the lab, I learned about linux user permissions and the difference between a normal user and the root user. I used the whoami and sudo whoami commands to compare the two and see how administrator privileges work. I also created a new user account using adduser and learned that sudo should only be used when higher permissions are needed to perform certain tasks.

Here are the photos of me trying out the "whoami" and making a new using adduser : 

<img width="500" height="350" alt="Screenshot From 2026-07-05 15-29-48" src="https://github.com/user-attachments/assets/831c4232-893f-4cc9-8c53-70ac7bdc18f6" />
<img width="500" height="350" alt="Screenshot From 2026-07-05 15-31-39" src="https://github.com/user-attachments/assets/7a4a891e-8768-423d-beb6-29877b06ab5f" />


For Part 4 

This part of the lab focused on basic networking in Ubuntu. By using the ip a command, i identified my private IP address and checked that the network was configured correctly. To confirm internet connectivity, I used ping with Google's DNS server (8.8.8.8). I then modified the /etc/hosts file by adding a custom hostname alias and verified that it worked using the ping command. Lastly, I explored the nslookup and whois commands to retrieve information about domains and see how domain names are linked to IP addresses.

Here are the photos: 

<img width="500" height="350" alt="Screenshot From 2026-07-05 15-32-44" src="https://github.com/user-attachments/assets/e11c4797-dd2f-46a1-88e7-4e3e05e63bf3" />
<img width="500" height="350" alt="Screenshot From 2026-07-05 15-33-11" src="https://github.com/user-attachments/assets/9c2f3dec-95c8-4e43-bd03-209d3b2ace88" />
<img width="500" height="350" alt="Screenshot From 2026-07-05 15-33-33" src="https://github.com/user-attachments/assets/5888b941-adef-4b1b-9092-aeb19b8e7bf2" />
<img width="500" height="350" alt="Screenshot From 2026-07-05 15-48-41" src="https://github.com/user-attachments/assets/6a885656-a2a6-42b5-b621-8c4cc9d03be6" />


Photo for the "nslookup" and "whois" :
<img width="500" height="350" alt="Screenshot From 2026-07-05 15-47-51" src="https://github.com/user-attachments/assets/39757beb-e49c-48af-a275-e9f62654d381" />


For Part 5 

I got to explore different commands to view system and hardware information. I used uname -a, lsb_release -a and hostnamectl to check details about the operating system. To learn more about the hardware, I ran lsusb, lspci, and viewed /proc/cpuinfo. I then compared the information shown in the terminal with what was displayed in Ubuntu's graphical settings to better understand the different ways of accessing system information.

Here are the photos: 

<img width="500" height="350" alt="Screenshot From 2026-07-05 15-34-48" src="https://github.com/user-attachments/assets/aebaf71c-4793-4ba9-a1d1-17b88dc83ca7" />
<img width="500" height="350" alt="Screenshot From 2026-07-05 15-35-36" src="https://github.com/user-attachments/assets/a37912bf-50d6-45a2-9b79-d281fa1e1627" />
<img width="500" height="350" alt="Screenshot From 2026-07-05 15-37-48" src="https://github.com/user-attachments/assets/c5c628ef-2451-44dc-8901-7cd8ee5db863" />


For Part 6 

For this part I explored different ways of installing software in Ubuntu. I updated the package list using sudo apt update. Upgraded existing packages with sudo apt upgrade and installed LibreOffice through the terminal using the APT package manager. I also used sudo apt search to look for available packages and explored Ubuntu's software repositories to better understand where trusted software comes from. 

Here is a photo of me installing LibreOffice using the APT package manager:

<img width="500" height="350" alt="Screenshot From 2026-07-05 15-09-22 (1)" src="https://github.com/user-attachments/assets/cac00853-ddb1-4478-93eb-96619c949e9d" />


Reflection 

Using the CLI throughout this lab gave me a better understanding of how Linux works because I had to complete most tasks using commands instead of relying on the graphical interface. At the start, I found it quite confusing and had to keep referring back to the lab guide. However, after practising the commands several times, I gradually became more comfortable using the terminal. I also learned that terminal-based editors such as Nano are better suited for remote access since they can be used without a graphical interface. Overall, this lab helped me build more confidence in using Linux and showed me that the CLI can be much faster and more efficient once I became familiar with the commands.
