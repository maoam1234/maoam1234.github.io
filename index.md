---
layout: default
title: Willkommen
---

<style>
  .spalten { display: flex; gap: 2rem; }
  .spalte { flex: 1; }
  .box { background: #f2f2f2; padding: 1rem; margin-bottom: 1rem; border-radius: 6px; }
</style>

<h1>🎓 Willkommen beim CampusMagazin</h1>

<div class="spalten">

  <!-- Videos -->
  <div class="spalte">
    <h2>🎥 Videos</h2>
    {% for video in site.videos %}
    <div class="box">
      <strong>{{ video.title }}</strong><br>
      <a href="{{ video.link }}">Ansehen</a>
    </div>
    {% endfor %}
  </div>

  <!-- Beiträge -->
  <div class="spalte">
    <h2>📰 Beiträge</h2>
    {% for post in site.beiträge %}
    <div class="box">
      <strong><a href="{{ post.link }}">{{ post.title }}</a></strong><br>
      {{ post.teaser }}
    </div>
    {% endfor %}
  </div>

  <!-- Über uns -->
  <div class="spalte">
    <h2>{{ site.about[0].title }}</h2>
    <p>{{ site.about[0].text }}</p>
  </div>

</div>
