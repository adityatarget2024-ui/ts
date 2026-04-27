<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>For Tashu, with love</title>
<meta name="description" content="A letter for Tashu baby — every reason, every promise, every sorry." />
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,500;1,400;1,500&family=Lora:ital,wght@0,400;0,500;1,400;1,500&display=swap" rel="stylesheet" />
<style>
  :root {
    --background: 30 35% 96%;
    --foreground: 345 30% 18%;
    --muted: 25 30% 90%;
    --muted-foreground: 345 15% 40%;
    --primary: 350 55% 45%;
    --primary-soft: 350 55% 60%;
    --border: 30 25% 85%;
    --card: 30 40% 98%;
    --accent: 28 70% 60%;
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }
  html, body { background: hsl(var(--background)); color: hsl(var(--foreground)); }
  body {
    font-family: 'Lora', Georgia, serif;
    line-height: 1.6;
    overflow-x: hidden;
    background:
      radial-gradient(circle at 20% 10%, hsla(350, 60%, 80%, 0.35), transparent 45%),
      radial-gradient(circle at 80% 30%, hsla(28, 80%, 75%, 0.30), transparent 50%),
      radial-gradient(circle at 50% 90%, hsla(345, 50%, 75%, 0.25), transparent 55%),
      hsl(var(--background));
    background-attachment: fixed;
  }
  body::before {
    content: "";
    position: fixed; inset: 0;
    background-image: url("data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='180' height='180'><filter id='n'><feTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='2' stitchTiles='stitch'/><feColorMatrix values='0 0 0 0 0  0 0 0 0 0  0 0 0 0 0  0 0 0 0.06 0'/></filter><rect width='100%' height='100%' filter='url(%23n)'/></svg>");
    pointer-events: none;
    opacity: 0.6;
    z-index: 1;
  }
  .serif { font-family: 'Playfair Display', Georgia, serif; }

  section { position: relative; z-index: 2; padding: 8rem 1.5rem; }

  /* ---------- HERO ---------- */
  .hero {
    min-height: 100dvh;
    display: flex; align-items: center; justify-content: center;
    text-align: center;
    overflow: hidden;
  }
  .bokeh { position: absolute; inset: 0; overflow: hidden; pointer-events: none; z-index: 0; }
  .bokeh span {
    position: absolute;
    border-radius: 50%;
    background: radial-gradient(circle, hsla(40, 100%, 90%, 0.85), hsla(30, 80%, 80%, 0) 70%);
    filter: blur(2px);
    animation: float 18s linear infinite;
  }
  @keyframes float {
    0%   { transform: translateY(20vh) scale(.9); opacity: 0; }
    10%  { opacity: .8; }
    90%  { opacity: .8; }
    100% { transform: translateY(-110vh) scale(1.1); opacity: 0; }
  }
  .hero-content { position: relative; z-index: 2; max-width: 780px; padding: 0 1rem; }
  .hero h1 {
    font-family: 'Playfair Display', serif;
    font-style: italic;
    font-weight: 500;
    font-size: clamp(4rem, 14vw, 9.5rem);
    line-height: 1;
    color: hsl(var(--foreground));
    letter-spacing: -0.02em;
    opacity: 0; transform: translateY(30px);
    animation: rise 1.6s ease-out .2s forwards;
  }
  .hero p {
    margin-top: 1.5rem;
    font-size: clamp(1.05rem, 2vw, 1.5rem);
    color: hsl(var(--muted-foreground));
    font-weight: 300;
    letter-spacing: .03em;
    opacity: 0; transform: translateY(30px);
    animation: rise 1.6s ease-out .9s forwards;
  }
  .hero .heart {
    margin: 3rem auto 0;
    width: 28px; height: 28px;
    color: hsl(var(--primary)); opacity: .55;
    animation: rise 1.6s ease-out 1.5s forwards, pulse 3s ease-in-out 2.5s infinite;
    opacity: 0; transform: translateY(30px);
  }
  @keyframes rise { to { opacity: 1; transform: translateY(0); } }
  @keyframes pulse { 0%,100% { opacity: .45; } 50% { opacity: .9; } }

  /* ---------- DIVIDERS / REVEAL ---------- */
  .reveal { opacity: 0; transform: translateY(36px); transition: opacity 1.2s ease, transform 1.2s ease; }
  .reveal.in { opacity: 1; transform: translateY(0); }
  .hairline {
    width: 64px; height: 1px;
    background: hsla(350, 55%, 45%, 0.35);
    margin: 0 auto;
  }

  /* ---------- APOLOGY ---------- */
  .apology { max-width: 720px; margin: 0 auto; text-align: center; }
  .apology .item {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.25rem, 2.4vw, 1.7rem);
    color: hsla(345, 30%, 20%, 0.92);
    line-height: 1.55;
    margin: 3rem 0;
  }

  /* ---------- ROSE DIVIDER ---------- */
  .rose-divider {
    text-align: center;
    padding: 5rem 1rem;
    position: relative;
  }
  .rose-divider .glyph {
    font-family: 'Playfair Display', serif;
    font-style: italic;
    font-size: clamp(2rem, 5vw, 3.5rem);
    color: hsl(var(--primary));
    opacity: .6;
    letter-spacing: .5em;
  }
  .rose-divider .ornament {
    width: 200px; max-width: 60%; height: 1px;
    background: linear-gradient(to right, transparent, hsla(350, 55%, 45%, .5), transparent);
    margin: 1.25rem auto;
  }
  .rose-divider .sub {
    color: hsl(var(--muted-foreground));
    font-style: italic;
    font-size: .95rem;
    letter-spacing: .25em;
    text-transform: uppercase;
  }

  /* ---------- REASONS ---------- */
  .reasons-wrap { max-width: 1100px; margin: 0 auto; }
  .reasons-wrap h2 {
    font-family: 'Playfair Display', serif;
    font-style: italic;
    font-size: clamp(2rem, 4.5vw, 3rem);
    text-align: center;
    color: hsl(var(--foreground));
    margin-bottom: .75rem;
  }
  .reasons-wrap .lead {
    text-align: center;
    color: hsl(var(--muted-foreground));
    font-size: 1.05rem;
    margin-bottom: 4rem;
  }
  .reasons {
    display: grid;
    grid-template-columns: 1fr;
    gap: 2.25rem 3rem;
  }
  @media (min-width: 760px) { .reasons { grid-template-columns: 1fr 1fr; } }
  .reason {
    border-left: 1px solid hsla(350, 55%, 45%, 0.2);
    padding: .25rem 0 .25rem 1.25rem;
    font-size: 1.1rem;
    color: hsla(345, 30%, 25%, 0.92);
    transition: border-color .3s ease;
    position: relative;
  }
  .reason:hover { border-color: hsla(350, 55%, 45%, 0.55); }
  .reason::before {
    content: "✦";
    position: absolute;
    left: -1.6rem; top: 0;
    color: hsla(350, 55%, 45%, .35);
    font-size: .85rem;
  }

  /* ---------- PROMISES ---------- */
  .promises-section {
    background: hsla(30, 50%, 97%, 0.6);
    backdrop-filter: blur(4px);
    border-top: 1px solid hsla(345, 30%, 80%, .5);
    border-bottom: 1px solid hsla(345, 30%, 80%, .5);
  }
  .promises-wrap { max-width: 720px; margin: 0 auto; }
  .promises-wrap .label {
    text-align: center;
    color: hsla(350, 55%, 45%, .85);
    text-transform: uppercase;
    letter-spacing: .35em;
    font-size: .8rem;
    margin-bottom: 1rem;
  }
  .promises-wrap .label-line {
    width: 48px; height: 1px;
    margin: 0 auto 4rem;
    background: hsla(350, 55%, 45%, .5);
  }
  .promise {
    display: flex; gap: 1.25rem; align-items: flex-start;
    margin-bottom: 2.25rem;
    font-family: 'Playfair Display', serif;
    font-style: italic;
    font-size: clamp(1.15rem, 2vw, 1.5rem);
    color: hsla(345, 30%, 22%, 0.95);
  }
  .promise .dot {
    width: 14px; height: 14px; flex-shrink: 0;
    margin-top: .55rem;
    background: hsl(var(--primary)); opacity: .55;
    clip-path: path("M7 12s-5-3.33-5-7a3 3 0 015-2.24A3 3 0 0112 5c0 3.67-5 7-5 7z");
  }

  /* ---------- CLOSING ---------- */
  .closing {
    text-align: center;
    min-height: 80vh;
    display: flex; align-items: center; justify-content: center;
  }
  .closing-inner { max-width: 680px; margin: 0 auto; }
  .closing .big {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.75rem, 4vw, 2.75rem);
    line-height: 1.35;
    color: hsl(var(--foreground));
  }
  .closing .signoff {
    margin-top: 4rem;
    color: hsl(var(--muted-foreground));
    font-style: italic;
  }
  .closing .name {
    font-family: 'Playfair Display', serif;
    font-size: 2rem;
    color: hsl(var(--primary));
    margin-top: .5rem;
  }

  footer {
    text-align: center;
    padding: 2rem 1rem 4rem;
    color: hsla(345, 20%, 40%, .55);
    font-size: .85rem;
    letter-spacing: .15em;
    text-transform: uppercase;
    position: relative; z-index: 2;
  }

  ::selection { background: hsla(350, 55%, 45%, .2); color: hsl(var(--primary)); }
</style>
</head>
<body>

<!-- HERO -->
<section class="hero">
  <div class="bokeh" id="bokeh"></div>
  <div class="hero-content">
    <h1>Tashu...</h1>
    <p>my favorite person in the whole world.</p>
    <svg class="heart" viewBox="0 0 24 24" fill="currentColor"><path d="M12 21s-7-4.5-9.5-9C.8 8.6 2.4 5 6 5c2 0 3.5 1 4.5 2.5C11.5 6 13 5 15 5c3.6 0 5.2 3.6 3.5 7-2.5 4.5-9.5 9-9.5 9z"/></svg>
  </div>
</section>

<!-- APOLOGY -->
<section>
  <div class="apology">
    <div class="hairline reveal"></div>
    <p class="item reveal">I am so incredibly sorry for making you upset. It breaks my heart to know I brought a shadow to your day.</p>
    <p class="item reveal">When I see you hurt, especially because of me, the whole world just feels wrong. I never want to be the reason your smile fades.</p>
    <p class="item reveal">I know I messed up, baby. I got it wrong, and I take full responsibility. You deserve nothing but warmth and understanding from me.</p>
    <p class="item reveal">Please know that my intention is never to push you away or make you feel less than adored. You are everything to me.</p>
    <div class="hairline reveal"></div>
  </div>
</section>

<!-- ROSE DIVIDER -->
<section class="rose-divider reveal">
  <div class="ornament"></div>
  <div class="glyph">❀</div>
  <div class="ornament"></div>
  <div class="sub">a small pause</div>
</section>

<!-- REASONS -->
<section>
  <div class="reasons-wrap">
    <h2 class="reveal">Just a few reasons why I love you...</h2>
    <p class="lead reveal">(though a lifetime wouldn't be enough to list them all)</p>
    <div class="reasons">
      <div class="reason reveal">The way you scrunch your nose when something makes you genuinely laugh.</div>
      <div class="reason reveal">How you hum those little melodies to yourself when you're just walking around the house or cooking.</div>
      <div class="reason reveal">The exact way your hand feels when it finds mine without even looking.</div>
      <div class="reason reveal">How you get completely invested in the tiny details of a story you're telling.</div>
      <div class="reason reveal">The way you look at me when you think I'm not paying attention.</div>
      <div class="reason reveal">How you fall asleep mid-sentence during our movie nights, fighting it the whole way.</div>
      <div class="reason reveal">The specific tone of your voice when you say my name when you're sleepy.</div>
      <div class="reason reveal">How fiercely you care about the people you love.</div>
      <div class="reason reveal">Your morning face before the world has demanded anything of you.</div>
      <div class="reason reveal">The fact that just knowing you exist makes my life feel infinitely better.</div>
    </div>
  </div>
</section>

<!-- PROMISES -->
<section class="promises-section">
  <div class="promises-wrap">
    <div class="label reveal">My promises to you</div>
    <div class="label-line reveal"></div>
    <div class="promise reveal"><span class="dot"></span>"I promise to listen to you, truly listen, even when it's hard."</div>
    <div class="promise reveal"><span class="dot"></span>"I promise to be a safe place for your heart, your worries, and your tears."</div>
    <div class="promise reveal"><span class="dot"></span>"I promise to learn from my mistakes and be better for you."</div>
    <div class="promise reveal"><span class="dot"></span>"I promise to never let an argument make you question how much I love you."</div>
    <div class="promise reveal"><span class="dot"></span>"I promise to choose you, every single day, over and over again."</div>
  </div>
</section>

<!-- CLOSING -->
<section class="closing">
  <div class="closing-inner">
    <p class="big reveal">You are my home, Tashu baby.<br/>Please forgive me.</p>
    <div class="signoff reveal">
      <p>Yours, always and completely,</p>
      <p class="name">Your boy</p>
    </div>
  </div>
</section>

<footer>made with every part of me · for you</footer>

<script>
  // Bokeh particles
  (function () {
    const bokeh = document.getElementById('bokeh');
    const COUNT = 24;
    for (let i = 0; i < COUNT; i++) {
      const s = document.createElement('span');
      const size = 30 + Math.random() * 120;
      s.style.width = size + 'px';
      s.style.height = size + 'px';
      s.style.left = (Math.random() * 100) + 'vw';
      s.style.bottom = (-Math.random() * 30) + 'vh';
      s.style.animationDuration = (14 + Math.random() * 18) + 's';
      s.style.animationDelay = (-Math.random() * 18) + 's';
      s.style.opacity = (0.4 + Math.random() * 0.5).toString();
      bokeh.appendChild(s);
    }
  })();

  // Scroll reveal
  (function () {
    const els = document.querySelectorAll('.reveal');
    const io = new IntersectionObserver((entries) => {
      entries.forEach(e => {
        if (e.isIntersecting) {
          e.target.classList.add('in');
          io.unobserve(e.target);
        }
      });
    }, { threshold: 0.15, rootMargin: '0px 0px -60px 0px' });
    els.forEach(el => io.observe(el));
  })();
</script>

</body>
</html>
# ts
