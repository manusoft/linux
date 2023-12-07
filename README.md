# Linux

# Ubuntu Commands Documentation

This comprehensive guide provides an overview of essential Ubuntu commands along with practical examples to help users navigate and manage their Ubuntu Linux systems effectively.

## Table of Contents

1. [Navigation Commands](#navigation-commands)
2. [File and Directory Operations](#file-and-directory-operations)
3. [System Information](#system-information)
4. [Package Management](#package-management)
5. [User and Group Management](#user-and-group-management)
6. [Process Management](#process-management)
7. [Network Commands](#network-commands)
8. [File Editing](#file-editing)
9. [System Services](#system-services)
10. [Permissions](#permissions)
11. [Archiving and Compression](#archiving-and-compression)
12. [Search Commands](#search-commands)

# Navigation Commands

Navigation commands are fundamental for moving around the file system and managing directories.

## 1. `pwd` - Print Working Directory

Print the current working directory.

```bash
pwd
```

**Example:**
```bash
/home/user/documents
```

## 2. `cd` - Change Directory

Change the current directory.

```bash
cd /path/to/directory
```

**Example:**
```bash
cd /home/user/documents
```

## 3. `ls` - List Files and Directories

List files and directories in the current directory.

```bash
ls
ls -l
ls -a
```

**Examples:**
```bash
# Basic listing
ls

# Detailed listing
ls -l

# Show hidden files
ls -a
```

These commands help you navigate through directories, understand your current location, and inspect the contents of a directory.

# File and Directory Operations

File and directory operations are essential for managing files, copying, moving, and removing them.

## 1. `cp` - Copy

Copy files or directories.

```bash
cp source_file destination
cp -r source_directory destination
```

**Examples:**
```bash
# Copy a file to a destination
cp file.txt /path/to/destination

# Copy a directory and its contents to a destination
cp -r directory /path/to/destination
```

## 2. `mv` - Move/Rename

Move or rename files or directories.

```bash
mv source destination
mv oldname.txt newname.txt
```

**Examples:**
```bash
# Move a file to a destination
mv file.txt /path/to/destination

# Rename a file
mv oldname.txt newname.txt
```

## 3. `rm` - Remove

Remove files or directories.

```bash
rm file.txt
rm -r directory
```

**Examples:**
```bash
# Remove a file
rm file.txt

# Remove a directory and its contents
rm -r directory
```

## 4. `mkdir` - Make Directory

Create a new directory.

```bash
mkdir new_directory
```

**Example:**
```bash
# Create a new directory
mkdir documents
```

These commands enable you to manage files and directories, whether you're copying them, moving them to a different location, renaming them, or deleting them. Use them with caution, especially when dealing with the rm command, as it permanently deletes files.

# System Information

System information commands provide details about the operating system and its configuration.

## 1. `uname` - Print System Information

Print system information.

```bash
uname -a
```

**Example:**
```bash
Linux hostname 5.4.0-104-generic #127-Ubuntu SMP Thu Apr 29 14:20:18 UTC 2021 x86_64 x86_64 x86_64 GNU/Linux
```

## 2. `lsb_release` - Display LSB Information

Display Linux Standard Base (LSB) information.

```bash
lsb_release -a
```

**Example:**
```bash
Distributor ID: Ubuntu
Description:    Ubuntu 20.04.2 LTS
Release:        20.04
Codename:       focal
```

## 3. `df` - Show Disk Space Usage

Show disk space usage.

```bash
df -h
```

**Example:**
```bash
Filesystem      Size  Used Avail Use% Mounted on
/dev/sda1        20G   8.2G   11G  44% /
```

These commands help you understand the system environment, kernel version, and disk space utilization, providing crucial information for system administration and troubleshooting.

# Package Management

Package management commands are used to install, upgrade, and remove software packages on Ubuntu.

## 1. `apt` - Advanced Package Tool

The `apt` command is the primary package management tool for Ubuntu.

### Update Package List

Update the local package database.

```bash
sudo apt update
```

### Upgrade Packages

Upgrade installed packages to their latest versions.

```bash
sudo apt upgrade
```

### Install Package

Install a new package.

```bash
sudo apt install package_name
```

### Remove Package

Remove a package.

```bash
sudo apt remove package_name
```

**Examples:**
```bash
# Update package list
sudo apt update

# Upgrade installed packages
sudo apt upgrade

# Install a new package
sudo apt install htop

# Remove a package
sudo apt remove firefox
```

These commands facilitate the installation, upgrade, and removal of software packages on your Ubuntu system. The apt tool ensures proper dependency management and simplifies package-related tasks.

# User and Group Management

User and group management commands are essential for handling user accounts and associated groups on Ubuntu.

## 1. `useradd` - Add a New User

Create a new user account.

```bash
sudo useradd username
```

**Example:**
```bash
sudo useradd john_doe
```

## 2. `passwd` - Change User Password

Change the password for a user.

```bash
sudo passwd username
```

**Example:**
```bash
sudo passwd john_doe
```

## 3. `usermod` - Modify User Properties

Modify user properties, such as group membership.

```bash
sudo usermod -aG groupname username
```

**Example:**
```bash
sudo usermod -aG sudo john_doe
```

These commands allow you to manage user accounts by creating new users, updating their passwords, and modifying their group memberships. Proper user and group management are crucial for controlling access and permissions on a system.

# Process Management

Process management commands are used to monitor and control running processes on Ubuntu.

## 1. `ps` - Display Information about Processes

Display information about running processes.

```bash
ps aux
```

**Example:**
```bash
USER       PID  %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
user      1234  0.0  0.1 123456  7890 ?        Ss   Dec01   0:00 /usr/bin/example
```

## 2. `top` - Display and Manage Processes

Display and manage processes in real-time.

```bash
top
```

**Example:**
```bash
top - 14:28:35 up  1:24,  1 user,  load average: 0.00, 0.01, 0.05
Tasks: 123 total,   1 running, 122 sleeping,   0 stopped,   0 zombie
%Cpu(s):  2.0 us,  1.0 sy,  0.0 ni, 96.8 id,  0.2 wa,  0.0 hi,  0.0 si,  0.0 st
MiB Mem :   7862.2 total,   1234.5 free,   4567.8 used,   1059.9 buff/cache
MiB Swap:   1024.0 total,    842.5 free,    181.5 used.   2787.2 avail Mem

  PID USER      PR  NI    VIRT    RES    SHR S  %CPU  %MEM     TIME+ COMMAND
 1234 user      20   0 123456  7890  5678 S   0.0   0.1   0:00.01 example
```

## 3. `kill` - Terminate a Process

Terminate a process by sending a signal.

```bash
kill process_id
```

**Example:**
```bash
kill 1234
```

These commands provide insights into running processes, their resource usage, and allow you to manage them effectively. Use caution when terminating processes to avoid unintended consequences.

# Network Commands

Network commands on Ubuntu are crucial for configuring network interfaces, checking connectivity, and monitoring network-related information.

## 1. `ifconfig` - Configure Network Interfaces

Configure network interfaces and display their configuration.

```bash
ifconfig
```

**Example:**
```bash
enp0s3: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 192.168.1.2  netmask 255.255.255.0  broadcast 192.168.1.255
        inet6 fe80::a00:27ff:fe51:bd4c  prefixlen 64  scopeid 0x20<link>
        ether 08:00:27:51:bd:4c  txqueuelen 1000  (Ethernet)
        RX packets 12345  bytes 6789012 (6.7 MB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 56789  bytes 12345678 (12.3 MB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
```

## 2. `ping` - Check Network Connectivity

Check network connectivity to a host.

```bash
ping example.com
```

**Example:**
```bash
PING example.com (93.184.216.34) 56(84) bytes of data.
64 bytes from 93.184.216.34: icmp_seq=1 ttl=56 time=11.1 ms
```

## 3. `netstat` - Display Network Connections

Display information about network connections, routing tables, and interface statistics.

```bash
netstat -a
```

**Example:**
```bash
Proto Recv-Q Send-Q Local Address           Foreign Address         State
tcp        0      0 0.0.0.0:22              0.0.0.0:*               LISTEN
udp        0      0 0.0.0.0:5353            0.0.0.0:*
```

These commands are essential for managing network configurations, checking connectivity, and troubleshooting network-related issues. The examples provided offer insights into current network configurations and connectivity checks.

## File Editing

File editing commands are used to create, view, and modify text files directly from the command line.

## 1. `nano` - Text Editor for the Command Line

Open a text file for editing using the `nano` text editor.

```bash
nano filename
```

**Example:**
```bash
nano document.txt
```

Use the arrow keys to navigate, and press `Ctrl + X` to exit (followed by `Y` to confirm changes and `Enter`).

## 2. `vim` - Highly Configurable Text Editor

Open a text file for editing using the `vim` text editor.

```bash
vim filename
```

**Example:**
```bash
vim document.txt
```

In `vim`, press `i` to enter insert mode, make changes, and press `Esc` to exit insert mode. To save changes and exit, type `:wq` and press `Enter`.

These commands provide basic text editing capabilities directly from the command line. Choose between `nano` for a simple interface or `vim` for a more powerful and feature-rich text editor.

# System Services

System services on Ubuntu are controlled using the `systemctl` command. This allows for starting, stopping, restarting, and checking the status of services.

## 1. `systemctl` - Control System Services

Control system services using the `systemctl` command.

### Start a Service

```bash
sudo systemctl start service_name
```

**Example:**
```bash
sudo systemctl start apache2
```

### Stop a Service

```bash
sudo systemctl stop service_name
```

**Example:**
```bash
sudo systemctl stop apache2
```

### Restart a Service

```bash
sudo systemctl restart service_name
```

**Example:**
```bash
sudo systemctl restart apache2
```

### Check Status of a Service

```bash
sudo systemctl status service_name
```

**Example:**
```bash
sudo systemctl status apache2
```

These commands provide a way to manage system services, such as web servers, databases, or other background processes. Use them to ensure that services are running as expected and to troubleshoot any issues.

# Permissions

Permissions in Linux determine who can access files and directories and what actions they can perform. The `chmod` and `chown` commands are used to modify file and directory permissions.

## 1. `chmod` - Change File Permissions

Change the permissions of a file or directory.

### Symbolic Notation

```bash
chmod permissions filename
```

**Example:**
```bash
chmod +x script.sh
```

### Octal Notation

```bash
chmod 755 filename
```

**Example:**
```bash
chmod 644 document.txt
```

## 2. `chown` - Change File Owner

Change the owner of a file or directory.

```bash
chown new_owner:new_group filename
```

**Example:**
```bash
chown john:users document.txt
```

These commands are crucial for controlling access to files and directories. The `chmod` command modifies permissions, specifying who can read, write, or execute a file, while the `chown` command changes the owner of a file, allowing specific users or groups to have control over it. Use these commands with caution to maintain a secure and well-managed file system.

# Archiving and Compression

Archiving and compression commands in Ubuntu are used to bundle files and reduce their size for efficient storage and transfer.

## 1. `tar` - Archive Files and Directories

Create and extract archive files using the `tar` command.

### Create a Tar Archive

```bash
tar -cvf archive.tar file1 file2
```

**Example:**
```bash
tar -cvf backup.tar /home/user/documents
```

### Extract a Tar Archive

```bash
tar -xvf archive.tar
```

**Example:**
```bash
tar -xvf backup.tar
```

## 2. `gzip` - Compress Files

Compress files using the `gzip` command.

### Compress a File

```bash
gzip filename
```

**Example:**
```bash
gzip document.txt
```

### Decompress a File

```bash
gzip -d filename.gz
```

**Example:**
```bash
gzip -d document.txt.gz
```

These commands allow you to create archives of multiple files or directories and compress individual files to save space. The combination of `tar` and `gzip` is commonly used for creating compressed archives on Ubuntu systems.

# Search Commands

Search commands in Ubuntu help locate files, directories, and content within files.

## 1. `find` - Search for Files and Directories

Search for files and directories based on various criteria.

```bash
find /path/to/search -name "filename"
```

**Example:**
```bash
find /home/user/documents -name "*.txt"
```

## 2. `grep` - Search for Patterns in Files

Search for patterns within files.

```bash
grep "pattern" filename
```

**Example:**
```bash
grep "error" log.txt
```

These commands are essential for locating files and content within them. The `find` command is versatile and allows for complex search criteria, while `grep` is powerful for searching within the content of files. These tools are invaluable for system administration and troubleshooting.





