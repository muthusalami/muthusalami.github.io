---
layout: post
title: About enterprise storage
excerpt: "Digging into the mysteries of enterprise storage "
modified: 2021-01-21
tags: [storage]
categories: storage
comments: true
pinned: true
share: true
image:
  feature:
---

I've taken up more technical portfolios recently and these opportunities have opened the world of enterprise storage to me. It is a world that is filled with intimidating machines and jargon, but I've developed a strong interest and liking with the knowledge I've developed over the year. It is incredible how these technologies are responsible for the data of the world and it fascinates me to understand how they are all being stored. That being said, it is important for us to understand the tools available and their capabilities, so as to achieve our desired solutions.

Storage has become increasingly relevant in the world we live in as we generate more data than ever before. Its universe can be quite difficult to navigate with its mysterious acronyms and jargon, especially for individuals like myself who do not come from a technical/IT background. Therefore I thought to briefly write a little about the key concepts to consolidate and share what I've learned so far.

## Storage types

* Storage Area Network (SAN)

Most common storage architecture used by businesses that is configured for high throughput and low latency. Data is stored centrally, allowing organisations to apply consistent methodologies and tools for security, data protection and disaster recovery.

It is block-based storage, that relies on high-speed network to connect to logical disk units (LUNS). A LUN is a cluster of blocks that forms a pool of storage and it presented to the server as a logical disk. SAN systems are highly available and resilient, allowing single points of failure.

Types of SAN
- Fibre Channel Protocol (FCP)
- Internet Small Computer System Interface (iSCSI)
- Fibre Channel over Ethernet (FCoE)
- Non-Volatile Memory Express over Fibre Channel (FC-NVMe)

* Network-attached Storage (NAS)

Similar to SAN, it manages and share storage centrally to multiple clients. However, NAS is Ethernet based, while SAN uses Ethernet and Fibre Channel. Futhermore, SAN prides and focuses on high performance and low latency, while NAS focuses on the ease of use and lower cost of ownership.

NAS protocols
- Common Internet File Services / Server Message Block (CIFS/SMB)
- Network File System (NFS)


## File and object protocols

* CIFS

* SMB

* NFS

* S3

## Concepts

* Logical Unit Numbers (LUN)

LUN is a portion of a configured set of disks that is presented to a host and mounted as a volume in the OS. The LUN can be configured as a portion of a RAID group, or be configured to use the total space available.  The LUN will be presented to the client as a mountable volume configured by the administrator, which in turns hides the remaining capacity on that RAID group.

* RAID

* Tiering
