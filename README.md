
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="theme-color" content="#0c0f14">
  <title>✦ your name — personal archive</title>
  <style>
    :root {
      --bg: #0c0f14;
      --panel: #11141c;
      --purple: #c5a0fa;
      --pink: #ed8cce;
      --blue: #78baff;
      --text: #e4d9f8;
      --muted: #9d8bab;
      --line: #393342;
    }

  * { box-sizing: border-box; }

    html { scroll-behavior: smooth; }

    body {
      margin: 0;
      background:
        radial-gradient(ellipse at 50% 0%, #21152d 0, transparent 42%),
        var(--bg);
      color: var(--text);
      font: 14px/1.8 "Trebuchet MS", sans-serif;
    }

    a {
      color: var(--blue);
      text-decoration: underline;
      text-underline-offset: 4px;
    }

    a:hover { color: var(--pink); }

    .page {
      width: min(900px, 94%);
      margin: 26px auto;
      padding: clamp(18px, 4vw, 42px);
      border: 1px solid var(--line);
      border-radius: 5px;
      background: rgba(12, 15, 20, .94);
      box-shadow: 0 0 40px #0005;
    }

    .ornament {
      overflow: hidden;
      color: #9d4a9b;
      text-align: center;
      white-space: nowrap;
      letter-spacing: 4px;
      font-size: 20px;
      line-height: 1.4;
      user-select: none;
    }

    header { text-align: center; }

    .eyebrow {
      color: var(--muted);
      font: 11px monospace;
      letter-spacing: 3px;
      text-transform: uppercase;
    }

    h1, h2, h3 {
      font-family: Georgia, "Times New Roman", serif;
      font-weight: normal;
    }

    h1 {
      margin: 12px 0 0;
      color: var(--pink);
      font-size: clamp(36px, 8vw, 66px);
      text-shadow: 2px 2px #512b61, 0 0 22px #c05cb544;
    }

    .subtitle {
      margin: 2px 0 20px;
      color: var(--purple);
      font-style: italic;
    }

    .nav {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 10px 24px;
      padding: 14px;
      border-top: 1px solid var(--line);
      border-bottom: 1px solid var(--line);
      font-size: 12px;
    }

    .hero {
      display: grid;
      grid-template-columns: 1.05fr .95fr;
      align-items: center;
      gap: 32px;
      padding: 42px 0;
    }

    .hero-art {
      position: relative;
      min-height: 290px;
      display: grid;
      place-items: center;
      overflow: hidden;
      border: 1px solid #65486d;
      background:
        radial-gradient(ellipse, #4d286a66, transparent 65%),
        repeating-linear-gradient(
          135deg, transparent 0 24px, #9b69c50a 25px 26px
        );
    }

    .hero-art::before,
    .hero-art::after {
      position: absolute;
      color: var(--pink);
      font-size: 25px;
    }

    .hero-art::before {
      content: "✧";
      top: 12px;
      left: 16px;
    }

    .hero-art::after {
      content: "✦";
      right: 18px;
      bottom: 10px;
    }

    /* CC0 character sprite sheet used as a placeholder. */
    .sprite {
      width: 150px;
      height: 180px;
      background-image: url(
        "https://opengameart.org/sites/default/files/13jump_1.png"
      );
      background-repeat: no-repeat;
      background-size: 900px auto;
      background-position: left center;
      image-rendering: pixelated;
      animation: sprite-walk 1.2s steps(6) infinite;
      filter: drop-shadow(0 0 12px #b98cff66);
    }

    @keyframes sprite-walk {
      from { background-position: 0 center; }
      to { background-position: -900px center; }
    }

    .hero-copy h2 {
      color: var(--purple);
      font-size: 27px;
      margin: 0 0 12px;
    }

    .status {
      display: inline-block;
      padding: 3px 10px;
      border: 1px solid #604878;
      background: #251b30;
      color: #e0b5fa;
      font: 11px monospace;
    }

    .divider {
      margin: 12px 0 20px;
      color: #b884ee;
      text-align: center;
      letter-spacing: 6px;
    }

    section { padding: 20px 0; }

    .section-title {
      margin: 0 0 18px;
      color: var(--pink);
      font-size: 25px;
      text-align: center;
      text-shadow: 0 0 15px #db73b833;
    }

    .about-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 14px;
    }

    .box {
      padding: 18px;
      border: 1px solid var(--line);
      background: var(--panel);
    }

    .box h3 {
      margin: 0 0 8px;
      color: var(--purple);
      font-size: 19px;
    }

    .box p { margin: 0; }

    .quote {
      padding: 26px 12px;
      color: #c3a3ed;
      text-align: center;
      font: italic 15px Georgia, serif;
    }

    .friends {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 12px;
    }

    .friend {
      flex: 1 1 145px;
      padding: 15px;
      border: 1px solid var(--line);
      background: var(--panel);
      text-align: center;
    }

    .sticker {
      display: block;
      width: 52px;
      height: 52px;
      margin: 0 auto 8px;
      object-fit: contain;
    }

    .badge-row {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 8px;
    }

    .badge {
      padding: 5px 12px;
      border: 1px solid #64466f;
      background: #211829;
      color: #dcb5ff;
      font: 11px monospace;
    }

    footer {
      padding-top: 22px;
      border-top: 1px solid var(--line);
      color: var(--muted);
      font-size: 11px;
      text-align: center;
    }

    @media (max-width: 620px) {
      .page { padding: 16px; margin: 10px auto; }
      .hero { grid-template-columns: 1fr; gap: 24px; }
      .hero-art { min-height: 235px; }
      .about-grid { grid-template-columns: 1fr; }
      .nav { gap: 8px 14px; }
    }

    @media (prefers-reduced-motion: reduce) {
      *, *::before, *::after {
        animation: none !important;
        scroll-behavior: auto !important;
      }
    }
  </style>
</head>
<body>
  <main class="page">
    <div class="ornament">୨୧ ── ⋆｡°✩ ── ୨୧ ── ⋆｡°✩ ── ୨୧</div>

  <header>
      <p class="eyebrow">personal archive · est. forever ago</p>
      <h1>your name</h1>
      <p class="subtitle">✧ somewhere between dreams and static ✧</p>
      <div class="nav">
        <a href="#about">about</a>
        <a href="#interests">interests</a>
        <a href="#friends">friends</a>
        <a href="#links">links</a>
      </div>
    </header>

  <div class="hero">
      <div class="hero-art" aria-label="Animated CC0 pixel-art character">
        <div class="sprite" role="img" aria-label="Fantasy character sprite"></div>
      </div>
    <div class="hero-copy">
        <span class="status">✦ ONLINE IN SPIRIT ✦</span>
        <h2>hello, stranger.</h2>
        <p>
          welcome to my little corner of the internet.
          this page is full of things i like, random thoughts,
          and bits of my brain scattered everywhere.
        </p>
        <p>
          <span style="color:var(--pink)">pronouns:</span> they / them<br>
          <span style="color:var(--pink)">currently:</span> daydreaming<br>
          <span style="color:var(--pink)">vibe:</span> purple things &amp; stars
        </p>
        <p><a href="#about">read more about me ↴</a></p>
      </div>
    </div>

  <div class="divider">✦ · · ───── ୨୧ ───── · · ✦</div>

   <section id="about">
      <h2 class="section-title">✧ about me ✧</h2>
      <div class="about-grid">
        <article class="box">
          <h3>the basics</h3>
          <p>
            hi! you can call me your nickname.
            i'm just a person collecting interests, making things,
            and spending too much time online.
          </p>
        </article>
        <article class="box">
          <h3>boundaries</h3>
          <p>
            be kind, respect people's boundaries, and ask before
            reposting personal artwork. read my links before interacting.
          </p>
        </article>
        <article class="box">
          <h3>currently into</h3>
          <p>
            fantasy worlds, character design, music, obscure games,
            pixel art, and pretty website layouts.
          </p>
        </article>
        <article class="box">
          <h3>little note</h3>
          <p>
            this is a work in progress. some artwork is placeholder
            material and will be replaced as the page develops.
          </p>
        </article>
      </div>
    </section>

   <div class="quote">
      “ i would rather be a mystery among the stars. ”
    </div>

   <div class="divider">୨୧ ── ⋆｡°✩ ── ୨୧ ── ⋆｡°✩ ── ୨୧</div>

   <section id="interests">
      <h2 class="section-title">✧ my little collection ✧</h2>
      <div class="friends">
        <article class="friend">
          <img class="sticker"
            src="https://cdn.jsdelivr.net/gh/hfg-gmuend/openmoji/color/svg/1F47E.svg"
            alt="Alien emoji sticker">
          <strong>games</strong>
          <p>digital worlds &amp; side quests</p>
        </article>
        <article class="friend">
          <img class="sticker"
            src="https://cdn.jsdelivr.net/gh/hfg-gmuend/openmoji/color/svg/1F338.svg"
            alt="Cherry blossom sticker">
          <strong>aesthetics</strong>
          <p>flowers, purple, lace &amp; stars</p>
        </article>
        <article class="friend">
          <img class="sticker"
            src="https://cdn.jsdelivr.net/gh/hfg-gmuend/openmoji/color/svg/1F3B5.svg"
            alt="Music note sticker">
          <strong>music</strong>
          <p>soundtrack to my existence</p>
        </article>
      </div>
    </section>

   <section>
      <h2 class="section-title">✧ status / byi ✧</h2>
      <div class="box">
        <p>
          ♡ slow replies sometimes<br>
          ♡ tone indicators appreciated<br>
          ♡ please don't copy my personal content<br>
          ♡ ask before sending friend requests
        </p>
        <div class="badge-row">
          <span class="badge">✦ dreamer</span>
          <span class="badge">☾ night owl</span>
          <span class="badge">୨୧ work in progress</span>
        </div>
      </div>
    </section>

  <section id="friends">
      <h2 class="section-title">✧ little stars ✧</h2>
      <div class="friends">
        <div class="friend">✧<br><a href="#">friend one</a></div>
        <div class="friend">☾<br><a href="#">friend two</a></div>
        <div class="friend">୨୧<br><a href="#">friend three</a></div>
      </div>
    </section>

  <section id="links">
      <h2 class="section-title">✧ find me elsewhere ✧</h2>
      <div class="nav">
        <a href="https://github.com/">github</a>
        <a href="#">strawpage</a>
        <a href="#">pronouns</a>
        <a href="#">art archive</a>
      </div>
    </section>

   <div class="divider">✦ · · ───── ୨୧ ───── · · ✦</div>
    <footer>
      <div class="ornament">୨୧ ── ⋆｡°✩ ── ୨୧</div>
      made with love, insomnia, and too many stars.
      <br>
      CC0 character placeholder: Hordana / OpenGameArt.
      OpenMoji stickers: CC BY-SA 4.0.
      <br>
      <a href="#top" onclick="window.scrollTo({top:0,behavior:'smooth'});return false;">
        back to the top ↑
      </a>
    </footer>
  </main>
</body>
</html>
