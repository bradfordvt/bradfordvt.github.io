---
title: "Linux/Apache2/MySQL/PHP (LAMP) Server / Jekyll Server Experimentation"
excerpt: "The page chronicles my experimentation with a low cost home web server.  It uses a Debian based Pogoplug Pro with a separate hard drive to store the OS and data.  The server resides behind a DMZ firewall isolating my local network router from the server."
url: page.href
header:
  image: /assets/images/LAMPBanner.png
  teaser: assets/images/LAMPBanner.png
  icon: assets/images/LAMPIcon.png
gallery:
  - url: /assets/images/PogoplugPro.jpg
    image_path: assets/images/PogoplugPro.jpg
    alt: "placeholder PogoplugPro"
    figcaption: "Cloud Engines Pogoplug Pro"
  - url: /assets/images/Sabrent EC-UEIS7.jpg
    image_path: assets/images/Sabrent EC-UEIS7.jpg
    alt: "placeholder Sabrent EC-UEIS7"
    figcaption: "Sabrent EC-UEIS7 ESATA/USB Drive"
  - url: /assets/images/PogoPlugProLAMPServer.png
    image_path: assets/images/PogoPlugProLAMPServer.png
    alt: "placeholder PogoPlugProLAMPServer"
    figcaption: "Debian Pogoplug Pro LAMP Server Configuration"
  - url: /assets/images/DMZDiagram.png
    image_path: assets/images/DMZDiagram.png
    alt: "placeholder DMZDiagram"
    figcaption: "DMZ SOHO Configuration"
---
I wanted to learn more about the way web servers work, so what better way than to implement one myself.  This experiment has given me a platform for testing out various aspects of a Linux/Apache2/MySQL/PHP Server and the software driving the site.  It also gives me a platform for experimenting with alternate server architectures, like Jekyll, to see how they are different and similar in operation.  This platform gives me many tools to gain insight and to compare the operation, benefits, and consequences of each type of web platform.

To keep my network secure and allow me access from the web outside of my home, I set up a Demilitarized Zone (DMZ) consisting of a secondary router.  One router and firewall directly connects to the WAN and only opens the ports necessary for the web server.  A second router and firewall is implemented to protect my local network as if I were connected to the WAN directly.  The DMZ allows me to add protections to my web server and only expose the ports that are really necessary.  A separate firewall is used to ensure a compromised server is not able to unlock more ports to the WAN.

+ **DMZ:** A DMZ for networking refers to a network where computers may reside that require access by people outside of your local network. A public web server is a good example.  Certain ports need to be available from the WAN that allow traffic from the internet to gain access to your site.  A firewall is usually integrated with the DMZ network to limit the exposure of ports to the WAN.  The network administrator only forwards those ports necessary to the web server and locks up the other ports to prevent access to the DMZ network by applications that are not web browsers.
+ **LAMP Server:** LAMP represent an implementation of the Apache2 server on Linux.  It stands for Linux/Apache2/MySQL/PHP.  A LAMP server is considered to be a dynamic web page server in that variables for a page may be evaluated dynamically and changed over time as the page is dynamically generated using PHP, Perl, Python, etc. as the page is presented.  This is in contrast to static web pages as served by the Jekyll Server where the HTML code is pre-generated.  For more information on the LAMP Server check out the [wikipedia page](https://en.wikipedia.org/wiki/LAMP_(software_bundle)).
+ **Jekyll Server:** Jekyll is a static web site generator that runs on the Ruby programming language.  It was developed primarily for blogging platforms where the data does not change over time.  Thus, the site may be generated once (or updated and regenerated), but it remains constant until the next generation.  Formatting of the web pages is simpler than using HTML as one is able to use a simple Markdown language to format the site.  Jekyll also supports Front Matter formatting to allow of reuse of common code block as an extra layer of template formatting.  For more information on the Jekyll Server check out [here](http://jekyllbootstrap.com/lessons/jekyll-introduction.html).

After setting up the DMZ, I discovered my son's Microsoft XBoxOne would no longer connect to the Microsoft server from my home network.  I found that Microsoft is unable to support the double NAT translation happening with the two routers.  Fortunately, the Pogoplug Pro ES02 I used for the server has a built-in WiFi port.  I was able to convert that WiFi into an Access Point to allow the XBox to connect to the DMZ network via WiFi.  That provided the necessary workaround for my son.

{% include gallery_with_caption caption="This is a gallery of key experimental configuration tried out as part of the evaluation." %}
