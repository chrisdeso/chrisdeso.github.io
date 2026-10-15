---
title: Now
permalink: /now/
description: What Chris is working on right now.
---
{% assign now = site.data.now %}
<p class="meta">Updated <time datetime="{{ now.updated | date_to_xmlschema }}">{{ now.updated | date: '%b %-d, %Y' }}</time></p>

<p class="lede">{{ now.headline }}</p>

{% for section in now.sections %}
<h2>{{ section.label | capitalize }}</h2>
<ul>
  {% for item in section.items %}
  <li>{% if item.url %}<a href="{{ item.url | relative_url }}">{{ item.text }}</a>{% else %}{{ item.text }}{% endif %}{% for link in item.links %}{% if forloop.first %} {% elsif forloop.last %} or {% else %}, {% endif %}<a href="{{ link.url }}">{{ link.label }}</a>{% endfor %}</li>
  {% endfor %}
</ul>
{% endfor %}

<p class="aside">This is a <a href="https://nownownow.com/about">now page</a>. Edit <code>_data/now.yml</code> to update it.</p>
