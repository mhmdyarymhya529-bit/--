/ (ریشه ریپو)
  index.html
  music1.mp3
  music2.mp3
  ...
  music66.mp3
<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>آهنگ های مها</title>
  <style>
    body {
      margin: 0;
      background-color: #000; /* مشکی */
      color: #ff0000; /* قرمز */
      font-family: Tahoma, sans-serif;
      text-align: center;
    }

    h1 {
      padding: 20px;
      border-bottom: 2px solid #ff0000;
      text-shadow: 0 0 10px #ff0000;
    }

    .track {
      margin: 15px auto;
      padding: 15px;
      border: 1px solid #ff0000;
      border-radius: 8px;
      background: #111;
      width: 90%;
      max-width: 600px;
      box-shadow: 0 0 10px rgba(255,0,0,0.5);
      transition: transform 0.3s;
    }

    .track:hover {
      transform: scale(1.02);
      box-shadow: 0 0 20px rgba(255,0,0,0.8);
    }

    p {
      margin-bottom: 8px;
      font-weight: bold;
    }

    audio {
      width: 100%;
      outline: none;
      filter: hue-rotate(330deg) saturate(1.2);
    }

    footer {
      margin-top: 30px;
      padding: 15px;
      border-top: 1px solid #ff0000;
      font-size: 12px;
      color: #ff4d4d;
    }
  </style>
</head>
<body>
  <h1>🎵 آهنگ های مها 🎵</h1>
  <div id="list"></div>

  <footer>تمامی آهنگ‌ها در این سایت متعلق به مها هستند.</footer>

  <script>
    const list = document.getElementById("list");
    const TOTAL = 66; // تعداد ترک‌ها

    for (let i = 1; i <= TOTAL; i++) {
      const div = document.createElement("div");
      div.className = "track";
      div.innerHTML = `
        <p>آهنگ شماره ${i}</p>
        <audio controls src="./music${i}.mp3"></audio>
      `;
      list.appendChild(div);
    }
  </script>
</body>
</html>
