---
layout: default
title: Recipes
permalink: /recipes/index.html
---
<div class="index">
<h1>{{ page.title }}</h1>
{% assign recipes_grouped = site.recipes | group_by: "category" | sort: "name" %}{% for group in recipes_grouped %}
<h2>{{ group.name | capitalize }}</h2>
{% assign recipes = group.items | sort: "title" %}{% for recipe in recipes %}
<article class="h-recipe">
<p><a href="{{ recipe.url | prepend: site.baseurl }}" class="p-name">{{ recipe.title }}</a></p>
</article>
{% endfor %}{% endfor %}
</div>
