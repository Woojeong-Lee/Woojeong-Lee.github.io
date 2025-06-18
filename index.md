---
layout: home
author_profile: true
---


<nav>
  <ul>
    {% for page in site.header_pages %}
      <li><a href="{{ page.url | relative_url }}">{{ page.title }}</a></li>
    {% endfor %}
  </ul>
</nav>

Welcome! This is Woojeong Lee's portfolio site.
