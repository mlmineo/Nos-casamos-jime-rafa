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
    :root{ --bg:#faf7f2; --ink:#2e2a26; --gold:#b08968; --sand:#e8dccb; --leaf:#7a8f69; }
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
    /* Botón musical con imagen */
    .music-btn{
      position:absolute;right:1rem;bottom:1rem;
      width:52px;height:52px;border-radius:50%;padding:0;border:2px solid #fff;
      background:rgba(255,255,255,.2);backdrop-filter:blur(2px);
      cursor:pointer;overflow:hidden;display:flex;align-items:center;justify-content:center;
      box-shadow:0 6px 20px rgba(0,0,0,.18);
    }
    .music-btn img{width:100%;height:100%;object-fit:cover;border-radius:50%;transition:.25s}
    .music-btn:hover img{transform:scale(1.06)}
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
      <h1 class="names">Jime & Rafa</h1>
      <p class="date">14 · 11 · 2025</p>
      <p class="subtitle">¡Nos casamos!</p>
      <div id="countdown" class="countdown"></div>
      <button id="rsvpBtn" class="btn primary">Confirmar asistencia</button>
    </div>

    <!-- Música -->
    <audio id="bgm" preload="auto" loop>
      <source src="audio/Axel-y-Abel-pintos-Somos-Uno.mp3" type="audio/mpeg">
    </audio>

    <!-- Botón musical usando tu imagen -->
    <button id="musicToggle" class="music-btn" aria-label="Música">
      <img src="anillos-jime-rafa.jpg" alt="Anillos Jime & Rafa">
    </button>
  </header>

  <main>
    <section class="card">
      <h2>El Civil</h2>
      <p><strong>Te esperamos el día Viernes 14/11, a las 13:30 hs</strong></p>
      <p>📍 Nuestra Señora del Buen Viaje 470, Morón</p>
      <a class="btn" target="_blank" rel="noopener" href="https://www.google.com/maps/search/?api=1&query=Nuestra+Se%C3%B1ora+del+Buen+Viaje+470+Mor%C3%B3n">Ver en Maps</a>
    </section>

    <section class="card">
      <h2>La Celebración</h2>
      <p><strong>Sábado 15/11 a las 20:00 hs</strong></p>
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

    <section class="gift card">
      <h2>Regalo</h2>
      <p>Tu presencia es lo más importante para nosotros. Si además querés hacernos un regalo te compartimos nuestros datos bancarios 💛</p>
      <div class="gift-boxes">
        <div class="gift-box">
          <p><strong>Alias:</strong> jime.la.gringa</p>
          <p><strong>CVU:</strong> 0000003100073131930184</p>
          <p><strong>Nombre:</strong> Mariela Jimena Ormeño</p>
          <button class="btn copy" data-copy="jime.la.gringa">Copiar alias</button>
        </div>
        <div class="gift-box">
          <p><strong>Alias:</strong> rocco.milo.luli.mp</p>
          <p><strong>CVU:</strong> 0000003100177678298698</p>
          <p><strong>Nombre:</strong> Sergio Ra Rodríguez Bentancur</p>
          <button class="btn copy" data-copy="rocco.milo.luli.mp">Copiar alias</button>
        </div>
      </div>
    </section>

    <section class="card rsvp" id="rsvp">
      <h2>Confirmación de asistencia</h2>
      <p>¡Nos encanta que quieras venir! Completá este formulario y te leemos.</p>
      <form id="rsvpForm">
        <div class="row">
          <label>Nombre y Apellido
            <input type="text" name="nombre" required />
          </label>
          <label>¿Asistís?
            <select name="asiste" required>
              <option value="Sí">Sí</option>
              <option value="No">No</option>
            </select>
          </label>
        </div>
        <div class="row">
          <label>Acompañantes
            <input type="number" name="acompanantes" min="0" value="0" required />
          </label>
          <label>Mensaje
            <input type="text" name="mensaje" placeholder="¿Algo que quieras decirnos? Recomienda algún tema para el baile" />
          </label>
        </div>
        <div class="actions">
          <button type="submit" class="btn primary">Enviar confirmación</button>
        </div>
        <p class="help">Las confirmaciones se envían a <strong>jimena.rocco@hotmail.com</strong>.</p>
      </form>
    </section>
  </main>

  <footer class="footer">
    <p>Con amor, Jime & Rafa • 14/11/2025</p>
  </footer>

  <script>
    // Cuenta regresiva (AR)
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

    // Música
    const bgm = document.getElementById('bgm');
    const musicBtn = document.getElementById('musicToggle'); // ✅ id correcto
    let musicOn = false;
    musicBtn.addEventListener('click', async () => {
      try{
        if(!musicOn){ await bgm.play(); musicOn = true; musicBtn.style.borderColor='#7a8f69'; }
        else { bgm.pause(); musicOn = false; musicBtn.style.borderColor='#fff'; }
      }catch(e){}
    });

    // Scroll al RSVP
    document.getElementById('rsvpBtn').addEventListener('click', ()=>{
      document.getElementById('rsvp').scrollIntoView({behavior:'smooth'});
    });

    // Copiar alias
    document.querySelectorAll('.copy').forEach(btn=>{
      btn.addEventListener('click', async ()=>{
        try{ await navigator.clipboard.writeText(btn.dataset.copy);
          btn.textContent='Copiado ✓'; setTimeout(()=>btn.textContent='Copiar alias',2000);
        }catch(e){}
      });
    });

    // Envío por mail (mailto)
    const form = document.getElementById('rsvpForm');
    function compose(data){
      return 'Confirmación boda Jime & Rafa%0A%0A' +
             'Nombre: ' + data.nombre + '%0A' +
             'Asiste: ' + data.asiste + '%0A' +
             'Acompañantes: ' + data.acompanantes + '%0A' +
             'Mensaje: ' + (data.mensaje||'');
    }
    form.addEventListener('submit', (e)=>{
      e.preventDefault();
      const data = Object.fromEntries(new FormData(form).entries());
      const subject = encodeURIComponent('Boda Jime & Rafa');
      const body = compose(data);
      window.location.href = 'mailto:jimena.rocco@hotmail.com?subject='+subject+'&body='+body;
    });
  </script>
</body>
</html>
