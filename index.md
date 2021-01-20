---
title: "Подкаст о технологиях и новостях из мира информационной безопасности"
---

<h2 class="mb-4 text-center">Список выпусков</h2>
<p>Подкаст о технологиях и новостях из мира информационной безопасности. Все эпизоды доступны в текстовом виде.</p>

<div class="row">

{% for post in site.posts %}
<div class="col-sm-12 col-md-6 d-flex">

<div class="card">
 <img src="assets/images/ep/{{ post.number }}.jpg" class="card-img-top" alt="">
 <div class="card-body">
   <h5 class="card-title"><a href="{{ post.url }}">#{{ post.number }}. {{ post.subtitle }} - "{{ post.title }}"</a></h5>
   <h6 class="card-subtitle mb-2 text-muted">{% include rudate.html date=post.date %}</h6>
   <p class="card-text">
{% include episode-media.html file=post.mp3file %}
   </p>
   <p class="text-justify">{{ post.excerpt | strip_html}}</p>
   <a href="{{ post.url }}" class="card-link">читать дальше</a>
   <a class="float-right" target="_blank" href="/assets/audio/{{ post.mp3file | uri_escape }}" download="{{ post.mp3file }}"><i class="fas fa-download"></i></a>
 </div>
</div>

</div>
{% endfor %}

</div>
