---
layout: post
title: Python in imaging workflows
excerpt: How can Python be used in imaging pipelines and workflows
modified: 2020-10-20
tags: [Python]
categories: Python
comments: true
pinned: true
share: true
image:
  feature:
---
### Basic Python

* <<copy a file>>

shut.copyfile( “C:\path\file1.ext”, “C:\path\file2.ext” )

* <<rename a file>>

import os

os.system( “move \\server\path\file1.ext C:\path\file2.ext” )

* <<re-sequence files>>

import os

for x in xrange ( 1, 101, 1 ):
	os.system( “move C:\file.%s.ext C:\path\file.%04d.ext” % ( x, x ) )

### Intermediate Python

* <<scan directories and apply an operation on specific file types>>

* <<converting image from file format A to file format B>>

* <<scanning for an image with specific metadata>> (geotag, exifinfo)

* <<modify Image Metadata>> (delete / edit /add)

* <<resize all images above a specific resolution>>

### Modules

* argparse

* PIL -python image library

* OpenImageIO -image processing (create slates)

* PySide / PyQt -

* Custom Python Classes
Advanced User Interface
	-Custom widgets and dialogs
	-QT applications
	-special drag-and-drop handling

* Multi-threading
Modules: multithreading thread, queue

* Process control and communication
Modules: process, subprocess, xmlrpc, reds

### Advanced Python
Modules: OpenimageIO, OpenEXR, PythonMagick
Modules: OpenColorIO, ColorPy
