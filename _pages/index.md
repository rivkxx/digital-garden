---
layout: page
title: Home
id: home
permalink: /
---

# 🪴 Rick's Garden

<p> This website is a place to dump thoughts, ideas, coding resources and a bunch of other stuff that i could use for myself :p </p>

<strong>Recently updated notes</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
