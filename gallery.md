---
layout: page
title: Gallery
permalink: /gallery/
---

<section id="gallery-section" class="hero is-fullheight has-text-centered">
  <div class="container is-fluid">
    <!-- Paintings Section -->
    <div id="paintings" class="gallery-category">
      <button class="collapsible">Paintings</button>
      <div class="content">
        <div class="category-projects-wrapper">
          <div class="image-grid">
          {% for file in site.static_files %}
            {% if file.path contains 'assets/images/art/paintings/' %}
              <div class="image-item">
                <figure class="gallery-project-image">
                  <img src="{{ file.path }}" alt="{{ file.name }}">
                </figure>
                <div class="gallery-card-content">
                  <p class="image-caption">{{ file.name | remove: 'assets/images/art/paintings/' | remove: '.jpg' | remove: '.JPG' | remove: '.png' | remove: '.PNG' }}</p>
                </div>
              </div>
            {% endif %}
          {% endfor %}
          </div>
        </div>
      </div>
    </div>
    <!-- Pantone postcards Section -->
    <div id="pantone" class="gallery-category">
      <button class="collapsible">Pantone Postcards</button>
      <div class="content">
        <div class="category-projects-wrapper">
          <div class="image-grid">
          {% for file in site.static_files %}
            {% if file.path contains 'assets/images/art/pantone/' %}
              <div class="image-item">
                <figure class="gallery-project-image">
                  <img src="{{ file.path }}" alt="{{ file.name }}">
                </figure>
                <div class="gallery-card-content">
                  <p class="image-caption">{{ file.name | remove: 'assets/images/art/pantone/' | remove: '.jpg' | remove: '.JPG' | remove: '.png' | remove: '.PNG' }}</p>
                </div>
              </div>
            {% endif %}
          {% endfor %}
          </div>
        </div>
      </div>
    </div>
    <!-- Ceramics Section -->
    <div id="ceramics" class="gallery-category">
      <button class="collapsible">Ceramics</button>
      <div class="content">
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
    </div>
    <!-- Sewing Section -->
    <div id="sewing" class="gallery-category">
      <button class="collapsible">Sewing</button>
      <div class="content">
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
  </div>
</section>

<script>
    document.addEventListener("DOMContentLoaded", function () {
    const sections = document.querySelectorAll(".collapsible");
    sections.forEach(section => {
      section.addEventListener("click", function () {
        this.classList.toggle("active");
        const content = this.nextElementSibling;
        if (content.style.display === "block") {
          content.style.display = "none";
        } else {
          content.style.display = "block";
        }
      });
    });
  });

</script>