# Gather Linux Info

|Information|RHEL Pre 7.0|Ubuntu Pre 15.04|Systemd Based|
|---|---|---|---|
|Date/Time|date|date|date|
|Hostname (FQDN)|hostname -f|hostname -f|hostname -f|
|IP Address|ip addr|ip addr|ip addr|
|Routing|ip route|ip route|ip route|
|Logged in users|w|w|w|
|All processes (BSD Style)|ps aux|ps aux|ps aux|
|All processes (POSIX Style)|ps -ef|ps -ef|ps -ef|
|Uptime|uptime|uptime|uptime|
|Hard DNS|cat /etc/hosts|cat /etc/hosts|cat /etc/hosts|
|DNS Resolvers|cat /etc/resolv.conf|cat /etc/resolv.conf|cat /etc/resolv.conf|
|Processes for user|ps -U <user>|ps -U <user>|ps -U <user>|
|Listening Ports|netstat -lntp|netstat -lntp|netstat -lntp|
|Mounted Devices|mount|mount|mount|
|System Mounts|cat /etc/fstab|cat /etc/fstab|cat /etc/fstab|
|Kernel Version (All)|uname -a|uname -a|uname -a|
|Release information|cat /etc/redhat-release|cat /etc/debian_version|cat /etc/os-release|
|Cron information|crontab -u -l <user>|crontab -u -l <user>|systemctl list-timers|
|Loaded Kernel Modules|lsmod|lsmod|lsmod|
|Running Services|chkconfig --list|service --status-all|systemctl list-units|
|Startup Script Directory|/etc/init.d|/etc/init.d|/usr/lib/systemd/system|
|Firewall Settings|iptables -L|iptables -L|firewall-cmd --list-all|
|Kernel Log|dmesg|dmesg|dmesg|
|Memory Usage|free -m|free -m|free -m|
|CPU Info|cat /proc/cpuinfo|cat /proc/cpuinfo|cat /proc/cpuinfo|
|PCI Devices|lspci|lspci|lspci|
|USB Devices|lsusb|lsusb|lsusb|
|Attached Disks|lsblk|lsblk|lsblk|
|Start Service|/etc/init.d/<name> start|service <name> start|systemctl start <name>|
|Stop Service|/etc/init.d/<name> stop|service <name> stop|systemctl stop <name>|
|Enable Service|chkconfig <name> on|update-rc.d <name> defaults|systemctl enable <name>|
|Disable Service|chkconfig <name> off|update-rc.d <name> disable|systemctl disable <name>|
|Service File Directory|/etc/init.d/|"/etc/rc{0|1|2|3|4|5|6}.d/"|/usr/lib/systemd/system/|
