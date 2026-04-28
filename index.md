---
layout: default
title: Accueil
---

# L'Écho de la Passerelle

Bienvenue à bord, Monsieur. Voici les derniers rapports de mission enregistrés :

---

{% for post in site.posts %}
### [{{ post.title }}]({{ post.url }})
*Publié le {{ post.date | date: "%d/%m/%Y" }}* — Catégories : {{ post.categories | join: ", " }}

{{ post.excerpt | strip_html | truncatewords: 30 }}
<br>
---
{% endfor %}
