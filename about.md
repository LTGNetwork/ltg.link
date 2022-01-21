---
layout: default
---
<script defer data-domain="ltg.link" src="https://analytics.ltg.link/js/plausible.js"></script>


{% assign redirects = site.pages | where_exp: "item", "item.redirect_to != nil" %}
{% for page in redirects %}
  [{{ page.url }}]({{ page.url | relative_url }}) 🔀 `{{ page.redirect_to }}`
  
{% endfor %}
