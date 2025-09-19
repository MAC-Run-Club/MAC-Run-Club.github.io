---
layout: default
title: Photos
description: MAC Run Club memories and highlights
---

# Club Photos

Capturing our running adventures and community moments around San Francisco.

## Photo Gallery

<div class="photo-carousel">
  <!-- Main display area -->
  <div class="carousel-main">
    <div class="carousel-container">
      <img id="main-photo" src="/assets/photos/WhatsApp Image 2025-09-04 at 18.38.23.jpeg" alt="MAC Run Club photo">
    </div>
    <button class="carousel-btn prev-btn" onclick="changePhoto(-1)">‹</button>
    <button class="carousel-btn next-btn" onclick="changePhoto(1)">›</button>
  </div>
  
  <!-- Thumbnail navigation -->
  <div class="carousel-thumbnails">
    <img class="thumbnail active" src="/assets/photos/WhatsApp Image 2025-09-04 at 18.38.23.jpeg" alt="Photo 1" onclick="showPhoto(0)">
    <img class="thumbnail" src="/assets/photos/WhatsApp Image 2025-09-09 at 18.17.31.jpeg" alt="Photo 2" onclick="showPhoto(1)">
    <img class="thumbnail" src="/assets/photos/WhatsApp Image 2025-09-11 at 19.08.16.jpeg" alt="Photo 3" onclick="showPhoto(2)">
    <img class="thumbnail" src="/assets/photos/WhatsApp Image 2025-09-18 at 18.40.52.jpeg" alt="Photo 4" onclick="showPhoto(3)">
    <img class="thumbnail" src="/assets/photos/WhatsApp Image 2025-09-18 at 21.48.37.jpeg" alt="Photo 5" onclick="showPhoto(4)">
  </div>
</div>

<script>
const photos = [
  "/assets/photos/WhatsApp Image 2025-09-04 at 18.38.23.jpeg",
  "/assets/photos/WhatsApp Image 2025-09-09 at 18.17.31.jpeg",
  "/assets/photos/WhatsApp Image 2025-09-11 at 19.08.16.jpeg",
  "/assets/photos/WhatsApp Image 2025-09-18 at 18.40.52.jpeg",
  "/assets/photos/WhatsApp Image 2025-09-18 at 21.48.37.jpeg"
];

let currentPhoto = 0;

function showPhoto(index) {
  currentPhoto = index;
  document.getElementById('main-photo').src = photos[index];
  
  // Update thumbnail active state
  document.querySelectorAll('.thumbnail').forEach((thumb, i) => {
    thumb.classList.toggle('active', i === index);
  });
}

function changePhoto(direction) {
  currentPhoto += direction;
  if (currentPhoto >= photos.length) currentPhoto = 0;
  if (currentPhoto < 0) currentPhoto = photos.length - 1;
  showPhoto(currentPhoto);
}

// Keyboard navigation
document.addEventListener('keydown', function(e) {
  if (e.key === 'ArrowLeft') changePhoto(-1);
  if (e.key === 'ArrowRight') changePhoto(1);
});
</script>

---
