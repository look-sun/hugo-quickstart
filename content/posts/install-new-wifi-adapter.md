---
title: "Install New Wifi Adapter"
date: 2023-06-09T01:25:23+09:00
draft: true
---

I want to use aircrack-ng.
But my Laptop-installed wifi module doestn't supports *monitor* mode.
I try whole day, and I realized too lately.

I thought, I must buy new wifi adapter.
But before a hours, I found very old wifi adapter made in before 2013year.

I know that I must install driver about that I found to use for my purposes.
I'm going, and this is my paper.

https://linux-hardware.org/?probe=f8e59b4c0f
This is my laptop's hardware list.
I could know my adapter's chipset with this.
and chipset is 'Ralink Technology RT2870/RT3070 Wireless Adapter'

I searched duckduckgo and google with 'install rt2870', 'install ralink', 'rt2870 driver', ......
but many link's suggestion can't run.
example: https://askubuntu.com/questions/641724/how-to-install-rt2870-rt3070-wireless-driver
this site's answer's git-links can't working.

And I found this(https://wiki.debian.org/rt2800usb).
First, I don't know what it says.
because I just typing 'deb http://http.debian.net/debian/ stretch main contrib non-free' into terminal.
It's so....

Following this page,
1. add a "non-free" component to **/etc/apt/sources.list**
2. update the list of available packages
3. install firmware package

But now, I can't download *firmware-ralink* or *firmware-misc-nonfree*
I don't know why.
내 생각엔, *sources.list*에 추가한 링크가 안먹는것 같다. 


last terminal input and output:

*conflicted@CF-samsung:~$ sudo apt-get update
Hit:2 http://security.ubuntu.com/ubuntu jammy-security InRelease                                  
Hit:3 http://kr.archive.ubuntu.com/ubuntu jammy InRelease                                               
Ign:1 http://cdn-fastly.deb.debian.org/debian jessie InRelease                                          
Hit:4 http://kr.archive.ubuntu.com/ubuntu jammy-updates InRelease                                      
Get:6 http://kr.archive.ubuntu.com/ubuntu jammy-backports InRelease [108 kB]                           
Ign:7 https://ppa.launchpadcontent.net/thopiekar/mt7601/ubuntu jammy InRelease              
Err:5 http://cdn-fastly.deb.debian.org/debian jessie Release                   
  404  Not Found [IP: 146.75.50.132 80]
Err:8 https://ppa.launchpadcontent.net/thopiekar/mt7601/ubuntu jammy Release                     
  404  Not Found [IP: 185.125.190.52 443]
Reading package lists... Done
E: The repository 'http://http.debian.net/debian jessie Release' does not have a Release file.
N: Updating from such a repository can't be done securely, and is therefore disabled by default.
N: See apt-secure(8) manpage for repository creation and user configuration details.
E: The repository 'https://ppa.launchpadcontent.net/thopiekar/mt7601/ubuntu jammy Release' does not have a Release file.
N: Updating from such a repository can't be done securely, and is therefore disabled by default.
N: See apt-secure(8) manpage for repository creation and user configuration details.*



해결 안되서 쓴 일기다.
This is the paper include my hoping.






https://ubuntuforums.org/showthread.php?t=1342593&highlight=rt2870
http://www.opendrivers.com/product/ralink/rt2870
