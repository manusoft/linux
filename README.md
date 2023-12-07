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

## Navigation Commands

### pwd
Print the current working directory.

```bash
pwd
```

### cd
Change the current directory.

```bash
cd /path/to/directory
```

### ls
List files and directories in the current directory.

```bash
ls
ls -l
ls -a
```

## File and Directory Operations

### cp
Copy files or directories.

```bash
cp file.txt /path/to/destination
cp -r directory /path/to/destination
```

### mv
Move or rename files or directories.

```bash
mv file.txt /path/to/destination
mv oldname.txt newname.txt
```

### rm
Remove files or directories.

```bash
rm file.txt
rm -r directory
```

### mkdir
Create a new directory.

```bash
mkdir new_directory
```

## System Information

### uname
Print system information.

```bash
uname -a
```

### lsb_release
Display LSB (Linux Standard Base) information.

```bash
lsb_release -a
```

### df
Show disk space usage.

```bash
df -h
```

## Package Management

### apt
Advanced Package Tool - package management.

```bash
sudo apt update
sudo apt upgrade
sudo apt install package_name
sudo apt remove package_name
```

## User and Group Management

### useradd
Add a new user.

```bash
sudo useradd username
```

### passwd
Change user password.

```bash
sudo passwd username
```

### usermod
Modify user properties.

```bash
sudo usermod -aG groupname username
```

## Process Management

### ps
Display information about running processes.

```bash
ps aux
```

### top
Display and manage processes.

```bash
top
```

### kill
Terminate a process.

```bash
kill process_id
```

## Network Commands

### ifconfig
Configure network interfaces.

```bash
ifconfig
```

### ping
Check network connectivity.

```bash
ping example.com
```

### netstat
Display network connections.

```bash
netstat -a
```

## File Editing

### nano
Text editor for the command line.

```bash
nano filename
```

### vim
Highly configurable text editor.

```bash
vim filename
```

## System Services

### systemctl
Control system services.

```bash
sudo systemctl start service_name
sudo systemctl stop service_name
sudo systemctl restart service_name
```

## Permissions

### chmod
Change file permissions.

```bash
chmod +x filename
```

### chown
Change file owner.

```bash
chown new_owner:new_group filename
```

## Archiving and Compression

### tar
Archive files and directories.

```bash
tar -cvf archive.tar file1 file2
```

### gzip
Compress files.

```bash
gzip filename
```

## Search Commands

### find
Search for files and directories.

```bash
find /path/to/search -name "filename"
```

### grep
Search for patterns in files.

```bash
grep "pattern" filename
```





