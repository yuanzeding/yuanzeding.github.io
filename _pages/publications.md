---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}
{% assign pubs = site.data.publications %}
{% assign firsts = pubs | where: "first_author", true %}

{% assign cit = site.data.citations %}
<div class="pub-top">
  <div class="pub-top__text">
    <p>{{ pubs | size }} refereed papers, {{ firsts | size }} of them first-author, spanning X-ray studies of accreting black holes and neutron stars to integral-field spectroscopy of AGN hosts and their circumgalactic gas. Below are my first-author papers with a key figure from each, followed by papers I contributed to.</p>
    <p>
      <a class="btn-pill" href="{{ cit.scholar_url }}">Google Scholar</a>
      <a class="btn-pill" href="https://ui.adsabs.harvard.edu/search/q=orcid%3A%220000-0002-5770-2666%22&amp;sort=date%20desc%2C%20bibcode%20desc&amp;p_=0">NASA ADS</a>
      <a class="btn-pill alt" href="https://orcid.org/0000-0002-5770-2666">ORCID</a>
    </p>
  </div>
  <div class="gs">
    <div class="gs__head"><span class="gs__title">Cited by</span><a class="gs__link" href="{{ cit.scholar_url }}">VIEW ALL</a></div>
    <table class="gs__table">
      <tr><th></th><th>All</th><th>{{ cit.since_label }}</th></tr>
      <tr><td>Citations</td><td>{{ cit.total }}</td><td>{{ cit.total_since }}</td></tr>
      <tr><td>h-index</td><td>{{ cit.h_index }}</td><td>{{ cit.h_index_since }}</td></tr>
      <tr><td>i10-index</td><td>{{ cit.i10_index }}</td><td>{{ cit.i10_index_since }}</td></tr>
    </table>
    <div class="gs__chart">
      <div class="gs__plot">
        <div class="gs__bars">{% for y in cit.per_year %}{% assign h = y.count | times: 100 | divided_by: cit.axis_max %}<div class="gs__col"><div class="gs__bar" style="height: {{ h }}%"><span class="gs__tip">{{ y.count }}</span></div></div>{% endfor %}</div>
        <div class="gs__years">{% for y in cit.per_year %}<span>{{ y.year }}</span>{% endfor %}</div>
      </div>
      <div class="gs__axis"><span>{{ cit.axis_max }}</span><span>{{ cit.axis_max | times: 3 | divided_by: 4 }}</span><span>{{ cit.axis_max | divided_by: 2 }}</span><span>{{ cit.axis_max | divided_by: 4 }}</span><span>0</span></div>
    </div>
    <div class="gs__foot">Google Scholar &middot; {{ cit.as_of }}</div>
  </div>
</div>

<h2>In preparation</h2>

<div class="pub pub--prelim">
  <a class="pub__thumb" href="{{ base_path }}/research/#cgm"><img src="{{ base_path }}/images/research/cgm_hlqso_nebulae.jpg" alt="Lyman-alpha nebulae around hyperluminous QSOs" loading="lazy"></a>
  <div class="pub__main">
    <div class="pub__title">The Hosting Environment of Active Galaxies at Redshift 2&ndash;3. I. The Nature of the Extended Ly&alpha; Nebulae around AGNs<span class="badge prelim">To be submitted</span></div>
    <div class="pub__authors"><b>Y. Ding</b>, C. C. Steidel, F. A. Harrison, et al.</div>
    <div class="pub__venue">in prep.</div>
    <div class="pub__summary">Keck/KCWI and MOSFIRE spectroscopy of 55 KBSS AGN at z ~ 2&ndash;3, spanning about 8 magnitudes in luminosity. Ly&alpha; nebular luminosity scales sublinearly with AGN power, and Ly&alpha; is broader than the Balmer lines in faint AGN. Both point to dense neutral clumps in the CGM. Type-2 nebulae suggest an obscured, gas-rich phase. <i>Preliminary results, subject to change.</i></div>
    <a class="btn-pill" href="{{ base_path }}/research/#cgm">Preliminary results</a>
  </div>
</div>

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
