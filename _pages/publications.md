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

{% assign items = site.publications | sort: 'title' %}

{% for post in items %}
  {% if (post.publicationText %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

{% for post in items %}
  {% if (post.publicationText %}
    {% assign goober = "Done already" %}
  {% else %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}
