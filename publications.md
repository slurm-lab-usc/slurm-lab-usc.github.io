---
layout: page
title: Publications
subtitle:
---

<style>
  /* Adjust the page width just for this page alone. */
  .container-md {
    max-width: 1800px; /* Set your desired maximum width */
    margin-left: auto;
    margin-right: auto;
  }

  /* Add any other custom styles for the page */
  body {
    margin: 0; /* Set margin to 0 for the entire body */
  }

  /* Year headers that divide the publication list. */
  h3.pub-year {
    margin-top: 40px;
    margin-bottom: 10px;
    padding-bottom: 6px;
    border-bottom: 2px solid #ddd;
  }
</style>

You can also find publications on <a href="https://scholar.google.com/citations?hl=en&user=ECHSnpYAAAAJ">Google Scholar</a> which may include some preprints not yet listed here.

<!-- Group publications by year (taken from the end of the venue string, e.g.,
     "Conference on Robot Learning (CoRL), 2025." -> "2025"), with one header and
     table per year. Groups appear in the same order as in _data/pubs.yml.
     Years up to and including `cutoff_year` are combined into one final
     "<cutoff_year> and Earlier" section. -->
{% assign cutoff_year = 2023 %}
{% assign pubs_by_year = site.data.pubs | group_by_exp: "pub", "pub.venue | strip | split: ' ' | last | remove: '.'" %}
{% for year_group in pubs_by_year %}
{% assign year_num = year_group.name | plus: 0 %}
{% if year_num > cutoff_year %}
<h3 class="pub-year" id="{{ year_group.name }}">{{ year_group.name }}</h3>
<table cellpadding="10" width="100%">
    {% for pub in year_group.items %}
        {% include pub.html %}
    {% endfor %}
</table>
{% endif %}
{% endfor %}

<h3 class="pub-year" id="{{ cutoff_year }}-and-earlier">{{ cutoff_year }} and Earlier</h3>
<table cellpadding="10" width="100%">
    {% for year_group in pubs_by_year %}
        {% assign year_num = year_group.name | plus: 0 %}
        {% if year_num <= cutoff_year %}
            {% for pub in year_group.items %}
                {% include pub.html %}
            {% endfor %}
        {% endif %}
    {% endfor %}
</table>

<!-- Daniel: doing this to add a separate workshop publication section. -->
<div style="height: 40px;"></div>

**Workshop Papers**

<!--Daniel: uses the same pub.html, but a different data.workshop_pubs -->
<table cellpadding="10" width="100%">
    {% for pub in site.data.workshop_pubs %}
        {% include pub.html %}
    {% endfor %}
</table>
