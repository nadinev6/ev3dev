# Write an SD Card Image (Linux CLI Tools)

* [Prerequisites](#prerequisites)
  * [Download SD card image](#download-sd-card-image)
* [Free disk space](#free-disk-space)
  * [Unmount SD card](#unmount-sd-card)
* [Decompress the downloaded image](#decompress-the-downloaded-image)
* [Check Write Completion)](*check-write-completion)
  
 

### Prerequisites

#### Download SD card image

The generic version 2.0.0 of ev3dev-scratch image is updated in this repository :xref:`ev3dev micropython image` 

The latest verified version (compatible with Rasberry Pi) can be found in this external respository https://github.com/ev3dev/ev3dev/releases


### Free disk space

Insert a blank or rewritable SD card (minimum 2GB capacity)

Run the following commad to create a new entry i.e ```[DISK_NAME]``` and a single partition (1)

```console
~ $ df
```

Output:

```console
@host ~/ $ df -h
Filesystem                  Size  Used Avail Use% Mounted on
/[PATH_NAME]/[DISK_NAME]1   119G   79G   34G  70% /
none                        4.0K     0  4.0K   0% /sys/fs/cgroup
udev                        7.8G   12K  7.8G   1% /dev
tmpfs                       1.6G  1.1M  1.6G   1% /run
none                        5.0M     0  5.0M   0% /run/lock
none                        7.9G  1.5M  7.9G   1% /run/shm
none                        100M  3.7M   97M   4% /run/user
/[PATH_NAME]/[DISK_NAME]1   2.0G  0.0G  2.0G   0% /media/user/LABEL


#### Unmount SD card


```console
~ $ sudo umount /dev/[DISK_NAME]1
```

### Decompress the downloaded image

cd to you downloads folder or replace with the path of the folder you have downloaded the image to
This unzips the zip file from this repository (or replace with path) and writes it to the SD card

```console
~ $ xzcat ~/Downloads/ev3dev_micropython_image.zip | sudo dd bs=4M of=/[PATH_NAME]/[DISK_NAME]1
```

### Check Write Completion

```console
~ $ sync
```
