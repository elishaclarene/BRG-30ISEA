## Lab 3b-2

The objective of this lab was to set up an Ubuntu environment using WSL2 on Windows and install Docker (my chosen addtional server) as an additional server component. Docker was configured as a container platform to allow applications and services to run in isolated environments.

Since the lab environment required Ubuntu running on WSL2, i installed WSL first. WSL allows Linux distributions to run directly on Windows without requiring a separate virtual machine.

Photo of me installing WSL : 

<img width="1000" height="600" alt="Screenshot 2026-07-10 191802" src="https://github.com/user-attachments/assets/c9005892-f438-425b-a400-fcc289c14a16" />


After enabling WSL, the Ubuntu Linux distribution was installed and configured and made my Linux user account to access the Ubuntu environment.

Then i verified the Ubuntu environment to ensure that it was running correctly on WSL2 before installing Docker.

Photo: 

<img width="900" height="100" alt="Screenshot 2026-07-10 193800" src="https://github.com/user-attachments/assets/26954764-bfde-40a6-a42c-56ecf42fe452" />

The photo above shows that the server environment was succuessfully prepared using Ubuntu on WSL2. 

As it was time to finally download Docker , i first prepared the system by doing this: 

<img width="900" height="500" alt="Screenshot 2026-07-10 194227" src="https://github.com/user-attachments/assets/230f6621-b589-4ee3-b6db-94b5ce7dc656" />

Once i have ensured that Ubuntu is updated and ready for the Docker installation. I downloaded it 


Photo of me downloading Docker : 

<img width="900" height="500" alt="Screenshot 2026-07-10 194612" src="https://github.com/user-attachments/assets/6ea64978-0ab2-4fea-abcd-ba7e8e04abd5" />

After installation, i started the Docker service to ensure that Docker was working correctly.

Photo: 

<img width="982" height="77" alt="Screenshot 2026-07-10 194715" src="https://github.com/user-attachments/assets/497918b4-8d1e-4622-8950-d67834ad5f93" />

I then tested the Docker container by using the hello world image to confirm that Docker could successfully download images and run containers.

Photo : 

<img width="900" height="500" alt="Screenshot 2026-07-10 194908" src="https://github.com/user-attachments/assets/6d32091d-a71b-473c-a6f8-c9e2bd2c23a2" />

This was the final verification that the Docker can successfully create and run commands. 


