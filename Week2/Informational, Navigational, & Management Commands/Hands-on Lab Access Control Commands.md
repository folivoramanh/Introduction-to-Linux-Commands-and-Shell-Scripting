# Exercise 1 - Viewing and modifying file access permissions
## 1.1 View file access permissions
`theia@theia-palasek182:/home/project$ cd /home/project`\
`theia@theia-palasek182:/home/project$ wget https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-LX0117EN-SkillsNetwork/labs/module%201/usdoi.txt`\
`theia@theia-palasek182:/home/project$ ls -l usdoi.txt`\
-rw-r--r-- 1 theia users 8121 Sep 28  2022 usdoi.txt
## 1.2 Change file access permissions
`theia@theia-palasek182:/home/project$ chmod -r usdoi.txt   `\            
`theia@theia-palasek182:/home/project$ ls -l usdoi.txt`\
--w------- 1 theia users 8121 Sep 28  2022 usdoi.txt\
`theia@theia-palasek182:/home/project$ chmod +r usdoi.txt     `\           
`theia@theia-palasek182:/home/project$ ls -l usdoi.txt`\
-rw-r--r-- 1 theia users 8121 Sep 28  2022 usdoi.txt\
`theia@theia-palasek182:/home/project$ chmod o-r usdoi.txt`\
`theia@theia-palasek182:/home/project$ ls -l usdoi.txt`\
-rw-r----- 1 theia users 8121 Sep 28  2022 usdoi.txt
# Exercise 2 - Understanding directory access permissions
## 2.1 View default directory access permissions
`theia@theia-palasek182:/home/project$ cd /home/project`\
`theia@theia-palasek182:/home/project$ mkdir test`\
`theia@theia-palasek182:/home/project$ ls -l`\
total 16\
drwxr-sr-x 2 theia users 4096 Sep  5 23:44 scripts\
drwxr-sr-x 2 theia users 4096 Sep  6 00:14 test\
-rw-r----- 1 theia users 8121 Sep 28  2022 usdoi.txt\
`theia@theia-palasek182:/home/project$ cd test`\
`theia@theia-palasek182:/home/project/test$ mkdir test2`\
`theia@theia-palasek182:/home/project/test$ cd ../`
## 2.2 Remove user execute permissions on your test directory
`theia@theia-palasek182:/home/project$ chmod u-x `\
`testtheia@theia-palasek182:/home/project$ cd test`\
bash: cd: test: Permission denied\
`theia@theia-palasek182:/home/project$ chmod u+x `\
`testtheia@theia-palasek182:/home/project$ chmod u-w`\
`testtheia@theia-palasek182:/home/project$ ls -l`\
total 16\
drwxr-sr-x 2 theia users 4096 Sep  5 23:44 scripts\
dr-xr-sr-x 3 theia users 4096 Sep  6 00:14 test\
-rw-r----- 1 theia users 8121 Sep 28  2022 usdoi.txt\
`theia@theia-palasek182:/home/project$ cd test`\
`theia@theia-palasek182:/home/project/test$ mkdir test_again`\
mkdir: cannot create directory ‘test_again’: Permission denied
# Practice exercises
## 1. List the permissions set for the file usdoi.txt that you downloaded to your project directory at the beginning of the lab.
`theia@theia-palasek182:/home/project/test$ cd /home/project`\
`theia@theia-palasek182:/home/project$ ls -l usdoi.txt`\
-rw-r----- 1 theia users 8121 Sep 28  2022 usdoi.txt
## 2. Revoke the write permission on usdoi.txt for the user, and verify your result.
`theia@theia-palasek182:/home/project$ chmod u-w  usdoi.txt`\
`theia@theia-palasek182:/home/project$ ls -l usdoi.txt`\
-r--r----- 1 theia users 8121 Sep 28  2022 usdoi.txt
## 3. What happens if you try to delete usdoi.txt after revoking write permissions for the user?
`theia@theia-palasek182:/home/project$ rm usdoi.txt`\ 
rm: remove write-protected regular file 'usdoi.txt'? 
> y
`theia@theia-palasek182:/home/project$ ls usdoi.txt`\
ls: cannot access 'usdoi.txt': No such file or directory
## 4. Create a new directory called tmp_dir in your home directory.
`theia@theia-palasek182:/home/project$ mkdir tmp_dir`
## 5. View the permissions of the newly created directory, tmp_dir.
`theia@theia-palasek182:/home/project$ ls -ld `\
tmp_dirdrwxr-sr-x 2 theia users 4096 Sep  6 00:21 tmp_dir
## 6. Revoke the user write permission for tmp_dir.
`theia@theia-palasek182:/home/project$ chmod u-w tmp_dir`
## 7. Check whether you can create a subdirectory of tmp_dir called sub_dir.
`theia@theia-palasek182:/home/project$ mkdir tmp_dir/sub_dir`\
mkdir: cannot create directory ‘tmp_dir/sub_dir’: Permission denied