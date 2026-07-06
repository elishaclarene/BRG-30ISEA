Lab 1b-1 

Overview
This lab focuses on building practical skills in Linux system administration, networking and secure communication using a virtual machine environment. This lab activity has taught me how a Linux server can be managed and accessed remotely through different networking tools and services.


Starting off, i had to download Apeche using "sudo apt install apeche2" and tested on my browser on http://127.0.0.1

Here are the photos of me downloading and testing :

<img width="500" height="350" alt="Screenshot From 2026-07-05 22-29-49" src="https://github.com/user-attachments/assets/c13c42cd-7c65-496f-8bd8-e8cc4048e8b7" />
<img width="500" height="350" alt="Screenshot From 2026-07-05 22-31-22" src="https://github.com/user-attachments/assets/67d59870-f43a-406d-8d2a-ab44c597abcd" />


Next i also had to install an SSH server as well as Nmap using "sudo apt install openssh-server nmap"

These are the photos of me downloading the both of them:

<img width="500" height="350" alt="Screenshot From 2026-07-06 00-10-08" src="https://github.com/user-attachments/assets/e7778ad6-0a37-48b7-974b-b0eff480911c" />
<img width="500" height="350" alt="Screenshot From 2026-07-06 00-08-27" src="https://github.com/user-attachments/assets/efe5e553-39cb-4e39-bbe8-4e5a065e4b8f" />


Next i had to find my VM ip by using "ip a" 

Here is the result that i got: 

<img width="500" height="350" alt="Screenshot From 2026-07-05 22-36-08" src="https://github.com/user-attachments/assets/1e5ca479-cc25-46f0-8f55-afd76c39ed4a" />


I now had to do an nmap ip scan

Here are the photos: 

<img width="500" height="350" alt="Screenshot From 2026-07-06 00-10-58" src="https://github.com/user-attachments/assets/61bd1900-70c3-4b79-af88-843114dffb8e" />
<img width="500" height="350" alt="Screenshot From 2026-07-06 00-10-08 (1)" src="https://github.com/user-attachments/assets/15a63710-7329-49c7-98d4-f46514263c09" />


Now UFW firewall 

Photo: 

<img width="722" height="464" alt="Screenshot From 2026-07-06 00-13-37" src="https://github.com/user-attachments/assets/75e4eab7-39e7-427a-a154-31e1269895cd" />


Next was to create a new user. 

Photo:

<img width="722" height="464" alt="Screenshot From 2026-07-06 00-29-56" src="https://github.com/user-attachments/assets/07c7a0bb-4147-4d49-acd5-300bd44ec114" />
SSH ip@user photo: 

<img width="653" height="504" alt="Screenshot From 2026-07-06 12-13-47" src="https://github.com/user-attachments/assets/46bcf8e4-65f4-49ae-af36-24c7f1c83e89" />


Next was to download the wget files 

Photo of me downloading successfully: 

<img width="500" height="350" alt="Screenshot From 2026-07-06 00-46-36" src="https://github.com/user-attachments/assets/2e16169e-d7ce-4310-9bf2-77c844f2395c" />

I then had to create a dictory called "books" and create tar

<img width="500" height="350" alt="Screenshot From 2026-07-06 00-47-43" src="https://github.com/user-attachments/assets/7f65a026-8fff-416c-adf8-fb4687141f85" />
<img width="500" height="350" alt="Screenshot From 2026-07-06 00-48-30" src="https://github.com/user-attachments/assets/09a2f411-6025-49fd-a32c-5524b4aba6b7" />

Then i had to compress with "bzip.2 book.tar" 

<img width="500" height="350" alt="Screenshot From 2026-07-06 00-49-20" src="https://github.com/user-attachments/assets/e4f3d27a-17a4-4318-acfd-8a98bdb5e556" />

After that i had to decompress using "bunzip2" then extract "tar -xvf"

<img width="500" height="404" alt="Screenshot From 2026-07-06 00-50-30" src="https://github.com/user-attachments/assets/b05bf793-cc8a-42fa-992e-724c84e66fbe" />




