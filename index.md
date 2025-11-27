<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>iamPSR — Rides • Explains • Shop</title>
  <meta name="description" content="iamPSR — PSR Rides, PSR Explains, shop, about and contact. Motorcycle rides, guides and curated gear.">
  <link rel="icon" href="/favicon.ico">
  <style>
    :root{
      --bg:#0f1724; /* deep slate */
      --card:#0b1220;
      --accent:#ff6a00; /* warm orange */
      --muted:#9aa4b2;
      --glass: rgba(255,255,255,0.04);
      --radius:12px;
      color-scheme: dark;
      font-family: Inter, system-ui, -apple-system, Segoe UI, Roboto, 'Helvetica Neue', Arial;
    }

    /* Light mode variables (toggled with .light-mode on <html>) */
    html.light-mode{
      --bg: #f6f7fb;
      --card: #ffffff;
      --accent: #ff6a00;
      --muted: #4b5563;
      --glass: rgba(2,6,23,0.04);
      color-scheme: light;
    }

    *{box-sizing:border-box}
    html,body{height:100%;margin:0;background:linear-gradient(180deg,var(--bg),#071021);color:var(--text,#e6eef6)}
    /* ensure readable text color in light mode */
    html.light-mode, html.light-mode body { --text:#071022; }

    a{color:var(--accent);text-decoration:none}
    .container{max-width:1150px;margin:0 auto;padding:28px}

    /* HEADER */
    header.main-header{display:flex;align-items:center;justify-content:space-between;gap:12px}
    .brand{display:flex;align-items:center;gap:12px}
    .logo{width:48px;height:48px;border-radius:10px;background:linear-gradient(135deg,var(--accent),#ff9500);display:flex;align-items:center;justify-content:center;font-weight:700;color:#021;box-shadow:0 6px 18px rgba(0,0,0,0.06)}
    .site-title{font-size:18px;font-weight:700;letter-spacing:0.2px}
    nav.desktop{display:flex;gap:12px;align-items:center}
    nav.desktop a{padding:8px 12px;border-radius:10px;font-weight:600}
    nav.desktop a:hover{background:var(--glass)}

    /* Theme toggle + mobile */
    .controls{display:flex;gap:8px;align-items:center}
    .icon-btn{background:transparent;border:1px solid rgba(0,0,0,0.06);padding:8px;border-radius:10px;cursor:pointer}
    .mobile-toggle{display:none;background:transparent;border:1px solid rgba(255,255,255,0.06);padding:8px;border-radius:10px}
    @media (max-width:820px){
      nav.desktop{display:none}
      .mobile-toggle{display:inline-flex}
    }

    /* mobile nav overlay */
    .mobile-nav-panel{position:fixed;inset:0;background:linear-gradient(180deg,rgba(2,6,23,0.9),rgba(2,6,23,0.96));backdrop-filter:blur(6px);display:none;z-index:60;padding:28px}
    .mobile-nav-panel.open{display:block}
    .mobile-nav-panel nav{display:flex;flex-direction:column;gap:12px}
    .mobile-nav-panel a{font-size:18px;padding:12px;border-radius:10px}

    /* HERO */
    .hero{display:grid;grid-template-columns:1fr 420px;gap:24px;align-items:center;margin:28px 0}
    .hero-card{background:linear-gradient(180deg,rgba(255,255,255,0.02),transparent);padding:28px;border-radius:16px;border:1px solid rgba(255,255,255,0.04)}
    .hero h1{margin:0;font-size:34px}
    .lead{color:var(--muted);margin-top:10px}
    .cta{display:flex;gap:12px;margin-top:18px}
    .btn{background:var(--accent);color:#021;padding:10px 14px;border-radius:10px;font-weight:700;border:none;cursor:pointer}
    .btn.ghost{background:transparent;border:1px solid rgba(255,255,255,0.06);color:inherit}

    /* cards & lists */
    section{margin:28px 0}
    .grid{display:grid;grid-template-columns:repeat(3,1fr);gap:16px}
    .card{background:var(--card);padding:16px;border-radius:12px;border:1px solid rgba(255,255,255,0.03)}
    .card h3{margin:6px 0}
    .muted{color:var(--muted);font-size:14px}

    /* shop grid */
    .shop-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:14px}
    .product{display:flex;flex-direction:column;gap:10px}
    .product img{width:100%;aspect-ratio:4/3;object-fit:cover;border-radius:8px}

    /* footer */
    footer{padding:20px 0;color:var(--muted);text-align:center}

    /* responsive */
    @media (max-width:1150px){.hero{grid-template-columns:1fr 360px}}
    @media (max-width:920px){.grid{grid-template-columns:repeat(2,1fr)}.shop-grid{grid-template-columns:repeat(2,1fr)}.hero{grid-template-columns:1fr}}
    @media (max-width:560px){
      .grid{grid-template-columns:1fr}.shop-grid{grid-template-columns:1fr}.container{padding:18px}
      .hero{gap:14px}
      .hero-card{padding:18px}
      .hero h1{font-size:26px}
      .cta{flex-direction:column}
      .btn{width:100%;padding:12px}
      .logo{width:44px;height:44px}
    }

    /* small helpers */
    .pill{display:inline-block;padding:6px 10px;border-radius:999px;background:rgba(255,255,255,0.03);font-weight:700}
    .meta{font-size:13px;color:var(--muted)}

    /* contact form styles */
    form.contact{display:grid;gap:10px}
    input[type=text],input[type=email],textarea{background:transparent;border:1px solid rgba(255,255,255,0.05);padding:10px;border-radius:8px;color:inherit}
    textarea{min-height:110px}
    .small{font-size:13px;color:var(--muted)}

    /* accessible focus */
    a:focus,button:focus,input:focus,textarea:focus{outline:3px solid rgba(255,106,0,0.16);outline-offset:3px}

    /* details summary small animation */
    details summary{cursor:pointer}
    details[open] > *{animation:fadeIn 240ms ease}
    @keyframes fadeIn{from{opacity:0;transform:translateY(-6px)}to{opacity:1;transform:none}}
  </style>
</head>
<body>
  <div class="container">
    <header class="main-header">
      <div class="brand">
        <div class="logo">PSR</div>
        <div>
          <div class="site-title">iamPSR</div>
          <div class="muted">Rides • Explains • Shop</div>
        </div>
      </div>

      <nav class="desktop" aria-label="Primary">
        <a href="#rides">PSR Rides</a>
        <a href="#explains">PSR Explains</a>
        <a href="#shop">Shop</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
      </nav>

      <div class="controls">
        <button id="themeToggle" class="icon-btn" aria-label="Toggle theme">🌓</button>
        <button class="mobile-toggle" id="mobileToggle" aria-expanded="false" aria-controls="mobileNav">Menu</button>
      </div>
    </header>

    <!-- mobile nav overlay -->
    <div id="mobileNav" class="mobile-nav-panel" aria-hidden="true">
      <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:18px">
        <div style="display:flex;gap:12px;align-items:center"><div class="logo">PSR</div><div style="font-weight:700">iamPSR</div></div>
        <div><button id="mobileClose" class="icon-btn" aria-label="Close menu">Close</button></div>
      </div>
      <nav>
        <a href="#rides">PSR Rides</a>
        <a href="#explains">PSR Explains</a>
        <a href="#shop">Shop</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
      </nav>
      <div style="margin-top:18px">
        <h4 style="margin:6px 0">Subscribe</h4>
        <p class="muted">Join the mailing list for ride alerts and gear drops.</p>
        <form action="#" onsubmit="alert('Replace form action with your provider');return false;" style="display:flex;flex-direction:column;gap:8px;margin-top:8px">
          <input type="email" placeholder="you@domain.com" required style="padding:10px;border-radius:8px;background:transparent;border:1px solid rgba(255,255,255,0.04);color:inherit">
          <div style="display:flex;gap:8px;align-items:center">
            <button class="btn" type="submit">Subscribe</button>
            <div class="small">Or email <a href="mailto:hello@iampsr.com">hello@iampsr.com</a></div>
          </div>
        </form>
      </div>
    </div>

    <!-- mobile nav panel -->
    <div id="mobileNav" style="display:none;margin-top:12px">
      <nav style="display:flex;flex-direction:column;gap:8px">
        <a href="#rides">PSR Rides</a>
        <a href="#explains">PSR Explains</a>
        <a href="#shop">Shop</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
      </nav>
    </div>

    <!-- HERO -->
    <section class="hero">
      <div class="hero-card" style="grid-column:1/-1">
        <h1>iamPSR — for riders who want depth</h1>
        <p class="lead">Long-form ride reports, curiosity-driven explainers about science and the universe, practical how-tos, and a curated shop for riders. PSR Explains breaks down how things work — from helmet tech to the physics of cornering — in clear, visual, and experiment-friendly essays.</p>
        <div class="cta">
          <a class="btn" href="#rides">Explore Rides</a>
          <a class="btn ghost" href="#explains">Read Explains</a>
        </div>

        <div style="margin-top:18px;display:flex;gap:12px;align-items:center">
          <div class="pill">New: Lachen → Lachung comparison</div>
          <div class="meta">Updated Nov 2025</div>
        </div>
      </div>

      <!-- Collapsible Quick Links placed below the hero so main section can use full width -->
      <div style="grid-column:1/-1;margin-top:18px">
        <details style="background:var(--card);padding:14px;border-radius:12px;border:1px solid rgba(255,255,255,0.04);">
          <summary style="font-weight:700;cursor:pointer;padding:8px 10px;border-radius:8px;list-style:none;">Quick Links & Subscribe</summary>
          <div style="display:grid;grid-template-columns:1fr 360px;gap:12px;margin-top:12px;align-items:start">
            <div>
              <h4 style="margin:6px 0">Quick Links</h4>
              <ul class="muted" style="padding-left:18px;margin:8px 0;line-height:1.6">
                <li><a href="#rides">Latest Ride: Leh ↔️ Ladakh (detailed comparison)</a></li>
                <li><a href="#explains">How to get permits (avoid travel agents)</a></li>
                <li><a href="#shop">Shop: PSR Essentials</a></li>
              </ul>
            </div>

            <div style="min-width:0">
              <h4 style="margin:6px 0">Subscribe</h4>
              <p class="muted">Join the mailing list for ride alerts and gear drops.</p>
              <form action="#" onsubmit="alert('Replace form action with your provider');return false;" style="display:flex;flex-direction:column;gap:8px;margin-top:8px">
                <input type="email" placeholder="you@domain.com" required style="padding:10px;border-radius:8px;background:transparent;border:1px solid rgba(255,255,255,0.04);color:inherit">
                <div style="display:flex;gap:8px;align-items:center">
                  <button class="btn" type="submit">Subscribe</button>
                  <div class="small">Or email <a href="mailto:hello@iampsr.com">hello@iampsr.com</a></div>
                </div>
              </form>
            </div>
          </div>
        </details>
      </div>
    </section>

    <!-- PSR RIDES -->
    <section id="rides">
      <h2>PSR Rides — Routes, Reviews & Ridecraft</h2>
      <p class="muted">In-depth ride reports, long & short routes, bike reviews, route planning, permits and real-world tips — everything a rider needs to plan and improve rides.</p>

      <!-- Featured ride (full width) -->
      <article class="card" style="margin-top:12px;display:block;">
        <img src="https://via.placeholder.com/1400x700?text=Featured+Ride+-+Leh+Ladakh" alt="Featured Leh Ladakh ride" class="hero-visual">
        <div style="display:flex;gap:14px;align-items:flex-start;margin-top:12px;flex-wrap:wrap">
          <div style="flex:1;min-width:220px">
            <h3 style="margin:6px 0">Leh ↔️ Ladakh — Complete Rider's Guide</h3>
            <p class="muted">A comprehensive guide combining long-ride strategy, permit notes, fuel planning, altitude tips and photo spots — written from multiple rides on the route.</p>
            <div style="display:flex;gap:8px;margin-top:10px"><a class="btn" href="#">Read Full Report</a><a class="btn ghost" href="#contact">Ask about this ride</a></div>
          </div>

          <div style="width:320px" class="glass-quickfacts">
            <h4 style="margin:4px 0">Quick Facts</h4>
            <ul class="muted" style="padding-left:16px;margin:8px 0;line-height:1.5">
              <li>Distance: ~1,200 km round trip</li>
              <li>Best time: Jun–Sep</li>
              <li>Permits: Inner Line Permit — local guesthouses help (avoid agents)</li>
              <li>Fuel: Carry a reserve for remote stretches</li>
            </ul>
          </div>
        </div>
      </article>

      <!-- Ride cards grid (emphasised) -->
      <div class="grid" style="margin-top:14px;grid-template-columns:repeat(3,1fr);">
        <article class="card">
          <img src="https://via.placeholder.com/800x480?text=Hill+Loop" alt="Hill Loop" style="width:100%;border-radius:8px;object-fit:cover;aspect-ratio:16/9">
          <h3>Lachen &amp; Lachung — Mountain Essentials</h3>
          <p class="muted">Short practical notes on acclimatisation, key passes and where to stop for the best views.</p>
        </article>

        <article class="card">
          <img src="https://via.placeholder.com/800x480?text=Coastal+Ride" alt="Coastal Ride" style="width:100%;border-radius:8px;object-fit:cover;aspect-ratio:16/9">
          <h3>Hyderabad → Kolkata — Planning a Multi-day Point-to-Point</h3>
          <p class="muted">How to split days, plan fuel stops, and manage fatigue on long transfers.</p>
        </article>

        <article class="card">
          <img src="https://via.placeholder.com/800x480?text=Short+Weekend" alt="Weekend Ride" style="width:100%;border-radius:8px;object-fit:cover;aspect-ratio:16/9">
          <h3>Weekend Loops — Quick Ride Ideas</h3>
          <p class="muted">A collection of short loop rides ideal for testing bike setup and camera positions.</p>
        </article>
      </div>
    </section>

    <!-- PSR EXPLAINS -->

    <!-- VISUAL EXPLAINER TEMPLATE (new) -->
    <section id="explains-template" style="margin-top:40px">
      <h2>PSR Explains — Visual Explainer Template</h2>
      <div class="card" style="margin-top:12px">
        <h3>Template Structure</h3>
        <p class="muted">Use this block when creating future PSR Explains posts. It keeps your science & universe explainers consistent, visual and easy to share.</p>

        <ul class="muted" style="margin:12px 0 0 18px;line-height:1.6">
          <li><strong>Hero Visual:</strong> A simple diagram or image representing the concept (e.g., how gyroscopic forces keep a motorcycle stable).</li>
          <li><strong>The Curiosity Hook:</strong> A short 2–3 line punchy question that sparks interest.</li>
          <li><strong>How It Works:</strong> A step-by-step breakdown in plain English.</li>
          <li><strong>The Science:</strong> Use real physics, astronomy, or engineering principles — but simplified.</li>
          <li><strong>Real Ride Connection:</strong> Show how the science appears in real riding (cornering, wind behaviour, braking forces).</li>
          <li><strong>Try-It-Yourself Experiment:</strong> A safe, small experiment readers can test at home.</li>
          <li><strong>Visual Diagram:</strong> One simple labelled image for clarity.</li>
        </ul>
      </div>
    </section>
    <section id="explains">
      <h2>PSR Explains — Curiosity & How Things Work</h2>
      <p class="muted">Short, curiosity-led explainers connecting science and everyday ridecraft. Clear visuals, a short experiment, and practical takeaways — designed to be concise and easy to read.</p>

      <div class="grid" style="margin-top:12px;grid-template-columns:repeat(2,1fr);gap:14px">
        <article class="card">
          <h3>How Gyroscopic Forces Help Stability</h3>
          <p class="muted">A short breakdown of gyroscopic precession and why tyres and speed affect balance — includes a small at-home demo you can try.</p>
          <div style="margin-top:8px"><a class="btn" href="#">Read</a></div>
        </article>

        <article class="card">
          <h3>Helmet Aerodynamics — Noise & Comfort</h3>
          <p class="muted">Quick notes on shell shapes, ventilation and how small design changes reduce buffeting on long rides.</p>
          <div style="margin-top:8px"><a class="btn" href="#">Read</a></div>
        </article>
      </div>
    </section>

    <!-- PSR EXPLAINS SUBPAGE TEMPLATE (new) -->
    <section id="explains-subpage-template" style="margin-top:40px">
      <h2>PSR Explains — Long‑Form Page Template</h2>
      <div class="card" style="margin-top:12px">
        <p class="muted">This is the layout to use when you create full standalone PSR Explains articles (science, universe, tech, how things work). Paste this into a new HTML file like <code>explains-gyroscopic.html</code>.</p>

        <pre style="white-space:pre-wrap;font-size:13px;background:rgba(255,255,255,0.03);padding:14px;border-radius:10px;border:1px solid rgba(255,255,255,0.05);overflow:auto">&lt;section class="explainer-hero"&gt;
  &lt;h1&gt;TITLE OF THE EXPLAINER&lt;/h1&gt;
  &lt;p&gt;A curiosity hook about the science / universe concept.&lt;/p&gt;
&lt;/section&gt;

&lt;section class="explainer-body"&gt;
  &lt;h2&gt;How It Works&lt;/h2&gt;
  &lt;p&gt;Break it down step by step.&lt;/p&gt;

  &lt;h2&gt;The Science Behind It&lt;/h2&gt;
  &lt;p&gt;Physics, astronomy or engineering explained simply.&lt;/p&gt;

  &lt;h2&gt;Real Ride Connection&lt;/h2&gt;
  &lt;p&gt;Explain how this principle appears during riding.&lt;/p&gt;

  &lt;h2&gt;Try It Yourself Experiment&lt;/h2&gt;
  &lt;ul&gt;
    &lt;li&gt;List of simple safe experiments&lt;/li&gt;
  &lt;/ul&gt;

  &lt;h2&gt;Visual Diagram&lt;/h2&gt;
  &lt;img src="diagram.jpg" alt="Concept diagram" style="width:100%;border-radius:10px;aspect-ratio:16/9;object-fit:cover"&gt;
&lt;/section&gt;</pre>
      </div>
    </section>

    <!-- SHOP -->
    <section id="shop">
      <h2>Shop — PSR Essentials</h2>
      <p class="muted">Curated items I use and recommend. Link to your affiliate or Shopify store from each product card.</p>

      <div class="shop-grid" style="margin-top:12px">

        <!-- NEW: Experiment Kit Card -->
        <div class="product card">
          <img src="https://via.placeholder.com/600x400?text=Experiment+Kit" alt="Experiment Kit">
          <h4>PSR Experiment Kit</h4>
          <div class="muted">For PSR Explains: gyroscope demos, airflow tests, light experiments. Perfect for science content & at‑home demonstrations.</div>
          <div style="margin-top:8px;display:flex;gap:8px"><a class="btn" href="#">View</a><a class="btn ghost" href="#">Buy</a></div>
        </div>

        <!-- existing cards -->
         style="margin-top:12px">
        <div class="product card">
          <img src="https://via.placeholder.com/600x400?text=PSR+Jacket" alt="PSR Jacket">
          <h4>PSR Riding Jacket</h4>
          <div class="muted">From ₹7,999 — Durable, ventilated, and crash-tested</div>
          <div style="margin-top:8px;display:flex;gap:8px"><a class="btn" href="#">View</a><a class="btn ghost" href="#">Buy</a></div>
        </div>

        <div class="product card">
          <img src="https://via.placeholder.com/600x400?text=Helmet" alt="Helmet">
          <h4>PSR Helmet</h4>
          <div class="muted">Lightweight full-face — camera mount friendly</div>
        </div>

        <div class="product card">
          <img src="https://via.placeholder.com/600x400?text=Toolkit" alt="Toolkit">
          <h4>PSR Toolkit</h4>
          <div class="muted">Compact multi-tool & tyre repair kit</div>
        </div>
      </div>
    </section>

    <!-- ABOUT -->
    <section id="about">
      <h2>About — Prem Singh (iamPSR)</h2>
      <p class="muted">I ride, test, and write. I share real ride experience, technical explainers, and curated gear — straight from the road.</p>

      <div class="grid" style="margin-top:12px">
        <div class="card">
          <h3>My approach</h3>
          <p class="muted">Honest, experience-driven content. I prioritise safety, practical tips, and useful templates for riders who want to improve their craft.</p>
        </div>

        <div class="card">
          <h3>Media & collaborations</h3>
          <p class="muted">If you're a brand or publisher, email me at <a href="mailto:hello@iampsr.com">hello@iampsr.com</a> — include brief details and budget.</p>
        </div>

        <div class="card">
          <h3>Tech stack</h3>
          <p class="muted">Static site — ready for GitHub Pages, Netlify or Vercel. No build step required for this template.</p>
        </div>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact">
      <h2>Contact</h2>
      <p class="muted">Questions, collaborations, or ride invites — drop a message.</p>

      <div style="display:grid;grid-template-columns:1fr 360px;gap:16px;margin-top:12px">
        <div class="card">
          <form class="contact" action="https://formspree.io/f/your-form-id" method="POST">
            <!-- Replace the action URL above with your Formspree / Netlify Forms endpoint or use a serverless function -->
            <label class="small">Name<input type="text" name="name" required></label>
            <label class="small">Email<input type="email" name="email" required></label>
            <label class="small">Message<textarea name="message" required></textarea></label>
            <div style="display:flex;gap:8px;align-items:center">
              <button class="btn" type="submit">Send</button>
              <div class="small">Or email <a href="mailto:hello@iampsr.com">hello@iampsr.com</a></div>
            </div>
          </form>
        </div>

        <aside class="card">
          <h4>Social</h4>
          <p class="muted">YouTube • Instagram • Threads • X</p>
          <h4 style="margin-top:12px">Location</h4>
          <p class="muted">Based in India — available for collaborations worldwide</p>
        </aside>
      </div>
    </section>

    <footer>
      <div class="muted">© <span id="year"></span> iamPSR — Built with ❤️ for riders</div>
    </footer>
  </div>

  <script>
    // theme handling (persisted)
    (function(){
      const themeToggle = document.getElementById('themeToggle');
      const prefersDark = window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches;
      const saved = localStorage.getItem('iampsr:theme');
      function applyTheme(t){
        if(t === 'light') document.documentElement.classList.add('light-mode');
        else document.documentElement.classList.remove('light-mode');
        themeToggle.textContent = (t === 'light') ? '🌞' : '🌙';
      }
      let theme = saved || (prefersDark ? 'dark' : 'light');
      applyTheme(theme);
      themeToggle.addEventListener('click', ()=>{
        theme = (document.documentElement.classList.contains('light-mode')) ? 'dark' : 'light';
        localStorage.setItem('iampsr:theme', theme);
        applyTheme(theme);
      });
    })();

    // mobile nav handling
    (function(){
      const mobileToggle = document.getElementById('mobileToggle');
      const mobileNav = document.getElementById('mobileNav');
      const mobileClose = document.getElementById('mobileClose');
      function openNav(){ mobileNav.classList.add('open'); mobileNav.setAttribute('aria-hidden','false'); mobileToggle.setAttribute('aria-expanded','true'); document.body.style.overflow='hidden'; }
      function closeNav(){ mobileNav.classList.remove('open'); mobileNav.setAttribute('aria-hidden','true'); mobileToggle.setAttribute('aria-expanded','false'); document.body.style.overflow=''; }
      mobileToggle.addEventListener('click', ()=>{ mobileNav.classList.contains('open') ? closeNav() : openNav(); });
      mobileClose.addEventListener('click', closeNav);
      // close on navigation
      mobileNav.querySelectorAll('a').forEach(a=>a.addEventListener('click', closeNav));
    })();

    // lightweight smooth image loading
    document.querySelectorAll('img').forEach(img=>{img.loading='lazy'});

    // Accessibility: focus trap not implemented (kept simple) but close on Escape
    document.addEventListener('keydown', (e)=>{ if(e.key === 'Escape'){ const mobileNav = document.getElementById('mobileNav'); if(mobileNav.classList.contains('open')){ mobileNav.classList.remove('open'); mobileNav.setAttribute('aria-hidden','true'); document.body.style.overflow=''; }}});

    // set year
    document.getElementById('year').textContent = new Date().getFullYear();
  </script>
</body>
</html>
