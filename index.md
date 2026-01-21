---
layout: default
title: Emekum
lang: fr
---

{% assign lang = page.lang | default: "fr" %}

## {% if lang == "fr" %}Articles récents{% endif %}
## {% if lang == "en" %}Recent Articles{% endif %}
## {% if lang == "ar" %}المقالات الحديثة{% endif %}

<ul>
  {% for post in site.posts %}
    {% if post.lang == lang %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        - {{ post.date | date: "%d %B %Y" }}
      </li>
    {% endif %}
  {% endfor %}
</ul>

