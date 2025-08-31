<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Introductions — Diego Estrada</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg: #0f172a;          /* slate-900 */
      --card: #111827;        /* gray-900 */
      --muted: #94a3b8;       /* slate-400 */
      --text: #e5e7eb;        /* gray-200 */
      --accent: #22d3ee;      /* cyan-400 */
      --ring: rgba(34, 211, 238, .35);
    }
    * { box-sizing: border-box; }
    html, body { height: 100%; }
    body {
      margin: 0;
      font-family: "Inter", system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, "Apple Color Emoji", "Segoe UI Emoji";
      background: radial-gradient(1000px 600px at 10% -10%, rgba(34,211,238,.12), transparent),
                  radial-gradient(1200px 800px at 110% 10%, rgba(14,165,233,.12), transparent),
                  var(--bg);
      color: var(--text);
      line-height: 1.6;
    }
    .container {
      max-width: 900px;
      margin: 40px auto;
      padding: 0 16px 32px;
    }
    header.hero {
      background: linear-gradient(180deg, rgba(255,255,255,.04), rgba(255,255,255,.02));
      border: 1px solid rgba(255,255,255,.08);
      border-radius: 20px;
      padding: 28px;
      box-shadow: 0 10px 30px rgba(0,0,0,.35);
      backdrop-filter: blur(6px);
    }
    .hero h1 { margin: 0 0 6px; font-size: 1.9rem; letter-spacing: .3px; }
    .hero p { margin: 6px 0; color: var(--muted); }
    .badges { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 12px; }
    .badge {
      border: 1px solid rgba(255,255,255,.12);
      padding: 6px 10px;
      border-radius: 999px;
      font-size: .88rem;
      background: rgba(2,6,23,.35);
    }

    .grid { display: grid; grid-template-columns: 1fr; gap: 16px; margin-top: 22px; }
    @media (min-width: 720px) { .grid { grid-template-columns: repeat(2, 1fr); } }

    .card {
      background: var(--card);
      border: 1px solid rgba(255,255,255,.08);
      border-radius: 16px;
      padding: 18px;
      box-shadow: 0 8px 24px rgba(0,0,0,.35);
      transition: transform .2s ease, box-shadow .2s ease, border-color .2s ease;
    }
    .card:hover { transform: translateY(-2px); border-color: rgba(34,211,238,.25); box-shadow: 0 14px 32px rgba(0,0,0,.45); }
    .card h2 { margin: 0 0 8px; font-size: 1.15rem; color: var(--accent); }
    .card p { margin: 8px 0; }
    .list { padding-left: 18px; margin: 6px 0 0; }

    /* Explicit style for the previously unstyled Fun Fact section */
    .fun-fact {
      position: relative;
      border-left: 3px solid var(--accent);
      outline: 0;
    }
    .fun-fact::after {
      content: "★";
      position: absolute; right: 14px; top: 14px; font-size: 18px; opacity: .5;
    }

    footer { color: var(--muted); font-size: .9rem; margin-top: 28px; text-align: center; }
    a { color: var(--accent); text-decoration: none; }
    a:focus, .card:focus { outline: 3px solid var(--ring); outline-offset: 2px; border-radius: 14px; }
  </style>
</head>
<body>
  <main class="container">
    <header class="hero" tabindex="0">
      <h1>Diego Estrada</h1>
      <p><strong>Preferred name:</strong> Diego</p>
      <p><strong>Current role:</strong> Runner/Busser at Gibson’s Steakhouse (Chicago)</p>
      <div class="badges">
        <span class="badge">Lewis University — Intro to CS</span>
        <span class="badge">Chicago, IL</span>
        <span class="badge">Hospitality + Tech</span>
      </div>
    </header>

    <section class="grid" aria-label="About Diego">
      <article class="card" tabindex="0">
        <h2>Job Responsibilities</h2>
        <p>
          Support front-of-house service at a high‑volume steakhouse: table resets, food running, guest requests,
          coordination with servers and kitchen, and keeping the dining room flowing during rushes. Strong focus on
          teamwork, communication, and attention to detail.
        </p>
      </article>

      <article class="card" tabindex="0">
        <h2>Hobbies & Special Interests</h2>
        <ul class="list">
          <li>PC hardware tinkering (eGPU builds, dual‑boot setups)</li>
          <li>Photography & video (Canon Rebel T7)</li>
          <li>Creative writing & game story rewrites</li>
          <li>DIY electronics and hands‑on fabrication (welding background)</li>
        </ul>
      </article>

      <article class="card" tabindex="0">
        <h2>Why I’m Pursuing This Degree</h2>
        <p>
          I’m aiming to blend real‑world problem solving with technology—starting with solid CS foundations and growing
          into areas like cybersecurity and embedded systems. Long term, I want to build practical tech that helps
          people and maybe even dabble in innovative transportation ideas.
        </p>
      </article>

      <article class="card" tabindex="0">
        <h2>Why I’m Taking This Course</h2>
        <p>
          To get comfortable turning ideas into code, practice version control, and build a portfolio site I can iterate
          on throughout the program.
        </p>
      </article>

      <article class="card fun-fact" tabindex="0" style="grid-column: 1 / -1;">
        <h2>Fun Fact</h2>
        <p>
          I once turned a modest ThinkPad into a tiny rendering rig with an external GPU dock I pieced together—after a
          lot of drivers, BIOS adventures, and coffee.
        </p>
      </article>
    </section>

    <footer>
      <p>© <span id="year"></span> Diego Estrada • Built for Lewis University’s Introductions activity • <a href="https://pages.github.com/" target="_blank" rel="noreferrer noopener">GitHub Pages</a></p>
    </footer>
  </main>
  <script>
    document.getElementById('year').textContent = new Date().getFullYear();
  </script>
</body>
</html>

- Remove all of the text in your README.md file.
- Add your application name and add yourself as the Author.
- Add credits for Eric Pogue, ChatGPT, and for this site where you utilized the template.
