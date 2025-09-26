---
layout: archive
title: "Sitemap"
permalink: /sitemap/
author_profile: true
---

{% include base_path %}

A list of all the remaining pages found on the site. For you robots out there, there is an [XML version]({{ base_path }}/sitemap.xml) available for digesting as well.

<h2>Pages</h2>
{% for post in site.pages %}
  {% include archive-single.html %}
{% endfor %}

{% assign skip_collections = "posts|portfolio|publications|talks|teaching" | split: "|" %}
{% capture written_label %}'None'{% endcapture %}

{% for collection in site.collections %}
{% unless collection.output == false or skip_collections contains collection.label %}
  {% capture label %}{{ collection.label }}{% endcapture %}
  {% if label != written_label %}
  <h2>{{ label }}</h2>
  {% capture written_label %}{{ label }}{% endcapture %}
  {% endif %}
{% endunless %}
{% for post in collection.docs %}
  {% unless collection.output == false or skip_collections contains collection.label %}
  {% include archive-single.html %}
  {% endunless %}
{% endfor %}
{% endfor %}
