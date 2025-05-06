<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Birthday Bash</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to right, #ffe3e3, #ffc2d1);
      margin: 0;
      padding: 0;
      scroll-behavior: smooth;
    }

    .container {
      text-align: center;
      padding: 60px 20px;
    }

    h1 {
      font-size: 36px;
      color: #d6336c;
    }

    .icons {
      display: flex;
      justify-content: center;
      gap: 60px;
      margin-top: 40px;
    }

    .icons div {
      cursor: pointer;
      transition: transform 0.3s;
    }

    .icons div:hover {
      transform: scale(1.2);
    }

    .icons i {
      font-size: 50px;
      color: #e64980;
    }

    .icons p {
      margin-top: 10px;
      font-size: 18px;
      color: #333;
    }

    section {
      display: none;
      padding: 100px 20px;
      background: white;
      border-top: 3px dashed #ffb3c1;
    }

    section.active {
      display: block;
    }

    .about-details {
      max-width: 600px;
      margin: auto;
      font-size: 18px;
      color: #444;
      text-align: left;
    }

    .gallery-images {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 20px;
      margin-top: 30px;
    }

    .gallery-images img {
      width: 250px;
      height: 180px;
      object-fit: cover;
      border-radius: 15px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.2);
    }

    .back-link {
      display: inline-block;
      margin-top: 30px;
      text-decoration: none;
      color: #ff69b4;
      font-weight: bold;
    }

    .back-link:hover {
      text-decoration: underline;
    }
  </style>

  <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
</head>
<body>

  <!-- Home Page -->
  <div class="container" id="home-page">
    <h1>🎉 Welcome to the Birthday jony 🎉</h1>
    <div class="icons">
      <div onclick="showSection('about')">
        <i class="fas fa-info-circle"></i>
        <p>About</p>
      </div>
      <div onclick="showSection('gallery')">
        <i class="fas fa-images"></i>
        <p>Gallery</p>
      </div>
    </div>
  </div>

  <!-- About Section -->
  <section id="about">
    <h1>About the Party</h1>
    <div class="about-details">
      <p><strong>Date:</strong> Saturday, 10th May 2025</p>
      <p><strong>Time:</strong> 5:00 PM – 9:00 PM</p>
      <p><strong>Location:</strong> Rose Garden Banquet Hall, Hyderabad</p>
      <p><strong>Events:</strong></p>
      <ul>
        <li>🎤 Welcome Speech</li>
        <li>🎁 Fun Games & Activities</li>
        <li>🎂 Cake Cutting Ceremony</li>
        <li>🎶 Music & Dance</li>
        <li>🍕 Dinner & Refreshments</li>
      </ul>
    </div>
    <a class="back-link" href="#" onclick="goBack()">← Back to Home</a>
  </section>

  <!-- Gallery Section -->
  <section id="gallery">
    <h1>Photo Gallery</h1>
    <p>Some amazing memories captured during the party!</p>
    <div class="gallery-images">
      <img src="https://images.unsplash.com/photo-1578926283496-5c18c2b68a5b?auto=format&fit=crop&w=600&q=80" alt="Birthday Cake">
      <img src="https://images.unsplash.com/photo-1604014238885-cd67d347573d?auto=format&fit=crop&w=600&q=80" alt="Party Fun">
      <img src="https://images.unsplash.com/photo-1555685812-4b943f1cb0eb?auto=format&fit=crop&w=600&q=80" alt="Balloons">
    </div>
    <a class="back-link" href="#" onclick="goBack()">← Back to Home</a>
  </section>

  <script>
    function showSection(sectionId) {
      document.getElementById('home-page').style.display = 'none';
      document.querySelectorAll('section').forEach(s => s.classList.remove('active'));
      document.getElementById(sectionId).classList.add('active');
    }

    function goBack() {
      document.getElementById('home-page').style.display = 'block';
      document.querySelectorAll('section').forEach(s => s.classList.remove('active'));
    }
  </script>
</body>
</html>


# birthday-website
