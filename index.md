<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>iamPSR — Stories, Rides & Gear</title>
  <meta name="description" content="iamPSR — motorcycle stories, tips, and the gear I use." />
  <style>
    :root{
      --bg: #f7f7f8;
      --card: #ffffff;
      --muted: #6b7280;
      --accent: #ff6a00; /* warm orange */
      --max-width: 1100px;
      --radius: 12px;
      --gap: 20px;
      font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    }
    html,body{height:100%;}
    body{
      margin:0;
      background:var(--bg);
      color:#111827;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.5;
      display:flex;
      justify-content:center;
      padding:40px 20px;
    }
    .wrap{width:100%;max-width:var(--max-width);}
    header{display:flex;align-items:center;justify-content:space-between;margin-bottom:28px}
    .brand{display:flex;align-items:center;gap:14px}
    .logo{width:56px;height:56px;border-radius:10px;background:linear-gradient(135deg,#111827,#1f2937);display:flex;align-items:center;justify-content:center;color:#fff;font-weight:700}
    .title{font-size:18px;font-weight:700}
    nav a{margin-left:18px;color:var(--muted);text-decoration:none;font-weight:600}

    .hero{background:linear-gradient(180deg, rgba(17,24,39,0.02), rgba(255,255,255,0));padding:34px;border-radius:16px;margin-bottom:28px;display:flex;gap:24px;align-items:center}
    .hero-left{flex:1}
    .hero h1{margin:0;font-size:28px}
    .hero p{margin:8px 0 0;color:var(--muted)}
    .hero-cta{margin-top:18px}
    .button{display:inline-block;padding:10px 16px;border-radius:10px;background:var(--accent);color:white;text-decoration:none;font-weight:700}

    .grid{display:grid;grid-template-columns:repeat(3,1fr);gap:var(--gap)}
    @media (max-width:900px){.grid{grid-template-columns:repeat(2,1fr)}}
    @media (max-width:600px){.grid{grid-template-columns:1fr}}

    .card{background:var(--card);border-radius:var(--radius);overflow:hidden;box-shadow:0 6px 18px rgba(15,23,42,0.06);display:flex;flex-direction:column}
    .thumb{height:170px;background:#dfe4ea;background-size:cover;background-position:center}
    .card-body{padding:16px;flex:1;display:flex;flex-direction:column}
    .kicker{font-size:12px;color:var(--muted);text-transform:uppercase;letter-spacing:0.08em;margin-bottom:8px}
    .card h3{margin:0 0 8px;font-size:16px}
    .excerpt{color:var(--muted);font-size:14px;flex:1}
    .meta{display:flex;gap:10px;align-items:center;margin-top:12px}
    .meta a{color:var(--accent);text-decoration:none;font-weight:700}

    .section-header{display:flex;align-items:end;justify-content:space-between;margin:26px 0 12px}
    .section-header h2{margin:0;font-size:18px}
    .small{color:var(--muted);font-size:14px}

    .products-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:var(--gap)}
    @media (max-width:1000px){.products-grid{grid-template-columns:repeat(3,1fr)}}
    @media (max-width:700px){.products-grid{grid-template-columns:repeat(2,1fr)}}
    @media (max-width:420px){.products-grid{grid-template-columns:1fr}}

    .prod{background:var(--card);border-radius:12px;padding:12px;display:flex;gap:12px;align-items:center;box-shadow:0 6px 14px rgba(15,23,42,0.04)}
    .prod img{width:56px;height:56px;object-fit:cover;border-radius:10px}
    .prod .pmeta{display:flex;flex-direction:column}
    .prod .pmeta .name{font-weight:700}
    .prod .pmeta .by{font-size:13px;color:var(--muted)}

    footer{margin-top:40px;color:var(--muted);font-size:13px;text-align:center}

    /* utility */
    .muted{color:var(--muted)}
    .center{display:flex;justify-content:center}
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <div class="brand">
        <div class="logo">PSR</div>
        <div>
          <div class="title">iamPSR</div>
          <div class="muted">stories, rides & gear</div>
        </div>
      </div>
      <nav aria-label="Main navigation">
        <a href="/">Home</a>
        <a href="/stories.html">Stories</a>
        <a href="/products.html">Products</a>
        <a href="/about.html">About</a>
      </nav>
    </header>

    <main>
      <section class="hero" aria-labelledby="hero-heading">
        <div class="hero-left">
          <h1 id="hero-heading">Motorcycle stories & practical gear — told simply.</h1>
          <p>Real rides, short tips, and the kit I actually use. New stories published weekly.</p>
          <div class="hero-cta">
            <a class="button" href="/stories.html">Read latest story</a>
            <a style="margin-left:12px;color:var(--muted);font-weight:600;text-decoration:none" href="/products.html">See my gear →</a>
          </div>
        </div>
        <div style="width:320px">
          <img alt="rider on road" src="https://images.unsplash.com/photo-1503376780353-7e6692767b70?q=80&w=800&auto=format&fit=crop" style="width:100%;border-radius:12px;display:block;box-shadow:0 10px 25px rgba(15,23,42,0.08)"/>
        </div>
      </section>

      <section aria-labelledby="featured">
        <div class="section-header">
          <h2 id="featured">Featured stories</h2>
          <div class="small">Latest & curated picks</div>
        </div>

        <div class="grid">
          <!-- Story card 1 -->
          <article class="card">
            <div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1504215680853-026ed2a45def?q=80&w=1400&auto=format&fit=crop')" role="img" aria-label="mountain road"></div>
            <div class="card-body">
              <div class="kicker">Long Ride</div>
              <h3>Himalayan Dawn — Lachen to Gurudongmar</h3>
              <p class="excerpt">A quiet morning climb, a frozen lake, and one very cold breakfast stop. Lessons from a high-altitude ride.</p>
              <div class="meta"><a href="/stories/lachen-gurudongmar.html">Read story</a><span class="muted">• 8 min read</span></div>
            </div>
          </article>

          <!-- Story card 2 -->
          <article class="card">
            <div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1519681393784-d120267933ba?q=80&w=1400&auto=format&fit=crop')" role="img" aria-label="motorcycle closeup"></div>
            <div class="card-body">
              <div class="kicker">Review</div>
              <h3>My Toolkit — The small things that matter</h3>
              <p class="excerpt">From tire plugs to a compact tool roll — gear that saved a ride and costs less than you think.</p>
              <div class="meta"><a href="/stories/toolkit.html">Read story</a><span class="muted">• 4 min read</span></div>
            </div>
          </article>

          <!-- Story card 3 -->
          <article class="card">
            <div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1471478336966-c9103f4a8fef?q=80&w=1400&auto=format&fit=crop')" role="img" aria-label="riding through trees"></div>
            <div class="card-body">
              <div class="kicker">Guide</div>
              <h3>Packing light for two weeks on the road</h3>
              <p class="excerpt">A minimal checklist that covers clothes, maintenance, and what to leave behind.</p>
              <div class="meta"><a href="/stories/packing-light.html">Read story</a><span class="muted">• 6 min read</span></div>
            </div>
          </article>
        </div>
      </section>

      <section aria-labelledby="products" style="margin-top:34px">
        <div class="section-header">
          <h2 id="products">Products I use</h2>
          <div class="small">Click any item to view all products</div>
        </div>

        <div class="products-grid">
          <a class="prod" href="/products.html#helmet">
            <img alt="helmet" src="https://images.unsplash.com/photo-1542291026-7eec264c27ff?q=80&w=800&auto=format&fit=crop">
            <div class="pmeta"><div class="name">Adventure Helmet</div><div class="by muted">Arai / Shoei / budget pick</div></div>
          </a>

          <a class="prod" href="/products.html#jacket">
            <img alt="jacket" src="https://images.unsplash.com/photo-1517248135467-4c7edcad34c4?q=80&w=800&auto=format&fit=crop">
            <div class="pmeta"><div class="name">Riding Jacket</div><div class="by muted">Breathable, protective</div></div>
          </a>

          <a class="prod" href="/products.html#boots">
            <img alt="boots" src="https://images.unsplash.com/photo-1519741491700-7ab4ec0f3d58?q=80&w=800&auto=format&fit=crop">
            <div class="pmeta"><div class="name">Riding Boots</div><div class="by muted">Waterproof & sturdy</div></div>
          </a>

          <a class="prod" href="/products.html#camera">
            <img alt="camera" src="https://images.unsplash.com/photo-1519183071298-a2962be90b15?q=80&w=800&auto=format&fit=crop">
            <div class="pmeta"><div class="name">Action Camera</div><div class="by muted">Compact & mountable</div></div>
          </a>
        </div>

        <div class="center" style="margin-top:18px">
          <a class="button" href="/products.html">See all products</a>
        </div>
      </section>

    </main>

    <footer>
      © "iamPSR" — Built with purpose. <a href="/privacy.html">Privacy</a>
    </footer>
  </div>
</body>
</html>
