---
layout: post-list
title: Home
permalink: /
---

# Welcome to My Digital Garden

This is where I share my thoughts, ideas, and learnings about technology, personal development, and the intersection of digital and analog life.

Feel free to explore my [latest posts](#latest), browse by [topics](#topics), or learn more [about me](/about).

## Getting Started

Take a look at my [first note](/notes/welcome) to begin your exploration of this digital garden.

## Recent Updates

<ul class="post-list">
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      <a href="{{ note.url | relative_url }}">{{ note.title }}</a>
      <span class="post-meta">{{ note.last_modified_at | date: "%B %d, %Y" }}</span>
    </li>
  {% endfor %}
</ul>

This digital garden template is free, open-source, and [available on GitHub here](https://github.com/maximevaillancourt/digital-garden-jekyll-template).

The easiest way to get started is to read this [step-by-step guide explaining how to set this up from scratch](https://maximevaillancourt.com/blog/setting-up-your-own-digital-garden-with-jekyll).

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
