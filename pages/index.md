---
layout: default
title: Articles
permalink: /
class: home
---

<section class="section is-small">
  <div class='columns'>
    <div class="column is-8 is-offset-2">
      <h3 class='title is-4 has-text-centered'> Recent posts </h3>
      {% for post in site.posts | sort: 'date' %}
      <div class='columns'>
        <div class="column">
          <h3 class="title is-4">
            <a href="{{ post.url | prepend: site.baseurl }}">
              {{ post.title }}
            </a>
          </h3>
        </div>
        <div class="column is-3 has-text-right is-hidden-mobile">
            <p> {{ post.date | date: "%b %-d, %Y" }} </p>
        </div>
      </div>
{% endfor %}
    </div>
  </div>
</section>
