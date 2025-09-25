<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>🎉 Feliz Cumpleaños 🎉</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Arial', sans-serif;
      background: url(https://http2.mlstatic.com/D_NQ_NP_890758-MPE90961430178_082025-O.webp) no-repeat center center fixed;
      background-size: cover;
      color: black;
      overflow-x: hidden;
      text-align: center;
    }

    .section {
      display: none;
      min-height: 100vh;
      padding: 40px;
    }

    .active {
      display: block;
    }

    h1 {
      font-size: 4.5em; /* Títulos aún más grandes */
      margin-top: 20px;
    }

    p {
      font-size: 2em; /* Dedicatoria y mensajes más grandes */
      max-width: 1000px;
      margin: 20px auto;
      line-height: 1.8;
    }

    button {
      background-color: #ff69b4;
      border: none;
      padding: 15px 30px;
      margin: 30px;
      border-radius: 12px;
      font-size: 1.4em;
      cursor: pointer;
      transition: background-color 0.3s;
    }

    button:hover {
      background-color: #ff1493;
      color: white;
    }

    .balloon {
      position: absolute;
      bottom: -150px;
      width: 80px;
      height: 100px;
      background-color: red;
      border-radius: 50% 50% 50% 50%;
      cursor: pointer;
      animation: float 8s linear infinite;
    }

    .balloon::after {
      content: "";
      position: absolute;
      bottom: -20px;
      left: 50%;
      width: 2px;
      height: 20px;
      background: #333;
      transform: translateX(-50%);
    }

    @keyframes float {
      0% { transform: translateY(0) rotate(0deg); }
      100% { transform: translateY(-120vh) rotate(15deg); }
    }

    .confetti {
      position: absolute;
      width: 10px;
      height: 10px;
      background-color: gold;
      opacity: 0.7;
      animation: fall 3s linear forwards;
    }

    @keyframes fall {
      to {
        transform: translateY(100vh) rotate(720deg);
        opacity: 0;
      }
    }
  </style>
</head>
<body>

  <!-- Pantalla inicial -->
  <div id="startScreen" class="section active">
    <h1>🎂 ¡Presiona el botón para comenzar la sorpresa! 🎂</h1>
    <button onclick="startCelebration()">Ver sorpresa</button>
  </div>

  <!-- Sección 1: Video -->
  <div class="section" id="videoSection">
    <h1>🎉 ¡Feliz Cumpleaños! 🎉</h1>
    <blockquote class="tiktok-embed" cite="https://www.tiktok.com/@papita_y_duquesa/video/7050494006052048134" data-video-id="7050494006052048134" style="max-width: 605px;min-width: 325px;" >
      <section>
        <a target="_blank" title="@papita_y_duquesa" href="https://www.tiktok.com/@papita_y_duquesa?refer=embed">@papita_y_duquesa</a>
        <a title="humor" target="_blank" href="https://www.tiktok.com/tag/humor?refer=embed">#humor</a>
        <a title="afhs" target="_blank" href="https://www.tiktok.com/tag/afhs?refer=embed">#afhs</a>
        <a title="felizcumpleaños" target="_blank" href="https://www.tiktok.com/tag/felizcumplea%C3%B1os?refer=embed">#felizcumpleaños</a>
        <a target="_blank" title="♬ sonido original - 😼☝🏻" href="https://www.tiktok.com/music/sonido-original-7050493980114438917?refer=embed">♬ sonido original - 😼☝🏻</a>
      </section>
    </blockquote>
    <script async src="https://www.tiktok.com/embed.js"></script>
    <button onclick="nextSection('videoSection','dedicatoriaSection')">➡ Siguiente</button>
  </div>

  <!-- Sección 2: Dedicatoria -->
  <div class="section" id="dedicatoriaSection">
    <h1>🎉🎉Un pequeño mensaje🎉🎉</h1>
    <p>
      Solo quería decirte que espero que pases un día maravilloso, que todo lo que hayas planeado para celebrar esta fecha tan importante salga bien; porque eres una persona única y especial.
      Sin que te des cuenta, me has apoyado un montón y por eso estoy muy agradecido.
      Muchas veces hiciste que todos los problemas que tenía se fueran por un instante con todas las cosas que me dices.
      Nunca cambies, porque puedo asegurar que para todas tus amigas eres muy importante.
      Espero que nuestra amistad siga durando muchos años más (así como te dije hace unos años, vuelvo a mencionarlo).
      ¡¡¡¡¡Feliz cumpleaños!!!!! 🥳
    </p>
    <img src="Primer recuerdo 2022-04-14.jpg" alt="Imagen especial" style="max-width:80%; border-radius:20px; margin-top:20px;">
    <br>
    <button onclick="nextSection('dedicatoriaSection','playlistsSection')">➡ Siguiente</button>
  </div>

  <!-- Sección 3: Playlists -->
  <div class="section" id="playlistsSection">
    <h1>🎶 Algo que pensé que ya no iba a hacer 🎶</h1>
    <p>Encontré la canción sobre soplar la vela que me habías contado antes XD, también encontré una playlist que según artículos te mejora el sueño (la probé durante 4 semanas y creo que si es verdad)</p>

    <!-- Playlist principal -->
    <iframe style="border-radius:12px"
      src="https://open.spotify.com/embed/playlist/5ValnKygEVa1JTVAKr6hIb?utm_source=generator"
      width="100%" height="380" frameBorder="0"
      allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"
      loading="lazy">
    </iframe>

    <!-- Playlist secundaria -->
    <iframe style="border-radius:12px"
      src="https://open.spotify.com/embed/playlist/2ubkArlehgWRhBmTtPuIuo?utm_source=generator"
      width="100%" height="380" frameBorder="0"
      allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"
      loading="lazy">
    </iframe>
  </div>

  <script>
    function startCelebration() {
      document.getElementById("startScreen").classList.remove("active");
      document.getElementById("videoSection").classList.add("active");
      releaseBalloons();
    }

    function nextSection(current, next) {
      document.getElementById(current).classList.remove("active");
      document.getElementById(next).classList.add("active");
      releaseBalloons();
    }

    function releaseBalloons() {
      for (let i = 0; i < 8; i++) {
        let balloon = document.createElement("div");
        balloon.classList.add("balloon");
        balloon.style.left = Math.random() * 100 + "vw";
        balloon.style.backgroundColor = getRandomColor();
        balloon.addEventListener("click", popBalloon);
        document.body.appendChild(balloon);

        setTimeout(() => { balloon.remove(); }, 8000);
      }
    }

    function popBalloon(e) {
      for (let i = 0; i < 20; i++) {
        let confetti = document.createElement("div");
        confetti.classList.add("confetti");
        confetti.style.left = e.clientX + "px";
        confetti.style.top = e.clientY + "px";
        confetti.style.backgroundColor = getRandomColor();
        document.body.appendChild(confetti);

        setTimeout(() => { confetti.remove(); }, 3000);
      }
      e.target.remove();
    }

    function getRandomColor() {
      const colors = ["#ff4d4d", "#ffcc00", "#66ff66", "#66ccff", "#ff99ff", "#ff9966"];
      return colors[Math.floor(Math.random() * colors.length)];
    }
  </script>

</body>
</html>
