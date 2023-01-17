---
layout: post
title: Ubiquiti Home Network Part&#58; II
excerpt: "The setup of my home network"
modified: 2021-01-20
tags: [network]
categories: network home
comments: true
pinned: true
share: true
image:
  feature:
---

This post is all about setting up my Ubiquiti home network and will serve as a personal resource/journal for the various devices.

## EdgeRouter X (ER-X) router set up 

1. Connect computer to the Eth 0 port on the ER-X

2. Open the network settings on your PC and set the IP address to 192.168.1.2 since the IP address of the ER-X is 192.168.1.1 (also the default gateway)

    Subnet mask: 255.255.255.0

3. Log into EdgeMax Web GUI. usr: 'ubnt' pwd: 'ubnt'

4. Commence basic set-up

5.  Settings

    Port: eth 0
    Internet connection type: DHCP
    Firewall: enable the default Firewall
    One Lan: *check*

    Leave default address and enable DHCP server

    Create a new user with a new password

6. Apply changes and reboot the router

7. Plug modem into eth 0 and move client connection to eth 1

8. Change IP and DNS settings to automatic on the client

9. 'ipconfig /release' to release the old IP address. 'ipconfig /renew' to get a new IP address

10. Log back into the EdgeMax Web GUI.

11. Bring up the CLI on the GUI. Log in with the credentials

12. type 'configure'

13. set 'system offload hwnat enable'

14. set 'system system offload ipsec enable'

15. type 'commit' and 'save'.

Credit to Toasty Answers for the easy to follow set-up.

[Toasty Answers - EdgeRouter X First Time Setup](https://www.youtube.com/watch?v=aECPxlT6Qq4){:target="_ blank"}

**Updating the ER-X**

1. Download the latest firmware from Ubiquiti.

2. Access the EdgeMax Web GUI and click on system and head to upgrade system image. Click 'upload a file'.

3. Upload the image and reboot and let it apply the update.

4. Log in again and the new version should be reflected on the dashboard.

**Other functions**

*Smart Queue*

*UPnP*


## Additional resources

* 'Gamer Setup' for the ER-X

[Gamer Setup - This router can save your marriage!](https://www.youtube.com/watch?v=o-g2P3R84dw){:target="_blank"}

* The Ubiquiti Universe

[Poseidwn Tech - Initial UniFi Setup for Beginners](https://www.youtube.com/watch?v=-6q-4lSBfmA){:target="_blank"}

* Unifi Cloud Key Gen2 Plus (UCK-G2-PLUS)

[Crosstalk Solutions - Cloud Key Gen2 Plus](https://www.youtube.com/watch?v=H_a1BCf1jH0){:target="_ blank"}

* Unifi US-16-150W

[Tom Morgan - Ubiquiti UniFi Switch 16 150W setup](https://www.youtube.com/watch?v=0_wXI5minS0){:target="_blank"}
