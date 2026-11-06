---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}
{% assign pubs = site.data.publications %}
{% assign firsts = pubs | where: "first_author", true %}

<div class="pub-stats">
  <div class="stat"><div class="stat__num">{{ pubs | size }}</div><div class="stat__lbl">Refereed papers</div></div>
  <div class="stat"><div class="stat__num">{{ firsts | size }}</div><div class="stat__lbl">First-author</div></div>
  <div class="stat"><div class="stat__num">2021</div><div class="stat__lbl">First paper</div></div>
</div>

<p>
  <a class="btn-pill" href="https://ui.adsabs.harvard.edu/search/q=orcid%3A%220000-0002-5770-2666%22&amp;sort=date%20desc%2C%20bibcode%20desc&amp;p_=0">Full list on NASA ADS</a>
  <a class="btn-pill alt" href="https://orcid.org/0000-0002-5770-2666">ORCID</a>
</p>

<h2>First-author papers</h2>

{% for p in pubs %}{% if p.first_author %}
<div class="pub">
  {% if p.image %}<a class="pub__thumb" href="https://doi.org/{{ p.doi }}"><img src="{{ base_path }}{{ p.image }}" alt="Figure from {{ p.title | strip_html }}" loading="lazy"></a>{% endif %}
  <div class="pub__main">
    <div class="pub__title">{{ p.title }}{% if forloop.first %}<span class="badge hot">New</span>{% endif %}</div>
    <div class="pub__authors">{{ p.authors }}</div>
    <div class="pub__venue">{{ p.year }}, <em>{{ p.journal }}</em>, {{ p.ref }}</div>
    {% if p.summary %}<div class="pub__summary">{{ p.summary }}</div>{% endif %}
    <a class="btn-pill" href="https://doi.org/{{ p.doi }}">Paper</a>
    <a class="btn-pill alt" href="https://ui.adsabs.harvard.edu/search/q=doi%3A%22{{ p.doi | url_encode }}%22">ADS</a>
  </div>
</div>
{% endif %}{% endfor %}

<h2>Contributed papers</h2>

{% for p in pubs %}{% unless p.first_author %}
<div class="pub pub--compact">
  <div class="pub__main">
    <div class="pub__title">{{ p.title }}</div>
    <div class="pub__authors">{{ p.authors }}</div>
    <div class="pub__venue">{{ p.year }}, <em>{{ p.journal }}</em>, {{ p.ref }}</div>
    <a class="btn-pill" href="https://doi.org/{{ p.doi }}">Paper</a>
    <a class="btn-pill alt" href="https://ui.adsabs.harvard.edu/search/q=doi%3A%22{{ p.doi | url_encode }}%22">ADS</a>
  </div>
</div>
{% endunless %}{% endfor %}
