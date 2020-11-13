---
layout: post
title: Playing film scans with FFmpeg
excerpt: "A short post on playing film scans with FFMpeg"
modified: 2020-11-13
tags: [ffmpeg ffplay film CLI]
categories: ffmpeg filmpres
comments: true
pinned: true
share: true
image:
  feature:
---

I have been trying to figure the best way to play film scans and learned a new trick from [reto.ch](https://reto.ch/){:target="_ blank"}!

## Playing a scan

{% highlight css %}
ffplay [DIRECTORY]/Scan_%06d.tif
{% endhighlight %}

>The regex %06d matches six digits long numbers, possibly with leading zeroes. This allows to read in ascending order, one image after the other,the full sequence inside one folder. Of course, the command must match the naming convention actually used.
