# Exercise 1 - Navigating Files and Directories
## 1.1. Get the location of the present working directory
```theia@theia-palasek182:/home/project$ pwd```\
/home/project
## 1.2. List the files and directories in a directory
```theia@theia-palasek182:/home/project$ ls```\
```theia@theia-palasek182:/home/project$ ls /bin```\
--long long list--\
```theia@theia-palasek182:/home/project$ ls /bin/ls```\
/bin/ls\
```theia@theia-palasek182:/home/project$ ls /bin/b*```\
--long long list--\
```theia@theia-palasek182:/home/project$ ls /bin/*r```\
/bin/bzip2recover  /bin/mkdir  /bin/vdir
/bin/dir           /bin/rmdir
/bin/fuser         /bin/tar
```theia@theia-palasek182:/home/project$ ls -la /etc```\
--very long list--

# Exercise 2 - Creating Files and Directories
## 2.1. Create a directory
```theia@theia-palasek182:/home/project$ mkdir scripts```\
```theia@theia-palasek182:/home/project$ ls```\
scripts
## 2.2. Change your current working directory
```theia@theia-palasek182:/home/project$ cd scripts```\
```theia@theia-palasek182:/home/project/scripts$ pwd```\
/home/project/scripts\
```theia@theia-palasek182:/home/project/scripts$ cd```\
```theia@theia-palasek182:~$ pwd```\
/home/theia\
```theia@theia-palasek182:~$ cd ..```\
theia@theia-palasek182:/home$ 
## 2.3. Create an empty file
```theia@theia-palasek182:/home$ cd```\
```theia@theia-palasek182:~$ touch myfile.txt```\
```theia@theia-palasek182:~$ ls```\
docker-compose
dsdriver
entrypoint.sh
gen-webpack.config.js
javasharedresources
lib
myfile.txt
node_modules
package.json
plugins
postgres
README.md
skills-network-extension-v0.1.0.tgz
src-gen
webpack.config.js
yarn.lock
```theia@theia-palasek182:~$ touch myfile.txt```\
```theia@theia-palasek182:~$ date -r myfile.txt```\
Tue Sep  5 23:46:31 EDT 2023
# Exercise 3 - Managing Files and Directories
## 3.1. Search for and locate files
```theia@theia-palasek182:~$ find /etc -name \'*.txt\' ```\
find: ‘/etc/ssl/private’: Permission denied
## 3.2. Remove files
```theia@theia-palasek182:~$ rm -i myfile.txt```\
rm: remove regular empty file 'myfile.txt'? 
>y
## 3.3. Move and rename a file
```theia@theia-palasek182:~$ touch users.txt```\
`theia@theia-palasek182:~$ mv users.txt user-info.txt`\
```theia@theia-palasek182:~$ mv user-info.txt /tmp```
## 3.4. Copy files
`theia@theia-palasek182:~$ cp /tmp/user-info.txt user-info.txt`\
`theia@theia-palasek182:~$ cp /etc/passwd users.txt`\
`theia@theia-palasek182:~$ ls`\
docker-compose
dsdriver
entrypoint.sh
gen-webpack.config.js
javasharedresources
lib
node_modules
package.json
plugins
postgres
README.md
skills-network-extension-v0.1.0.tgz
src-gen
user-info.txt
users.txt
webpack.config.js
yarn.lock
# Practice exercises
## 1. Display the contents of the /home directory.
`theia@theia-palasek182:~$ ls /home`\
project  theia
## 2. Ensure that you are in your home directory.
`theia@theia-palasek182:~$ cd`\
`theia@theia-palasek182:~$ pwd`\
/home/theia
## 3. Create a new directory called tmp and verify its creation.
`theia@theia-palasek182:~$ mkdir tmp`\
`theia@theia-palasek182:~$ ls`\
docker-compose
dsdriver
entrypoint.sh
gen-webpack.config.js
javasharedresources
lib
node_modules
package.json
plugins
postgres
README.md
skills-network-extension-v0.1.0.tgz
src-gen
tmp
user-info.txt
users.txt
webpack.config.js
yarn.lock
## 4. Create a new, empty file named display.sh in the tmp directory, and verify its creation.
`theia@theia-palasek182:~$ cd tmp`\
`theia@theia-palasek182:~/tmp$ touch display.sh`\
`theia@theia-palasek182:~/tmp$ ls -l`\
total 0\
-rw-r--r-- 1 theia theia 0 Sep  5 23:59 display.sh
## 5. Create a copy of display.sh, called report.sh, within the same directory.
```theia@theia-palasek182:~/tmp$ cp display.sh report.sh```
## 6. Move your copied file, report.sh, up one level in the directory tree to the parent directory. Verify your changes.
`theia@theia-palasek182:~/tmp$ mv report.sh ../`\
`theia@theia-palasek182:~/tmp$ ls `\
display.sh\
`theia@theia-palasek182:~/tmp$ ls ../`\
docker-compose
dsdriver
entrypoint.sh
gen-webpack.config.js
javasharedresources
lib
node_modules
package.json
plugins
postgres
README.md
report.sh
skills-network-extension-v0.1.0.tgz
src-gen
tmp
user-info.txt
users.txt
webpack.config.js
yarn.lock
## 7. Delete the file display.sh.
`theia@theia-palasek182:~/tmp$ rm -i display.sh`\
rm: remove regular empty file 'display.sh'? 
> y
## 8. List the files in /etc directory in the ascending order of their access time.
``theia@theia-palasek182:~/tmp$ ls -ltr /etc/``\
total 668\
--very long root--
## 9. Copy the file /var/log/bootstrap.log to your current directory.
```theia@theia-palasek182:~/tmp$ cp /var/log/bootstrap.log .```