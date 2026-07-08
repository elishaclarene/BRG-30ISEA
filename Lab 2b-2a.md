## Lab 2b-2a 

For this lab, i explored the basics of Bash scripting and Linux automation. I practised managing files and directories, creating and executing Bash scripts, using loops and conditional statements and automating simple system monitoring tasks. These activities helped me understand how Bash scripts can simplify repetitive tasks and improve efficiency when working in a Linux environment.

### Part 1 
First i created a new directory named Lab2B-2A inside the documents folder and navigated into it using the cd command. This provided a dedicated workspace to keep all files and scripts for the lab organised.

Photo: 

<img width="600" height="200" alt="Screenshot From 2026-07-08 11-40-37" src="https://github.com/user-attachments/assets/bdab758e-9643-4643-b02c-462e1d04ade3" />

After that i used the "touch" command to create an empty file named notes.txt. I then used the "ls" command to verify that the file had been successfully created.

<img width="600" height="100" alt="Screenshot From 2026-07-08 11-42-14" src="https://github.com/user-attachments/assets/e3da4fc9-70e1-4a17-a8e2-e54703112192" />


I copied notes.txt to a new file named backup.txt using the "cp" command. This shows how files can be duplicated while preserving the original.

<img width="600" height="100" alt="Screenshot From 2026-07-08 11-43-35" src="https://github.com/user-attachments/assets/0bf6a761-cc9d-4d72-903d-7e6892d128b7" />


After that i renamed backup.txt to renamed.txt using the "mv" command. This showed that the "mv" command can be used to rename files as well as move them between directories.

<img width="600" height="100" alt="Screenshot From 2026-07-08 11-44-35" src="https://github.com/user-attachments/assets/c7f973f1-29b3-4ea7-bd10-ab02002479b4" />


Once that was all done, i removed renamed.txt using the "rm" command and confirmed that only the required files remained in the directory. This demonstrated how to safely delete files from the Linux filesystem.

Photo: 

<img width="600" height="100" alt="Screenshot From 2026-07-08 11-45-29" src="https://github.com/user-attachments/assets/362b89ce-6c1f-4acd-8042-5cd13674fd39" />


### Part 2
Now it was time to start with the Bash scripts.

I created a Bash script named hello_world.sh using the nano text editor. The script began with the shebang (#!/bin/bash) to specify the Bash interpreter and used "echo" commands to display messages when the script was executed.

Photo of the Bash script : 

<img width="600" height="400" alt="Screenshot From 2026-07-08 11-48-34" src="https://github.com/user-attachments/assets/62a1bac0-50b8-408a-8c0a-ab5f3120083c" />


After that i used "chmod 754" to make the script executable. This permission setting gives the owner read, write, and execute permissions, the group read and execute permissions and others read-only permission.

Photo: 

<img width="600" height="200" alt="Screenshot From 2026-07-08 11-51-27" src="https://github.com/user-attachments/assets/f669ad07-cc5a-42c7-9c19-56978f3efb38" />

I then executed the script using "./hello_world.sh" which displayed the messages defined in the script. This confirmed that the script was working correctly after its permissions had been updated.

Photo: 

<img width="600" height="100" alt="Screenshot From 2026-07-08 11-53-49" src="https://github.com/user-attachments/assets/a307de67-f5eb-4211-9ea4-fdbf5ce7cc2b" />

This demonstrates the successful execute of the Bash script using nano text "./" . The script runs through each echo commands and displays the message in the terminal. 


### Part 3 
I made another Bash script that accepted user input using the "read" command. The script also used if, elif and else statements to display different messages based on the users input, followed by a for loop that counted from 1 to 5.

Photo of the Bash script: 

<img width="600" height="400" alt="Screenshot From 2026-07-08 11-56-20" src="https://github.com/user-attachments/assets/5f0ec016-d97c-4748-a1f4-4d3fdae8e9cb" />
<img width="600" height="200" alt="Screenshot From 2026-07-08 11-56-35" src="https://github.com/user-attachments/assets/59253e18-7d2b-4dec-8644-c227a4ee534a" />

I ran the script and entered my name when prompted (I used "Student") . The script evaluated the input using conditional statements and then executed the for loop to display a sequence of numbers, decision-making and repetition in Bash scripting.

<img width="600" height="200" alt="Screenshot From 2026-07-08 11-59-57" src="https://github.com/user-attachments/assets/58fcf503-fbed-4f10-9fd5-82d5447bceb4" />

### Part 4 
Again i made another Bash script that automates basic system monitoring tasks. The script repeatedly displayed memory usage, disk usage and running processes using the free -h, df -h and top commands with a short delay between each iteration.

Photo of the Bash script : 

<img width="600" height="400" alt="Screenshot From 2026-07-08 12-03-15" src="https://github.com/user-attachments/assets/37aaf271-cdf4-46af-b2a5-978be6ac7fc0" />
<img width="600" height="200" alt="Screenshot From 2026-07-08 12-03-40" src="https://github.com/user-attachments/assets/e9e61035-4691-4a50-915c-54fe3647737c" />

The script above shows that it uses a for loop to repeat the monitoring process, display system information using free -h, df -h and top. PLus pauses between each iteration using the sleep command. 

I executed the monitoring script to observe the current system resources. The script automatically collected and displayed system information multiple times, showing how Bash scripting can be used to automate repetitive administrative tasks.


Photo : 

<img width="600" height="400" alt="Screenshot From 2026-07-08 12-07-50" src="https://github.com/user-attachments/assets/90529207-4db2-4dc6-95f6-4bdaf047b01a" />
<img width="600" height="400" alt="Screenshot From 2026-07-08 12-08-02" src="https://github.com/user-attachments/assets/2cb966f2-89fb-4b83-815c-03376a05de58" />
<img width="600" height="400" alt="Screenshot From 2026-07-08 12-08-17" src="https://github.com/user-attachments/assets/5d0487ce-a614-4eb6-a229-65f94e7a6ade" />


## Reflection 

In this lab, i used the "mkdir" command to create a new directory for my work. To view the contents of a file without opening it in a graphical interface, i can use commands such as cat or less in the terminal. The "chmod 777" command gives all users full read, write and execute permissions on a file, although it is generally less secure than using more restrictive permissions like "754". The #!/bin/bash line at the beginning of a script tells Linux to execute the script using the Bash shell. If invalid input is entered, the script follows the appropriate condition such as the "else" statement or may display an error if no validation is included. The "free -h" command displays system memory usage in a human-readable format including total, used and available memory. To monitor network bandwidth in a Bash script, i could use tools such as ifstat, vnstat or nload to display network traffic and usage.







