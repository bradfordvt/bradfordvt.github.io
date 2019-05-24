---
title: "telnetsrvlib"
excerpt: "Fork of the ianepperson/telnetsrvlib repository to port the code to Python3"
url: page.href
header:
  image: /assets/images/GitHub_Logo.png
  icon: /assets/images/GitHub_Logo128.png
  teaser: assets/images/GitHub_Logo.png
gallery:
  - url: /assets/images/GitHub_Logo.png
    image_path: assets/images/GitHub_Logo.png
    alt: "placeholder GitHub_Logo"
---
This project is a fork of the ianepperson/telnetsrvlib repository to port the code to Python3.  I needed a Telnet server that was Python based for some experimentation I was doing with some myHDL designs.  These experiments needed to marry functional software with simulations of hardware designs to be able to evaluate whether the descriptions for the software was able to control various types of hardware designs and interfaces.  Decoupling the myHDL simulation from the applications was required and the Telnet interface made a simple bridge between both application modules.

The Epperson version of telnetsrvlib only runs with Python2.  I needed a Python3 version.  Not much work has been done with telentsrvlib since its release and it was released to PyPy prior to the release of Python3.  This project is my port of that software to run with Python3.

{% include gallery caption="This is gallery of key concepts being investigated by the working group." %}

[https://github.com/bradfordvt/telnetsrvlib](https://github.com/bradfordvt/telnetsrvlib)
