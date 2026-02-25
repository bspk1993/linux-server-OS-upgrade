# linux-server-OS-upgrade

**cat /etc/os-release

uname -r(optional)

dpkg -l(package installations)

tar -czf etc_backup.tar.gz /etc

apt update

apt upgrade -y

do-release-upgrade

cat /etc/os-release**


# CPU Utilization & memory utilization ,disk space issues

CPU Usage:
top: Displays real-time, interactive CPU and memory usage.

mpstat: Provides detailed CPU utilization reports.

vmstat 1 5: Displays system statistics, including CPU load, over a period.

Memory Usage:

free -m: Shows total, used, and free memory in megabytes.

cat /proc/meminfo: Provides detailed information on system memory.

Disk space usage and increasing 

lslbk- check the existing usage/partitions

df -h - which filesystem need space

sudo resize2fs /dev/sda3,4 etc with any name

# Mounting EFS to EC2 instance 

give 2049 port in inbound rule of the EC2 instance 

sudo apt-get update && sudo apt-get install -y amazon-efs-utils.

creat the mount point - sudo mkdir -p /mnt/efs

give the mounting command in EFS like - sudo mount -t efs -o tls fs-12345678:/ /mnt/efs

check with df -h



