---
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: single
---

<!-- barre de navigation horizontale -->
<div style="display: flex; justify-content: center; gap: 120px; margin-bottom: 40px; padding: 20px; background-color: none; border-radius: 8px;">
  <a href="#zine" style="text-decoration: none; color: #333; font-size: 15px;font-weight: thin; padding: 10px 20px; border: none; border-radius: 4px;">zines</a>
  <a href="/musique/" style="text-decoration: none; color: #333; font-size: 15px; font-weight: thin ; padding: 10px 20px; border: none; border-radius: 4px;">musiques</a>
  <a href="/photos/" style="text-decoration: none; color: #333; font-size: 15px; font-weight: thin; padding: 10px 20px; border: none; border-radius: 4px;">photos</a>
  <a href="#peintures" style="text-decoration: none; color: #333; font-size: 15px; font-weight: thin; font-size: 15px; padding: 10px 20px; border: none; border-radius: 4px;">peintures</a>
</div>


<!-- 2026 -->

<h3 style="margin-top: 30px;">2026</h3>

<div class="gallery-grid">
  {% for post in site.posts %}
    {% assign year = post.date | date: "%Y" %}
    {% if year == "2026" and post.categories contains "dessins" and post.image %}
      
      <div style="border: 1px solid #eee; padding: 5px; text-align: center;">
        
        <img 
          src="{{ post.image | relative_url }}" 
          alt="{{ post.title }}"
          style="width: 100%; height: auto; cursor: pointer;"
          onclick="openLightbox(
            '{{ post.image | relative_url }}',
            '{{ post.custom_caption | default: "" | escape }}',
            '{{ post.size | default: "" | escape }}',
            '{{ post.date | date: "%d %B %Y" }}'
          )"
        >

      </div>

    {% endif %}
  {% endfor %}
</div>


<!-- 2025 -->
<h3 style="margin-top: 30px;">2025</h3>

<div class="gallery-grid">
  {% for post in site.posts %}
    {% assign year = post.date | date: "%Y" %}
    {% if year == "2025" and post.categories contains "dessins" and post.image %}
      
      <div style="border: 1px solid #eee; padding: 5px; text-align: center;">
        
        <img 
          src="{{ post.image | relative_url }}" 
          alt="{{ post.title }}"
          style="width: 100%; height: auto; cursor: pointer;"
          onclick="openLightbox(
            '{{ post.image | relative_url }}',
            '{{ post.custom_caption | default: "" | escape }}',
            '{{ post.size | default: "" | escape }}',
            '{{ post.date | date: "%d %B %Y" }}'
          )"
        >

      </div>

    {% endif %}
  {% endfor %}
</div>

<!-- 2024 -->
<h3 style="margin-top: 30px;">2024</h3>

<div class="gallery-grid">
  {% for post in site.posts %}
    {% assign year = post.date | date: "%Y" %}
    {% if year == "2024" and post.categories contains "dessins" and post.image %}
      
      <div style="border: 1px solid #eee; padding: 5px; text-align: center;">
        
        <img 
          src="{{ post.image | relative_url }}" 
          alt="{{ post.title }}"
          style="width: 100%; height: auto; cursor: pointer;"
          onclick="openLightbox(
            '{{ post.image | relative_url }}',
            '{{ post.custom_caption | default: "" | escape }}',
            '{{ post.size | default: "" | escape }}',
            '{{ post.date | date: "%d %B %Y" }}'
          )"
        >

      </div>

    {% endif %}
  {% endfor %}
</div>

<!-- 2023 -->
<h3 style="margin-top: 30px;">2023</h3>

<div class="gallery-grid">
  {% for post in site.posts %}
    {% assign year = post.date | date: "%Y" %}
    {% if year == "2023" and post.categories contains "dessins" and post.image %}
      
      <div style="border: 1px solid #eee; padding: 5px; text-align: center;">
        
        <img 
          src="{{ post.image | relative_url }}" 
          alt="{{ post.title }}"
          style="width: 100%; height: auto; cursor: pointer;"
          onclick="openLightbox(
            '{{ post.image | relative_url }}',
            '{{ post.custom_caption | default: "" | escape }}',
            '{{ post.size | default: "" | escape }}',
            '{{ post.date | date: "%d %B %Y" }}'
          )"
        >

      </div>

    {% endif %}
  {% endfor %}
</div>

<!-- 2022 -->
<h3 style="margin-top: 30px;">2022</h3>

<div class="gallery-grid">
  {% for post in site.posts %}
    {% assign year = post.date | date: "%Y" %}
    {% if year == "2022" and post.categories contains "dessins" and post.image %}
      
      <div style="border: 1px solid #eee; padding: 5px; text-align: center;">
        
        <img 
          src="{{ post.image | relative_url }}" 
          alt="{{ post.title }}"
          style="width: 100%; height: auto; cursor: pointer;"
          onclick="openLightbox(
            '{{ post.image | relative_url }}',
            '{{ post.custom_caption | default: "" | escape }}',
            '{{ post.size | default: "" | escape }}',
            '{{ post.date | date: "%d %B %Y" }}'
          )"
        >

      </div>

    {% endif %}
  {% endfor %}
</div>

<style>
 .gallery-grid {
  column-count: 3;
  column-gap: 20px;
}

/* écrans moyens et tablettes */
@media (max-width: 1000px) {
  .gallery-grid {
    column-count: 2;
  }
}

/* mobiles */
@media (max-width: 600px) {
  .gallery-grid {
    column-count: 1;
  }
}

.gallery-item {
  break-inside: avoid;
  margin-bottom: 20px;
  border: 1px solid #eee;
  padding: 5px;
  display: inline-block;
  width: 100%;
}

.gallery-item img {
  width: 100%;
  height: auto;
  display: block;
}
  .gallery-title {
    font-size: 0.9em;
    color: #666;
    margin-top: 5px;
  }
</style>


<!-- Note : Pour les autres catégories (Zine, Photos, Peinture), vous pouvez créer des fichiers similaires ou ajouter des blocs ici si vous avez des posts dans ces catégories -->

<div id="lightbox" style="display:none; position:fixed; top:0; left:0; width:100%; height:100%; background:rgba(0,0,0,0.9); z-index:999;">

  <!-- IMAGE CENTRÉE (indépendante) -->
  <img id="lightbox-img"
       src=""
       style="position:absolute; top:50%; left:50%; transform:translate(-50%, -50%); max-width:70vw; max-height:80vh;">

  <!-- TEXTE À DROITE -->
  <div style="position:absolute; right:40px; top:50%; transform:translateY(-50%); width:250px; color:white;">
    <div id="lightbox-caption" style="font-size:18px;"></div>
    <div id="lightbox-size" style="font-size:18px;"></div>
    <div id="lightbox-date" style="margin-top:10px; font-size:14px; opacity:0.7;"></div>
  </div>

</div>

<!-- javascript de l'ouverture en grand des images -->
<script>
function openLightbox(src, caption, size, date) {
  const lightbox = document.getElementById("lightbox");

  lightbox.style.display = "block";

  document.getElementById("lightbox-img").src = src;
  document.getElementById("lightbox-caption").innerText = caption || "";
  document.getElementById("lightbox-size").innerText = size || "";
  document.getElementById("lightbox-date").innerText = date || "";
}

document.getElementById("lightbox").onclick = function() {
  this.style.display = "none";
}
</script>