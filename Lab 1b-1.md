## Lab 1b-1 

Overview
This lab focuses on building practical skills in Linux system administration, networking and secure communication using a virtual machine environment. This lab activity has taught me how a Linux server can be managed and accessed remotely through different networking tools and services.


Starting off, i had to download Apeche using "sudo apt install apeche2" and tested on my browser on http://127.0.0.1

Here are the photos of me downloading and testing it. Everything was working fine! 

<img width="500" height="350" alt="Screenshot From 2026-07-05 22-29-49" src="https://github.com/user-attachments/assets/c13c42cd-7c65-496f-8bd8-e8cc4048e8b7" />
<img width="500" height="350" alt="Screenshot From 2026-07-05 22-31-22" src="https://github.com/user-attachments/assets/67d59870-f43a-406d-8d2a-ab44c597abcd" />



Next i also had to install an SSH server as well as Nmap using "sudo apt install openssh-server nmap"

These are the photos of me downloading the both of them:

<img width="500" height="350" alt="Screenshot From 2026-07-06 00-10-08" src="https://github.com/user-attachments/assets/e7778ad6-0a37-48b7-974b-b0eff480911c" />
<img width="500" height="350" alt="Screenshot From 2026-07-06 00-08-27" src="https://github.com/user-attachments/assets/efe5e553-39cb-4e39-bbe8-4e5a065e4b8f" />



Next i had to find my VM ip by using "ip a" 

Here is the result that i got: 

<img width="500" height="350" alt="Screenshot From 2026-07-05 22-36-08" src="https://github.com/user-attachments/assets/1e5ca479-cc25-46f0-8f55-afd76c39ed4a" />


Next, i used Nmap to scan the IP address in order to detect open ports and see what services were active on the machine.

Here are the photos: 

<img width="500" height="350" alt="Screenshot From 2026-07-06 00-10-58" src="https://github.com/user-attachments/assets/61bd1900-70c3-4b79-af88-843114dffb8e" />
<img width="500" height="350" alt="Screenshot From 2026-07-06 00-10-08 (1)" src="https://github.com/user-attachments/assets/15a63710-7329-49c7-98d4-f46514263c09" />

You see from the photos that port 80 and 22 are open and active.



I then set up the UFW firewall to manage incoming and outgoing network traffic.
Photo which shows the active rules:

<img width="722" height="464" alt="Screenshot From 2026-07-06 00-13-37" src="https://github.com/user-attachments/assets/75e4eab7-39e7-427a-a154-31e1269895cd" />


Next step was to create a new user and i have named it labuser

Photo:

<img width="700" height="400" alt="Screenshot 2026-07-08 181913" src="https://github.com/user-attachments/assets/8bcfc9c2-b88d-47e7-86d4-0243c5687065" />


Here is also a photo of me using SSH username@ip:

<img width="653" height="504" alt="Screenshot From 2026-07-06 12-13-47" src="https://github.com/user-attachments/assets/46bcf8e4-65f4-49ae-af36-24c7f1c83e89" />


Next was to download the wget files 

Photo of me downloading successfully: 

<img width="500" height="350" alt="Screenshot From 2026-07-06 00-46-36" src="https://github.com/user-attachments/assets/2e16169e-d7ce-4310-9bf2-77c844f2395c" />

After that, I created a directory called books and used the tar command to create an archive of the files in that folder.

<img width="500" height="350" alt="Screenshot From 2026-07-06 00-47-43" src="https://github.com/user-attachments/assets/7f65a026-8fff-416c-adf8-fb4687141f85" />
<img width="500" height="350" alt="Screenshot From 2026-07-06 00-48-30" src="https://github.com/user-attachments/assets/09a2f411-6025-49fd-a32c-5524b4aba6b7" />

Then i had to compress with "bzip.2 book.tar" 

<img width="500" height="350" alt="Screenshot From 2026-07-06 00-49-20" src="https://github.com/user-attachments/assets/e4f3d27a-17a4-4318-acfd-8a98bdb5e556" />

After that i had to decompress using "bunzip2" then extract "tar -xvf"

<img width="500" height="425" alt="Screenshot 2026-07-08 182131" src="https://github.com/user-attachments/assets/2bc13b7d-eb98-4823-9bb9-f05f27604f15" />




## Challenge Activities 

### Challenge 1 : 
As i did not have a partner machine, i used SSH to access my Ubuntu virtual machine from my host system and created a file remotely using the command line. This demonstrated how SSH allows remote system management through terminal access.

Here is a photo of me creating a file. "Hi labuser" :

<img width="505" height="351" alt="Screenshot 2026-07-06 105119" src="https://github.com/user-attachments/assets/a38b8086-3d34-4758-974c-d5494fb7cc34" />
<img width="505" height="355" alt="Screenshot 2026-07-06 110528" src="https://github.com/user-attachments/assets/d2126bce-3d58-46f7-b81d-916330bdcb31" />



### Challenge 2 : 

I attempted to launch gedit over SSH. Although the command started, no graphical window appeared because SSH provides terminal access only. Graphical applications require access to a display server (or X11 forwarding) which was not configured so gedit could not be used remotely. 

<img width="500" height="350" alt="Screenshot From 2026-07-06 11-10-59" src="https://github.com/user-attachments/assets/aed92df2-b760-4c85-8649-50c84abb2dcf" />



### Challenge 3 : 

For challenge 3 i had to use "scp file.txt user@host:/destination/" to send a file over the network. 
In this case i did "TEST1.txt" 

<img width="500" height="350" alt="Screenshot From 2026-07-06 11-52-36" src="https://github.com/user-attachments/assets/c366bad1-7407-4b26-8bdc-3b8f64f327a4" />


## Virtual NetWorking
For this part i had to clone my VM 

Here is a photo of me successfully cloning my VM:

<img width="498" height="467" alt="Screenshot 2026-07-06 120133" src="https://github.com/user-attachments/assets/306cd7f0-9969-4226-a7ea-1de07cb86a7a" />

I made sure that both was using the same NAT network adaptor before i procceded. 

By using my main VM first which i will refer to as "VM1". I checked its IP by using "ip a" 
This was the result that i got: 

<img width="500" height="350" alt="Screenshot From 2026-07-06 12-05-41" src="https://github.com/user-attachments/assets/bbef5ed7-dde4-42c2-bc20-7978cbb6f91a" />

Next i did the same thing with the clone which i will refer to as "VM2"
Results : 

<img width="500" height="350" alt="Screenshot From 2026-07-06 15-40-01" src="https://github.com/user-attachments/assets/b69bff8d-fbe2-4410-8cc5-00e4d419c071" />


After i found the IP of both VM, I went on VM1 and ping VM2.
Results : 

<img width="500" height="350" alt="Screenshot From 2026-07-06 12-08-57" src="https://github.com/user-attachments/assets/04f1f124-2355-4d39-a82f-e9f4649343f8" />


I also did the same thing but this time i ping VM1 in VM2.
Results : 

<img width="500" height="350" alt="Screenshot From 2026-07-06 15-41-40" src="https://github.com/user-attachments/assets/a44ecafb-4204-4b55-9c15-d67d8c478603" />


### Reflection 
This lab helped me understand how different Linux features work together to keep a system secure and efficient. I learned that a firewall helps manage which services and ports can be accessed, reducing the risk of unauthorised connections. Using SSH gave me a better understanding of how Linux can be used as a server as i was able to access and manage the system remotely without being physically at the machine. I also realised that file compression is useful because it reduces file sizes making it easier and faster to store and transfer over a network. Lastly, creating different user accounts showed me how user privilege management improves security by limiting what each user can access or modify, helping to protect important system files and settings.
