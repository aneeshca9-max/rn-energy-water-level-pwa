
<!DOCTYPE html>
<html lang="ml">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>RN Energy – Water Level Controller</title>

  <!-- PWA Meta -->
  <meta name="theme-color" content="#0a2a43" />
  <link rel="manifest" href="manifest.json">

  <style>
    *{
      box-sizing:border-box;
      font-family: "Segoe UI", sans-serif;
    }

    body{
      margin:0;
      background:linear-gradient(180deg,#081c2e,#020b12);
      color:#fff;
      text-align:center;
    }

    header{
      padding:16px;
      background:#0a2a43;
      box-shadow:0 2px 10px rgba(0,0,0,.5);
    }

    header h1{
      margin:0;
      font-size:20px;
      letter-spacing:1px;
    }

    header span{
      color:#00e0ff;
      font-size:13px;
    }

    .container{
      padding:20px;
      display:flex;
      justify-content:space-around;
      gap:20px;
      flex-wrap:wrap;
    }

    .tank{
      width:120px;
      height:220px;
      border:3px solid #00e0ff;
      border-radius:10px;
      position:relative;
      overflow:hidden;
      background:#02131f;
    }

    .water{
      position:absolute;
      bottom:0;
      width:100%;
      height:60%;
      background:linear-gradient(180deg,#00e0ff,#0077aa);
      animation:wave 2s infinite ease-in-out;
    }

    @keyframes wave{
      0%{transform:translateY(0)}
      50%{transform:translateY(-4px)}
      100%{transform:translateY(0)}
    }

    .label{
      margin-top:10px;
      font-weight:bold;
    }

    .controls{
      margin-top:30px;
    }

    button{
      padding:12px 22px;
      margin:10px;
      border:none;
      border-radius:30px;
      font-size:15px;
      font-weight:bold;
      cursor:pointer;
      color:#000;
    }

    .on{
      background:#00ff88;
    }

    .off{
      background:#ff4444;
      color:#fff;
    }

    footer{
      margin-top:30px;
      font-size:12px;
      opacity:.7;
    }
  </style>
</head>

<body>

<header>
  <h1>RN ENERGY</h1>
  <span>Smart Water Level Controller</span>
</header>

<div class="container">

  <div>
    <div class="tank">
      <div class="water" style="height:70%"></div>
    </div>
    <div class="label">Main Tank</div>
  </div>

  <div>
    <div class="tank">
      <div class="water" style="height:45%"></div>
    </div>
    <div class="label">Filter Tank</div>
  </div>

</div>

<div class="controls">
  <button class="on">MOTOR ON</button>
  <button class="off">MOTOR OFF</button>
</div>

<footer>
  © 2026 RN Energy • PWA Demo Interface
</footer>

</body>
</html>
