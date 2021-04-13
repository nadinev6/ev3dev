# Flash OS Image to microSD Card  

* [Prerequisites](#prerequisites)
  * [Download SD card image](#download-sd-card-image)
* [Download balenaEtcher](#download-balenaetcher)
* [Flash ev3dev2](#flash-ev3dev2)
  * 1 [Copy image link](#copy-image-link)
  * 2 [Select device](#select-device)
  * 2 [Flash image](#flash-image)

  
 

### Prerequisites

#### Download SD card image

The generic version 2.0.0 of ev3dev-scratch image is updated in this repository and [found here](https://github.com/ev3dev/ev3dev/releases/download/ev3dev-stretch-2020-04-10/ev3dev-stretch-ev3-generic-2020-04-10.zip)

The latest verified version (compatible with Rasberry Pi) can be found in this external respository https://github.com/ev3dev/ev3dev/releases

### Download balenaEtcher

Software | Version | Download  
------------- | ------------- | -------------
balenaEtcher  | v1.5.116 |  [64bit](https://github.com/balena-io/etcher/releases/download/v1.5.116/balenaEtcher-Portable-1.5.116.exe?d_id=8a514ffb-fc38-4cf4-bfc2-80e68de5450eR)

<br>

### Flash ev3dev2


#### Copy image link

Select ':link: Flash from URL'

<br>

 <img src="https://github.com/nadinev6/ev3dev/blob/main/Windows/balenaEtcher.png">
 
 #### Select device
 
 Click 'Select target' and balena will automatically detect an external drive 
 
 Right click and copy & paste the link to the generic version 2.0.0 of ev3dev-stretch on this page
 

 <kbd>
⚠️ This is overwrite anything on the disk selected
 </kbd>

#### Flash image
 
 Click 'Flash!'
 
 The software will first decompress the drive. This should take a few minutes
 
 It will the begin installing the ev3dev2 OS
 
 You can then remove the SD card and insert it into the EV3 device via the SD card slot

<br>

 <img src="https://github.com/nadinev6/ev3dev/blob/main/Windows/balena-icon.jpg" width="28"> (Credits: https://www.balena.io/etcher/) 
