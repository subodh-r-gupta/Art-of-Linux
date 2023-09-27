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

