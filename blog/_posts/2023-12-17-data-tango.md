---
layout: post
title: Data Tango&#58; Exploring Restic
excerpt:
modified:
tags: [blog, restic]
categories: blog
comments: true
pinned: true
share: true
image:
  feature:
---

![restic]({{ site.url }}/assets/originals/file_utility/restic.gif)

What is restic?

[Restic](https://restic.net/){:target="\_ blank"} is a free and open source backup program available on Linux, BSD, MacOS, and Windows. It works with many different storage types (Local, Network, Cloud) and is designed to create and manage backups.

Key features:
Deduplication
Encryption
Incremental Backups
Snapshot Management
Cross-platform Compatibility

1. Create Restic repository as backup destination
   {% highlight css %}
   restic -r D:/dpx-restic init
   {% endhighlight %}

2. Initiate backup
   {% highlight css %}
   restic -r D:/dpx-restic backup C:/Users/MATT-THINKPAD/Documents/dpx-source/
   {% endhighlight %}

3. Check snapshots
   {% highlight css %}
   restic -r D:\dpx-restic snapshots
   {% endhighlight %}

4. List files in repository
   {% highlight css %}
   restic -r D:\dpx-restic ls latest
   {% endhighlight %}

5. Verifying backups
   {% highlight css %}
   restic check D:\dpx-restic
   {% endhighlight %}

6. Restoring files
   {% highlight css %}
   restic -r D:\dpx-restic\ restore "latest:/C/Users/MATT-THINKPAD/Documents/dpx-source/" --target "C:\Users\MATT-THINKPAD\OneDrive - nyu.edu\Desktop\dpx-restore"
   {% endhighlight %}

7. Restore files from a specific snapshot
   Get a list of snapshots
   {% highlight css %}
   restic -r 'D:\dpx-restic\' snapshots
   {% endhighlight %}

   Restore from snapshot
   {% highlight css %}
   restic -r D:\dpx-restic restore 2297f849 --target "C:\Users\MATT-THINKPAD\OneDrive - nyu.edu\Desktop\dpx-restore"
   {% endhighlight %}
