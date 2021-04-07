# Write an SD Card Image (Linux CLI Tools)

* [Prerequisites](#prerequisites)
  * [Download SD card image](#download-sd-card-image)
  * [Unzip the folder](#unzip-the-folder)
* [Identify disk path](#identify-disk-path)
  * [Unmount SD card](#unmount-sd-card)
* [Write to disk](#write-to-disk)
* [Check Write Completion)](*check-write-completion)
  


### Prerequisites

#### Download SD card image 

The generic version 2.0.0 of ev3dev-scratch image is updated in this repository :xref:`ev3dev micropython image` 

The latest verified version (compatible with Rasberry Pi) can be found in this external respository https://github.com/ev3dev/ev3dev/releases


#### Unzip the folder

cd to you downloads folder or replace with the path of the folder you have downloaded the image to

```console
cd Downloads
```

This unzips the zip file from this repository

```console
unzip ev3dev_micropython_image.zip
```
Identify the disks on your system

```console
diskutil
```


### Identify disk path

Insert a blank or rewritable SD card, then run the same command and take note of the path [DISK_NAME]

```console
diskutil
```
Output:

```console
[DISK_NAME]
   #:                       TYPE NAME                    SIZE       IDENTIFIER
   0:     FDisk_partition_scheme                        *2.0 GB     mydisk
   1:                 DOS_FAT_32 LABEL                   2.0 GB     mydisk1s1
```

#### Unmount SD card

.. warning::
 You will lose all the contents by writing the image to the card
 Make sure you select the correct disk name to avoid losing content

Replace [DISK_NAME] with the path that was returned on your console

```console
diskutil unmountDisk [DISK_NAME]
```


### Write to disk

```console
sudo dd if=~/Downloads/ev3dev.1900MB.img of=/dev/rdisk1 bs=4m
```

### Check Write Progress
```console
^T
```
