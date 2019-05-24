---
title: "WordCloudTool"
excerpt: "Application to create a word cloud from many different file inputs."
url: page.href
header:
  image: /assets/images/wordcloudtool.png
  icon: /assets/images/wordcloudtool128x128.png
  teaser: assets/images/wordcloudtool.png
gallery:
  - url: /assets/images/wordcloudtool.png
    image_path: assets/images/wordcloudtool.png
    alt: "placeholder wordcloudtool"
  - url: /assets/images/wordcloudtoolQt5.png
    image_path: assets/images/wordcloudtoolQt5.png
    alt: "placeholder wordcloudtoolQt5"
  - url: /assets/images/wordcloudtoolQt5cloud.png
    image_path: assets/images/wordcloudtoolQt5cloud.png
    alt: "placeholder wordcloudtoolQt5cloud"
  - url: /assets/images/wordcloudtoolQt5histogram.png
    image_path: assets/images/wordcloudtoolQt5histogram.png
    alt: "placeholder wordcloudtoolQt5histogram"
---
# Background
I was tired of the kind of output I could obtain from free web based word cloud tools (e.g., WordClouds, TagCrowd, ABCYa! Word Clouds, Tagul, Tagxedo, Tricklar, WordItOut, Wordle).  All I wanted to do was to parse a set of documents and find the keyword most prominent in the documents.  Most of these tools are made for producing fancy graphics with the word cloud.  Many are limited on the text format they can process.  Others place limits on the number of files you can parse for free.  Others also do not provide a means to define your own list of filter "stop words."

I wanted to create a tool I could own and use as I pleased.  I also wanted to be able to define my own set of "stop words" to filter out common words from the processing.  I also wanted to create an application using many of my software design patterns I have learned over the years.  The WordCloudTool is the embodiment of what I was trying to use.  I hope you enjoy it.  The interface is a graphical interface from either Qt5 or Tkinter.  The code is still a work in progress, but the Qt5 version is operational.

I will be updating this post as development proceeds.

{% include gallery caption="This is gallery of key concepts being investigated by the working group." %}

[https://github.com/bradfordvt/WordCloudTool](https://github.com/bradfordvt/WordCloudTool)
