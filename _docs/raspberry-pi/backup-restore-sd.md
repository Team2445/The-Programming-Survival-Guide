---
layout: default
category: Raspberry Pi
order: 2
title: Backing up and Restoring SD Card
---
>NOTE: For this guide, you will need a Linux or Mac  

## Backup
1. Plug in the SD Card you would like to backup into your computer
2. Open up a Terminal window  
3. `sudo fdisk -l` to view the available disks to identify the raspberry pi  
You should have output similar to this:  

```shell
Disk /dev/sda: 30 GiB, 32212254720 bytes, 62914560 sectors
Units: sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes
Disklabel type: dos
Disk identifier: 0xf5e7c3c1

Device     Boot    Start      End  Sectors Size Id Type
/dev/sda1  *        2048 54527999 54525952  26G 83 Linux
/dev/sda2       54530046 62912511  8382466   4G  5 Extended
/dev/sda5       54530048 62912511  8382464   4G 82 Linux swap / Solaris


Disk /dev/sdb: 14.9 GiB, 15931539456 bytes, 31116288 sectors
Units: sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes
Disklabel type: dos
Disk identifier: 0x738a4d67

Device     Boot  Start      End  Sectors  Size Id Type
/dev/sdb1         8192   532479   524288  256M  c W95 FAT32 (LBA)
/dev/sdb2       532480 31116287 30583808 14.6G 83 Linux
```  

4. Once you identify your disk, run this command
```shell
sudo dd if=/dev/sdx of=~/Desktop/YYYY-MM-name-of-backup.img
```
> Where `sdx` is your SD card. In this example, it is `sdb`


## Restore
1. Plug in the SD Card you would like to restore into your computer
2. Open up a Terminal window  
3. `sudo fdisk -l` to view the available disks to identify the raspberry pi  
You should have output similar to this:  

```shell
Disk /dev/sda: 30 GiB, 32212254720 bytes, 62914560 sectors
Units: sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes
Disklabel type: dos
Disk identifier: 0xf5e7c3c1

Device     Boot    Start      End  Sectors Size Id Type
/dev/sda1  *        2048 54527999 54525952  26G 83 Linux
/dev/sda2       54530046 62912511  8382466   4G  5 Extended
/dev/sda5       54530048 62912511  8382464   4G 82 Linux swap / Solaris


Disk /dev/sdb: 14.9 GiB, 15931539456 bytes, 31116288 sectors
Units: sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes
Disklabel type: dos
Disk identifier: 0x738a4d67

Device     Boot  Start      End  Sectors  Size Id Type
/dev/sdb1         8192   532479   524288  256M  c W95 FAT32 (LBA)
/dev/sdb2       532480 31116287 30583808 14.6G 83 Linux
```  

4. Once you identify your disk, run this command  

> WARNING: THIS WILL FORMAT ALL DATA ON THE DISK SPECIFIED. DOUBLE CHECK THAT YOU ARE FORMATING THE RIGHT DISK SINCE THERE WILL BE NO CONFIRMATION WHEN YOU RUN THIS COMMAND  

```shell
sudo dd if=~/Desktop/YYYY-MM-name-of-backup.img of=/dev/sdx bs=4M
```
> Where `sdx` is your SD card. In this example, it is `sdb`


