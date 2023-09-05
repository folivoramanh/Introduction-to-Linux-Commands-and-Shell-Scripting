# Exercise 1 - Upgrading and installing packages
## 1.1 Updating your Linux sytem's package list index
```theia@theia-palasek182:/home/project$ sudo apt update```

--long update return--
## 1.2. Upgrading nano
```theia@theia-palasek182:/home/project$ sudo apt upgrade nano```

--still long update--
## 1.3. Installing Vim
```theia@theia-palasek182:/home/project$ sudo apt install vim```

--another long update--
# Exercise 2 - Creating and editing files with nano
## 2.1 Navigating to the project directory
```theia@theia-palasek182:/home/project$ cd /home/project```

```theia@theia-palasek182:/home/project$``` 
## 2.2 Creating and editing a text file with nano
```theia@theia-palasek182:/home/project$ nano hello_world.txt```

--move to hello.txt--

write to file:\
Hello world!\
This is the second line of my first-ever text file created with nano.

--ctrl + x then y then enter--

```theia@theia-palasek182:/home/project$```
## 2.3 Verifying your new text file
```theia@theia-palasek182:/home/project$ cat hello_world.txt```

"Hello world! \
This is the second line of my first-ever text file created with nano."

# Exercise 3 - Creating and editing files with Vim
## 3.1 Quick intro to Vim
```theia@theia-palasek182:/home/project$ vim```
## 3.2 Creating and editing a text file with Vim
```theia@theia-palasek182:/home/project$ vim hello_world_2.txt```\
--do insert in vim--\
```theia@theia-palasek182:/home/project$ cat hello_world_2.txt```\
Hello World!\
This is the second line.
# Practice Exercises
## 1. Using nano, edit your new hello_world.txt file to add a new line containing the following text: This is line three of my new file.
```theia@theia-palasek182:/home/project$ nano hello_world.txt```\
```theia@theia-palasek182:/home/project$ cat hello_world.txt```

Hello world!\
This is the second line of my first-ever text file created with nano.\
This is line three of my new file.
## 2. Using Vim, create a file called done.txt that prints "I am done with the lab!" when you execute the file with Bash.
```theia@theia-palasek182:/home/project$ vim done.txt```\
```theia@theia-palasek182:/home/project$ cat done.txt```\
I am done with the lab!