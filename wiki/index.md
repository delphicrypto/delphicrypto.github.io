---
layout: page
nav: true
order: 1
---

Welcome to the **Ozeki Knowledge Base**. 
Here you will find our collection of articles and podcasts where we distill and simplify the latest and most important scientific advances in various technical fields.

<h1 class="page-heading">Pages</h1>

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
