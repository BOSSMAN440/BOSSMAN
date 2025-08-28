<!DOCTYPE html>
<html lang="pl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Galeria BSCMC.PL</title>
  <style>
    body {
      background: #111;
      color: #fff;
      font-family: 'Segoe UI', Tahoma, sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 20px;
      min-height: 100vh;
    }

    h1 {
      margin-bottom: 30px;
      background: linear-gradient(90deg, #00ffff, #ff00ff, #00ffff);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      font-size: 3em;
      text-align: center;
    }

    .gallery {
      display: flex;
      flex-wrap: wrap;
      gap: 20px;
      justify-content: center;
    }

    .gallery a {
      display: inline-block;
      border-radius: 12px;
      overflow: hidden;
      transition: transform 0.3s, box-shadow 0.3s;
    }

    .gallery a:hover {
      transform: scale(1.05);
      box-shadow: 0 0 20px #ff00ff, 0 0 40px #00ffff;
    }

    .gallery img {
      display: block;
      max-width: 300px;
      height: auto;
      border-radius: 12px;
    }
  </style>
</head>
<body>

  <h1>Galeria BSCMC.PL</h1>

  <div class="gallery">
    <a href="https://postimg.cc/DWp8tZj0" target="_blank">
      <img src="https://i.postimg.cc/DWp8tZj0/igrzyska.png" alt="igrzyska">
    </a>

    <a href="https://postimg.cc/8JSDjg0D" target="_blank">
      <img src="https://i.postimg.cc/8JSDjg0D/amongus.png" alt="amongus">
    </a>

    <a href="https://postimg.cc/hf5BVd52" target="_blank">
      <img src="https://i.postimg.cc/hf5BVd52/tnt-run.png" alt="tnt-run">
    </a>
  </div>

</body>
</html>
