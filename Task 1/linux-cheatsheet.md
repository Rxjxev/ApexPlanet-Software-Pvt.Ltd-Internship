# Linux Cheat Sheet

Linux is the most widely used operating system in cybersecurity and penetration testing due to its stability, flexibility, and powerful command-line tools. Most security tools such as Nmap, Wireshark, Metasploit, and Burp Suite run efficiently on Linux-based systems like Kali Linux.

---

## File System Commands

Linux follows a hierarchical file system structure starting from the root (`/`).

pwd  
Displays the present working directory.

ls  
Lists files and directories in the current directory.

ls -l  
Displays detailed information including permissions and ownership.

ls -a  
Shows hidden files.

cd directory_name  
Changes the current directory.

cd ..  
Moves one directory up.

cd /  
Moves to the root directory.

---

## File & Directory Management

touch file.txt  
Creates an empty file.

mkdir folder_name  
Creates a new directory.

rm file.txt  
Deletes a file.

rm -r folder_name  
Deletes a directory and its contents.

cp source destination  
Copies files.

mv source destination  
Moves or renames files.

---

## File Permissions & Ownership

Linux permissions control who can read, write, or execute files.

### Permission Types
- r (read)
- w (write)
- x (execute)

### Permission Representation
- Owner
- Group
- Others

chmod 777 file.txt  
Gives read, write, and execute permissions to everyone (not recommended for production).

chmod 755 file.txt  
Common permission for scripts and binaries.

chown user:user file.txt  
Changes file owner and group.

---

## User & Process Management

whoami  
Displays current user.

id  
Shows user ID and group ID.

ps  
Displays running processes.

top  
Shows real-time process monitoring.

kill PID  
Terminates a process.

---

## Package Management (APT)

APT is used to install, update, and manage software packages.

sudo apt update  
Updates package list.

sudo apt upgrade  
Upgrades installed packages.

sudo apt install package-name  
Installs a package.

sudo apt remove package-name  
Removes a package.

---

## Networking Commands

ifconfig  
Displays network interfaces and IP addresses.

ip a  
Modern alternative to ifconfig.

ping google.com  
Checks network connectivity.

netstat -tuln  
Displays open ports and listening services.

ss -tuln  
Modern replacement for netstat.

traceroute google.com  
Shows the path taken by packets.

---

## Disk & System Information

df -h  
Shows disk usage.

du -sh folder_name  
Shows folder size.

uname -a  
Displays system information.

hostname  
Shows system hostname.

---

## File Viewing & Editing

cat file.txt  
Displays file content.

less file.txt  
Views large files.

nano file.txt  
Terminal-based text editor.

vim file.txt  
Advanced text editor.

---

## Logs & Monitoring (Important for Security)

tail -f /var/log/syslog  
Monitors system logs.

journalctl  
Displays system logs.

---

## Commonly Used in Cybersecurity

sudo  
Runs command with administrative privileges.

history  
Shows command history.

clear  
Clears terminal screen.
