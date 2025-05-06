---
layout: default
title: Home
permalink: /
---

<div class="home-content">
  <h1>Welcome to My Digital Garden</h1>

  <p>This is where I share my thoughts, ideas, and learnings about technology, personal development, and the intersection of digital and analog life.</p>

  <p>Feel free to explore my <a href="#latest">latest posts</a>, browse by <a href="#topics">topics</a>, or learn more <a href="/about">about me</a>.</p>

  <h2 id="latest">Latest</h2>
  <ul class="post-list">
    {% for post in site.posts %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <span class="post-meta">{{ post.date | date: "%B %d, %Y" }} · {{ post.content | number_of_words | divided_by: 200 | plus: 1 }} minute read</span>
      </li>
    {% endfor %}
  </ul>

  <h2 id="topics">Topics</h2>
  <div class="topics">
    {% assign tags = site.tags | sort %}
    {% for tag in tags %}
      <a href="/tags/{{ tag[0] }}" class="topic-tag">{{ tag[0] }}</a>
    {% endfor %}
  </div>

  <h2>Recent Updates</h2>
  <ul class="post-list">
    {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
    {% for note in recent_notes limit: 5 %}
      <li>
        <a href="{{ note.url | relative_url }}">{{ note.title }}</a>
        <span class="post-meta">{{ note.last_modified_at | date: "%B %d, %Y" }}</span>
      </li>
    {% endfor %}
  </ul>
</div>

This digital garden template is free, open-source, and [available on GitHub here](https://github.com/maximevaillancourt/digital-garden-jekyll-template).

The easiest way to get started is to read this [step-by-step guide explaining how to set this up from scratch](https://maximevaillancourt.com/blog/setting-up-your-own-digital-garden-with-jekyll).

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
