---
layout: post
title: Installing Tesseract on Windows
excerpt:
modified:
tags: [tools, tesseract]
categories: blog
comments: true
pinned: true
share: true
image:
  feature:
---

PyTesseract is a widely used open-source OCR engine for Python that read and recognizes text in images. It determines text lines that are fixed pitch and slices the words into characters based on the pitch. While it is known for its accuracy and versatility, it can be challenging to install it in a Windows environment.

## Installation steps

1\. [Download and install Tesseract](https://github.com/UB-Mannheim/tesseract/wiki){:target="\_ blank"}

2\. Add _TESSDATA_PREFIX_ in the System Environment Variables:

```
Variable Name - TESSDATA_PREFIX
Variable Value - C:\Program Files (x86)\Tesseract-OCR\tessdata
```

3\. Add another environment variable _tesseract_.

```
Variable Name - tesseract
Variable Value - C:\Program Files (x86)\Tesseract-OCR\tesseract.exe
```

4\. Add the path in the PATH environment.

```
Variable Value –C:\Program Files (x86)\Tesseract-OCR
```
