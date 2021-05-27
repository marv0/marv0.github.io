---
layout: page
title: About
permalink: /about/
weight: 3
---

# **About The Author**

Hi I am **{{ site.author.name }}** :wave:,<br>
Hello, I am Marvin! I am an avid learner and enjoy solving problems using code. My other hobby is writing about topics I like; most commonly technology and other stuff I find interesting.

<div class="row">
{% include about/skills.html title="Programming Skills" source=site.data.programming-skills %}
{% include about/skills.html title="Other Skills" source=site.data.other-skills %}
</div>

<div class="row">
{% include about/timeline.html %}
</div>
