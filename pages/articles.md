---
layout: default
title: Articles
permalink: /articles/
class: articles
---

<section class="section is-small">
  <div class='columns'>
    <div class="column is-8 is-offset-2">
      <h3 class='title is-4 has-text-centered'> Recent Articles </h3>
      {% for article in site.data.articles %}
      <div class='columns'>
        <div class="column">
          <h3 class="title is-4">
            <a href="{{ article.url | prepend: site.baseurl }}">
              {{ article.name }}
            </a>
          </h3>
        </div>
        <div class="column is-3 has-text-right is-hidden-mobile">
            <p> {{ article.date | date: "%b %-d, %Y" }} </p>
        </div>
      </div>
{% endfor %}
    </div>
  </div>
</section>
