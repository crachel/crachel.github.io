---
layout: default
---

Welcome. I'm Craig Rachel. This is my personal site, where I write about the
things I'm building and thinking about.

## Posts

<ul class="post-list">
{% for post in site.posts %}
  <li class="post-list-item">
    <time class="post-list-date" datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%b %-d, %Y" }}</time>
    <a class="post-list-link" href="{{ post.url | relative_url }}">{{ post.title }}</a>
    {% if post.excerpt %}
    <p class="post-list-excerpt">{{ post.excerpt | strip_html | strip_newlines | truncatewords: 30 }}</p>
    {% endif %}
  </li>
{% endfor %}
</ul>

<p><a href="{{ '/feed.xml' | relative_url }}">Subscribe via RSS</a></p>
