## Lab 1b-2

The objective of this lab was to learn how Linux manages users, groups and file permissions. I created multiple user accounts, configured a shared group, assigned permissions to directories and files, tested access using different user accounts and explored how sudo privileges affect system access.


Firstly, i created three user accounts named alice, bob, and mallory using the "adduser" command. Each user was assigned its own home directory and default group.

Photo of me making alice: 

<img width="700" height="400" alt="Screenshot From 2026-07-06 16-21-43" src="https://github.com/user-attachments/assets/82fa9cac-8141-46c8-a396-6684903df860" />



Photo of me making bob: 

<img width="700" height="400" alt="Screenshot From 2026-07-06 16-24-07" src="https://github.com/user-attachments/assets/946ce53f-7c1c-4756-be8c-319333b6a979" />



Photo of me making mallory:

<img width="700" height="200" alt="Screenshot From 2026-07-06 16-26-22" src="https://github.com/user-attachments/assets/f821c280-f199-4ebc-ab41-6c037d066550" />






Then i proceeded to make a new group called sharedgroup using the groupadd command and verified that it was successfully created by checking the system group database.

<img width="700" height="100" alt="Screenshot From 2026-07-06 16-33-34" src="https://github.com/user-attachments/assets/5933ce35-2e88-4b0d-96f2-bca61cbb6619" />




After that I made a shared directory named /home/shared to store files that would later be shared between selected users.


photo of me making the shared directory: 

<img width="700" height="100" alt="Screenshot From 2026-07-06 16-34-39" src="https://github.com/user-attachments/assets/9c66a696-20de-4564-8f5f-b187a1d25410" />





Once i have finish making the sharing directory, i made 10 empty files inside /home/shared using the touch command with Bash brace expansion.


The photo here shows me making 10 empty files and me checking it in the shared directory: 

<img width="700" height="200" alt="Screenshot From 2026-07-06 16-36-47 (1)" src="https://github.com/user-attachments/assets/1bf24163-eb0f-44d4-a1a7-040370f615c2" />






Now i have changed the group ownership of the shared directory and all its files to sharedgroup using the chgrp -R command.

This photo verifies that the group ownership of the shared directory and its files was changed to sharedgroup

<img width="735" height="281" alt="Screenshot From 2026-07-06 16-38-34" src="https://github.com/user-attachments/assets/238a736d-8e83-488a-a11c-2bf4978ef970" />










## Challenge Task : sudo access

## Clean up task 

## Reflection questions

