---
title: "Publications"
permalink: /publications/
description: "Journal papers, conference papers, workshops, and under-review manuscripts."
---

<!-- <p class="lead">IEEE-style citations with placeholders for PDF/DOI links. Update entries by editing the Markdown files in <code>_publications/</code>.</p> -->

{% assign pubs = site.publications | sort: 'year' | reverse %}

## Journal Papers
{% for p in pubs %}{% if p.category == "Journal Papers" %}
{% include pub_item.html citation=p.citation pdf=p.pdf doi=p.doi %}
{% endif %}{% endfor %}

## Conference Papers
{% for p in pubs %}{% if p.category == "Conference Papers" %}
{% include pub_item.html citation=p.citation pdf=p.pdf doi=p.doi %}
{% endif %}{% endfor %}

## Workshops
{% for p in pubs %}{% if p.category == "Workshops" %}
{% include pub_item.html citation=p.citation pdf=p.pdf doi=p.doi %}
{% endif %}{% endfor %}

## Under Review
<div class="notice">Under-review items are shown without PDF/DOI buttons by default. Add links if/when preprints become available.</div>

{% for p in pubs %}{% if p.category == "Under Review" %}
<div class="pub">
  <div class="pub__cite">{{ p.citation }}</div>
</div>
{% endif %}{% endfor %}
