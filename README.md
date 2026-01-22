# Tnk-inovation
TheNewK
<!DOCTYPE html>
<html lang="ro">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>TNK Innovation – Idei de Marketing</title>

<style>
body { margin:0;font-family:Arial, Helvetica, sans-serif;background:#0f172a;color:#e5e7eb; }
header { background:linear-gradient(135deg, #6366f1, #22d3ee); padding:60px 20px; text-align:center; color:white; }
section { padding:60px 20px; max-width:1100px; margin:auto; }
h2 { color:#38bdf8; text-align:center; margin-bottom:30px; }
.cards { display:grid; grid-template-columns:repeat(auto-fit, minmax(260px, 1fr)); gap:20px; }
.card { background:#020617; border-radius:16px; padding:25px; box-shadow:0 10px 25px rgba(0,0,0,0.4); text-align:center; }
.highlight { border:2px solid #38bdf8; transform:scale(1.05); }
.price { font-size:36px; color:#38bdf8; margin:20px 0; }
ul { list-style:none; padding:0; }
ul li { margin:10px 0; }
.btn { display:block; margin:12px auto 0; padding:14px 26px; border-radius:30px; text-decoration:none; font-weight:bold; width:85%; }
.revolut { background:#6366f1; color:white; }
.confirm { background:#38bdf8; color:#020617; cursor:pointer; border:none; }
.whatsapp { background:#22c55e; color:#020617; }
footer { background:#020617; padding:30px; text-align:center; font-size:14px; color:#9ca3af; }
</style>
</head>

<body>

<header>
<h1>TNK Innovation</h1>
<p>Plătești simplu prin Revolut. Confirmi instant pe WhatsApp. PDF automat.</p>
</header>

<section>
<h2>Pachete de preț</h2>
<div class="cards">

<!-- BASIC -->
<div class="card">
<h3>Basic</h3>
<div class="price">99€</div>
<ul>
<li>✔ 5 idei marketing</li>
<li>✔ Strategie generală</li>
<li>✔ Livrare PDF</li>
</ul>
<a class="btn revolut" href="https://revolut.me/irinel19tnk" target="_blank">Plătește cu Revolut</a>
<button class="btn confirm" onclick="generatePDF('Basic','99€')">Descarcă PDF confirmare</button>
<a class="btn whatsapp" href="https://wa.me/40746821167?text=Am%20plătit%20pachetul%20Basic%20–%2099€" target="_blank">Comandă pe WhatsApp</a>
</div>

<!-- PRO -->
<div class="card highlight">
<h3>Pro</h3>
<div class="price">249€</div>
<ul>
<li>✔ 15 idei personalizate</li>
<li>✔ Strategie completă</li>
<li>✔ Social Media inclus</li>
<li>✔ Suport 7 zile</li>
</ul>
<a class="btn revolut" href="https://revolut.me/irinel19tnk" target="_blank">Plătește cu Revolut</a>
<button class="btn confirm" onclick="generatePDF('Pro','249€')">Descarcă PDF confirmare</button>
<a class="btn whatsapp" href="https://wa.me/40746821167?text=Am%20plătit%20pachetul%20Pro%20–%20249€" target="_blank">Comandă pe WhatsApp</a>
</div>

<!-- PREMIUM -->
<div class="card">
<h3>Premium</h3>
<div class="price">499€</div>
<ul>
<li>✔ Strategie full brand</li>
<li>✔ Funnel vânzări</li>
<li>✔ Consultanță 1:1</li>
<li>✔ Suport 30 zile</li>
</ul>
<a class="btn revolut" href="https://revolut.me/irinel19tnk" target="_blank">Plătește cu Revolut</a>
<button class="btn confirm" onclick="generatePDF('Premium','499€')">Descarcă PDF confirmare</button>
<a class="btn whatsapp" href="https://wa.me/40746821167?text=Am%20plătit%20pachetul%20Premium%20–%20499€" target="_blank">Comandă pe WhatsApp</a>
</div>

</div>
</section>

<section>
<h2>Colaborare WhatsApp</h2>
<div class="card">
<p>Colaborări, pachete personalizate sau întrebări? Scrie direct pe WhatsApp.</p>
<a class="btn whatsapp" href="https://wa.me/40746821167?text=Salut,%20vreau%20o%20colaborare" target="_blank">📲 Discută pe WhatsApp</a>
</div>
</section>

<footer>
© 2026 TNK Innovation · Persoană fizică · Plată Revolut
</footer>

<script>
function generatePDF(pachet, suma){
  const content = `CONFIRMARE PLATĂ – TNK INNOVATION\n\nPachet: ${pachet}\nSuma: ${suma}\nMonedă: EUR\nData: ${new Date().toLocaleDateString('ro-RO')}\n\nPlata reprezintă achiziția unui serviciu digital.\nFurnizor: TNK Innovation\nTip: Persoană Fizică\n\nMulțumim pentru colaborare!`;
  const blob = new Blob([content],{type:"application/pdf"});
  const url = URL.createObjectURL(blob);
  const a = document.createElement("a");
  a.href=url;
  a.download=`Confirmare_${pachet}.pdf`;
  a.click();
  URL.revokeObjectURL(url);
}
</script>

</body>
</html>
