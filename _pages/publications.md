---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

Selected Publication:
1. Increased future occurrences of the exceptional 2018–2019 Central European drought under global warming
V Hari, O Rakovec, Y Markonis, M Hanel, R Kumar
Scientific reports 10 (1), 12207
315	2020

2. Indian summer monsoon rainfall: implications of contrasting trends in the spatial variability of means and extremes
S Ghosh, H Vittal, T Sharma, S Karmakar, KS Kasiviswanathan, ...
PloS one 11 (7), e0158670
151	2016

3. 
4. 


{% include base_path %}

<!-- New style rendering if publication categories are defined -->
{% if site.publication_category %}
  {% for category in site.publication_category  %}
    {% assign title_shown = false %}
    {% for post in site.publications reversed %}
      {% if post.category != category[0] %}
        {% continue %}
      {% endif %}
      {% unless title_shown %}
        <h2>{{ category[1].title }}</h2><hr />
        {% assign title_shown = true %}
      {% endunless %}
      {% include archive-single.html %}
    {% endfor %}
  {% endfor %}
{% else %}
  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% endif %}



