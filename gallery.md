---
layout: page
title: Gallery
permalink: /gallery/
---

<section id="gallery-section" class="hero is-fullheight has-text-centered">
  <div class="container is-fluid">
    <!-- Art Section -->
    <div id="art" class="gallery-category">
      <h3 class="category-title">Art</h3>
      <hr>
      <div class="category-projects-wrapper">
        <div class="image-grid">
        {% for file in site.static_files %}
          {% if file.path contains 'assets/images/art/' %}
            <div class="image-item">
              <figure class="gallery-project-image">
                <img src="{{ file.path }}" alt="{{ file.name }}">
              </figure>
              <div class="gallery-card-content">
                <p class="image-caption">{{ file.name | remove: 'assets/images/art/' | remove: '.jpg' | remove: '.JPG' | remove: '.png' | remove: '.PNG' }}</p>
              </div>
            </div>
          {% endif %}
        {% endfor %}
        </div>
      </div>
    </div>
    <!-- Ceramics Section -->
    <div id="ceramics" class="gallery-category">
      <h3 class="category-title">Ceramics</h3>
      <hr>
      <div class="category-projects-wrapper">
        {% assign ceramics_images = site.static_files | where: "path", "/assets/images/ceramics/" %}
        <div class="image-grid">
          {% for file in site.static_files %}
          {% if file.path contains 'assets/images/ceramics/' %}
            <div class="image-item">
              <figure class="gallery-project-image">
                <img src="{{ file.path }}" alt="{{ file.name }}">
              </figure>
              <div class="gallery-card-content">
                <p class="image-caption">{{ file.name | remove: 'assets/images/ceramics/' | remove: '.jpg' | remove: '.JPG' | remove: '.png' | remove: '.PNG' }}</p>
              </div>
            </div>
          {% endif %}
        {% endfor %}
        </div>
      </div>
    </div>
    <!-- Sewing Section -->
    <div id="sewing" class="gallery-category">
      <h3 class="category-title">Sewing</h3>
        <hr>
        <div class="category-projects-wrapper">
        {% assign sewing_images = site.static_files | where: "path", "/assets/images/sewing/" %}
        <div class="image-grid">
          {% for file in site.static_files %}
          {% if file.path contains 'assets/images/sewing/' %}
            <div class="image-item">
              <figure class="gallery-project-image">
                <img src="{{ file.path }}" alt="{{ file.name }}">
              </figure>
              <div class="gallery-card-content">
                <p class="image-caption">{{ file.name | remove: 'assets/images/sewing/' | remove: '.jpg' | remove: '.JPG' | remove: '.png' | remove: '.PNG' }}</p>
              </div>
            </div>
          {% endif %}
        {% endfor %}
        </div>
      </div>
    </div>
  </div>
</section>
