---
layout: page
nav: true
order: 1
---

Welcome to the **Ozeki Knowledge Base**. 
Here you will find our collection of articles and podcasts where we distill and simplify the latest and most important scientific advances in various technical fields.

<h1 class="page-heading">Categories</h1>

{% for cat_posts in site.categories %}
{% assign cat = cat_posts[0] %}
{% assign posts = cat_posts[1] %}
{% assign cat_url_encode = cat | url_encode | replace: '+', '%20' %}
* <a class="category-list-link" href="{{ '/category/#/' | relative_url | append: cat_url_encode }}">{{ cat }} ({{posts.size}})</a>
{% endfor %}


<h1 class="page-heading"> All Pages</h1>

<ul>
  {% for post in site.posts %}
  <li>
    <a href="{{ post.url }}" title="{{ post.title }}">
      <span class="date">
        <span class="day">{{ post.date | date: '%d' }}</span>
        <span class="month"><abbr>{{ post.date | date: '%b' }}</abbr></span>
        <span class="year">{{ post.date | date: '%Y' }}</span>
      </span>
      <span class="title">{{ post.title }}</span>
    </a>
  </li>
  {% endfor %}
</ul>
