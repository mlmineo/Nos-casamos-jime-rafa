<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Jime & Rafa · 14/11/2025</title>
  <meta name="description" content="Invitación de boda de Jime & Rafa" />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Playfair+Display:wght@400;600&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg:#faf7f2; --ink:#2e2a26; --gold:#b08968; --sand:#e8dccb; --leaf:#7a8f69;
    }
    *{box-sizing:border-box}
    html,body{margin:0;padding:0;background:var(--bg);color:var(--ink);font-family:Montserrat,system-ui,Arial,sans-serif}
    .hero{
      position:relative;min-height:75vh;
      background:linear-gradient(180deg,rgba(0,0,0,.15),rgba(0,0,0,.35)),url('1.jpg') center/cover no-repeat;
      display:grid;place-items:center
    }
    .overlay{position:absolute;inset:0;background:radial-gradient(transparent,rgba(0,0,0,.25))}
    .hero-inner{position:relative;text-align:center;color:#fff;padding:2rem}
    .names{font-family:'Great Vibes',cursive;font-size:4rem;margin:.25rem 0}
    .names span{color:var(--gold)}
    .date{font-family:'Playfair Display',serif;font-weight:600;letter-spacing:.3rem}
    .subtitle{opacity:.9;margin:.5rem 0 1rem}
    .countdown{margin:1rem auto;font-weight:600;background:rgba(255,255,255,.15);padding:.5rem 1rem;border-radius:999px;backdrop-filter:blur(4px)}
    .btn{display:inline-block;border:none;background:var(--gold);color:#fff;padding:.75rem 1.25rem;border-radius:999px;cursor:pointer;text-decoration:none;font-weight:600;transition:.2s}
    .btn:hover{transform:translateY(-2px);box-shadow:0 6px 20px rgba(0,0,0,.15)}
    .btn.primary{background:var(--leaf)} .btn.outline{background:transparent;border:2px solid var(--leaf);color:var(--leaf)}
    
    /* 🔔 NUEVO estilo para el botón musical con imagen */
    .music-btn{
      position:absolute;right:1rem;bottom:1rem;
      border-radius:50%;padding:0;border:2px solid #fff;
      background:rgba(255,255,255,.2);
      cursor:pointer;overflow:hidden;width:48px;height:48px;
      display:flex;align-items:center;justify-content:center;
    }
    .music-btn img{
      width:100%;height:100%;object-fit:cover;border-radius:50%;
      transition:.3s;
    }
    .music-btn:hover img{transform:scale(1.05)}
    
    main{max-width:960px;margin:auto;padding:2rem 1rem}
    .card{background:#fff;border:1px solid var(--sand);border-radius:18px;padding:1.25rem 1.5rem;margin:1rem 0;box-shadow:0 6px 30px rgba(0,0,0,.06)}
    .card h2{font-family:'Playfair Display',serif;margin-top:0;color:var(--leaf)}
    .gallery .grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(180px,1fr));gap:.6rem}
    .gallery img{width:100%;height:180px;object-fit:cover;border-radius:12px}
    .gift .gift-boxes{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:1rem}
    .gift .gift-box{border:1px dashed var(--sand);border-radius:14px;padding:1rem}
    .row{display:grid;grid-template-columns:1fr 1fr;gap:1rem}
    label{display:flex;flex-direction:column;font-weight:600;gap:.35rem}
    input,select{padding:.7rem .8rem;border:1px solid var(--sand);border-radius:10px;font:inherit}
    .actions{display:flex;gap:.6rem;flex-wrap:wrap;margin-top:.75rem}
    .footer{padding:2rem 1rem;text-align:center;color:#6b625a}
    @media (max-width:640px){.names{font-size:3rem}.gallery img{height:150px}.row{grid-template-columns:1fr}}
  </style>
</head>
<body>
  <header class="hero">
    <div class="overlay"></div>
    <div class="hero-inner">
      <h1 class="names">Jime <span>&</span> Rafa</h1>
      <p class="date">14 · 11 · 2025</p>
      <p class="subtitle">¡Nos casamos!</p>
      <div id="countdown" class="countdown"></div>
      <button id="rsvpBtn" class="btn primary">Confirmar asistencia</button>
    </div>

    <!-- Música: -->
    <audio id="bgm" preload="auto" loop>
      <source src="audio/Axel-y-Abel-pintos-Somos-Uno.mp3" type="audio/mpeg">
    </audio>
    <!-- 🔔 Botón musical con imagen -->
    <button id="musicToggle" class="music-btn" aria-label="Música">
      <img src="anillos-jime-rafa.jpg" alt="Anillos Jime & Rafa">
    </button>
  </header>

  <!-- Resto del contenido igual -->
  <!-- (lo omití para no duplicar todo el HTML de nuevo, tu contenido sigue igual) -->

  <script>
    const target = new Date('2025-11-14T13:30:00-03:00').getTime();
    const cd = document.getElementById('countdown');
    function tick(){
      const now = Date.now();
      let diff = Math.max(0, target - now);
      const d = Math.floor(diff/86400000); diff%=86400000;
      const h = Math.floor(diff/3600000); diff%=3600000;
      const m = Math.floor(diff/60000); diff%=60000;
      const s = Math.floor(diff/1000);
      cd.textContent = d+"d "+h+"h "+m+"m "+s+"s";
    }
    setInterval(tick,1000); tick();

    const bgm = document.getElementById('bgm');
    const musicBtn = document.getElementById('musicToggle');
    let musicOn = false;
    musicBtn.addEventListener('click', async () => {
      try{
        if(!musicOn){ await bgm.play(); musicOn = true; musicBtn.style.borderColor='#7a8f69'; }
        else { bgm.pause(); musicOn = false; musicBtn.style.borderColor='#fff'; }
      }catch(e){}
    });
  </script>
</body>
</html>
