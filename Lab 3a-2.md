## Lab 3a-2

The objective of this lab was to secure a web server by enabling HTTPS using a free TLS certificate from Let's Encrypt. This involved setting up an Apache web server on my AWS EC2 instance, configuring my DuckDNS domain name, installing Certbot and verifying that HTTPS was successfully enabled. At the end of the lab, the website could be securely accessed through HTTPS, ensuring encrypted communication between the client and the server.


I first made my Ubuntu EC2 instance that was launched through the AWS Management Console. During the setup, i made a security group that was configured to allow inbound traffic for SSH (Port 22), HTTP (Port 80) and HTTPS (Port 443). These rules were necessary to allow remote administration of the server and enable users to access the web application over both HTTP and HTTPS.

The existing .pem key pair from the previous lab was reused to securely connect to the instance through SSH.

Photo of my instance running : 


<img width="1500" height="850" alt="Screenshot 2026-07-09 222401" src="https://github.com/user-attachments/assets/2be39550-ed4d-40e2-ad15-6c705dd53be5" />


After the instance was running, an SSH connection was established from the local computer using the .pem key. Successfully connecting to the server, confirming that the EC2 instance was accessible and ready for configuration.


I then downloaded Apache as the web server that would host the website. I used the command " sudo apt install apache2 -y "

After that was done, i checked to verify that the service was running correctly.

Photo that shows that my Apeche was running : 

<img width="900" height="600" alt="Screenshot 2026-07-09 223058" src="https://github.com/user-attachments/assets/28ee1e4c-ecb2-4e44-b156-403ed1ea355a" />

In the photo above ^ shows that that the apeche webserver was successfully installed and is running 


I then checked on my webserver and this is what it showed: 

<img width="1300" height="900" alt="Screenshot 2026-07-09 223236" src="https://github.com/user-attachments/assets/e36ee3f4-650e-466f-8c3a-94655f248f1a" />

This photo ^ proves that the apeche webserver is publicly accessible over HTTP.


Once that was done, i made a new DuckDNS subdomain as the previous domain from lab 3a-1 was no longer available. The domain's IP address was then updated to point to my EC2 instances new public IPv4 address.


<img width="1300" height="500" alt="Screenshot 2026-07-09 223704" src="https://github.com/user-attachments/assets/482a4582-0f39-42e6-8e07-afbc21b7b5b1" />


When the DNS record was updated, the domain was tested by accessing it through a web browser. The Apache Default Page was displayed successfully using the DuckDNS domain which confirmed that the DNS configuration was working correctly.

Photo that proves that my domain is correctly resolved to my webserver:
<img width="1500" height="900" alt="Screenshot 2026-07-09 224005" src="https://github.com/user-attachments/assets/1969f277-7dbb-418e-9fa6-13bd3c29b823" />


I then downloaded Certbot using snap packages to obtain and manage TLS certificates from Let's Encrypt. 

Photo of my certificate :

<img width="900" height="600" alt="Screenshot 2026-07-09 224908" src="https://github.com/user-attachments/assets/6b8eafc7-ed0b-4a38-95b1-736034e73bdf" />

This proves that Let's Encrpyt has successfully issued and installed TLS certificate.

After that i tested on my browser : 

<img width="1000" height="900" alt="Screenshot 2026-07-09 225007" src="https://github.com/user-attachments/assets/83cb70a0-87a0-4fad-81f0-2a20afb0f538" />

The browser displayed a padlock icon which indicated that the website was using a secure HTTPS connection.

The certificate details were also inspected by clicking the padlock icon. 

<img width="1000" height="500" alt="Screenshot 2026-07-09 225112" src="https://github.com/user-attachments/assets/8dfcca55-7699-437e-a882-0060e00b663c" />


### Reflection 

HTTPS is important because it helps protect the data sent between the users browser and the web server by encrypting the connection, making it more secure. During this lab, I learned that my websites TLS certificate was issued by Let's Encrypt which is a free and trusted certificate authority. The certificate is valid for about 90 days and it can be renewed automatically using Certbot, making it easier to keep the website secure. If the certificate expires and is not renewed, browsers will warn users that the website is not secure which can reduce trust and prevent users from accessing the site safely. I also learned that Let's Encrypt requires port 80 or 443 to be open because it needs to verify that the domain is correctly connected to the web server before issuing the TLS certificate.
