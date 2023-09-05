# Exercise 1 - Browsing Directories

## 1.1. Viewing files in the current working directory

```theia@theia-palasek182:/home/project$ ls```

## 1.2. Viewing files and directories within any directory

```theia@theia-palasek182:/home/project$ ls /bin```

bash          dd             lessfile       ps          uname

bunzip2       df             lesskey        pwd        uncompress

bzcat         dir            lesspipe       rbash       vdir

bzcmp         dmesg          ln             readlink    wdctl

bzdiff        dnsdomainname  login          rm          which

bzegrep       domainname     ls             rmdir    ypdomainname

bzexe         echo           lsblk          rnano       zcat

bzfgrep       egrep          mkdir          run-parts   zcmp

bzgrep        false          mknod          sed         zdiff

bzip2         fgrep          mktemp         sh          zegrep

bzip2recover  findmnt        more           sh.distrib  zfgrep

bzless        fuser          mount          sleep       zforce

bzmore        grep           mountpoint     stty        zgrep

cat           gunzip         mv             su          zless

chgrp         gzexe          nano           sync        zmore

chmod         gzip           netstat        tar         znew

chown         hostname       nisdomainname  tempfile

cp            kill           pidof          touch

dash          less           ping           true

date          lessecho       ping6          umount

```theia@theia-palasek182:/home/project$ ls /sbin```

acpi_available  ifconfig           on_ac_power

agetty          initctl            pam_extrausers_chkpwd

apm_available   installkernel      pam_extrausers_update

badblocks       ip6tables          pam_tally

blkdiscard      ip6tables-restore  pam_tally2

blkid           ip6tables-save     pivot_root

blockdev        ipmaddr            plipconfig

cfdisk          iptables           rarp

chcpu           iptables-restore   raw

ctrlaltdel      iptables-save      resize2fs


debugfs         iptunnel           route

dumpe2fs        isosize            runuser

e2fsck          killall5           sfdisk

e2image         ldconfig           shadowconfig

e2label         ldconfig.real      slattach

e2undo          logsave            start-stop-daemon

fdisk           losetup            sulogin

findfs          mii-tool           swaplabel

fsck            mke2fs             swapoff

fsck.cramfs     mkfs               swapon

fsck.ext2       mkfs.bfs           switch_root

fsck.ext3       mkfs.cramfs        sysctl

fsck.ext4       mkfs.ext2          tune2fs

fsck.minix      mkfs.ext3          unix_chkpwd

fsfreeze        mkfs.ext4          unix_update

fstab-decode    mkfs.minix         wipefs

fstrim          mkhomedir_helper   xtables-multi

getty           mkswap             zramctl

hwclock         nameif

```theia@theia-palasek182:/home/project$ ls /usr```

bin  games    lib    libx32  man   share

doc  include  lib32  local   sbin  src

```theia@theia-palasek182:/home/project$ ls /home```

project  theia

```theia@theia-palasek182:/home/project$ ls /media```

# Exercise 2 - Navigating Directories

## 2.1. Changing your present working directory to your home directory

```theia@theia-palasek182:/home/project$ cd ~```

```theia@theia-palasek182:~$ ```

## 2.2. Changing your present working directory to its parent directory

```theia@theia-palasek182:~$ cd ..```

```theia@theia-palasek182:/home$ ```
## 2.3. Changing working directory to root directory
```theia@theia-palasek182:/home$ cd /```

```theia@theia-palasek182:/$ ```
## 2.4. Changing your present working directory to a child directory
```theia@theia-palasek182:/$ cd bin```

```theia@theia-palasek182:/bin$```
#### second solution
```theia@theia-palasek182:/$ cd ./bin```

```theia@theia-palasek182:/bin$ ```
## 2.5. Changing from your working directory back to your home directory
```theia@theia-palasek182:/bin$ cd ../home/theia```

```theia@theia-palasek182:~$```
#### second sol
```theia@theia-palasek182:/bin$ cd ~```

```theia@theia-palasek182:~$ ```
## 2.6. Changing from your working directory to your ```project``` directory
```theia@theia-palasek182:~$ cd ../project```

```theia@theia-palasek182:/home/project$ ```
# Exercise 3 - Using tab completion and the command history
## 3.1. Scrolling through your command history
```theia@theia-palasek182:/home/project$ cd ~```
#### Apply by scrolling up to get the previous command
```theia@theia-palasek182:~$ cd ../project```
## 3.2. Using tab completion
#### type: 
```theia@theia-palasek182:/home/project$ cd /bi```
#### and tab: 
```theia@theia-palasek182:/home/project$ cd /bin/```
#### finish task
```theia@theia-palasek182:/bin$ ls /home/```

project  theia

```theia@theia-palasek182:/bin$ ls /home/theia/```

docker-compose      lib     README.md

dsdriver   node_modules  skills-network-extension-v0.1.0.tgz    

entrypoint.sh    package.json  src-gen

gen-webpack.config.js  plugins    
   webpack.config.js

javasharedresources    postgres   yarn.lock

```theia@theia-palasek182:/bin$ ls /home/theia/dsdriver/```
# Practice Exercise
## 1. List the contents of the root directory.
``` theia@theia-palasek182:/$ ls```

bin   dev  home  lib32  libx32  mnt  proc  run   srv  tmp

var boot  etc  lib   lib64  media   opt  root  sbin  sys 

usr
## 2. Change directories to your default home directory.
```theia@theia-palasek182:/$ cd ~```
```theia@theia-palasek182:~$ ```
## 3. Verify your current working directory is /home/theia.
```theia@theia-palasek182:~$ pwd```

/home/theia
## 4. Use tab completion to change directories to /bin.
```theia@theia-palasek182:/$ cd /b```

bin/  boot/ 

```theia@theia-palasek182:/$ cd /bin/```

```theia@theia-palasek182:/bin$ ```
## 5. Use your terminal's command history to change directories back to your home directory.
```theia@theia-palasek182:/bin$ cd ~```

```theia@theia-palasek182:~$ ```