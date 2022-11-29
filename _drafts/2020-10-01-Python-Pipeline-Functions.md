---
layout: post
title: Python in imaging workflows
excerpt: How can Python be used in imaging pipelines and workflows
modified: 2020-12-23
tags: [Python]
categories: Python
comments: true
pinned: true
share: true
image:
  feature:
---
## Basic Python

* <<copy a file>>

shut.copyfile( “C:\path\file1.ext”, “C:\path\file2.ext” )

* <<rename a file>>

import os

os.system( “move \\server\path\file1.ext C:\path\file2.ext” )

* <<re-sequence files>>

import os

for x in xrange ( 1, 101, 1 ):
	os.system( “move C:\file.%s.ext C:\path\file.%04d.ext” % ( x, x ) )

## Intermediate Python

* <<scan directories and apply an operation on specific file types>>

python scanandfixme.py -fileType .jpg -operation deleteMyFace

* <<converting image from file format A to file format B>>

python convertALLJPEGS.py -dir /dir1/dir2 .jpg .exr

* <<scanning for an image with specific metadata >> (geotag, exifinfo)

python chezSerge.py -dir /dir1/dir2 -ext .jpg -coord 45.3323 32.3233

* <<modify Image Metadata>> (delete / edit /add)

python resizeallimages.py -dir /dir1/dir2 -ext .jpg -res 2048x2048

* <<resize all images above a specific resolution>>


## Modules

* argparse

* PIL - python image library. Basic image manipulation. Does not support 32-bit

* OpenImageIO - advance image processing. Can load images with multi-channels and supports 32-bit. Useful to create slates

* PySide / PyQt - ???

* Custom Python Classes
Advanced User Interface
	-Custom widgets and dialogs
	-QT applications
	-special drag-and-drop handling

* Multi-threading
Modules: multithreading thread, queue

* Process control and communication
Modules: process, subprocess, xmlrpc, reds

## Advanced Python I

* Custom Python Classes

* Advanced User Interface
  * Custom Widgets and dialogs
  * QT applications
  * Special Drag-and-Drop handling
  * Gesture

Modules: PySide / PyQt

## Advanced Python II

* Multi-threading
  * Modules: multi-threading, thread and queue

* Process control and communication
  * Modules: process, subprocess, xmlrpc, redis

* Database
  * Modules: redis, sqlite3, mongodb

* Persistence
  * Modules: yaml, json, pickle/Cpickle

## Advanced Python III

* Image processing / Compositing
  * Modules: OpenImageIO, OpenEXR, PythonMagick

* Colour Science
  * Modules: OpencolorIO, ColorPy

* Computer Vision
  * Modules: simpleCV, pycv

* Math / Simulation
 * Modules: NumPy, Matplotlib, SciPy

## Advanced Python IV

* Geometrical
  * Modules: alembic / alembicgl

* Volumes / Voxels
  * Modules: pyopenvdb

* Particles
  * Modules: partio
