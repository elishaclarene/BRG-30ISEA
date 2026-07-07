## Lab 1b-3

The objective of this lab was to practise using Linux command-line tools to search for files, inspect file contents and analyse text. I used commands such as find, grep, less, du, sed, sort and uniq to locate files, search for keywords and perform basic text analysis.

First step was to download the gutenberg.tar.bz2 file.

<img width="700" height="200" alt="Screenshot From 2026-07-06 21-31-41" src="https://github.com/user-attachments/assets/9e8fa110-5cfa-4f1d-9697-f2071f0661cf" />


In the photo you see on top, u can see that i used the ls -l command to display the files in the current directory. The output showed the file permissions, ownership, file size and modification date for each text file, allowing me to verify that the files were available before starting the lab.


After i have checked the files, i used the tree command to display the directory structure of the working folder. This helped me to get a clear overview of the available text files and how they were organised.

Photo: 

<img width="700" height="150" alt="Screenshot From 2026-07-06 21-32-01" src="https://github.com/user-attachments/assets/d2bb7a72-eeaf-4f40-b4a8-8d6b591523be" />

By using "tree", it helps me show the directory hierarchy of the extracted dataset 


I also tried the "less" command to open and inspect the contents of a text file without modifying it. This command is useful for viewing text files page by page especially when working with larger files.

<img width="700" height="400" alt="Screenshot From 2026-07-06 21-33-17" src="https://github.com/user-attachments/assets/665c5ca3-0298-4d82-894c-671da1a877ca" />


Then i used the find command to search the current directory for all files with the .txt extension. The command successfully listed the available text files.



After that i tried searching for a keyword. In this case i was looking for the word "Ishmael"
I used the command : grep -r "Ishmael".

This is the results that i got: 

<img width="700" height="100" alt="Screenshot From 2026-07-06 21-39-06" src="https://github.com/user-attachments/assets/2b2143e7-db26-4390-906a-8e2f1ca157e6" />



Other than trying to find a keyword, i also tried finding with context
By using the the -C option with grep to display the matching line together with its surrounding context. Though the sample file contained only one line, the command demonstrated how contextual searches work.

Photo: 

<img width="700" height="100" alt="Screenshot From 2026-07-06 21-41-44" src="https://github.com/user-attachments/assets/ad8f8486-e868-4b58-8e6e-48e08217b1f8" />


Once that was done, i started to find the file size. By using the find . -type f -size 94c -exec ls -lh {} \; 
These were the results that I got: 


<img width="700" height="100" alt="Screenshot From 2026-07-06 21-44-39" src="https://github.com/user-attachments/assets/68ae3eeb-1363-4184-b558-7596f7801f31" />



In addition, i also used the command : find . -type f -printf '%T+ %p\n' | sort


<img width="700" height="100" alt="Screenshot From 2026-07-06 21-46-50" src="https://github.com/user-attachments/assets/aa54933b-1175-4279-936b-e4831518851d" />

I listed the files together with their modification dates and sorted the results in chronological order. This makes it easier to identify files based on when they were last modified.


Once that was done, i tried to find the largest files by using "du -a . | sort -nr | head" 

<img width="700" height="125" alt="Screenshot From 2026-07-06 21-49-14" src="https://github.com/user-attachments/assets/4da10fc6-49f0-4710-aa37-bf7c01b94d53" />


I also analysed the word frequency. 
By using the command : sed -e 's/\s/\n/g' < frankenstein.txt | sort | uniq -c | sort -nr | head 

Here are the results that i got : 

<img width="700" height="200" alt="Screenshot From 2026-07-06 21-51-27" src="https://github.com/user-attachments/assets/3ed1755f-a39b-468d-bd60-d035fd5093f1" />


## Analytical Questions to Answer 
 How many times does the string “verdigris” appear? (enter a number)    NIL
- What is the surname of the author of the filename “1107.txt”? (case sensitive)   NIL
- What is the surname of the author of the file that is exactly 255258 bytes? (case sensitive)    NIL 
- What is the filename of the file with the 3rd oldest creation date?   NIL 
- Find the word that follows the text: “Next day there was a surprise for Jack” (Case-sensitive, no spaces)   NIL



 ## Reflection 
I found the grep command to be the most useful because it allowed me to quickly search for specific words in text files instead of reading through them manually. These search tools can also be valuable in cybersecurity investigations as they help analysts locate suspicious files, keywords or logs more efficiently when examining large amounts of data. Scripting could further improve repetitive search tasks by automating commands that need to be run multiple times which saves time and reduces the chance of human error. One limitation I noticed was that grep only searches for the text you specify so choosing the wrong keyword may result in missing useful information. Similarly, find requires the correct search criteria such as the filename or file size, otherwise it may not return the expected results.


