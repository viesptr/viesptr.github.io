# viesptr.github.io
<!doctype html>
<html lang="de">
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
