---
layout: page
title: Photo Gallery
permalink: /gallery/
---

<div class="gallery">
    {% for image in site.static_files %}
        {% if image.path contains 'assets/gallery/' %}
            <div class="gallery-item">
                <img src="{{ image.path | relative_url }}" alt="Gallery Image" class="gallery-img" onclick="openModal(this)">
            </div>
        {% endif %}
    {% endfor %}
</div>

<!-- Modal for expanded image view -->
<div id="galleryModal" class="modal">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <img id="modalImage" class="modal-img">
    </div>
</div>
