---
Date: 2022-07-31
Author: Jimmy Briggs <jimmy.briggs@jimbrig.com>
Tags: ["#Topic/Dev", "#Type/Reference"]
Alias: ["Git Commands"]
---

# Linux Commands Reference

*Source: *

[TOC]

## ls

The ls command is used to list files and directories in the current working directory. 
This is going to be one of the most frequently used Linux commands you must know of:

```bash
ls
```

## pwd

The pwd command allows you to print the current working directory on your terminal. 
It’s a very basic command and solves its purpose very well:

```bash
pwd
```

## cd

While working within the terminal, moving around within directories is pretty much a necessity. 
The cd command is one of the important Linux commands you must know and it will help you to navigate through directories:

```bash
cd <directory-path>
```

## mkdir

The mkdir command allows you to create directories from within the terminal. 
The default syntax is mkdir followed by the directory name:

```bash
mkdir <folder-name>
```

## mv and cp

The cp and mv commands are equivalent to the copy-paste and cut-paste in Windows. 
But since Linux doesn’t really have a command for renaming files, 
we also make use of the mv command to rename files and folders:

```bash
cp <source> <destination>
mv <source> <destination>
```

## rm

The rm command is used to delete files and folders and is one of the important Linux commands you must know:

```bash
rm <file-name>
rm -r <folder/directory-name>
```

## touch

To create a new file, the touch command will be used. 
The touch keyword followed by the file name will create a file in the current directory:

```bash
touch <file-name>
```

## ln

To create a link to another file, we use the ln command. 
This is one of the important Linux commands that you should know if you’re planning to work as a Linux administrator:

```bash
ln -s <source-path> <link-name>
```

## cat, echo and less

When you want to output the contents of a file, or print anything to the terminal output, we make use of the cat or 
echo commands:

```bash
cat <file-name>
echo <Text-to-print-on-terminal>
```

The less command is used when the output printed by any command is larger than the screen space and needs scrolling. 
The less command allows use to break down the output and scroll through it with the use of the enter or space keys:

```bash
cat /boot/grub/grub.cfg  | less
```

## man

The man pages offer a really efficient way to know the functionality of pretty much all the packages that you 
can download using the package managers in your Linux distro:

```bash
man <command>
```

## clear

Clear the terminal display:

```bash
clear
```

## uname and whoami

The uname and whoami commands allow you to know some basic information which comes really handy when you work on 
multiple systems:

```bash
uname -a
```

```bash
whoami
```

## tar, zip and unzip

The tar command in Linux is used to create and extract archived files in Linux. We can extract multiple different 
archive files using the tar command. To create an archive, we use the -c parameter and to extract an archive, 
we use the -x parameter:

```bash
tar -cvf <archive-name> <files-seperated-by-space>
tar -xvf <archive-name>
```

```bash
zip <archive name> <file names separated by space>
unzip <archive name>
```

## grep

If you wish to search for a specific string within an output, the grep command comes into the picture. We can pipe (|) 
the output to the grep command and extract the required string:

```bash
<Any-command-with-output> | grep "<string-to-find>"
```

## head and tail

When outputting large files, the head and the tail commands come in handy:

```bash
head <file-name>
tail <file-name>
```

## diff, comm, cmp

Linux offers multiple commands to compare files. The diff, comm, and cmp commands compare differences and are some of 
the most useful Linux commands you must know:

```bash
diff <file-1> <file-2>
```

The cmp command only tells use the line number which is different:

```bash
cmp <file-1> <file-2>
```

The text that’s aligned to the left is the text that’s only present in file 1. The center-aligned text is present only 
in file 2. And the right-aligned text is present in both the files:

```bash
comm <file-1> <file-2>
```

## sort

The sort command will provide a sorted output of the contents of a file:

```bash
sort <filename>
```

## export

The export command is specially used when exporting environment variables in runtime:

```bash
export <variable-name>=<value>
```

## ssh

The ssh command allows us to connect to an external machine on the network with the use of the ssh protocol:

```bash
ssh username@hostname
```

## service

The service command in Linux is used for starting and stopping different services within the operating system: 

```bash
service ssh status
service ssh stop
service ssh start
```

## ps, kill and killall

While we’re on the topic of processes, let’s see how we can find active processes and kill them. To find the running 
processes, we can simply type ps in the terminal prompt and get the list of running processes.

```bash
ps
kill <process-id>
killall <process-name>
```

## df and mount

Mount means that we’ll connect the device to a folder so we can access the files from our filesystem:

```bash
mount /dev/cdrom /mnt
```

To see the mounted devices and get more information about them, we make use of the df command:

```bash
df -h
```

## chmod and chown

The chmod and chown commands give us the functionality to change the file permissions and file ownership are the 
most important Linux commands you should know. The main difference between the functions of the two commands is that 
the chmod command allows changing file permissions, while chown allows us to change the file owners:

```bash
chmod <parameter> <filename>
```

```bash
chown <user:group> <filename>
```

## ifconfig and traceroute

The ifconfig command will give you the list of all the network interfaces along with the IP addresses, MAC addresses and 
other information about the interface:

```bash
ifconfig
```

When working with traceroute, you can simply specify the IP address, the hostname or the domain name of the endpoint:

```bash
traceroute <destination-address>
```

## wget

If you want to download a file from within the terminal, the wget command is one of the handiest command-line 
utilities available:

```bash
wget <link-to-file>
wget -c <link-to-file>
```

## ufw and iptables

UFW and IPTables are firewall interfaces for the Linux Kernel’s netfilter firewall. IPTables directly passes firewall 
rules to netfilter while UFW configures the rules in IPTables which then sends those rules to netfilter:

```bash
iptables -A INPUT -p tcp -m tcp --dport 80 -j ACCEPT
```

```bash
ufw allow 80
```

## apt, pacman, yum, rpm

Different distros of Linux make use of different package managers:

Debian and Debian-based distros:

```bash
apt install <package-name>
```

Arch and Arch-based distros:

```bash
pacman -S <package-name>
```

Red Hat and Red Hat-based distros:

```bash
 yum install <package-name>
```

Fedora and CentOS:

```bash
yum install <package>
```

## sudo

This command is equivalent to having logged in as root (based on what permissions you have as a sudoer):

```bash
sudo <command-you-want-to-run>
```

## cal

The cal command displays a well-presented calendar on the terminal:

```bash
cal
cal May 2020
```

## alias

If you know a command that you run very often, it’s time to create an alias: 

```bash
alias lsl="ls -l"
```

## dd

This command was created to convert and copy files from multiple file system formats:

```bash
dd if = /dev/sdb of = /dev/sda
```

## whereis

The whereis command will output the exact location of any command that you type in after the whereis command:

```bash
whereis sudo
```

The whatis command gives us an explanation of what a command actually is:

```bash
whatis sudo
```

## top

It shows a live view of the processes and all the information accompanying those processes like memory usage, CPU usage, 
etc:

```bash
top
```

## useradd and usermod

The useradd or adduser commands are the exact same commands where adduser is just a symbolic link to the useradd command. 
This command allows us to create a new user in Linux:

```bash
useradd user -d /home/user
```

The usermod command, on the other hand, is used to modify existing users:

```bash
usermod user -a -G sudo, audio, mysql
```

## passwd

The passwd command lets you set the password for your own account, or if you have the permissions, set the password 
for other accounts:

```bash
passwd
```

***

## Appendix: Links and References

- [[Developer/Development]]
- [[Templates/Development/Linux]]
- [[Bash]]

***

Jimmy Briggs <jimmy.briggs@jimbrig.com> | 2022