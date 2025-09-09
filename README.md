# viesptr.github.io
<!doctype html>
<html lang="de">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Meine Karte</title>
  <meta name="description" content="Eigene Google-MyMaps-Ansicht als eingebettete Karte." />
  <style>
    :root { color-scheme: light dark; }
    body {
      margin: 0;
      font-family: system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif;
      line-height: 1.5;
      display: grid;
      min-height: 100dvh;
      grid-template-rows: auto 1fr auto;
      background: #f7f7f9;
    }
    header, footer {
      padding: 1rem clamp(1rem, 4vw, 2rem);
      background: white;
      border-block: 1px solid #e5e5e9;
    }
    main {
      padding: clamp(1rem, 4vw, 2rem);
      display: grid;
      gap: 1rem;
    }
    .map-wrap {
      /* responsive 16:9 */
      position: relative;
      width: 100%;
      max-width: 1200px;
      margin-inline: auto;
      aspect-ratio: 16 / 9;
      border-radius: 12px;
      overflow: hidden;
      box-shadow: 0 6px 24px rgba(0,0,0,.08);
      background: #ddd;
    }
    .map-wrap iframe {
      position: absolute;
      inset: 0;
      width: 100%;
      height: 100%;
      border: 0;
    }
    .fallback {
      text-align: center;
      font-size: .95rem;
    }
    a.btn {
      display: inline-block;
      margin-top: .5rem;
      padding: .6rem .9rem;
      border-radius: 10px;
      background: #1a73e8;
      color: #fff;
      text-decoration: none;
    }
    a.btn:hover { filter: brightness(1.05); }
  </style>
</head>
<body>
  <header>
    <h1>Eigene Google-Karte</h1>
    <p>Die Karte unten ist per iFrame eingebettet und passt sich der Bildschirmgröße an.</p>
  </header>

  <main>
    <div class="map-wrap" role="region" aria-label="Google-Map">
      <iframe
        src="https://www.google.com/maps/d/embed?mid=1RrZXlYOUo_MJFEpHSYOBddpmwFpFRWs&ehbc=2E312F"
        loading="lazy"
        referrerpolicy="no-referrer-when-downgrade"
        allowfullscreen>
      </iframe>
    </div>

    <p class="fallback">
      Falls die Karte nicht lädt, öffne sie direkt:
      <a class="btn" href="https://www.google.com/maps/d/viewer?mid=1RrZXlYOUo_MJFEpHSYOBddpmwFpFRWs&ll=0%2C0&z=2" target="_blank" rel="noopener">Karte in neuem Tab öffnen</a>
    </p>
  </main>

  <footer>
    <small>&copy; <span id="year"></span> – Eingebettete Google-MyMaps-Ansicht</small>
    <script>document.getElementById('year').textContent = new Date().getFullYear();</script>
  </footer>
</body>
</html>
