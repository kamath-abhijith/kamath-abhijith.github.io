---
layout: default
permalink: /about.html
title: About Me
description: Get to know what I'm up too
header-img: 
last-updated: 2020-10-30 5:55 PM
---

<h1 class="mx-auto" style="font-family:Avenir;">{{ page.title }}</h1>

I broadly work in the areas of signal/image processing, and in particular, sub-Nyquist sampling theory and inverse problems.

The current areas of focus are in "sampling" signals using time-encoded measurements! This is quite nonintuitive to imagine, but they have found a lot of interesting applications in neuromorphic cameras and audio sensors. The priciple lies in defining an event, and recording a set of time instants whenever the event occurs. The signal is encoded using those time instants. As an example, the figure below shows the signal $y(t)$ "sampled" at times $t'_n$ when the event that the reference sinusoid $r(t)$ and the signal have zero difference.

<p align="center">
  <img width="460" src="https://i.imgur.com/NQLlEXT.png">
</p>

Such sampling methods are efficient in the sense of sampling energy and complexity in the number of samples obtained. Further, such sampling methods have deep mathematical foundations, whilst being practical! Even more, a lot of modern day signal processing from such measurements utilse learning based algorithms! Overall, it makes for a holistic area of research involving a lot of interesting topics, with several important applications. See my [publications](/publications.html) for some deeper insights!