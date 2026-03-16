<!DOCTYPE html><html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>La Velada del Campo 2</title>
<style>
body{margin:0;font-family:Arial,Helvetica,sans-serif;background:#111827;color:white}
header{background:linear-gradient(90deg,#1f2937,#4b5563);padding:50px;text-align:center}
h1{font-size:50px;margin:0;color:#fbbf24}
.subtitle{font-size:22px;margin-top:10px;color:#f3f4f6}
.container{max-width:1200px;margin:auto;padding:20px}
.section{background:#1f2937;padding:30px;margin-top:30px;border-radius:16px;box-shadow:0 5px 15px rgba(0,0,0,0.3)}
h2{color:#fbbf24}
button{background:#22c55e;border:none;padding:14px 20px;color:white;border-radius:10px;font-size:18px;cursor:pointer;transition:0.3s}
button:hover{opacity:0.85}
button.disabled{background:gray;cursor:not-allowed}
input{width:100%;padding:12px;margin-top:8px;margin-bottom:15px;border:none;border-radius:6px}
.success{display:none;background:#065f46;padding:15px;border-radius:10px;margin-top:10px;text-align:center}
</style>
</head>
<body><header>
<h1>🥊 La Velada del Campo 2</h1>
<div class="subtitle">⏰ Hora: <strong>AÚN POR DECIDIR</strong></div>
<p>Combates, fiesta, espectáculo y bebidas para todos.</p>
</header><div class="container"><div class="section">
<h2>📋 Inscripción Combates</h2>
<p>Si quieres participar en los combates de boxeo, rellena tu inscripción:</p>
<button onclick="showForm()">Inscribirte</button>
<div id="contract" style="display:none; margin-top:15px">
<form onsubmit="submitForm(event)">
<label>Nombre</label>
<input required>
<label>Altura (cm)</label>
<input type="number" required>
<label>Peso (kg)</label>
<input type="number" required>
<label>Gmail</label>
<input type="email" required placeholder="tuemail@gmail.com">
<label>Firma (nombre completo)</label>
<input required>
<button type="submit">Enviar inscripción</button>
</form>
<div id="successMessage" class="success">Leeremos tu solicitud, ¡gracias por querer participar en este evento!</div>
</div>
</div><div class="section">
<h2>🎉 ¿Te interesa venir?</h2>
<p>Pulsa el botón si quieres asistir a la fiesta:</p>
<button id="interestBtn" onclick="interest()">Me interesa la fiesta</button>
<div class="counter">Personas interesadas: <span id="count">0</span></div>
</div><div class="section">
<h2>Sobre el evento</h2>
<p>La Velada del Campo 2 será una noche inolvidable con combates emocionantes, fiesta, espectáculo y bebidas. Muy pronto anunciaremos la hora y más sorpresas.</p>
</div><script>
let count=0;
let interestClicked=false;

function showForm(){
 document.getElementById('contract').style.display='block';
}

function submitForm(e){
 e.preventDefault();
 document.getElementById('successMessage').style.display='block';
 // Nota: Esto NO enviará el Gmail a tu correo automáticamente. Para recibir emails, necesitas conectar un backend o servicio de correo.
}

function interest(){
 if(!interestClicked){
   count++;
   document.getElementById('count').innerText=count;
   let btn=document.getElementById('interestBtn');
   btn.classList.add('disabled');
   btn.disabled=true;
   interestClicked=true;
 }
}
</script></body>
</html>
