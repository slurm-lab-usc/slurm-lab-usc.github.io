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

You can also find publications on <a href="https://scholar.google.com/citations?hl=en&user=ECHSnpYAAAAJ">Google Scholar</a>.

<!-- Just make a table and iterate through publications. -->
<table cellpadding="10" width="100%">
    {% for pub in site.data.pubs %}
        {% include pub.html %}
    {% endfor %}
