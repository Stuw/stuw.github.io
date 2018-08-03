---
title: "Еженедельный подкаст об информационной безопасности"
---

## Безопасность для всех

Еженедельное, информационно-развлекательное шоу об информационной безопасности.

Новости за прошедшую неделю и полезная информация по различным темам.

## Список выпусков

{% for post in site.posts %}
<h3>{{ post.number }}. {{ post.title }} - {{ post.rudate }} - <a href="{{ post.url }}">{{ post.subtitle }}</a></h3>
{% include episode-media.html file=post.mp3file %}
{{ post.excerpt }}
<a href="{{ post.url }}" >подробнее...</a>
{% endfor %}
