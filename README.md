<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <title>Aviator Prédiction 🇲🇬</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #220000;
      color: #fff;
      text-align: center;
      padding: 40px;
    }
    h1 {
      color: #ff4d4d;
    }
    #predictBtn {
      background-color: #ff4d4d;
      border: none;
      color: #fff;
      padding: 15px 30px;
      font-size: 18px;
      cursor: pointer;
      border-radius: 8px;
    }
    #prediction {
      margin-top: 20px;
      font-size: 32px;
      color: #ffd700;
    }
    #history {
      margin-top: 30px;
      text-align: left;
      max-width: 400px;
      margin-left: auto;
      margin-right: auto;
    }
    .entry {
      border-bottom: 1px solid #550000;
      padding: 5px 0;
    }
    #footer {
      margin-top: 40px;
      font-size: 16px;
      color: #ff9999;
    }
  </style>
</head>
<body>
  <h1>Aviator Prédiction 🇲🇬</h1>
  <p><strong>Famille 🎁🎁</strong></p>
  <button id="predictBtn">Faire une prédiction</button>
  <div id="prediction"></div>
  <div id="history">
    <h3>Historique</h3>
    <div id="historyList"></div>
  </div>
  <div id="footer">
    Code : <strong>A777A</strong>
  </div>

  <script>
    const predictBtn = document.getElementById("predictBtn");
    const predictionDiv = document.getElementById("prediction");
    const historyList = document.getElementById("historyList");

    predictBtn.addEventListener("click", () => {
      const randomMultiplier = (Math.random() * (100 - 1.01) + 1.01).toFixed(2);
      predictionDiv.textContent = `Multiplicateur prédit : x${randomMultiplier}`;
      const entry = document.createElement("div");
      entry.className = "entry";
      const date = new Date().toLocaleTimeString();
      entry.textContent = `${date} - x${randomMultiplier}`;
      historyList.prepend(entry);
    });
  </script>
</body>
</html>
