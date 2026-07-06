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



After that i added alice and bob to sharedgroup using the usermod -aG command and verified their group memberships.

These photo shows that both alice and bob has been added to the sharedgroup group: 

<img width="700" height="200" alt="Screenshot From 2026-07-06 16-40-57" src="https://github.com/user-attachments/assets/1479b3f4-85c6-46af-938a-852b9e804923" />



I then changed the permissions of the shared directory to 770, allowing the owner and group members full access while denying access to other users. From this i have learnt that 770 is a numeric permission mode used with the chmod command to control access to files or directories. 

Photo of me showing that the shared directory permission were updated to allow only own and group members to have full access: 
<img width="700" height="99" alt="Screenshot From 2026-07-06 16-42-21" src="https://github.com/user-attachments/assets/e677932f-af5b-436b-a0d9-b7e13312813e" />



I changed the permissions of the files again inside the shared directory to 750 that gives the owner full access while allowing group members to read and execute the files.

During this step, I noticed that my normal user account could no longer access /home/shared because it was not the owner or a member of sharedgroup. I used sudo to complete the remaining administrative tasks.


This shows that the file permission was successfully updated: 

<img width="700" height="250" alt="Screenshot From 2026-07-06 16-49-00" src="https://github.com/user-attachments/assets/b9ad1b1e-0910-4051-b2bb-9b9d1812c549" />


This photo shows the problem that i have faced as my normal account could no long access it as it was not an owner or group member. 

<img width="700" height="250" alt="Screenshot From 2026-07-06 16-50-44" src="https://github.com/user-attachments/assets/70600240-e0b4-4304-b687-fefc96789dfb" />



Once that was done i started the users access. I switched between alice, bob and mallory using the su command and verified each users identity with whoami.
Alice and bob were able to access the shared directory because they were members of sharedgroup while mallory received a permission denied message because she was not part of the group.



This section is me testing for alice and i also made a new file to test:


This verified alice as a memeber of the sharedgroup and could access the shared directory
<img width="700" height="300" alt="Screenshot From 2026-07-06 16-52-36" src="https://github.com/user-attachments/assets/31a7516e-c3c2-4e72-ace6-933983dfad33" />

This is making making a new file and it showing:

<img width="700" height="200" alt="Screenshot From 2026-07-06 16-55-00" src="https://github.com/user-attachments/assets/49af4db1-cd7f-46cd-b6e7-5369e09d579b" />



This section is me testing for bob and doing the exact same thing i did for alice. 

<img width="730" height="399" alt="Screenshot From 2026-07-06 16-57-11" src="https://github.com/user-attachments/assets/2b033717-6c0f-410c-9bb8-2da242080a75" />
<img width="743" height="295" alt="Screenshot From 2026-07-06 16-57-24" src="https://github.com/user-attachments/assets/1b6ca596-cfc1-49f8-abb2-dada2a0ac42a" />



Now this is me testing mallory who is not part of the sharedgroup..

This photo shows that a user who is not part of the sharedgroup cannot access the shared directory

<img width="700" height="150" alt="Screenshot From 2026-07-06 16-59-18" src="https://github.com/user-attachments/assets/d25d1339-3f4d-4059-9e88-c09589e3cda4" />



## Challenge Task : sudo access

Previously mallory was not able to access but now i added mallory to the sudo group and verified that she could successfully run sudo ls /root. Demonstrating how sudo grants temporary administrative privileges.


<img width="700" height="150" alt="Screenshot From 2026-07-06 17-02-34" src="https://github.com/user-attachments/assets/25a6a4f4-1416-47b3-be49-7fd1c72c375c" />


## Clean up task 
After completing the lab, i removed the shared directory and its contents using the rm -r command and verified that the directory had been deleted.

<img width="700" height="100" alt="Screenshot From 2026-07-06 17-04-13" src="https://github.com/user-attachments/assets/d44b2226-bace-4489-b1e2-bd02ce2a3c85" />


## Reflection questions

From this lab, i learned that linux permissions are managed using the owner, group and others. While Windows ACL provides more detailed permission settings for individual users and groups. I also understood the difference between "chmod 770" and "750" where 770 gives both the owner and group full access while 750 only allows the group to read and execute files. Another important lesson was that adding a user to the "sudo" group gives them administrative privileges so it should only be given to trusted users because they can make changes to the system. Using "su" and "whoami" also helped me confirm which user i was testing with, making sure the permission results were accurate.


