---
layout: page
title: News
permalink: /news/
---

BSGSA members: please send your achievements, small or large, to us so that we may post them here! For more news, see the [UC Berkeley SPH's Biostatistics news feed](http://sph.berkeley.edu/about-us/school-news?field_tags_tid=11).

<ul class="listing">
{% for post in site.categories.news %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
    {% assign year = y %}
    <li class="listing-seperator">{{ y }}</li>
  {% endif %}
  <li class="listing-item">
    <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
    <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>
