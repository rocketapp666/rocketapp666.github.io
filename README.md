<!DOCTYPE html>
<html lang="zh-CN">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>跳转中...</title>
  <style>
    html, body {
      height: 100%;
      margin: 0;
    }
    body {
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: -apple-system, "PingFang SC", "Microsoft YaHei", sans-serif;
      background: #f5f5f5;
      color: #333;
    }
    .message {
      font-size: 1.3rem;
      text-align: center;
    }
    .count {
      font-weight: 600;
      color: #2563eb;
    }
  </style>
</head>
<body>
  <div class="message">正在前往新主页... <span class="count" id="count">3</span></div>
  <script>
    var seconds = 3;
    var el = document.getElementById("count");
    var timer = setInterval(function () {
      seconds--;
      if (seconds <= 0) {
        clearInterval(timer);
        window.location.href = "https://abc.com";
      } else {
        el.textContent = seconds;
      }
    }, 1000);
  </script>
</body>
</html>
