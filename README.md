<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Invitation Mariage</title>
  <link href="https://fonts.googleapis.com/css2?family=Amiri&display=swap" rel="stylesheet">
  <style>
    body, html {
      margin: 0;
      padding: 0;
      height: 100%;
      font-family: 'Amiri', serif;
      overflow: hidden;
    }

    /* Fond avec motif marocain */
    body {
      background: url('fond-marocain.jpg') no-repeat center center fixed;
      background-size: cover;
      display: flex;
      justify-content: center;
      align-items: center;
      color: #fff;
    }

    /* Overlay semi-transparent */
    .overlay {
      background: rgba(0,0,0,0.5);
      padding: 50px 30px;
      text-align: center;
      border-radius: 15px;
      max-width: 800px;
      width: 90%;
    }

    h1 {
      font-size: 3em;
      margin-bottom: 0.2em;
      text-shadow: 2px 2px 8px #000;
    }

    p {
      font-size: 1.3em;
      margin: 10px 0;
    }

    .btn {
      display: inline-block;
      margin-top: 20px;
      padding: 15px 40px;
      background: #d4af37;
      color: #000;
      text-decoration: none;
      font-weight: bold;
      border-radius: 12px;
      transition: 0.3s;
      box-shadow: 2px 2px 8px #000;
    }

    .btn:hover {
      background: #b88f2c;
    }

    /* Animation de légers motifs marocains */
    .pattern {
      position: absolute;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: url('motif-marocain.png') repeat;
      opacity: 0.1;
      animation: movePattern 20s linear infinite;
      pointer-events: none;
    }

    @keyframes movePattern {
      0% { background-position: 0 0; }
      100% { background-position: 1000px 1000px; }
    }

  </style>
</head>
<body>
  <div class="pattern"></div>
  <div class="overlay">
    <h1>Vous êtes invités à notre mariage !</h1>
    <p>Saad & [NIAMA]</p>
    <p>Le 14 Septembre 2025 . 20H00  à [VILLA BENSAMMOU BOUSKOURA ]</p>
    <a href="https://maps.app.goo.gl/qygZ64TZWfqAXfBb6?g_st=ic" class="btn" target="_blank">Voir le lieu sur la carte</a>
    <br><br>
    <button class="btn" onclick="toggleMusic()">🎵 Jouer / Pause Musique</button>
  </div>

  <!-- Musique -->
  <audio id="music" loop>
    <source src="musique-mariage.mp3" type="audio/mpeg">
    Votre navigateur ne supporte pas la lecture audio.
  </audio>

  <script>
    const music = document.getElementById('music');
    function toggleMusic() {
      if (music.paused) {
        music.play();
      } else {
        music.pause();
      }
    }
  </script>
</body>
</html>
