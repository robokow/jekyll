---
layout: page
title: Archive
permalink: /archive/
---

<div class="page-archive">
{% for post in site.posts %}
  {% assign post_month_year = post.date | date: "%B %Y" %}
  {% assign newer_post_month_year = post.next.date | date: "%B %Y" %}
  {% if post_month_year != newer_post_month_year %}
    <h3 class="section-header-archive">
      {{ post_month_year }}
    </h3>
  {% endif %}
  <p>
    <a href="{{ post.url }}" class="post-title-archive">{{ post.title }}</a>
    <small class="text-muted">{{ post.date | date_to_string }}</small>
  </p>
{% endfor %}
</div>