---
layout: default
---

### Testing LTG Redirect
{% assign redirects = site.pages | where_exp: "item", "item.redirect_to != ltg" %}
{% for page in redirects %}
  [{{ page.url }}]({{ page.url | relative_url }}) 🔀 `{{ page.redirect_to }}`
  ---
{% endfor %}

### Testing Taympers Redirect
{% assign redirects = site.pages | where_exp: "item", "item.redirect_to != taympers" %}
{% for page in redirects %}
  [{{ page.url }}]({{ page.url | relative_url }}) 🔀 `{{ page.redirect_to }}`
  ---
{% endfor %}
