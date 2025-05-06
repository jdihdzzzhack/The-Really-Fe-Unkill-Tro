<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Сайт со скриптами</title>
  <style>
    body {
      background: #111;
      color: #fff;
      font-family: Arial;
      padding: 20px;
    }
    .script-box {
      background: #222;
      border: 1px solid #444;
      padding: 10px;
      margin-bottom: 10px;
      position: relative;
    }
    button.copy-btn {
      position: absolute;
      top: 10px;
      right: 10px;
      background: #e74c3c;
      color: white;
      border: none;
      padding: 5px 10px;
      cursor: pointer;
      border-radius: 4px;
    }
  </style>
</head>
<body>
  <h1>Мои скрипты</h1>

  <div class="script-box">
    <pre id="script1">loadstring(game:HttpGet("https://pastebin.com/raw/12345678"))()</pre>
    <button class="copy-btn" onclick="copyToClipboard('script1')">Скопировать</button>
  </div>

  <div class="script-box">
    <pre id="script2">print("Привет, мир!")</pre>
    <button class="copy-btn" onclick="copyToClipboard('script2')">Скопировать</button>
  </div>

  <script>
    function copyToClipboard(id) {
      const text = document.getElementById(id).innerText;
      navigator.clipboard.writeText(text).then(() => {
        alert("Скрипт скопирован!");
      });
    }
  </script>
</body>
</html>
