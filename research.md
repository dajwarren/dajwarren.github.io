---
title: Research
layout: page
thumbnail: graduation-cap
---
# The Scottish Vowel Length Rule
I am currently examining the impact of coda consonant voicing on vowel timing in language varieties spoken in the North East of Scotland. The primary focus is on the Scottish Vowel Length Rule (Aitken's Law), the name given to a phenomenon across much of Scotland and the very north of England in which a vowel is realised with a greater duration if it precedes any voiced fricative, the rhotic phoneme, or a morpheme boundary.


{% for post in site.posts %}
  {% if post.categories contains "SVLR"%}
  <h2 id="{{ category | first }}-ref">{{ category | first }}</h2>
  <ul>
        <li>
          <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
          <small class="hidden-xs">{{ post.date | date: "%B %-d, %Y" }}</small>
        </li>
    </ul>
  {% endif %}
{% endfor %}
