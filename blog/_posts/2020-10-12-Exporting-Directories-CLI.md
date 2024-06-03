---
layout: post
title: Creating a List of Files of a Directory With Command-line
excerpt:
modified: 2020-09-13
tags: [cli, tools]
categories: blog
comments: true
pinned: true
share: true
image:
  feature:
---

I recently had to provide a list of files in a USB thumbdrive/stick and learned a sweet trick via CLI. This method provides a text, _Word_ or _Excel_ file that lists all the files and folders inside a specific directory within your computer.

## Basic command structure

Syntax:

```css
DIR [pathname(s)] [display_format] [file_attributes] [sorted] [time] [options]
```

Example:

```css
dir /s > output.doc
```

_dir_ lists all the files and folders contained in the folder

_/s_ will list all the files in the subfolders as well

_Output.doc_ is the document file containing the entire directory and the details. It may be in another format such as a simple _.txt_ file which can be edited on Notepad.

## Listing only certain types of files

The command will be:

```css
dir /s \*.pdf > output_pdf.doc
```

(_.pdf)_ is a wildcard function that will only select _.pdf_ files.

## List bare format (no heading, sizes or summary)

The switch _/b_ will list file names, however when displaying subfolders with dir /b /s, the command will return a full pathname.

```css
dir /b /s > output_pdf.doc
```

## Using the _tree_ command instead of _dir_

This command will produce a tree listing of the current directory

```css
tree /f > output.txt
```

_/f_ displays the names of the files within each directory listed.

_/a_ may be used to specify alternative (_ascii_) characters to be used to draw the tree diagram so that it can be printed by printers that do not support the line and box drawing characters.
