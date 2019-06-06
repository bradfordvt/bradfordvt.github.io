---
title: "Network Attached Storage (NAS) Experimentation"
excerpt: "The page chronicles my experimentation into finding a sufficient Network Attached Storage solution for my home storage needs."
url: page.href
header:
  image: /assets/images/NASBanner.png
  teaser: assets/images/NASBanner.png
  icon: assets/images/NASHeaderLogo_small.png
gallery:
  - url: /assets/images/Seagate_Expansion1TB.jpg
    image_path: assets/images/Seagate_Expansion1TB.jpg
    alt: "placeholder Seagate_Expansion1TB"
    figcaption: "Seagate Expansion 1TB USB Drive"
  - url: /assets/images/DesktopUSBExpansionDiagram.png
    image_path: assets/images/DesktopUSBExpansionDiagram.png
    alt: "placeholder DesktopUSBExpansionDiagram"
    figcaption: "Diagram of desktop backup configuration"
  - url: /assets/images/Seagate_GoFlexFreeAgent2.jpg
    image_path: assets/images/Seagate_GoFlexFreeAgent2.jpg
    alt: "placeholder Seagate_GoFlexFreeAgent2"
    figcaption: "Seagate GoFlex FreeAgent 2TB USB Drive"
  - url: /assets/images/techspecs-wndr4500-product-diagram.jpg
    image_path: assets/images/techspecs-wndr4500-product-diagram.jpg
    alt: "placeholder techspecs-wndr4500-product-diagram"
    figcaption: "Netgear WNDR4500 with ReadyShare"
  - url: /assets/images/WNDR4500ReadyShareDiagram.png
    image_path: assets/images/WNDR4500ReadyShareDiagram.png
    alt: "placeholder WNDR4500ReadyShareDiagram"
    figcaption: "WNDR4500 ReadyShare Configuration"
  - url: /assets/images/Cirago_NS2000.jpg
    image_path: assets/images/Cirago_NS2000.jpg
    alt: "placeholder Cirago_NS2000"
    figcaption: "Cirago NS-2000 Network USB Storage Link+"
  - url: /assets/images/CiragoNS2000Diagram.png
    image_path: assets/images/CiragoNS2000Diagram.png
    alt: "placeholder CiragoNS2000Diagram"
    figcaption: "Cirago NS-2000 Configuration"
  - url: /assets/images/Seagate_BackupPlus.jpg
    image_path: assets/images/Seagate_BackupPlus.jpg
    alt: "placeholder Seagate_BackupPlus"
    figcaption: "Seagate BackupPlus 2TB USB Drive"
  - url: /assets/images/WD_MyCloud2TB.jpg
    image_path: assets/images/WD_MyCloud2TB.jpg
    alt: "placeholder WD_MyCloud2TB"
    figcaption: "Western Digital MyCloud 2TB"
  - url: /assets/images/WD_MyCloud2TBDiagram.png
    image_path: assets/images/WD_MyCloud2TBDiagram.png
    alt: "placeholder WD_MyCloud2TBDiagram"
    figcaption: "MyCloud Backup Configuration"
  - url: /assets/images/PogoplugPro.jpg
    image_path: assets/images/PogoplugPro.jpg
    alt: "placeholder PogoplugPro"
    figcaption: "Cloud Engines Pogoplug Pro"
  - url: /assets/images/PogoPlugProDiagram.png
    image_path: assets/images/PogoPlugProDiagram.png
    alt: "placeholder PogoPlugProDiagram"
    figcaption: "Debian Pogoplug Pro NAS Configuration"

---
Network Attached Storage (NAS) for my home office was the most important home project and required a lot of product evaluations and experimentation.  I tried a few commercial products hoping for an "Off-the-Shelf" solution to my NAS needs.  I will try to show you my thought process and progression of technology and reveal my assessment of each of the options I have tried.

+ **USB External Drive:** Initially, I used external USB disk drives attached to my home office desktop PC as a share server.  This was a Seagate 1TB USB Expansion Drive.  When I needed to back up my laptop and other computers on the network, I would have to leave the desktop PC on.  This was cumbersome and was not a very energy efficient solution.  Eventually, I added a Seagate 2TB GoFlex Free Agent USB Drive for redundant backup of the Expansion Drive.
+ **Netgear ReadyShare:** The Netgear router I upgraded my home network to incorporated 2 USB ports that supported the ReadyShare service hosted by the router software.  I initially connected 2 USB External Drives to these ports that were originally connected to my desktop PC.  The configuration of the drive access was easy.  However, the availability of the drives was not reliable.  Each drive contained its own separate power supply, so I figured there was a limited load on the router USB port.  I played around with using a USB hub connecting these drives to the router and found the drives were still visible correctly using the hub and a single USB port on the router.  The reliability improved significantly, but not available all the time.  However, it provided me with a NAS that was more efficient and more convenient than using the desktop PC.  Still I tried to find a more reliable solution that could also handle automatic redundancy backup.
+ **Cirago NS-2000:** The NS-2000 is a small NAS device with a 1Gb Ethernet interface hosting 4 USB 2.0 ports that support SMB and WebDAV sharing protocols as well as being a streaming server and and bittorrent server.  The device was simple to install and configure. I moved the Seagate Expansion Drive from the ReadyShare to the NS-2000 to start testing.  The NS-2000 was certainly more reliable and the ReadyShare hosting a single drive also improved the reliability for that NAS.  I wanted to find a scalable solution.  The ReadyShare technology already failed that test.  The next step was to add a second drive to the NS-2000.  Adding 3 small USB Flash sticks to the NS-2000 was successful and ran for about a week before the unit stopped working.  It turned out the device heated up too hot and the software stopped running.  There was clearly a power overloading problem.  So I tried to use 2 USB External drives with independent power supplies to reduce the power consumption on the USB interfaces.  No change.  The NS-2000 could not reliably handle more than one drive.  However, after a month of operation, the NS-2000 overheated again and stopped working.  After cooling down and powering back up, it would work again.  Not an ideal situation.  The NS-2000 is really meant for hosting 4 USB flash devices.  I did find the power supply shipped with the unit was underrated for what was specified.  That power supply eventually died and I replaced it.  The NS-2000 has been running fine with 4 USB Flash drives varying in size from 64GB to 128GB.
+ **Western Digital MyCloud:** The WD MyCloud 2TB NAS looked extremely promising to serve as a sufficient home NAS server of all the products tested.  However, the software controlling the unit has a number of architectural issues.  The good news is it is Linux based and allows for access from SSH to work around the Web-based control panel used as the default control tool.  The architectural problem is the way WD implemented the streaming service tools.  To create the thumbnails of all video and image files, WD uses a program to run in the foreground to parse each directory and test each file and create a thumbnail if an image or video is located.  That program runs at the same priority as the Web interface making the Web control panel inoperative if many image or video files are copied to the drive.  The second architectural problem is the backup procedure relies on Rsync to copy shares to a backup USB drive.  If too many files are copied to the drive before the first backup, Rsync fails to complete successfully.  Thus, the MyCloud is not a great drive to replace an existing drive that is heavily populated.  It does work great if you incrementally add files at a slow pace.  A third architectural problem is the firmware and Linux software is stored on the same drive as the NAS data is stored.  So if the OS gets corrupted during an update, all the data is then lost.  This is where having a separate USB drive for backup is necessary.
+ **Pogoplug Pro:** Cloud Engines Pogoplug Pro provides a 1Gb Ethernet interface and 4 USB 2.0 ports controlled by a Linux cloud platform.  It is designed to provide a personal cloud share drive that is accessible locally as well as from the web.  However, the performance for local access is slow because communications with the Pogoplug has to pass through the Cloud Engines server.  Cloud Engines used to allow the owner to enable the SSH interface to the embedded Linux, but has since disabled it.  The concept of the unit is good, but the implementation is flawed.
+ **Pogoplug Pro Debian Hack:** Fortunately, there is a version of Debian Linux that has been ported to the Pogoplug Pro hardware.  Implementation requires expert understanding of embedded systems to understand how to reflash the u-boot and the Linux image.  The Linux filesystem can be placed on a USB Flash Stick and even a SATA drive to decouple the root filesystem from the storage drives of the system.  That way the OS is independent of the storage drives making the Pogoplug a cleaner solution than the MyCloud.  Once the unit is reworked with Debian running, it is open to be configured for any application supported by Debian Linux.  The NAS model is easily supported as a standard Linux file server.  Using only 5 Watts of power and support for external USB drives makes it an ideal NAS.  It would be better if the USB were 3.0 instead of 2.0 to gain better performance, but the speed of the ARM processor would not really allow support for such performance improvement.  Why the Pogoplug instead of the Raspberry Pi?  The Pogoplug Pro cost was $15 US vs. >$40 for the RPi.

{% include gallery_with_caption caption="This is a gallery of key experimental configuration tried out as part of the evaluation." %}
