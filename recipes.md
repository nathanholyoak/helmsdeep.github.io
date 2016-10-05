---
layout: page
title: Recipes
permalink: /recipes/index.html
---

{% assign recipes = site.recipes | sort: "title" %}{% for recipe in recipes %}
<p><a href="{{ recipe.url | prepend: site.baseurl }}">{{ recipe.title }}</a></p>
{% endfor %}
