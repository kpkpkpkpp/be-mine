<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Diya 💖</title>

  <style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      font-family: Arial, sans-serif;
      overflow: hidden;
    }

    .card {
      background: white;
      padding: 30px 20px;
      border-radius: 20px;
      text-align: center;
      box-shadow: 0 10px 30px rgba(0,0,0,0.2);
      width: 90%;
      max-width: 350px;
    }

    h1 {
      margin-bottom: 25px;
      color: #ff4d6d;
      font-size: 24px;
      line-height: 1.3;
    }

    button {
      padding: 12px 22px;
      font-size: 16px;
      border: none;
      border-radius: 30px;
      cursor: pointer;
    }

    #yes {
      background-color: #ff4d6d;
      color: white;
      margin-right: 10px;
    }

    #no {
      background-color: #ccc;
      position: absolute;
    }
  </style>
</head>
<body>

  <div class="card">
    <h1>Diya 💕<br>Will you be my Valentine?</h1>
    <button id="yes">Yes 💖</button>
    <button id="no">No 🙃</button>
  </div>

  <script>
    const noBtn = document.getElementById("no");

    noBtn.addEventListener("touchstart", moveButton);
    noBtn.addEventListener("mouseover", moveButton);

    function moveButton() {
      const x = Math.random() * (window.innerWidth - noBtn.offsetWidth);
      const y = Math.random() * (window.innerHeight - noBtn.offsetHeight);
      noBtn.style.left = x + "px";
      noBtn.style.top = y + "px";
    }

    document.getElementById("yes").addEventListener("click", () => {
      document.body.innerHTML = `
        <div style="
          height:100vh;
          display:flex;
          justify-content:center;
          align-items:center;
          background:linear-gradient(135deg,#ff9a9e,#fad0c4);
          font-family:Arial;
          text-align:center;
          padding:20px;">
          <h1 style="color:white;font-size:28px;line-height:1.4;">
            💖 Diya 💖<br><br>
            The night we met,<br>
            I knew it had to be you ✨<br><br>
            Happy Valentine’s Day 💕
          </h1>
        </div>
      `;
    });
  </script>

</body>
</html>
