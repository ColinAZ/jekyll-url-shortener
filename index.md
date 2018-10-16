---
layout: default
---

{% assign redirects = site.pages | where_exp: "item", "item.redirect_to != nil" %}
{% for page in redirects %}
  [{{ page.url }}]({{ page.url }}) 🔀 `{{ page.redirect_to }}`

  > {{ page.title }}

  ---
{% endfor %}
