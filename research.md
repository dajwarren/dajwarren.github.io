---
title: Research
layout: page
thumbnail: graduation-cap
---
# The Scottish Vowel Length Rule

{% for post in site.posts %}
  {% if post.categories contains "svlr"%}
  <h2 id="{{ category | first }}-ref">{{ category | first }}</h2>
  <ul>
        <li>
          <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
          <small class="hidden-xs">{{ post.date | date: "%B %-d, %Y" }}</small>
        </li>
    </ul>
  {% endif %}
{% endfor %}
