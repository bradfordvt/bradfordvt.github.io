---
title: "Print Server Experimentation"
excerpt: "The page chronicles my experimentation into finding a sufficient Print Server solution for my home printing needs.  My requirements have changed over time as technology changed and services like Google Cloudprint arrived."
url: page.href
header:
  image: /assets/images/PrintServerBanner.png
  teaser: assets/images/PrintServerBanner.png
  icon: assets/images/PrintServerIcon.png
gallery:
  - url: /assets/images/Netgear_PS101.jpg
    image_path: assets/images/Netgear_PS101.jpg
    alt: "placeholder Netgear_PS101"
    figcaption: "Netgear PS101 Parallel Port Print Server"
  - url: /assets/images/Netgear_PS121.jpg
    image_path: assets/images/Netgear_PS121.jpg
    alt: "placeholder Netgear_PS121"
    figcaption: "Netgear PS121 USB Print Server"
  - url: /assets/images/JetDirect175x.jpg
    image_path: assets/images/JetDirect175x.jpg
    alt: "placeholder JetDirect175x.jpg"
    figcaption: "JetDirect 175x"
  - url: /assets/images/PogoplugMobileV.jpg
    image_path: assets/images/PogoplugMobileV.jpg
    alt: "placeholder Pogoplug Mobile V3"
    figcaption: "Pogoplug Mobile V3"
  - url: /assets/images/PogoplugMobilePrintServer.png
    image_path: assets/images/PogoplugMobilePrintServer.png
    alt: "placeholder PogoplugMobilePrintServer"
    figcaption: "Pogoplug Mobile Print Server"

---
As I added more PCs to my home, I found it difficult to be able to print something out because I was on the wrong PC.  I was working with Linux and with Windows on different PCs, but only had one inkjet printer and two dot matrix printers.  I wanted to be able to access the inkjet printer from both PCs if that was possible.  The inkjet printer and the dot matrix printers all used the standard Centronics parallel printer interface connector.  I set up my Linux PC to act as a print server for the inkjet printer and that worked for the time being.

When I upgraded my Windows PC, I obtained a new inkjet printer that used a USB interface.  My Windows PC became my son's PC to play on.  Now I had 3 PCs needing to share 4 printers, but only the inkjet printers were needing to be shared.  The new inkjet printer was an all-in-one printer with FAX/Scan/Print capability.

I found I could use the Netgear PS101 Print Server to connect my original inkjet printer to the network and share it out to all the PCs.  That worked well and solved that problem.  Netgear has a PS121 Print Server that supports USB printers.  I tried that and it worked for printing, but it would not support scan operations on my second printer.  It was only unidirectional 9100 (jetdirect) protocol.  So I ended up installing a JetDirect 175x Print Server from HP for that office printer.  That allowed me to both print and scan over the network.

When I started using my smartphone, I found I wanted to print from my phone.  None of my printers were able to support the necessary printer interfaces.  Google provided a cloud printing service for Android phones that sounded promising, but how to support that on my network?  Fortunately, someone has written a cloudprint service for Linux.  My old Linux PC came to the rescue again.  I installed the cloudprint service and was able to print from my phone via the Google cloudprint service.

Leaving my Linux PC on was not very energy efficient for the few times I would need to print from my phone.  So I made due with turning it on when I needed to print for a few years.  There had to be a better solution instead of purchasing a cloudprint ready printer.  My printer was still working well.

I did some research and found I could purchase a Pogoplug Mobile V3 for around $7US and that a Debian Linux version was available for it if you know how to hack into it.  That was a small cost to experiment with and find a solution to my print server problem.  So I purchased it, installed Debian, and installed the necessary software to create a nice little low power print server.  I recycled the hard drive from my old laptop that died to provide a cache for CUPS printing as well.  So now I have a low power Google cloudprint server accessing all my printers on my network and added a JetDirect interface for one of my newer USB printers.  Problem solved.

{% include gallery_with_caption caption="This is a gallery of key experimental configuration tried out as part of the evaluation." %}
