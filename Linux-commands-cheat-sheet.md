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

## Performance monitoring and statistics
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

## User information and User account management
Usage | Command
------|--------
Display the user and group ids of current user |	id
Display the last users who have logged onto the system | last
Show who is logged into the system currently |	who
Show who is logged in and what they are doing |	w
Create a group named "test" | groupadd test
Create an account named john, with a comment of "John Smith" and create the user's home directory | useradd -c "John Smith" -m john
Delete the john's account |	userdel john
Add the john's account to the sales group	| usermod -aG sales john
