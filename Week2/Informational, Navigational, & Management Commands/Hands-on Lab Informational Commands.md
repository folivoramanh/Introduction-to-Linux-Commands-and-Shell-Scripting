# Exercise 1 - Informational Commands
## 1.1. Display the name of the current user
```theia@theia-palasek182:/home/project$ whoami```\
theia
## 1.2. Get basic information about the operating system
```theia@theia-palasek182:/home/project$ uname```\
Linux\
```theia@theia-palasek182:/home/project$ uname -a```\
Linux theia-palasek182 5.4.0-156-generic #173-Ubuntu SMP Tue Jul 11 07:25:22 UTC 2023 x86_64 x86_64 x86_64 GNU/Linux
## 1.3. Obtain the user and group identity information
```theia@theia-palasek182:/home/project$ id```\
uid=1000(theia) gid=1000(theia) groups=1000(theia),27(sudo),100(users)
## 1.4 Get available disk space
```theia@theia-palasek182:/home/project$ df```\
Filesystem     1K-blocks     Used Available Use% Mounted on
overlay        101986876 57080012  40486628  59% /
tmpfs              65536        0     65536   0% /dev
tmpfs           16361252        0  16361252   0% /sys/fs/cgroup
/dev/vda2      101986876 57080012  40486628  59% /etc/hosts
shm                65536        0     65536   0% /dev/shm
tmpfs           28937800       16  28937784   1% /run/secrets/kubernetes.io/serviceaccount
tmpfs           16361252        0  16361252   0% /proc/acpi
tmpfs           16361252        0

```theia@theia-palasek182:/home/project$ df -h```\
Filesystem      Size  Used Avail Use% Mounted on
overlay          98G   55G   39G  59% /
tmpfs            64M     0   64M   0% /dev
tmpfs            16G     0   16G   0% /sys/fs/cgroup
/dev/vda2        98G   55G   39G  59% /etc/hosts
shm              64M     0   64M   0% /dev/shm
tmpfs            28G   16K   28G   1% /run/secrets/kubernetes.io/serviceaccount
tmpfs            16G     0   16G   0% /proc/acpi
tmpfs            16G     0   16G   0% /proc/scsi
tmpfs            16G     0   16G   0% /sys/firmware
## 1.5. View currently running processes
```theia@theia-palasek182:/home/project$ ps```\
    PID TTY          TIME CMD
    92 pts/0    00:00:00 bash
   355 pts/0    00:00:00 ps
```theia@theia-palasek182:/home/project$ ps -e```\
    PID TTY          TIME CMD
     1 ?        00:00:00 sh
     7 ?        00:00:00 entrypoi
    35 ?        00:00:00 cron
    36 ?        00:00:01 node
    47 ?        00:00:00 sh
    48 ?        00:00:00 node
    59 ?        00:00:03 node
    70 ?        00:00:03 node
    85 ?        00:00:00 node
    92 pts/0    00:00:00 bash
   309 ?        00:00:00 node
   356 pts/0    00:00:00 ps
   
## 1.6. Get information on the running processes and system resources
```theia@theia-palasek182:/home/project$ top```\
--long text--\
```theia@theia-palasek182:/home/project$ top -n 10```\
--long text--
## 1.7. Display Messages
```theia@theia-palasek182:/home/project$ echo "Welcome to the linux lab"```\
Welcome to the linux lab\
```theia@theia-palasek182:/home/project$ echo -e "This will be printed nin two lines"``` \
This will be printed\
in two lines
## 1.8. Display date and time
```theia@theia-palasek182:/home/project$ date```\
Tue Sep  5 22:44:26 EDT 2023\
```theia@theia-palasek182:/home/project$ date "+%D"```\
09/05/23\
```theia@theia-palasek182:/home/project$ date "+%d"```\
05\
```theia@theia-palasek182:/home/project$ date "+%h"```\
Sep\
```theia@theia-palasek182:/home/project$ date "+%m"```\
09\
```theia@theia-palasek182:/home/project$ date "+%Y"```\
2023\
```theia@theia-palasek182:/home/project$ date "+%T"```\
22:45:13\
```theia@theia-palasek182:/home/project$ date "+%H"```\
22
## 1.9. View the Reference Manual For a Command
```theia@theia-palasek182:/home/project$ man ls```\
--refer to reference manual for command--\
```theia@theia-palasek182:/home/project$ man -k```\
apropos what?

# Practice exercises
## 1. Get basic information about the operating system.
```theia@theia-palasek182:/home/project$ uname```\
Linux
## 2. View all running processes on the system.
```theia@theia-palasek182:/home/project$ ps -e```\
   PID TTY          TIME CMD
     1 ?        00:00:00 sh
     7 ?        00:00:00 entryp
    35 ?        00:00:00 cron
    36 ?        00:00:01 node
    47 ?        00:00:00 sh
    48 ?        00:00:00 node
    59 ?        00:00:05 node
    70 ?        00:00:11 node
    85 ?        00:00:00 node
    92 pts/0    00:00:00 bash
   309 ?        00:00:00 node
   494 pts/0    00:00:00 ps
## 3. Get the table of processes and sort by memory usage.
```theia@theia-palasek182:/home/project$ top```\
top - 22:53:27 up 6 days, 13:21
Tasks:  12 total,   1 running, 
%Cpu(s):  3.9 us,  2.5 sy,  0.0
KiB Mem : 32722504 total,  5884
KiB Swap:        0 total,      

   PID USER      PR  NI 
    48 theia     20   0 
    59 theia     20   0 
    36 theia     20   0 
    70 theia     20   0 
    85 theia     20   0 
   309 theia     20   0 
    92 theia     20   0 
   495 theia     20   0 
     7 theia     20   0 
    35 root      20   0 
    47 theia     20   0 
     1 theia     20   0 
## 4. Display the current time.
```theia@theia-palasek182:/home/project$ date "+%T"```\
22:54:09
## 5. Using one command, display the messages "Hello!" and "Goodbye!" separated by a new line.
`theia@theia-palasek182:/home/project$ echo -e "Hello! \nGoodbye!"`\
Hello! \
Goodbye!