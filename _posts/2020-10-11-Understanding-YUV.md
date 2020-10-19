---
layout: post
title: Understanding the YUV format
excerpt: A brief summary and explanation of the YUV format
modified: 2020-10-19
tags: [Video, YUV, Colour]
categories: Video
comments: true
pinned: true
share: true
image:
  feature:
---

**Y value** = Luminance value
Overall brightness of the pixel. It is a grayscale value.

**U (CB) value**  = Chrominance value
Specifically the Blue  

**V (CR) value**  = Chrominance value
Specifically the Red

The **U & V values**  are coordinates instead of brightness values with positive and negative values.

## Why not stick to RGB?

Colour and brightness information and combined within the three channels in RGB. i.e. Increasing the **R** channel will increase both the colour and brightness value in tandem. In simpler terms, both properties are combined in the same value.

In a YUV system, the brightness information is completely separated from the colour information. In other words, more control is afforded.

## Practical application

**Backward compatibility** - Black and White TVs can't take RGB signals since the brightness value is baked into the colour values which it doesn't understand. Whereas YUV has the Y value which can be processed by the television set, by ignoring the colour components.

**Chroma sub-sampling** - YUV allows the user to remove information specifically from the colour values without affecting the overall luminance of it. This is particularly useful during image compression and an effective means in processing images.
