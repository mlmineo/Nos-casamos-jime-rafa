<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Jime & Rafa · 14/11/2025</title>
  <meta name="description" content="Invitación de boda de Jime & Rafa" />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Playfair+Display:wght@500;700&family=Montserrat:wght@400;500;700&display=swap" rel="stylesheet">
  <style>
    :root{ --bg:#f9d392; --ink:#2e2a26; --gold:#b08968; --sand:#e8dccb; --leaf:#7a8f69; }
    *{box-sizing:border-box}
    html,body{margin:0;padding:0;background:var(--bg);color:var(--ink);font-family:Montserrat,system-ui,Arial,sans-serif}

    .hero{
      position:relative;min-height:75vh;
      background:var(--bg);
      display:grid;place-items:center
    }
    .overlay{position:absolute;inset:0;background:radial-gradient(transparent,rgba(0,0,0,.08))}
    .hero-inner{position:relative;text-align:center;color:#fff;padding:2rem}

    /* Imagen integrada */
    .hero-logo{
      display:block;margin:0 auto 1.25rem auto;
      width:min(62vw,420px);height:auto;
      border-radius:14px;box-shadow:none;
      mix-blend-mode:multiply;
      filter:contrast(1.06) saturate(1.06) brightness(0.98);
    }

    /* Tipos + grandes */
    .names{font-family:'Great Vibes',cursive;font-size:5.2rem;margin:.35rem 0;color:#fff}
    .date{font-family:'Playfair Display',serif;font-weight:700;letter-spacing:.35rem;color:#fff;font-size:1.5rem}
    .subtitle{opacity:.95;margin:.5rem 0 1rem;color:#fff}

    /* Pastilla de countdown */
    .countdown{
      margin:1.25rem auto 1rem;
      font-weight:700;letter-spacing:.05em;
      background:rgba(0,0,0,.16);
      padding:.6rem 1rem;border-radius:999px;
      backdrop-filter:blur(3px);color:#fff;display:inline-block
    }

    .btn{display:inline-block;border:none;background:var(--gold);color:#fff;padding:.75rem 1.25rem;border-radius:999px;cursor:pointer;text-decoration:none;font-weight:600;transition:.2s}
    .btn:hover{transform:translateY(-2px);box-shadow:0 6px 20px rgba(0,0,0,.15)}
    .btn.primary{background:var(--leaf)} .btn.outline{background:transparent;border:2px solid var(--leaf);color:var(--leaf)}

    /* Botón musical flotante */
    .music-btn{
      position:fixed;right:18px;bottom:18px;
      width:56px;height:56px;border-radius:50%;padding:0;border:0;
      background:#7a8f69;color:#fff;
      display:grid;place-items:center;
      box-shadow:0 8px 30px rgba(0,0,0,.22);
      cursor:pointer;z-index:1000;
      transition:transform .15s ease, box-shadow .15s ease, background .2s ease;
    }
    .music-btn:hover{transform:translateY(-2px);box-shadow:0 10px 34px rgba(0,0,0,.26)}
    .music-btn.is-on{background:#4f6b4b}

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

    @media (max-width:640px){
      .names{font-size:3.8rem}
      .date{font-size:1.25rem;letter-spacing:.28rem}
      .gallery img{height:150px}.row{grid-template-columns:1fr}
      .hero-logo{width:min(80vw,360px)}
    }
  </style>
</head>
<body>
  <header class="hero">
    <div class="overlay"></div>
    <div class="hero-inner">
      <img src="anillos-jime-rafa.jpg" class="hero-logo" alt="Anillos Jime & Rafa">
      <h1 class="names">Jime & Rafa</h1>
      <p class="date">14 · 11 · 2025</p>
      <p class="subtitle">¡Nos casamos!</p>
      <button id="rsvpBtn" class="btn primary">Confirmar asistencia</button>
    </div>

    <!-- Audio -->
    <audio id="bgm" preload="auto" loop playsinline>
      <source src="audio/somos-uno.mp3" type="audio/mpeg">
      Tu navegador no soporta el elemento de audio.
    </audio>

    <!-- Botón musical con icono -->
    <button id="musicToggle" class="music-btn" aria-label="Música">
      <svg viewBox="0 0 24 24" width="22" height="22" aria-hidden="true">
        <path d="M12 3v11.55a3.5 3.5 0 1 1-2-3.15V6.5l9-2V13.3a3.5 3.5 0 1 1-2-3.15V3.5l-5 1V3z" fill="currentColor"/>
      </svg>
    </button>
  </header>

  <main>
    <!-- ⏳ Cuenta regresiva arriba del WhatsApp -->
    <div id="countdown" class="countdown" aria-live="polite"></div>

    <section class="card">
      <h2>El Civil</h2>
      <p><strong>Te esperamos el día Viernes 14/11, a las 13:30 hs</strong></p>
      <p>📍 Nuestra Señora del Buen Viaje 470, Morón</p>
      <a class="btn" target="_blank" rel="noopener" href="https://www.google.com/maps/search/?api=1&query=Nuestra+Se%C3%B1ora+del+Buen+Viaje+470+Mor%C3%B3n">Ver en Maps</a>
    </section>

    <section class="card">
      <h2>La Celebración</h2>
      <p><strong>Festejamos juntos el día Sábado 15/11 a las 20:00 hs</strong></p>
      <p>📍 Puente Gualeguaychú 1359, General Rodríguez, Provincia de Buenos Aires</p>
      <a class="btn" target="_blank" rel="noopener" href="https://www.google.com/maps/search/?api=1&query=Puente+Gualeguaych%C3%BA+1359+General+Rodr%C3%ADguez+Buenos+Aires">Ver en Maps</a>
    </section>

    <section class="gallery card">
      <h2>Nuestra historia</h2>
      <div class="grid">
        <img src="1.jpg" alt="Jime y Rafa 1" loading="lazy"/>
        <img src="2.jpg" alt="Jime y Rafa 2" loading="lazy"/>
        <img src="3.jpg" alt="Jime y Rafa 3" loading="lazy"/>
        <img src="4.jpg" alt="Jime y Rafa 4" loading="lazy"/>
        <img src="5.jpg" alt="Jime y Rafa 5" loading="lazy"/>
        <img src="6.jpg" alt="Jime y Rafa 6" loading="lazy"/>
        <img src="7.jpg" alt="Jime y Rafa 7" loading="lazy"/>
        <img src="8.jpg" alt="Jime y Rafa 8" loading="lazy"/>
        <img src="9.jpg" alt="Jime y Rafa 9" loading="lazy"/>
      </div>
    </section>

    <section class="card rsvp" id="rsvp">
      <h2>Confirmación de asistencia</h2>
      <p>¡Nos encanta que quieras venir! Completá este formulario y confirmá por WhatsApp 💬</p>

      <form id="rsvpForm">
        <div class="form-group">
          <label for="nombre">Nombre y Apellido</label>
          <input type="text" id="nombre" name="nombre" placeholder="Tu nombre completo" required>
        </div>
        <div class="form-group">
          <label for="asistencia">¿Asistís?</label>
          <select id="asistencia" name="asistencia" required>
            <option value="Sí">Sí</option>
            <option value="No">No</option>
          </select>
        </div>
        <div class="form-group">
          <label for="acompanantes">Acompañantes</label>
          <input type="number" id="acompanantes" name="acompanantes" value="0" min="0" required>
        </div>
        <div class="form-group">
          <label for="cancion">Recomendá un temazo para el baile 💃🕺</label>
          <input type="text" id="cancion" name="cancion" placeholder="¿Qué querés escuchar?">
        </div>
        <button type="submit" class="btn">Enviar confirmación</button>
      </form>

      <p class="note">Las confirmaciones se envían por WhatsApp al <strong>+54 9 11 6044-9885</strong>.</p>
    </section>
  </main>

  <footer class="footer">
    <p>Con amor, Jime & Rafa • 14/11/2025</p>
  </footer>

  <script>
    /* ⏳ Cuenta regresiva al CIVIL: 14/11/2025 13:30 (-03:00) */
    (function setupCountdown(){
      const cd = document.getElementById('countdown');
      if(!cd) return;
      const target = new Date('2025-11-14T13:30:00-03:00').getTime();
      const z2 = n => String(n).padStart(2,'0');
      function tick(){
        const now = Date.now();
        let diff = Math.max(0, target - now);
        const d = Math.floor(diff/86400000); diff%=86400000;
        const h = Math.floor(diff/3600000);  diff%=3600000;
        const m = Math.floor(diff/60000);    diff%=60000;
        const s = Math.floor(diff/1000);
        if (target <= now) { cd.textContent = '¡Hoy es el gran día! 💍'; clearInterval(timer); return; }
        cd.textContent = `${d}d ${z2(h)}h ${z2(m)}m ${z2(s)}s`;
      }
      const timer = setInterval(tick, 1000); tick();
    })();

    /* 🎶 Música robusta (autoplay + desbloqueo en primer toque) */
    const bgm = document.getElementById('bgm');
    const musicBtn = document.getElementById('musicToggle');
    let musicOn = false;
    bgm.volume = 0.28; bgm.muted = false;

    bgm.addEventListener('error', () => {
      console.error('No se pudo cargar audio/somos-uno.mp3. Verificá ruta y nombre.');
    });

    window.addEventListener('load', async () => {
      try { await bgm.play(); musicOn = true; musicBtn.classList.add('is-on'); }
      catch { console.log('Autoplay bloqueado. Tocá el botón 🎵'); }
    });

    const unlock = async () => {
      try { if (!musicOn) { await bgm.play(); musicOn = true; musicBtn.classList.add('is-on'); } }
      catch {}
      document.removeEventListener('click', unlock);
      document.removeEventListener('touchstart', unlock, {passive:true});
    };
    document.addEventListener('click', unlock);
    document.addEventListener('touchstart', unlock, {passive:true});

    musicBtn.addEventListener('click', async (ev) => {
      ev.stopPropagation();
      try{
        if (!musicOn) { await bgm.play(); musicOn = true; musicBtn.classList.add('is-on'); }
        else { bgm.pause(); musicOn = false; musicBtn.classList.remove('is-on'); }
      }catch(e){}
    });

    /* WhatsApp RSVP */
    document.getElementById("rsvpForm").addEventListener("submit", function(e){
      e.preventDefault();
      const nombre = encodeURIComponent(document.getElementById("nombre").value);
      const asistencia = encodeURIComponent(document.getElementById("asistencia").value);
      const acompanantes = encodeURIComponent(document.getElementById("acompanantes").value);
      const cancion = encodeURIComponent(document.getElementById("cancion").value);
      const mensaje = `¡Hola! Soy ${nombre}. Confirmo asistencia: ${asistencia}. Acompañantes: ${acompanantes}. Sugerencia musical: ${cancion}.`;
      const telefono = "5491160449885";
      const url = `https://wa.me/${telefono}?text=${mensaje}`;
      window.open(url, "_blank");
    });

    /* Scroll al RSVP */
    document.getElementById('rsvpBtn').addEventListener('click', ()=>{
      document.getElementById('rsvp').scrollIntoView({behavior:'smooth'});
    });

    /* Copiar alias (si agregás botones .copy en la sección Regalo) */
    document.querySelectorAll('.copy').forEach(btn=>{
      btn.addEventListener('click', async ()=>{
        try{ await navigator.clipboard.writeText(btn.dataset.copy);
          btn.textContent='Copiado ✓'; setTimeout(()=>btn.textContent='Copiar alias',2000);
        }catch(e){}
      });
    });
  </script>
</body>
</html>
