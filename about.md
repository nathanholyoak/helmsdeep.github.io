---
layout: page
title: About
permalink: /about.html
---

This is helmsdeep.org.

<h2>Contributors</h2>

<ul class="contributors">
{% for a in site.data.authors %}
{% assign author_data = site.authors | where:"author", a[0] %}{% assign author = author_data | first %}
<li>{% if a[1].gravatar %}<img src="https://www.gravatar.com/avatar/{{ a[1].gravatar }}?s=32" class="avatar" />{% endif %}<a href="{{ author.url | prepend: site.baseurl }}">{{ a[1].name }}</a></li>
{% endfor %}
</ul>
