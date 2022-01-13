---
layout: default
title: Home
---
<h1>Welcome!</h1>

<h2>Posts</h2>

<p>Welcome to my website! Here I post what I've been up to, the projects I've been working on and talk about Game Dev.</p>

  <ul class="post-list">
    {% for post in site.posts %}
      {% if post.category == 'blog' %}
      <li>


        <h2>
          <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
        </h2>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
        <p>
            {{ post.excerpt }}
        </p>
      </li>
      {% endif %}
    {% endfor %}
  </ul>