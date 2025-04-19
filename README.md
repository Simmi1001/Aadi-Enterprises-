<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Aadi Enterprises</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap" rel="stylesheet">
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Inter', sans-serif;
    }
    body {
      background: #f8f9fa;
      color: #333;
    }
    header {
      background: #ffffff;
      padding: 20px 40px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }
    nav a {
      margin: 0 15px;
      text-decoration: none;
      color: #333;
      font-weight: 500;
    }
    .hero {
      padding: 60px 40px;
      background: url('https://images.unsplash.com/photo-1600585154340-be6161a56a0c') no-repeat center/cover;
      color: white;
      text-shadow: 1px 1px 4px rgba(0,0,0,0.5);
    }
    .hero h1 {
      font-size: 48px;
      max-width: 600px;
    }
    .section {
      padding: 60px 40px;
    }
    .section h2 {
      margin-bottom: 20px;
      font-size: 32px;
      color: #222;
    }
    .products {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 20px;
    }
    .product-card {
      background: white;
      border-radius: 10px;
      overflow: hidden;
      box-shadow: 0 2px 6px rgba(0,0,0,0.1);
    }
    .product-card img {
      width: 100%;
      height: 180px;
      object-fit: cover;
    }
    .product-card .info {
      padding: 15px;
    }
    .footer {
      background: #222;
      color: white;
      text-align: center;
      padding: 20px;
    }
    .whatsapp-button {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background: #25d366;
      color: white;
      padding: 12px 18px;
      border-radius: 50px;
      font-weight: bold;
      text-decoration: none;
      box-shadow: 0 2px 5px rgba(0,0,0,0.3);
    }
  </style>
</head>
<body>
  <header>
    <h2>Aadi Enterprises</h2>
    <nav>
      <a href="#home" onclick="showPage('home')">Home</a>
      <a href="#taps" onclick="showPage('taps')">Taps</a>
      <a href="#plants" onclick="showPage('plants')">Plants</a>
    </nav>
  </header>

  <!-- Home Page Content -->
  <div id="home" class="page-content">
    <section class="hero">
      <h1>Upgrade Your Home with Premium Kitchen & Bathroom Accessories</h1>
    </section>

    <section class="section">
      <h2>Our Products</h2>
      <div class="products">
        <div class="product-card" onclick="showPage('plants')">
          <img src="https://images.unsplash.com/photo-1601049089078-32a5665e0e9e" alt="Kitchen Organizer" />
          <div class="info">
            <h4>Kitchen Organizer</h4>
            <p>₹499</p>
          </div>
        </div>
        <div class="product-card" onclick="showPage('taps')">
          <img src="https://images.unsplash.com/photo-1590080876394-84012b21d1d3" alt="Bathroom Tap" />
          <div class="info">
            <h4>Bathroom Tap</h4>
            <p>₹799</p>
          </div>
        </div>
        <div class="product-card" onclick="showPage('plants')">
          <img src="https://images.unsplash.com/photo-1618221226484-d7fbb101c8a2" alt="Wall Mirror" />
          <div class="info">
            <h4>Wall Mirror</h4>
            <p>₹1,299</p>
          </div>
        </div>
      </div>
    </section>
  </div>

  <!-- Taps Page Content -->
  <div id="taps" class="page-content" style="display: none;">
    <section class="section">
      <h2>Taps</h2>
      <div class="products">
        <div class="product-card">
          <img src="https://images.unsplash.com/photo-1563779686-1f9ab5e2a8c5" alt="Bathroom Tap" />
          <div class="info">
            <h4>Bathroom Tap</h4>
          </div>
        </div>
      </div>
    </section>
  </div>

  <!-- Plants Page Content -->
  <div id="plants" class="page-content" style="display: none;">
    <section class="section">
      <h2>Artificial Plants</h2>
      <div class="products">
        <div class="product-card">
          <img src="https://images.unsplash.com/photo-1616627984393-663ebaa0f13d" alt="Artificial Plant" />
          <div class="info">
            <h4>Artificial Plant</h4>
          </div>
        </div>
      </div>
    </section>
  </div>

  <footer class="footer">
    <p>&copy; 2025 Aadi Enterprises. All rights reserved.</p>
  </footer>

  <a href="https://wa.me/919870498277?text=Hi , I want to know more about your products . " class="whatsapp-button" target="_blank">Chat on WhatsApp</a>

  <script>
    function showPage(page) {
      // Hide all pages
      document.querySelectorAll('.page-content').forEach(function (content) {
        content.style.display = 'none';
      });

      // Show the selected page
      document.getElementById(page).style.display = 'block';
    }

    // Initially show the Home page
    showPage('home');
  </script>
</body>
</html>
