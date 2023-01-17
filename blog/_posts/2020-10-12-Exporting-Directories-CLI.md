---
layout: post
title: How to export a list of files in CLI
excerpt: How to export a list of files in CLI
modified: 2020-09-13
tags: [cli, command prompt, windows, excel, word, manifest]
categories: cli windows
comments: true
pinned: true
share: true
image:
  feature:
---

I recently had to provide a list of files in a USB thumbdrive/stick and learned a sweet trick via CLI. This method provides a text, *Word* or *Excel* file that lists all the files and folders inside a specific directory within your computer.

## Basic command structure

Syntax:

{% highlight css %}
DIR [pathname(s)] [display_format] [file_attributes] [sorted] [time] [options]
{% endhighlight %}

Example:

{% highlight css %}
dir /s > output.doc
{% endhighlight %}

*dir* lists all the files and folders contained in the folder

*/s* will list all the files in the subfolders as well

*Output.doc* is the document file containing the entire directory and the details. It may be in another format such as a simple *.txt* file which can be edited on Notepad.

## Listing only certain types of files

The command will be:

{% highlight css %}
dir /s *.pdf > output_pdf.doc
{% endhighlight %}

(*.pdf)* is a wildcard function that will only select *.pdf* files.

## List bare format (no heading, sizes or summary)

The switch */b* will list file names, however when displaying subfolders with dir /b /s, the command will return a full pathname.

{% highlight css %}
dir /b /s > output_pdf.doc
{% endhighlight %}

## Using the *tree* command instead of *dir*

This command will produce a tree listing of the current directory

{% highlight css %}
tree /f > output.txt
{% endhighlight %}

*/f* displays the names of the files within each directory listed.

*/a* may be used to specify alternative (*ascii*) characters to be used to draw the tree diagram so that it can be printed by printers that do not support the line and box drawing characters.