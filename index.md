<!doctype html>
.controls{display:flex;gap:8px;align-items:center}
.mobile-toggle{display:none}
.hero{margin:22px 0}
.hero h1{font-size:32px;margin:0}
.lead{color:var(--muted);margin-top:8px}
.grid{display:grid;grid-template-columns:repeat(3,1fr);gap:14px;margin-top:14px}
.card{background:var(--card);padding:14px;border-radius:12px;border:1px solid rgba(255,255,255,0.03)}
img{max-width:100%;border-radius:10px}
footer{margin:28px 0;text-align:center;color:var(--muted)}
/* responsive */
@media(max-width:920px){.grid{grid-template-columns:repeat(2,1fr)}.mobile-toggle{display:inline-flex}.desktop{display:none}}
@media(max-width:560px){.grid{grid-template-columns:1fr}.hero h1{font-size:22px}}
</style>
</head>
<body>
<div class="container">
<header>
<div class="brand"><div class="logo">PSR</div><div><strong>iamPSR</strong><div style="font-size:13px;color:var(--muted)">Rides • Explains • Shop</div></div></div>
<nav class="desktop" aria-label="Primary">
<a href="/rides/leh-ladakh.html">PSR Rides</a>
<a href="/explains/gyroscopic.html">PSR Explains</a>
<a href="/shop.html">Shop</a>
<a href="/about.html">About</a>
<a href="/contact.html">Contact</a>
</nav>
<div class="controls">
<button id="themeToggle" aria-label="Toggle theme">🌓</button>
<button class="mobile-toggle" id="mobileToggle">Menu</button>
</div>
</header>

<main>
<section class="hero">
<h1>iamPSR — for riders who want depth</h1>
<p class="lead">Rides: in-depth reports, reviews and routes. Explains: short curiosity-driven science and how-it-works essays. Shop: curated experiment kits & gear.</p>
<div style="margin-top:12px"><a class="card" href="/rides/leh-ladakh.html" style="display:inline-block;padding:10px 14px;background:var(--accent);color:#021;border-radius:8px;font-weight:700">Featured Ride — Leh ↔ Ladakh</a></div>
</section>

<section>
<h2>PSR Rides (Preview)</h2>
<div class="grid">
<div class="card"><img src="https://via.placeholder.com/800x480?text=Leh+Ride" alt="Leh Ride"><h3>Leh ↔ Ladakh — Full guide</h3><p style="color:var(--muted)">Long-form route plan + permits & fuel notes.</p></div>
<div class="card"><img src="https://via.placeholder.com/800x480?text=Coastal+Ride" alt="Coastal Ride"><h3>Hyderabad → Kolkata planning</h3><p style="color:var(--muted)">How to do long transfers safely.</p></div>
<div class="card"><img src="https://via.placeholder.com/800x480?text=Weekend+Loop" alt="Weekend Loop"><h3>Weekend Loops</h3><p style="color:var(--muted)">Short ride ideas to test setup.</p></div>
</div>
</section>

<section style="margin-top:18px">
<h2>PSR Explains (Preview)</h2>
<div class="grid" style="grid-template-columns:repeat(2,1fr);">
<div class="card"><h3>Gyroscopic stability</h3><p style="color:var(--muted)">Short explainers connecting physics to riding.</p></div>
<div class="card"><h3>Helmet aerodynamics</h3><p style="color:var(--muted)">Why shape and vents matter.</p></div>
</div>
</section>
</main>

<footer>
<div style="color:var(--muted)">© <span id="year"></span> iamPSR — Built for riders</div>
</footer>
</div>

<script>
document.getElementById('year').textContent = new Date().getFullYear();
(function(){const t=document.getElementById('themeToggle');const pref=localStorage.getItem('iampsr:theme');if(pref==='light')document.documentElement.classList.add('light-mode');t.addEventListener('click',()=>{document.documentElement.classList.toggle('light-mode');localStorage.setItem('iampsr:theme', document.documentElement.classList.contains('light-mode')?'light':'dark')});})();
</script>
</body>
</html>
