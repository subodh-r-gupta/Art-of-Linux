# Linux Commands : Cheat Sheet
---

## System Information Commands
Usage | Command
------|--------
Display Linux system information	| uname -a
Display kernel release information	| uname -r
Show which version of Red Hat is installed	| cat /etc/redhat-release
Show how long the system has been up and running + load	| uptime
Show system host name	| hostname
Display all local IP addresses of the host  |	hostname -I
Show system reboot history	| last reboot
Show the current date and time	| date
Show this month's calendar	| cal
show who is online	| w
show Who you are logged in as	| whoami

## Hardware Information Commands
Usage | Command
------|--------
Display messages in kernel ring buffer	| dmesg
Display CPU information	| cat /proc/cpuinfo
Display memory information	| cat /proc/meminfo
Display free and used memory ( -h for human readable, -m for MB, -g for GB.)	| free -h
Display PCI devices	| lspci -tv
Display USB devices	| lsusb -tv
Display DMI/SMBIOS (hardware info) from the BIOS	| dmidecode
Show info about disk sda	| hdparm -i /dev/sda
Perform a read speed test on disk sda	| hdparm -tT /dev/sda
Test for unreadable blocks on disk sda	| badblocks -s /dev/sda

## Performance monitoring and statistics Commands
Usage | Command
------|--------
Display and manage the top processes	| top
Interactive process viewer (top alternative)	| htop
Display processor related statistics	| mpstat 1
Display virtual memory statistics	| vmstat 1
Display I/O statistics	| iostat 1
Display the last 100 syslog messages  (Use /var/log/syslog for Debian based systems.)	| tail -100 /var/log/messages
Capture and display all packets on interface eth0	| tcpdump -i eth0
Monitor all traffic on port 80 ( HTTP )	| tcpdump -i eth0 'port 80'
List all open files on the system	| lsof
List files opened by user	| lsof -u user
Display free and used memory ( -h for human readable, -m for MB, -g for GB.)	| free -h
Execute "df -h", showing periodic updates	| watch df -h

## User information and User account management Commands
Usage | Command
------|--------
Display the user and group ids of current user |	id
Display the last users who have logged onto the system | last
Show who is logged into the system currently |	who
Show who is logged in and what they are doing |	w
Create a group named "test" | groupadd test
Create an account named john, with a comment of "John Smith" and create the user's home directory | useradd -c "John Smith" -m john
Delete john's account |	userdel john
Add john's account to the sales group	| usermod -aG sales john

## File and Directory commands
Usage | Command
------|--------
List all files in a long listing (detailed) format	| ls -al
Display the present working directory	| pwd
Create a directory	| mkdir directory-name
Remove (delete) file	| rm file
Remove the directory and its contents recursively	| rm -r directory
Forcefully remove a file without prompting for confirmation	| rm -f file
Forcefully remove directory recursively	| rm -rf directory
Copy file1 to file2	| cp file1 file2
Copy source_directory recursively to destination. If destination exists, copy source_directory into destination,
otherwise create destination with the contents of source_directory. |	cp -r source_directory destination
Rename file1 to file2. If file2 is an existing directory, move file1 into directory file2	| mv file1 file2	
Create symbolic link to linkname	| ln -s /path/to/file linkname
Create an empty file or update the access and modification times of file |	touch file
View the contents of file	| cat file
Browse through a text file	| less file
Display the first 10 lines of file	| head file
Display the last 10 lines of file	| tail file
Display the last 10 lines of file and "follow" the file as it grows |	tail -f file

## File Permissions
Legends in command outputs , Example command ls -ali
Legend | Meaning
-------|--------
U | User
G | Group
W | World	

Permissions in command outputs, Example command ls -ali
Legend | Meaning
-------|--------
r | Read 
w | write 
x | execute
\- | no access

## Process Management Commands
Usage | Command
------|--------
Display your currently running processes	| ps
Display all the currently running processes on the system |	ps -ef
Display process information for processname	| ps -ef \| grep processname
Display and manage the top processes	| top
Interactive process viewer (top alternative)	| htop
Kill process with process ID of pid	kill | pid
Kill all processes named processname	| killall processname
Start program in the background	| program &
Display stopped or background jobs	| bg
Brings the most recent background job to foreground	| fg
Brings job n to the foreground	| fg n

## Networking Commands
Usage | Command
------|--------
Display all network interfaces and IP address	| ip a
Display eth0 address and details	| ip addr show dev eth0
Query or control network driver and hardware settings	| ethtool eth0
Send ICMP echo request to host	| ping host
Display whois information for domain | whois domain
Display DNS information for domain	| dig domain
Reverse lookup of IP_ADDRESS	| dig -x IP_ADDRESS
Display DNS IP address for domain	| host domain
Display the network address of the host name |	hostname -i
Display all local IP addresses of the host |	hostname -I
Download http://domain.com/file	| wget http://domain.com/file
Display listening tcp and udp ports and corresponding programs	| netstat -nutlp


## File Archival and Extraction Commands
Usage | Command
------|--------
Create tar named archive.tar containing directory |	tar cf archive.tar directory
Extract the contents from archive.tar | 	tar xf archive.tar
Create a gzip compressed tar file name archive.tar.gz | 	tar czf archive.tar.gz directory
Extract a gzip compressed tar file | tar xzf archive.tar.gz
Create a tar file with bzip2 compression	| tar cjf archive.tar.bz2 directory
Extract a bzip2 compressed tar file |	tar xjf archive.tar.bz2

Package Management Commands
Usage | Command
------|--------
Search for a package by keyword | yum search keyword
Install package | yum install package
Display description and summary information about package |	yum info package
Install package from local file named package.rpm	| rpm -i package.rpm
Remove/uninstall package |	yum remove package
Install software from source code | "tar zxvf sourcecode.tar.gz
cd sourcecode
./configure
make
make install
"
	


