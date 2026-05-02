---
layout: page
title: "musiques"
permalink: /musiques/
---

<h1 style="text-align: center;">Mes musiques</h1>
<p style="text-align: center;"><a href="/">&larr; Retour à l'accueil</a></p>

<div style="display: grid; grid-template-columns: repeat(auto-fill, minmax(200px, 1fr)); gap: 20px; max-width: 1200px; margin: 0 auto;">
  {% for post in site.posts %}
    {% if post.categories contains "musiques" %}
      <div style="border: 1px solid #eee; padding: 5px; text-align: center;">
        {% if post.image %}
          <img src="{{ post.image | absolute_url }}" alt="{{ post.title }}" style="max-width: 100%; height: auto; display: block; margin: 0 auto;">
        {% else %}
          <div style="width: 100%; height: 150px; background: #eee; display: flex; align-items: center; justify-content: center; color: #999;">Pas d'image</div>
        {% endif %}
        <h4>{{ post.title }}</h4>
        <p>{{ post.date | date: "%d %B %Y" }}</p>
      </div>
    {% endif %}
  {% endfor %}
</div>