---
permalink: /cybersecurity_awareness_campaign/
title: "How to use Passwords according to the NIST as of August 2025"
author_profile: true
redirect_from: 
  - "/nmp/"
  - "/nmp.html"
---




<!DOCTYPE html>
<html>
<head>
  <title>Image Slideshow</title>
  <style>
    body { display: flex; justify-content: center; align-items: center; height: 100vh; margin: 0; background: #111; }
    img { max-width: 90%; max-height: 90%; border-radius: 10px; }
  </style>
</head>
<body>
  <img id="slideshow" src="image1.jpg" alt="Slide">
  <script>
    const images = [
      "image1.jpg", "image2.jpg", "image3.jpg",
      "image4.jpg", "image5.jpg", "image6.jpg",
      "image7.jpg", "image8.jpg", "image9.jpg",
      "image10.jpg"
    ];
    let index = 0;
    document.body.addEventListener("click", () => {
      index = (index + 1) % images.length;
      document.getElementById("slideshow").src = images[index];
    });
  </script>
</body>
</html>
