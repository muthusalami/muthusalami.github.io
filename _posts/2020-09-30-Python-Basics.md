---
layout: post
title: Python basics
excerpt: Basic concepts in Python
modified: 2020-09-13
tags: [python, Homebrew, Anaconda, Atom, PyCharm, repl.it]
categories: Python
comments: true
pinned: true
share: true
image:
  feature:
---

This post purely serves as a journal as I progress towards learning Python and will be updated as I go along.

## 0) Set up - Installing Python

For Windows, Python 3 can be installed and managed using [**Anaconda**](https://anaconda.com/){:target="_ blank"}

For Mac, Python 3 can be installed and managed using [**Homebrew**](https://brew.sh/){:target="_ blank"}.

## 0) Set up - Choosing an IDE to write and run the scripts

[**repl.it**](https://repl.it/){:target="_ blank"} (Online in-browser IDE)

[**Atom IDE**](https://atom.io/){:target="_ blank"}

Running the terminal in Atom: **⌘ + I**

[**PyCharm IDE**](https://www.jetbrains.com/pycharm/){:target="_ blank"}

## 1) Variables & Strings
**Variables** store information; it can be text or numbers.

{% highlight css %}
first.name = 'matthew'
last.name = 'yang'
{% endhighlight %}

first.name & last.name are **variables**.
'matthew' & 'yang' are the **values**.

**Strings** are text or are a combination of text within quotes. They include:
* Letters
* Numbers
* Punctuation
* Special characters

It can be either in single or double quotes. Do note to use double quotes if your string is a quote.
{% highlight css %}
'like this'
"like this"
{% endhighlight %}

The **len()** command in Python provides the length of something. For example, it tells you the number of characters when used in strings.

Example:
{% highlight css %}
name.count = len(first.name)
print(name.count)
{% endhighlight %}

The result will be *7* since 'matthew' has seven characters.

**Slicing** will index or sequence strings by their character[s]. The first character in the string will be indexed as 0.

Example:
{% highlight css %}
name = 'matthew'
print(name[0])
{% endhighlight %}

The result will be *m*.

A range of characters can be called using ':'.

Example:
{% highlight css %}
name = 'matthew'
print(name[0:4])
{% endhighlight %}

The result will be *matt*.
