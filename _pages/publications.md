---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}



{% with '2018 2020' as yearlist %}
  {% for year in list.split %}
    <ol>
    {% for post in site.publications reversed %}
      {% if post.year == yearlist %}
        <li> {% include archive-single.html %}</li>
      {% endif %}
    {% endfor %}
    </ol>
  {% endfor %}
{% endwith %}


