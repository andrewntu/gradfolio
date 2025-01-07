---
title:
layout: default
permalink: /news/
published: true
---


<div class="publicationContainer">

	<div class="gallery">


  {% for publication in site.publications %}

  {% if publication.redirect %}
  <div class="publicationTile">
          <a href="{{ publication.redirect }}" target="_blank">
          <span>
              <h2>{{ publication.title }}</h2>
              <br/>
              <p>{{ publication.description }}</p>
          </span>
          </a>
  </div>

  {% else %}

  <div class="publicationTile">
          <a href="{{ publication.url | prepend: site.baseurl | prepend: site.url }}">
          <span>
              <h2>{{ publication.title }}</h2>
              <br/>
              <p>{{ publication.description }}</p>
          </span>
          </a>
  </div>

  {% endif %}

  {% endfor %}

	</div>

</div>
