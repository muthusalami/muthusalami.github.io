---
layout: post
title: Google Analytics for GitHub Pages
excerpt: How to set up Google Analytics for GitHub Pages
modified:
tags: [blog]
categories: blog
comments: true
pinned: true
share: true
image:
  feature:
---

This post covers the set up of Google Analytics for GitHub Pages.

1\. Go to Google Analytics and create a Google Analytics account for the site you would like to track.

2\. Take note of the tracking ID and copy the code snippet provided that looks like the following:

```html
<script async src="https://www.googletagmanager.com/gtag/js?id=UA-XXXXXXXXX-X"></script>
    <script>
      window.dataLayer = window.dataLayer || [];
      function gtag(){dataLayer.push(arguments);}
      gtag('js', new Date());

      gtag('config', 'UA-XXXXXXXXX-X');
</script>
```
{:start="3"}
3\. Create a new .HTML file in your *_includes* folder that contains the code snippet and name it **google_analytics.html**.

4\. Add the following code to your default layout: _layouts/default.html.

```
{% raw %}
{% include google_analytics.html %}
{% endraw %}
```