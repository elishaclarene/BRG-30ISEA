## Lab 2b-1 

In this lab, i learned how to deploy a web server using Amazon EC2. I created an Ubuntu virtual machine in AWS, connected to it using SSH, installed Apache and hosted my own webpage online. I also learned how to transfer files to the server, create links to those files and monitor AWS costs using a budget alert.


I first created an EC2 instance using Ubuntu and configured the required network settings. A security group called ssh-and-web was created to allow SSH access for remote connection and HTTP access for viewing the webpage through a browser.

I used these following settings :
OS: Ubuntu Server 26.04 LTS
Instance type: t3.micro
Security group: ssh-and-web
SSH port: 22
HTTP port: 80


A photo of me setting the security settings:

<img width="1500" height="600" alt="Screenshot 2026-07-08 214612" src="https://github.com/user-attachments/assets/517e5f01-1e9d-40a4-8696-13c161ba646e" />


Next i launched my instance : 

<img width="1500" height="800" alt="Screenshot 2026-07-08 214959" src="https://github.com/user-attachments/assets/9914a7a9-480e-4219-8e76-5cb3b13ab36d" />



I then connected to the Ubuntu server using SSH with the key pair which was .pem that was created during the setup.
 I used the ssh -i aws-webserver-key.pem ubuntu@<public-ip> command. 

This allowed me to remotely access and manage the cloud server through the terminal.

This photo shows that the .pem file has been listed: 

<img width="700" height="400" alt="Screenshot 2026-07-08 215342" src="https://github.com/user-attachments/assets/dc221513-adb4-4f20-818e-e979d6dcadb3" />
<img width="700" height="400" alt="Screenshot 2026-07-08 215619" src="https://github.com/user-attachments/assets/28252b6f-4d37-4326-b089-54dc6f94b246" />

The photo above ^ shows that i logged into my AWS EC2 server over SSH which means that i had a successful SSH connection. 


After connecting to the server, I updated the Ubuntu packages and installed Apache. I used "sudo apt update" and "sudo apt install apache2"
I then checked the Apache service status by using "systemctl status apache2" to confirm that it was running successfully.

Photo: 

<img width="700" height="600" alt="Screenshot 2026-07-08 215940" src="https://github.com/user-attachments/assets/50db1e16-17bd-467d-a9f4-d2d5ccc37c84" />

You can see from the photo above ^ that Active: active(running)


After installing Apache, i tested the default Apache webpage using the EC2 public IP address on my webpage.
<img width="1500" height="700" alt="Screenshot 2026-07-08 220137" src="https://github.com/user-attachments/assets/7dad5669-fbdb-427a-9375-592aafb8c0d5" />

Once i have confirmed that the apache was running correctly, i proceeded to edit the index.html to create my own webpage. I did this by using the command "sudo nano /var/www/html/index.html" 


<img width="900" height="600" alt="Screenshot 2026-07-08 220654" src="https://github.com/user-attachments/assets/0f9dc3c7-2532-4777-8e41-234ba5babc4b" />



I edited the HTML file and added my own content. After refreshing the webpage, I was able to view the changes through the EC2 public IP address.

<img width="837" height="475" alt="Screenshot 2026-07-08 220742" src="https://github.com/user-attachments/assets/e5485052-49a6-4a60-9609-4fa552fd421b" />




### File Transfer & Permissions 

Once i was able to edit, i learned how to transfer files to the web server by downloading a file using wget and moving it into the Apache web directory.

Photo that wget was successfully downloaded: 
<img width="900" height="600" alt="Screenshot 2026-07-08 221029" src="https://github.com/user-attachments/assets/be234eeb-b813-48ac-9147-0e8f8c836958" />


And another photo that shows the PDF in my home directory in the folder that apache serves to visitors:
<img width="900" height="83" alt="Screenshot 2026-07-08 221145" src="https://github.com/user-attachments/assets/aaf900b3-c0ef-402d-9255-b053fe07d1c6" />


After transferring the file, i edited the HTML page and created a hyperlink using an anchor tag so that the file could be accessed through the webpage.

A photo of adding a hyperlink to my webpage: 

<img width="600" height="250" alt="Screenshot 2026-07-08 221747" src="https://github.com/user-attachments/assets/f3401265-1a23-4948-9e75-9f4f2420aa68" />


This what the PDF shows when i opened the link from the webpage : 

<img width="1000" height="750" alt="Screenshot 2026-07-08 221847" src="https://github.com/user-attachments/assets/38d7a8e1-5ec4-4e7f-9e35-35e680158724" />




### Budget and Cost Monitoring in AWS 

To prevent unexpected charges, i created a budget alert in AWS. This helped me understand the importance of monitoring cloud resources because running unused instances can result in additional costs. 

Photo:
<img width="1500" height="600" alt="Screenshot 2026-07-08 222953" src="https://github.com/user-attachments/assets/31fe9904-26d9-4a3e-884c-7b31dac8e07d" />


After completing the lab, i terminated the EC2 instance to ensure that no unnecessary resources were left running.

Photo: 

<img width="1500" height="800" alt="Screenshot 2026-07-08 223402" src="https://github.com/user-attachments/assets/9e5936bb-a58f-4e42-90a4-b30e64ea8965" />



### Reflection Questions 

Through this lab, i learned that cloud deployment provides more flexibility compared to local virtualisation because servers can be accessed remotely through the internet and resources can be adjusted when needed without managing physical hardware. Apache serves files by retrieving content stored in its web directory, such as "/var/www/html/" and i verified this by accessing my EC2 public IP address and viewing the webpage after modifying the "index.html" file. I also learned that Linux file ownership and permissions are important because they control who can access or modify files which is why administrator privileges like "sudo" are sometimes required. Leaving cloud instances running can result in unexpected charges and security risks so resources should be monitored and terminated when they are no longer needed. Lastly, I learned that DNS is used globally to translate domain names into IP addresses while "/etc/hosts" is a local file that manually maps names to IP addresses on a specific device, making it more suitable for testing or small environments.

