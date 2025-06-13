<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Phishing Simulado</title>
  <style>
    body { background-color: #f9f9f9; font-family: 'Segoe UI', sans-serif; text-align: center; padding: 60px; }
    .card {
      background-color: white;
      padding: 40px;
      margin: auto;
      max-width: 600px;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    img { max-width: 120px; }
    h1 { color: #e74c3c; }
    p { font-size: 18px; color: #555; }
    .emoji { font-size: 48px; margin-top: 10px; }
  </style>
</head>
<body>
  <div class="card">
    <img src="https://katoki.coop/wp-content/uploads/2024/09/logo-katoki.png" alt="Logo Institucional">
    <h1>¡Oops! 😅</h1>
    <p><strong>Has sido víctima de un simulagro de phishing.</strong></p>
    <p>Pero tranquilo(a), este fue solo un ejercicio de concientización.</p>
    <div class="emoji">🧠🛡️</div>
    <p><em>Recuerda: nunca hagas clic en enlaces sospechosos, tampoco ingreses tus credenciales sin verificar la fuente.</em></p>
  </div>
  <script>
  (function() {
    const params = new URLSearchParams(window.location.search);
    const usuario = params.get("usuario") || "desconocido";

    const data = {
      usuario: usuario,
      navegador: navigator.userAgent,
      hora: new Date().toISOString()
    };

    fetch("https://script.google.com/macros/s/AKfycbwvLrWTIiVWZukRjtN0PaRu3-DncUGU5q1aO62oNFc/dev", {
      method: "POST",
      mode: "no-cors",
      headers: {
        "Content-Type": "application/json"
      },
      body: JSON.stringify(data)
    });
  })();
</script>
</body>
</html>
