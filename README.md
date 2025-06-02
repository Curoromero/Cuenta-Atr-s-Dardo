<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Cuenta Atrás Archivos Dardo</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <!-- Digital/Segment Font -->
  <link href="https://fonts.googleapis.com/css2?family=Share+Tech+Mono&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      min-height: 100vh;
      background: radial-gradient(circle at 60% 40%, #141e30 0%, #243b55 80%, #0a2239 100%);
      color: #fff;
      font-family: 'Share Tech Mono', monospace;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      overflow: hidden;
    }

    h1 {
      font-size: 3.2rem;
      letter-spacing: 0.08em;
      padding: 0.7em 1.2em;
      margin-bottom: 1.2rem;
      text-align: center;
      background: linear-gradient(90deg, #00ffd0, #0099ff, #f7971e, #ffd200, #00ffd0 90%);
      background-size: 200% 200%;
      animation: gradientMove 7s linear infinite;
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      filter: drop-shadow(0 0 24px #00f2fe76);
      border-radius: 16px;
    }
    .subtitle {
      font-size: 1.7rem;
      margin-bottom: 2rem;
      text-align: center;
      color: #ffd200;
      letter-spacing: 0.05em;
      text-shadow: 0 0 8px #0099ffaa;
      font-family: 'Montserrat', Arial, sans-serif;
      font-weight: bold;
      background: linear-gradient(90deg, #ffd200 0%, #00ffd0 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }
    .end-note {
      font-size: 1.1rem;
      margin-top: 2rem;
      color: #a6ffcb;
      letter-spacing: 0.03em;
      text-align: center;
      font-family: 'Montserrat', Arial, sans-serif;
      background: linear-gradient(90deg, #a6ffcb 0%, #ffd200 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      text-shadow: 0 0 6px #ffd20066;
    }

    @keyframes gradientMove {
      0%{background-position:0% 50%}
      50%{background-position:100% 50%}
      100%{background-position:0% 50%}
    }

    .clock-container {
      background: rgba(10, 25, 47, 0.88);
      border: 2.5px solid #32fff6;
      border-radius: 32px;
      box-shadow: 0 0 64px #00eaff44, 0 0 8px #fff5;
      padding: 2.5rem 3.5rem;
      display: flex;
      gap: 2.5rem;
      position: relative;
      z-index: 2;
    }

    .segment {
      display: flex;
      flex-direction: column;
      align-items: center;
      min-width: 80px;
    }

    .digit {
      font-size: 4.2rem;
      font-family: 'Share Tech Mono', monospace;
      color: #32fff6;
      background: linear-gradient(180deg, #00ffd0 0%, #0099ff 100%);
      box-shadow: 0 0 24px #00ffd0bb, 0 0 8px #fff2;
      border-radius: 10px;
      padding: 0.1em 0.3em;
      margin-bottom: 0.4em;
      text-shadow:
        0 0 12px #00ffd0,
        0 0 4px #00ffd0,
        0 0 2px #fff;
      transition: all 0.2s;
      letter-spacing: 0.1em;
      min-width: 1.2em;
      text-align: center;
      user-select: none;
    }

    .label {
      font-size: 1.1rem;
      color: #ffd200;
      letter-spacing: 0.04em;
      text-transform: uppercase;
      margin-top: -0.3em;
      font-family: 'Montserrat', Arial, sans-serif;
      text-shadow: 0 0 4px #ffd20099;
      user-select: none;
    }

    .colon {
      font-size: 4.2rem;
      color: #32fff6;
      margin: 0 0.2em;
      text-shadow: 0 0 16px #00ffd0;
      align-self: flex-end;
    }

    .neon-bar {
      width: 80vw;
      max-width: 720px;
      height: 4px;
      background: linear-gradient(90deg, #00ffd0 0%, #ffd200 100%);
      box-shadow: 0 0 32px #00ffd088, 0 0 16px #ffd20044;
      margin: 2.2rem 0 2.5rem 0;
      border-radius: 2px;
      opacity: 0.9;
    }

    @media (max-width: 700px) {
      h1 { font-size: 2rem; }
      .subtitle { font-size: 1.1rem;}
      .clock-container { padding: 1.2rem 0.2rem; gap: 1.1rem;}
      .digit, .colon { font-size: 2rem;}
      .segment {min-width: 40px;}
      .neon-bar {width: 98vw;}
      .end-note {font-size: 0.9rem;}
    }
  </style>
  <!-- For label font -->
  <link href="https://fonts.googleapis.com/css?family=Montserrat:700&display=swap" rel="stylesheet">
</head>
<body>
  <div class="neon-bar"></div>
  <h1>Cuenta Atrás Archivos Dardo</h1>
  <div class="subtitle">Cuenta atrás de 7 días</div>
  <div class="clock-container">
    <div class="segment">
      <span class="digit" id="days">00</span>
      <span class="label">DÍAS</span>
    </div>
    <span class="colon">:</span>
    <div class="segment">
      <span class="digit" id="hours">00</span>
      <span class="label">HORAS</span>
    </div>
    <span class="colon">:</span>
    <div class="segment">
      <span class="digit" id="minutes">00</span>
      <span class="label">MIN</span>
    </div>
    <span class="colon">:</span>
    <div class="segment">
      <span class="digit" id="seconds">00</span>
      <span class="label">SEG</span>
    </div>
  </div>
  <div class="end-note">Finaliza el 9 de junio de 2025</div>
  <div class="neon-bar"></div>
  <script>
    // Countdown to June 9, 2025 00:00:00 UTC
    const endDate = new Date(Date.UTC(2025, 5, 9, 0, 0, 0)); // Months are 0-indexed

    function pad(n) {
      return String(n).padStart(2, '0');
    }

    function updateCountdown() {
      const now = new Date();
      const diff = endDate - now;
      if (diff > 0) {
        const days = Math.floor(diff / (1000 * 60 * 60 * 24));
        const hours = Math.floor((diff / (1000 * 60 * 60)) % 24);
        const minutes = Math.floor((diff / (1000 * 60)) % 60);
        const seconds = Math.floor((diff / 1000) % 60);

        document.getElementById('days').textContent = pad(days);
        document.getElementById('hours').textContent = pad(hours);
        document.getElementById('minutes').textContent = pad(minutes);
        document.getElementById('seconds').textContent = pad(seconds);
      } else {
        document.getElementById('days').textContent = '00';
        document.getElementById('hours').textContent = '00';
        document.getElementById('minutes').textContent = '00';
        document.getElementById('seconds').textContent = '00';
        clearInterval(timer);
      }
    }

    updateCountdown();
    const timer = setInterval(updateCountdown, 1000);
  </script>
</body>
</html>
