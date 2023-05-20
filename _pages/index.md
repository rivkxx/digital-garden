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

<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
body {
  padding: 25px;
  background-color: white;
  color: black;
  font-size: 25px;
}

.dark-mode {
  background-color: black;
  color: white;
}
</style>
</head>
<body>
  
<p>Click the button to toggle between dark and light mode for this page.</p>

<button onclick="myFunction()">Toggle dark mode</button>

<script>
function myFunction() {
   var element = document.body;
   element.classList.toggle("dark-mode");
}
</script>
