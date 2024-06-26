---
layout: post
title: Managing Film Scans With FFmpeg
excerpt:
modified: 2020-11-13
tags: [ffmpeg, cli, tools, dpx]
categories: blog
comments: true
pinned: true
share: true
image:
  feature:
---

I have been trying to figure the best way to play and manage film scans and learned a bag of new tricks from [reto.ch](https://reto.ch/){:target="\_ blank"}!

## Playing a DPX sequence

{% highlight css %}
ffplay [DIRECTORY]/Scan\_%06d.tif
{% endhighlight %}

The regex %06d matches six digits long numbers, possibly with leading zeroes. This allows to read in ascending order, one image after the other,the full sequence inside one folder. Of course, the command must match the naming convention actually used.

## Make a ProRes file from the scan sequence

{% highlight css %}
ffmpeg
-f image2 \
 -framerate 24 \
 -i [DIRECTORY]/Scan\_%06d.tif \
 -c:v prores_ks \
 -profile:v 3 \
 -filter:v "scale=1440:1080:flags=lanczos, pad=1920:1080:240:0" \
 ProRes.mov
{% endhighlight %}

_f_ image2 forces the image file de-muxer for single image files
_framerate_ sets the frame rate to 24
NOTE: The previous two parameters must be before the input file, because they are applied to the input file.
_i_ path, name and extension of the input file
The regex %06d matches six digits long numbers, possibly with
leading zeroes. This allows to read in ascending order, one
image after the other, the full sequence inside one folder.
The command must of course match the naming convention
actually used.
_c:v_ chooses the ProRes video codec
_profile:v_ the flavour ProRes 422 HQ has the video profile 3
_filter:v_ filters the video stream:
_ scaling to the correct size
[we use the Lanczos scaling algorithm which is slower but
better than the default bilinear algorithm]
_ padding the 4:3 format into the 16:9 HD format with pillar box

## Make a H264 file from the scan sequence

{% highlight css %}
ffmpeg \
 -f image2 \
 -framerate 24 \
 -i DUFAY*TIFF/Dufay*%06d.tif \
 -c:v libx264 \
 -preset veryslow \
 -qp 18 \
 -filter:v "scale=1440:1080:flags=lanczos, pad=1920:1080:240:0" \
 -pix_fmt yuv420p \
 Scan_H264_1.mp4
{% endhighlight %}

Make an access file H.264 directly form the conservation files TIFF.
_c:v_ chooses the H.264 codec by using the libx264 library
_preset_ chooses the very slow preset which gives the best result
_qp_ a quantisation parameter of 18 means “visually lossless”

## Make a H264 file from the ProRes file

{% highlight css %}
ffmpeg \
 -i ProRes.mov \
 -c:v libx264 \
 -preset veryslow \
 -qp 18 \
 -pix_fmt yuv420p \
 -an \
 Scan_H264_2.mp4
{% endhighlight %}

_an_ prevents an empty audio track ([a]udio [n]o)
