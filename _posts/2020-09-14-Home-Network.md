---
layout: post
title: Part 1&#58; My home network journal
excerpt: "Laying out my network plan for my future Ubiquiti setup"
modified: 2020-09-19
tags: [network, ubiquiti, unifi, edgemax, wifi]
categories: network renovation
comments: true
pinned: true
share: true
image:
  feature:
---

This post will be part of a series documenting the network component of my upcoming renovation of my new apartment. The apartment is over 20 years old hence a major overhaul is required and the renovation is a great opportunity to lay CAT6 to all the rooms in the house for the 1Gbps/10Gbps network 🤓.

My research began with [this](https://www.patnotebook.com/bto-networking-singapore/){:target="_ blank"} article on [patnotebook.com](https://patnotebook.com){:target="_ blank"} detailing the conversion of telephone points to RJ45 data points in newer BTO (Build to Order) flats in Singapore. Newer flats in Singapore have CAT6 cables already nicely laid in the house, however many of the points are terminated with a telephone jack instead of RJ45. Based on the article, it seems that BTO flats only have one point terminated as RJ45, which is definitely not enough 😁.

That being said, I will have to lay my own cables and design my own network infrastructure since my flat is a legacy model.

A great networking and Ubiquiti resource is Evan McCann's tech blog - [McCann Tech](https://evanmccann.net/){:target="_ blank"}. There are many nice articles that explain networking jargon in simple terms and breaks down the Ubiquiti universe in sizeable chunks. He is extremely detailed in doing breakdowns and making comparisons on the many Ubiquiti products. I would recommend his site as essential reading for whoever is considering putting together a Ubiquiti system!

### Recommended McCann reading list

* [Ubiquiti’s UniFi Ecosystem Explained](https://evanmccann.net/blog/unifi-ecosystem-overview){:target="_ blank"}
* [UniFi Switches Explained](https://evanmccann.net/blog/2020/6/unifi-switches-explained){:target="_ blank"}
* [UniFi Switch Comparison and Buyer's Guide](https://evanmccann.net/blog/2020/6/unifi-switches-buyers-guide){:target="_ blank"}
* [UniFi Wireless Access Point Buyer's Guide](https://evanmccann.net/blog/unifi-ap-breakdown){:target="_ blank"}
* [Wi-fi&#58; Isn't Magic Some Tips For Planning A Home Network](https://evanmccann.net/blog/home-network-tips){:target="_ blank"}
* [Ubiquiti FAQ](https://evanmccann.net/blog/2020/6/ubiquiti-faq){:target="_ blank"}

I plan to update my progress with subsequent posts, but for now I've made a simple diagram detailing the essential hardware required for the network setup. I've decided to go full Ubiquiti for my first setup because it is well documented 'enterprise' solution and it seems easy to put together. I won't deny that it is overkill for a home environment but this project is too exciting to pass.

### The hardware diagram

![Network diagram]({{ site.url }}/assets/originals/Network_diagram.jpg)

### The breakdown and costs

* Commscope CAT6A CS44Z1 WHT C6A 4/23 F/UTP RL 500M
* 12U Server Rack
* [24-Port Keystone Patch Panel](https://www.amazon.com/LINKOMM-24-Port-Unshielded-Blank-Keystone/dp/B0719N5117/ref=pd_di_sccai_4/142-1063064-5847132?_encoding=UTF8&pd_rd_i=B0719N5117&pd_rd_r=b9bfe1aa-d03d-440a-b7ec-0a10ce53923d&pd_rd_w=ft3ps&pd_rd_wg=A8jLg&pf_rd_p=5415687b-2c9d-46da-88a4-bbcfe8e07f3c&pf_rd_r=1D618MXDFFA9AJ8Y9HNG&refRID=1D618MXDFFA9AJ8Y9HNG&th=1){:target="_ blank"}
* [CAT6A Unshielded Keystone Jack](https://www.amazon.com/LINKOMM-Cat6A-Profile-Keystone-Orange/dp/B07R3Z93NN/ref=sr_1_13?dchild=1&keywords=cat6a%2Bunshielded&qid=1603116313&sr=8-13&th=1){:target="_ blank"}
* Ubiquiti EdgeRouter X
* Unifi Switch 16 150W Gen 1
* Unifi Cloud Key Gen2
