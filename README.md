<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>MemeZone by Keshav</title>
  <style>
    body {
      margin: 0;
      font-family: "Poppins", sans-serif;
      background: linear-gradient(135deg, #1e1e2f, #292943);
      color: #fff;
      text-align: center;
    }

    header {
      background: #ff5e5e;
      padding: 20px 0;
      font-size: 2rem;
      font-weight: bold;
      letter-spacing: 2px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
    }

    .buttons {
      margin: 30px 0;
    }

    button {
      background: #fff;
      color: #292943;
      border: none;
      padding: 12px 25px;
      border-radius: 25px;
      margin: 10px;
      font-size: 1rem;
      font-weight: 600;
      cursor: pointer;
      transition: 0.3s;
    }

    button:hover {
      background: #ff5e5e;
      color: white;
      transform: scale(1.05);
    }

    .meme-section {
      display: none;
      margin-top: 30px;
    }

    .meme-section.active {
      display: block;
      animation: fadeIn 0.5s ease;
    }

    .memes {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
    }

    .memes img {
      width: 280px;
      border-radius: 12px;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
      transition: 0.3s;
    }

    .memes img:hover {
      transform: scale(1.05);
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
  </style>
</head>
<body>
  <header>MemeZone 😂 – By Keshav</header>

  <div class="buttons">
    <button onclick="showCategory('school')">🏫 School</button>
    <button onclick="showCategory('parents')">🏠 Parents</button>
    <button onclick="showCategory('office')">💼 Office</button>
  </div>

  <!-- School Memes -->
  <div id="school" class="meme-section active">
    <div class="memes">
      <img src="https://i.imgur.com/XM7tRva.jpeg" alt="school meme 1" />
      <img src="https://i.imgur.com/yf4ZtMg.jpeg" alt="school meme 2" />
      <img src="https://i.imgur.com/JeY9L8F.jpeg" alt="school meme 3" />
    </div>
  </div>

  <!-- Parents Memes -->
  <div id="parents" class="meme-section">
    <div class="memes">
      <img src="https://i.imgur.com/Eq7EJtb.jpeg" alt="parents meme 1" />
      <img src="https://i.imgur.com/VD5ukTB.jpeg" alt="parents meme 2" />
      <img src="https://i.imgur.com/1Xz9t7B.jpeg" alt="parents meme 3" />
    </div>
  </div>

  <!-- Office Memes -->
  <div id="office" class="meme-section">
    <div class="memes">
      <img src="https://i.imgur.com/CtNY7hH.jpeg" alt="office meme 1" />
      <img src="https://i.imgur.com/8oJcT0q.jpeg" alt="office meme 2" />
      <img src="https://i.imgur.com/UnJ1i4b.jpeg" alt="office meme 3" />
    </div>
  </div>

  <script>
    function showCategory(category) {
      document.querySelectorAll('.meme-section').forEach(sec => sec.classList.remove('active'));
      document.getElementById(category).classList.add('active');
    }
  </script>
</body>
</html>
