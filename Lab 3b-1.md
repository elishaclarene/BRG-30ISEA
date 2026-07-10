## Lab 3b-1 

The objective of this lab is to automate file backups using a Bash script, compress the backup into a ZIP archive, schedule the script using cron jobs and securely transfer the backup to a cloud server using SCP.


First step was the open Ubuntu :

<img width="1000" height="800" alt="Screenshot From 2026-07-10 15-34-38" src="https://github.com/user-attachments/assets/fe8f2152-d35d-4307-81bd-4898f492f2c2" />


This photo shows my current environment before creating the backup automation. It basically shows my starting directory and existing files/folders

<img width="700" height="300" alt="Screenshot From 2026-07-10 15-37-10" src="https://github.com/user-attachments/assets/49b57c6a-d2ac-4704-97d8-addddd355355" />


After that, i started to create sample files and folders inside the Documents directory to simulate user data that would be backed up.

Photo: 

<img width="700" height="300" alt="Screenshot From 2026-07-10 15-41-38" src="https://github.com/user-attachments/assets/0bf946ba-5a9b-430c-af06-af30d8181544" />


I then created a backup folder to store copied files before compression:

<img width="700" height="90" alt="Screenshot From 2026-07-10 15-43-29" src="https://github.com/user-attachments/assets/caf840cf-53be-4254-85d0-d9154cc96551" />


I created a Bash script that stores the current date in a variable, copies all files from Documents to the backup folder, compresses the backup into a ZIP archive and copies the ZIP file into the home directory.

Then i made the script executable using chmod 777

Photo: 

<img width="700" height="100" alt="Screenshot From 2026-07-10 15-46-03" src="https://github.com/user-attachments/assets/1fe5fcfa-c749-4fd8-92ae-b6dded2a5e72" />

This shows ^ that the execute permission was granted to the Bash script.

After i have granted the execute permission on the script, i executed it. 

Photo: 

<img width="700" height="400" alt="Screenshot From 2026-07-10 15-47-20" src="https://github.com/user-attachments/assets/f9dd0b97-1e2b-4660-be0a-fa9ecb64f84a" />

This photo above ^ proves that the backup script executed succesfully. You can also see the .ZIP file which demonstrates that the backup archrive was successfully created.

I then installed the script to be system wide, so i moved the script into /usr/bin so it could be executed from any location.

Photo: 

<img width="700" height="400" alt="Screenshot From 2026-07-10 15-49-37" src="https://github.com/user-attachments/assets/4e2096a8-afc0-4016-8d8e-6c26e48e00d9" />


After that i made it into a scheduled automatic execution, so i configured /etc/crontab so the script runs automatically every hour.

Photo: 

<img width="700" height="400" alt="Screenshot From 2026-07-10 15-52-02" src="https://github.com/user-attachments/assets/0ca5c10b-3030-479b-a70f-cfc7d1ed6356" />

This photo above ^ shows that the backup script has been scheduled to run automatically every hour.


Now i had to download the backup to the cloud. 

I first made an instance : 

<img width="1500" height="800" alt="Screenshot 2026-07-10 160459" src="https://github.com/user-attachments/assets/cf2c040c-62ff-4f42-b74c-efa7421b3fc1" />


Once my instance was running, i used scp with an SSH private key to securely transfer the ZIP archive to an Amazon EC2 instance.

Photo: 

<img width="700" height="200" alt="Screenshot From 2026-07-10 16-13-17" src="https://github.com/user-attachments/assets/6700a762-7bc4-42f3-b612-d6581110b86f" />

This photo ^ demonstrates the backup archive was securely transferred to a cloud server using SCP.


Then i verified the cloud backup, so i connected to the EC2 instance using SSH and confirmed that the ZIP archive was successfully uploaded.

Photo: 

<img width="700" height="400" alt="Screenshot From 2026-07-10 16-15-16" src="https://github.com/user-attachments/assets/23332a5a-8b4e-40da-b869-8b5ae6614b19" />
<img width="700" height="200" alt="Screenshot From 2026-07-10 16-15-29" src="https://github.com/user-attachments/assets/acd3d330-57d2-4497-b7dd-42e2df5776a8" />


## Reflection 

From this lab, i learned that using absolute paths is important because cron jobs do not always know the current working directory, so using the full file path ensures the script runs correctly. Exporting backups to the cloud also provides an extra copy of important files, making it easier to recover data if the local backup is lost. Compared to running a script manually, cron automatically executes the script at scheduled times, making the backup process more efficient and consistent. I also learned that if SSH keys are not accepted beforehand, the SCP transfer may stop and wait for user confirmation, preventing the automation from completing successfully. Lastly, customising login messages with tools like figlet and neofetch can make the login screen more informative by displaying useful system information in a clearer and more personalised way.




