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
</style>

You can also find publications on <a href="https://scholar.google.com/citations?hl=en&user=ECHSnpYAAAAJ">Google Scholar</a> which may include some preprints not yet listed here.

<!-- Just make a table and iterate through publications. -->
<table cellpadding="10" width="100%">
    {% for pub in site.data.pubs %}
        {% include pub.html %}
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
