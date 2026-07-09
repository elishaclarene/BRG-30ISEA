## Lab 3a-1

This lab focused on setting up an internet-facing web server using cloud infrastructure. I configured an AWS EC2 virtual machine, connected it with a free DuckDNS domain, hosted a website using Nginx and secured the website with HTTPS using a Let's Encrypt SSL certificate.


### Setting up AWS EC2 instance

I started by launching an Ubuntu EC2 instance on AWS.

The security group was configured to allow:
- Port 22 for SSH access
- Port 80 for HTTP traffic
- Port 443 for HTTPS traffic

Photo of me launching instance : 

<img width="1500" height="705" alt="Screenshot 2026-07-09 151712" src="https://github.com/user-attachments/assets/47f9d77d-dddf-4e7b-9ad2-8beb92ea3982" />

After launching the instance, i connected to the server through SSH and updated the system packages.



### Configuring DuckDNS domain

I then used DuckDNS to create a free subdomain. My subdomain was : lab3a1-clarene.duckdns.org

Photo: 

<img width="1000" height="750" alt="Screenshot 2026-07-09 153120" src="https://github.com/user-attachments/assets/15615262-909d-4129-a1ff-f138d8ecbc82" />


I created an updated DuckDNS script that was created on the server to link the domain name with the EC2 public IP address. The script was then made executable and tested by using " chmod 700 duck.sh " and "./duck.sh"


<img width="850" height="200" alt="Screenshot 2026-07-09 153652" src="https://github.com/user-attachments/assets/44477fcc-da6c-4f95-a056-4254418602bf" />

The photo above ^ shows the nslookup which shows that the domain is resolving


### Installing Nginx web server

After that, i downloaded Nginx and was installed as the web server for hosting the website.

Photo: 

<img width="900" height="450" alt="Screenshot 2026-07-09 153918" src="https://github.com/user-attachments/assets/5b90d0fa-603e-4737-b8b2-20785b69d28a" />

This photo above ^ shows that Nginx is running. You can see from the photo of the " active : active (running) " 

Then i checked if the default Nginx welcome page was accessed through my servers public IP address to confirm that the web server was working correctly.


Photo that shows the Nginx welcome page: 

<img width="1300" height="300" alt="Screenshot 2026-07-09 154118" src="https://github.com/user-attachments/assets/5206b4e4-244d-46b9-85bf-7058cb046b4e" />



### Configuring DNS resolution

Then i tested the connection between the DuckDNS domain and the EC2 server by using " ping lab3a1-clarene.duckdns.org " 

Photo: 

<img width="900" height="130" alt="Screenshot 2026-07-09 154438" src="https://github.com/user-attachments/assets/1cf7a08a-d2ca-4871-bfb8-54e02c1868af" />

The returned IP address was compared with the EC2 public IP address to confirm that the domain was pointing to the correct server which it was.



### Enabling HTTPS with Let's Encrypt

To secure the website, Certbot was installed to obtain a free SSL/TLS certificate from Let's Encrypt.

<img width="900" height="500" alt="Screenshot 2026-07-09 160656" src="https://github.com/user-attachments/assets/13e6b668-c1f5-4433-9607-e78ffef3fa45" />

After the successful installation, i accessed the website by using HTTPS and it displayed a secure connection with a padlock icon.

Photo:

<img width="1200" height="400" alt="Screenshot 2026-07-09 160740" src="https://github.com/user-attachments/assets/9a34e8cc-0a44-429c-8412-b636106bf4bb" />


Here are more photos of the certificate details: 

<img width="900" height="500" alt="Screenshot 2026-07-09 160916" src="https://github.com/user-attachments/assets/f0a3be7d-704a-4531-a257-a6d8bc0a5585" />


Another picture of me testing renewal : 

<img width="900" height="400" alt="Screenshot 2026-07-09 161109" src="https://github.com/user-attachments/assets/4a621b20-5891-4653-b31e-e65fc17356d9" />



### Problems i encountered and solutions

I actually encountered some problems at first with Certbot.

Photo of my cert having some problems with authentication : 

<img width="900" height="500" alt="Screenshot 2026-07-09 155607" src="https://github.com/user-attachments/assets/e676138d-f77f-4d30-9fef-bfb441610ffe" />


I then found out that the IP in the DuckDNS was different: 

<img width="1300" height="400" alt="Screenshot 2026-07-09 160217" src="https://github.com/user-attachments/assets/375932a3-daa7-44a7-9032-7556362eb6c1" />


Once i found out the source of the problem, i forced DuckDNS to update : 

<img width="900" height="200" alt="Screenshot 2026-07-09 160424" src="https://github.com/user-attachments/assets/2ea9b2fb-6993-4022-b547-a556c533fce8" />


When i went to checked back, the IP address was updated.

<img width="1558" height="470" alt="Screenshot 2026-07-09 160517" src="https://github.com/user-attachments/assets/eb0a6954-a6e6-45cb-9fa8-78d7f38e8186" />

After that, i was successful in getting the certificate. 



### Reflection questions

DNS plays an important role in internet presence as it allows users to access websites using domain names that are easy to remember instead of having to remember IP addresses. DNS propagation takes time because the updated DNS records need to be distributed and refreshed across different DNS servers around the world. Let’s Encrypt validates domain ownership by checking that the person requesting the certificate has control over the domain, usually through DNS records or a temporary web server verification. Without TLS configured on a public-facing site, data sent between users and the server can be exposed to attackers, leading to risks such as data theft or man-in-the-middle attacks. Leaving a cloud VM running for months can also result in unnecessary costs especially if the resources are not being used which is why it is important to monitor usage and terminate unused instances.

