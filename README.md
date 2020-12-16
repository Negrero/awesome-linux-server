# 9 things to do in your first 10 minutes on a Linux server
(ref article)[https://opensource.com/article/20/12/linux-server]
1. First contact
  
```
cat /etc/redhat-release
uname -a
hostnamectl
uptime
```

2. is anyone else on board?

```
who
who -Hu
grep sh$ /etc/passwd
```

3. Physical or virtual machine

```
dmidecode -s system-manufacturer
dmidecode -s system-product-name
lshw -c system | grep product | head -1
cat /sys/class/dmi/id/product_name
cat /sys/class/dmi/id/sys_vendor
```

4. Hardware

```
lscpu or cat /proc/cpuinfo
lsmem or cat /proc/meminfo
ifconfig -a
ethtool <devname>
lshw
lspci
dmidecode
```

5. Installed software

```
rpm -qa
rpm -qa | grep <pkgname>
rpm -qi <pkgname>
yum repolist
yum repoinfo
yum install <pkgname>
ls -l /etc/yum.repos.d/
```

6. Running processes and services

```
pstree -pa 1
ps -ef
ps auxf
systemctl
```

7. Network connections

```
netstat -tulpn
netstat -anp
lsof -i
ss
iptables -L -n
cat /etc/resolv.conf
```

8. Kernel

```
uname -r
cat /proc/cmdline
lsmod
modinfo <module>
sysctl -a
cat /boot/grub2/grub.cfg
```

9. Logs

```
dmesg
tail -f /var/log/messages
journalctl
```