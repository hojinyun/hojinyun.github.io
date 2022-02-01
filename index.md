---
title: "Welcome"
layout: splash
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/ocean-with-rocks.jpg
  actions:
    - label: "About Me"
      url: "/About-Me/"
excerpt: "I am a student majoring in Computer Engineering at HKUST, who is interested is in computer vision and robotics."
---
# Recent Posts
<div class="grid__wrapper">
  {% for post in site.posts limit:12 %}
    {% include archive-single.html type="list" %}
  {% endfor %}
</div>