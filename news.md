---
title: "News"
permalink: /news/
description: "Updates on publications, talks, grants, and milestones."
---

<!-- <p class="lead">Reverse-chronological updates. Add a new Markdown file to <code>_posts/</code> to publish an item.</p> -->

{% for post in site.posts %}
  <article class="card" style="margin: 14px 0;">
    <h2 class="h2" style="margin-top:0;"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <div class="post-meta">{{ post.date | date: "%B %d, %Y" }}{% if post.venue %} · {{ post.venue }}{% endif %}{% if post.acceptance_rate %} · Acceptance rate: {{ post.acceptance_rate }}{% endif %}</div>
    <div>{{ post.excerpt }}</div>
  </article>
{% endfor %}

<hr/>

<!-- <div class="notice">
  <strong>Template:</strong> create <code>_posts/YYYY-MM-DD-title.md</code> with optional fields like <code>venue</code> and <code>acceptance_rate</code>.
</div> -->
