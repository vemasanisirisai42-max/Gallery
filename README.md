# Ex.08 Design of Interactive Image Gallery
# Date:22-10-25
# AIM:
To design a web application for an inteactive image gallery with minimum five images.

# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Disney Princesses</title>
  <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Dancing+Script&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      font-family: 'Great Vibes', cursive;
      background: linear-gradient(120deg, #f0e4d7, #f8c3c1, #d3a6d6);
      color: #333;
      background-size: 300% 300%;
      animation: backgroundShift 12s ease infinite;
    }

    @keyframes backgroundShift {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    h1 {
      text-align: center;
      font-size: 3.5rem;
      margin: 40px 0 20px;
      background: linear-gradient(to right, #ff66b2, #ffccff);
      -webkit-background-clip: text;
      color: transparent;
      text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
    }

    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 25px;
      padding: 30px;
      max-width: 1400px;
      margin: auto;
    }

    .gallery-item {
      position: relative;
      overflow: hidden;
      border-radius: 16px;
      cursor: pointer;
      box-shadow: 0 10px 25px rgba(255, 105, 180, 0.3);
      transition: transform 0.4s ease, box-shadow 0.4s ease;
    }

    .gallery-item:hover {
      transform: scale(1.05);
      box-shadow: 0 20px 40px rgba(255, 105, 180, 0.5);
    }

    .gallery-item img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.4s ease;
    }

    .gallery-item:hover img {
      transform: scale(1.15);
    }

    .caption {
      position: absolute;
      bottom: 0;
      background: rgba(255, 255, 255, 0.85);
      width: 100%;
      padding: 12px;
      text-align: center;
      font-size: 16px;
      color: #9b59b6;
      font-weight: bold;
      letter-spacing: 1px;
    }

    /* Modal */
    .modal {
      display: none;
      position: fixed;
      inset: 0;
      background-color: rgba(0, 0, 0, 0.95);
      justify-content: center;
      align-items: center;
      z-index: 999;
    }

    .modal img {
      max-width: 90%;
      max-height: 90%;
      border: 5px solid #ff66b2;
      border-radius: 12px;
      box-shadow: 0 0 40px #ff66b2;
    }

    .modal .close {
      position: absolute;
      top: 25px;
      right: 35px;
      font-size: 40px;
      color: #fff;
      cursor: pointer;
      text-shadow: 0 0 15px #ff66b2;
    }

    footer {
      text-align: center;
      padding: 20px;
      font-size: 18px;
      font-family: 'Dancing Script', cursive;
      color: #fff;
      background-color: #9b59b6;
      border-top: 4px solid #ffccff;
    }
  </style>
</head>
<body>

  <h1>👑 Disney Princesses</h1>

  <div class="gallery">
    <div class="gallery-item" onclick="openModal('cin.jpg')">
      <img src="cin.jpg" alt="Cinderella">
      <div class="caption">Cinderella</div>
    </div>
    <div class="gallery-item" onclick="openModal('sw.jpg')">
      <img src="sw.jpg" alt="Snow White">
      <div class="caption">Snow White</div>
    </div>
    <div class="gallery-item" onclick="openModal('ar.jpg')">
      <img src="ar.jpg" alt="Aurora">
      <div class="caption">Aurora</div>
    </div>
    <div class="gallery-item" onclick="openModal('al.jpg')">
      <img src="al.jpg" alt="Ariel">
      <div class="caption">Ariel</div>
    </div>
    <div class="gallery-item" onclick="openModal('be.jpg')">
      <img src="be.jpg" alt="Belle">
      <div class="caption">Belle</div>
    </div>
    <div class="gallery-item" onclick="openModal('rap.jpg')">
      <img src="rap.jpg" alt="Rapunzel">
      <div class="caption">Rapunzel</div>
    </div>
    <div class="gallery-item" onclick="openModal('mer.jpg')">
      <img src="mer.jpg" alt="Merida">
      <div class="caption">Merida</div>
    </div>
    <div class="gallery-item" onclick="openModal('moa.jpg')">
      <img src="moa.jpg" alt="Moana">
      <div class="caption">Moana</div>
    </div>
  </div>

  <!-- Modal -->
  <div class="modal" id="imageModal">
    <span class="close" onclick="closeModal()">&times;</span>
    <img id="modalImage" src="" alt="Princess">
  </div>

  <footer>
    &copy; 2025 designed by ABIRAMI (24900822). All Rights Reserved.
  </footer>

  <script>
    function openModal(src) {
      const modal = document.getElementById('imageModal');
      const modalImg = document.getElementById('modalImage');
      modalImg.src = src;
      modal.style.display = 'flex';
    }

    function closeModal() {
      const modal = document.getElementById('imageModal');
      modal.style.display = 'none';
    }
  </script>
</body>
</html>
```
# OUTPUT:
![alt text](<Screenshot 2025-05-11 012202.png>)

![alt text](<Screenshot 2025-05-11 012214.png>)

![alt text](<Screenshot 2025-05-11 012225.png>)

![alt text](<Screenshot 2025-05-11 012238.png>)

![alt text](<Screenshot 2025-05-11 012247.png>)

# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
