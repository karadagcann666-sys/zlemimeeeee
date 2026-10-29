
<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Özlemimeeeeee ❤️</title>
  <meta name="theme-color" content="#080808">
  <style>
    * { box-sizing: border-box; }

    body {
      margin: 0;
      min-height: 100vh;
      overflow-x: hidden;
      background: radial-gradient(ellipse at top, #38000b, #100006 48%, #030303);
      color: white;
      font-family: Georgia, "Times New Roman", serif;
      text-align: center;
    }

    .container {
      min-height: 100vh;
      padding: 65px 20px 45px;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      position: relative;
      z-index: 1;
    }

    .heart {
      color: #ff173d;
      font-size: 76px;
      animation: heartbeat 1.3s infinite;
      filter: drop-shadow(0 0 18px #ff003c);
    }

    h1 {
      font-size: clamp(43px, 11vw, 76px);
      margin: 18px 0;
      color: #ff3155;
      text-shadow: 0 0 12px #f03, 0 0 35px #8a001b;
    }

    .subtitle {
      font-size: 19px;
      line-height: 1.8;
      max-width: 500px;
      color: #f5d8df;
    }

    .divider {
      width: 110px;
      height: 2px;
      background: #ff2349;
      box-shadow: 0 0 12px #ff1744;
      margin: 25px 0;
    }

    button {
      margin-top: 22px;
      padding: 15px 25px;
      background: linear-gradient(135deg, #ff1744, #a00025);
      color: white;
      border: 1px solid #ff627d;
      border-radius: 30px;
      font-size: 17px;
      font-weight: bold;
      box-shadow: 0 0 25px #a0002555;
      cursor: pointer;
      -webkit-tap-highlight-color: transparent;
    }

    button:active { transform: scale(.97); }

    #message {
      display: none;
      max-width: 500px;
      margin-top: 28px;
      padding: 24px;
      line-height: 1.9;
      font-size: 18px;
      color: #ffe2e8;
      background: #25000bba;
      border: 1px solid #a91b3b;
      border-radius: 18px;
      box-shadow: 0 0 25px #ff003322;
      animation: appear .8s ease;
    }

    .footer {
      margin-top: 40px;
      color: #c78a98;
      font-size: 14px;
    }

    .floating-heart {
      position: fixed;
      bottom: -40px;
      color: #ff244b;
      pointer-events: none;
      opacity: .65;
      animation: floatUp linear forwards;
      z-index: 0;
    }

    @keyframes heartbeat {
      0%, 100% { transform: scale(1); }
      15% { transform: scale(1.15); }
      30% { transform: scale(1); }
      45% { transform: scale(1.09); }
    }

    @keyframes floatUp {
      to { transform: translateY(-115vh) rotate(35deg); opacity: 0; }
    }

    @keyframes appear {
      from { opacity: 0; transform: translateY(12px); }
      to { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>
<body>
  <main class="container">
    <div class="heart">♥</div>

    <h1>Özlemim</h1>

    <p class="subtitle">
      Bu dünyada binlerce insan var,<br>
      ama benim kalbim yalnızca seni seçti. ❤️
    </p>

    <div class="divider"></div>

    <p class="subtitle">
      Sen benim en güzel tesadüfüm,<br>
      en kıymetli hayalim ve kalbimin en güzel yerisin.
    </p>

    <button id="openButton" onclick="openMessage()">
      Mesajımı Aç ❤️
    </button>

    <div id="message">
      <h2 style="color:#ff3155">Sana, Özlemim ❤️</h2>
      Bazen sana ne kadar değer verdiğimi anlatacak
      kelimeleri bulamıyorum. Senin gülüşün günümü,
      sesin içimi, varlığın dünyamı güzelleştiriyor.
      <br><br>
      Mesafeler ne olursa olsun, kalbimdeki yerin
      hep aynı. İyi ki hayatımdasın, iyi ki varsın.
      <br><br>
      <strong>Seni çok seviyorum. ❤️</strong>
    </div>

    <div class="footer">
      Kalbimin en güzel köşesi sana ait. ♥
    </div>
  </main>

  <script>
    function openMessage() {
      const message = document.getElementById("message");
      const button = document.getElementById("openButton");

      message.style.display = "block";
      button.textContent = "Seni Çok Seviyorum ❤️";
      button.onclick = function () {
        message.style.display =
          message.style.display === "none" ? "block" : "none";
      };
    }

    function createHeart() {
      const heart = document.createElement("span");
      heart.className = "floating-heart";
      heart.textContent = Math.random() > 0.5 ? "♥" : "❤";
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.fontSize = (12 + Math.random() * 22) + "px";
      const duration = 5 + Math.random() * 5;
      heart.style.animationDuration = duration + "s";
      document.body.appendChild(heart);
      setTimeout(() => heart.remove(), duration * 1000);
    }

    setInterval(createHeart, 450);
  </script>
</body>
</html>
