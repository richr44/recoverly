<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Recoverly — Back &amp; Nerve Recovery Tracker</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />

  <!-- Basic SEO -->
  <meta name="description" content="Recoverly helps you track back, glute, and leg nerve symptoms with simple daily logs, trends, and a clear recovery timeline. Designed for people recovering from lumbar or spine surgery." />
  <meta name="keywords" content="recoverly, recovery tracker, back surgery, lumbar surgery, spine surgery, laminectomy, microdiscectomy, nerve pain, sciatica, pain log, surgery recovery app" />

  <!-- Open Graph / Link previews -->
  <meta property="og:title" content="Recoverly — Back &amp; Nerve Recovery Tracker" />
  <meta property="og:description" content="Track back, glute, and leg nerve symptoms in one place. See trends, export a PDF report, and bring better data to your care team." />
  <meta property="og:type" content="website" />
  <meta property="og:url" content="https://richr44.github.io/recoverly/" />
  <meta property="og:image" content="https://richr44.github.io/recoverly/favicon.png" />

  <!-- Favicon -->
  <link rel="icon" href="favicon.png" type="image/png" />

  <!-- Simple, clean styling -->
  <style>
    :root {
      --bg: #050810;
      --card-bg: #0e111a;
      --card-border: rgba(255,255,255,0.06);
      --accent: #3b82f6;
      --accent-soft: rgba(59,130,246,0.14);
      --text-main: #f9fafb;
      --text-muted: #9ca3af;
      --pill-bg: rgba(15,23,42,0.9);
      --shadow-soft: 0 18px 45px rgba(0,0,0,0.65);
      --radius-lg: 20px;
      --radius-pill: 999px;
      --max-width: 960px;
    }

    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "SF Pro Text", sans-serif;
      background: radial-gradient(circle at top, #111827 0, #020617 55%, #000 100%);
      color: var(--text-main);
      -webkit-font-smoothing: antialiased;
    }

    .page {
      min-height: 100vh;
      padding: 32px 16px 40px;
      display: flex;
      justify-content: center;
    }

    .shell {
      width: 100%;
      max-width: var(--max-width);
    }

    header.hero {
      display: grid;
      grid-template-columns: minmax(0, 1.25fr) minmax(0, 1fr);
      gap: 32px;
      align-items: center;
      margin-bottom: 40px;
    }

    @media (max-width: 840px) {
      header.hero {
        grid-template-columns: minmax(0, 1fr);
      }
    }

    .pill {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 6px 12px;
      border-radius: var(--radius-pill);
      background: linear-gradient(90deg, rgba(34,197,94,0.15), rgba(59,130,246,0.15));
      border: 1px solid rgba(148,163,184,0.35);
      color: var(--text-muted);
      font-size: 12px;
    }

    .pill span.dot {
      width: 7px;
      height: 7px;
      border-radius: 999px;
      background: #22c55e;
      box-shadow: 0 0 0 4px rgba(34,197,94,0.25);
    }

    h1 {
      margin: 16px 0 8px;
      font-size: clamp(2.1rem, 4vw, 2.6rem);
      letter-spacing: -0.03em;
    }

    h1 span.accent {
      color: var(--accent);
    }

    .tagline {
      font-size: 15px;
      line-height: 1.6;
      color: var(--text-muted);
      max-width: 34rem;
    }

    .hero-meta {
      display: flex;
      flex-wrap: wrap;
      gap: 8px 16px;
      margin: 16px 0 24px;
      font-size: 13px;
      color: var(--text-muted);
    }

    .hero-meta span.badge {
      padding: 4px 10px;
      border-radius: var(--radius-pill);
      background: rgba(15,23,42,0.9);
      border: 1px solid rgba(148,163,184,0.3);
    }

    .cta-row {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      align-items: center;
      margin-bottom: 24px;
    }

    .cta-primary {
      border-radius: 14px;
      padding: 11px 18px;
      border: none;
      background: linear-gradient(135deg, #3b82f6, #22c55e);
      color: #0b1020;
      font-weight: 600;
      font-size: 14px;
      cursor: default;
      display: inline-flex;
      align-items: center;
      gap: 8px;
      box-shadow: 0 14px 35px rgba(37,99,235,0.45);
    }

    .cta-primary .tag {
      font-size: 11px;
      text-transform: uppercase;
      letter-spacing: 0.08em;
      opacity: 0.85;
    }

    .cta-secondary {
      font-size: 13px;
      color: var(--text-muted);
    }

    .hero-list {
      display: grid;
      grid-template-columns: minmax(0, 1fr);
      gap: 8px;
      margin-top: 10px;
      font-size: 13px;
      color: var(--text-muted);
    }

    .hero-list strong {
      color: var(--text-main);
      font-weight: 500;
    }

    .hero-right {
      display: flex;
      justify-content: center;
    }

    .phone-frame {
      width: 270px;
      border-radius: 46px;
      padding: 10px;
      background: radial-gradient(circle at top left, #1f2937, #020617);
      box-shadow: var(--shadow-soft);
      border: 1px solid rgba(148,163,184,0.45);
      position: relative;
    }

    .phone-inner {
      border-radius: 36px;
      overflow: hidden;
      background: #020617;
      border: 1px solid rgba(15,23,42,0.9);
    }

    .phone-inner img {
      display: block;
      width: 100%;
      height: auto;
    }

    .phone-label {
      position: absolute;
      bottom: -14px;
      left: 50%;
      transform: translateX(-50%);
      padding: 4px 10px;
      border-radius: var(--radius-pill);
      background: rgba(15,23,42,0.95);
      border: 1px solid rgba(148,163,184,0.4);
      font-size: 11px;
      color: var(--text-muted);
      backdrop-filter: blur(12px);
    }

    /* Sections */

    section {
      margin-bottom: 36px;
    }

    .section-title {
      font-size: 16px;
      font-weight: 600;
      margin-bottom: 10px;
    }

    .row-2 {
      display: grid;
      grid-template-columns: minmax(0, 1.2fr) minmax(0, 1fr);
      gap: 20px;
    }

    @media (max-width: 840px) {
      .row-2 {
        grid-template-columns: minmax(0, 1fr);
      }
    }

    .card-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
      gap: 14px;
    }

    .card {
      background: var(--card-bg);
      border-radius: var(--radius-lg);
      border: 1px solid var(--card-border);
      padding: 14px 16px;
      box-shadow: 0 12px 30px rgba(0,0,0,0.55);
    }

    .card h3 {
      margin: 0 0 6px;
      font-size: 14px;
    }

    .card p {
      margin: 0;
      font-size: 13px;
      line-height: 1.6;
      color: var(--text-muted);
    }

    .pill-row {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-top: 6px;
    }

    .pill-tag {
      font-size: 11px;
      padding: 4px 9px;
      border-radius: var(--radius-pill);
      background: var(--pill-bg);
      border: 1px solid rgba(148,163,184,0.4);
      color: var(--text-muted);
    }

    /* Screenshots */

    .screenshots {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(210px, 1fr));
      gap: 18px;
    }

    .shot {
      background: var(--card-bg);
      border: 1px solid var(--card-border);
      border-radius: var(--radius-lg);
      padding: 10px 10px 12px;
      box-shadow: 0 14px 34px rgba(0,0,0,0.6);
    }

    .shot img {
      width: 100%;
      height: auto;
      border-radius: 14px;
      display: block;
      border: 1px solid rgba(31,41,55,0.9);
    }

    .shot-caption {
      margin-top: 6px;
      font-size: 12px;
      color: var(--text-muted);
    }

    /* Footer */

    footer {
      margin-top: 24px;
      padding-top: 16px;
      border-top: 1px solid rgba(31,41,55,0.9);
      font-size: 12px;
      color: var(--text-muted);
      display: flex;
      flex-wrap: wrap;
      gap: 8px 16px;
      justify-content: space-between;
      align-items: center;
    }

    footer a {
      color: var(--accent);
      text-decoration: none;
    }

    footer a:hover {
      text-decoration: underline;
    }

    .footer-links {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      align-items: center;
    }
  </style>
</head>
<body>
  <div class="page">
    <main class="shell">

      <!-- HERO -->
      <header class="hero">
        <div>
          <div class="pill">
            <span class="dot"></span>
            <span>Companion tracker for back &amp; nerve recovery</span>
          </div>

          <h1>
            See your <span class="accent">recovery</span> more clearly.
          </h1>

          <p class="tagline">
            Recoverly helps you log back, glute, and leg nerve symptoms in one place — so you can spot trends, avoid overdoing it, and bring better data to your surgeon or PT.
          </p>

          <div class="hero-meta">
            <span class="badge">Daily pain &amp; activity check-ins</span>
            <span class="badge">History &amp; simple trends</span>
            <span class="badge">PDF report for appointments</span>
          </div>

          <div class="cta-row">
            <button class="cta-primary" type="button">
              <span>Coming soon on the App Store</span>
              <span class="tag">Not yet available</span>
            </button>
            <div class="cta-secondary">
              Built for people recovering from lumbar or spine surgery
              <br /> (laminectomy, microdiscectomy, fusion, or similar).
            </div>
          </div>

          <div class="hero-list">
            <div><strong>Track what actually happens</strong> — pain, nerve symptoms, walking, sitting, and “overdid it” days.</div>
            <div><strong>See your weeks at a glance</strong> — a calendar of mild, moderate, and severe days.</div>
            <div><strong>Show your team real data</strong> — export a PDF summary before follow-ups.</div>
          </div>
        </div>

        <div class="hero-right">
          <div class="phone-frame">
            <div class="phone-inner">
              <!-- Replace with your Today screenshot -->
              <img src="images/screenshot-today.png" alt="Recoverly Today view showing daily pain and activity log." />
            </div>
            <div class="phone-label">
              Today’s check-in with pain, nerve, and activity in one place.
            </div>
          </div>
        </div>
      </header>

      <!-- WHO IT'S FOR / HOW IT HELPS -->
      <section class="row-2">
        <div>
          <h2 class="section-title">Who Recoverly is for</h2>
          <div class="card">
            <h3>People in the slow, messy middle of recovery</h3>
            <p>
              If you’ve had lumbar or spine surgery — like a laminectomy, microdiscectomy, or fusion — it can be hard to explain how you’ve really been feeling over the last few weeks.
            </p>
            <p style="margin-top: 8px;">
              Recoverly gives you a simple way to track:
            </p>
            <ul style="margin: 6px 0 0 18px; padding: 0; color: var(--text-muted); font-size: 13px; line-height: 1.6;">
              <li>Back, glute, and leg nerve pain (0–10)</li>
              <li>Tingling, numbness, and spasms</li>
              <li>Walking and sitting tolerance in minutes</li>
              <li>Days that simply felt like “too much”</li>
            </ul>
            <div class="pill-row">
              <span class="pill-tag">Lumbar surgery</span>
              <span class="pill-tag">Sciatica &amp; nerve pain</span>
              <span class="pill-tag">Post-op recovery</span>
            </div>
          </div>
        </div>

        <div>
          <h2 class="section-title">What Recoverly does (and doesn’t) do</h2>
          <div class="card">
            <h3>Built to track your story — not replace care</h3>
            <p>
              Recoverly is a personal tracking tool. It doesn’t decide what’s “normal,” diagnose problems, or tell you what to do next. Only your medical team can do that.
            </p>
            <p style="margin-top: 8px;">
              Instead, it helps you:
            </p>
            <ul style="margin: 6px 0 0 18px; padding: 0; color: var(--text-muted); font-size: 13px; line-height: 1.6;">
              <li>Walk into appointments with a clear picture of your last few weeks</li>
              <li>Notice patterns between activity and pain flare-ups</li>
              <li>Keep a calmer record when your memory is foggy or stressed</li>
            </ul>
            <p style="margin-top: 8px; font-size: 12px; color: var(--text-muted);">
              Always talk to your surgeon, doctor, or PT about medical questions or new symptoms.
            </p>
          </div>
        </div>
      </section>

      <!-- FEATURES -->
      <section>
        <h2 class="section-title">Key features</h2>
        <div class="card-grid">
          <div class="card">
            <h3>Fast daily check-in</h3>
            <p>
              Log back, glute, leg nerve pain, tingling, spasms, walking, sitting, and “overdid it” in under a minute so you can move on with your day.
            </p>
          </div>
          <div class="card">
            <h3>Calendar of your days</h3>
            <p>
              A simple calendar shows mild (green), moderate (orange), and severe (red) days at a glance, plus dots for missing days so you remember what you didn’t track.
            </p>
          </div>
          <div class="card">
            <h3>Weekly trend insights</h3>
            <p>
              See how the last 7 days compare to the week before — for pain, mobility, and nerve activity — without needing to read complicated charts.
            </p>
          </div>
          <div class="card">
            <h3>PDF report for appointments</h3>
            <p>
              Export a clean PDF with charts and key stats so your care team can review your recovery between visits or use it during follow-ups.
            </p>
          </div>
        </div>
      </section>

      <!-- SCREENSHOTS -->
      <section>
        <h2 class="section-title">Screenshots</h2>
        <div class="screenshots">
          <div class="shot">
            <img src="images/screenshot-today.png" alt="Recoverly Today view showing daily pain and activity sliders." />
            <div class="shot-caption">See today’s pain and activity at a glance.</div>
          </div>

          <div class="shot">
            <img src="images/screenshot-today-zoom.png" alt="Close-up of Recoverly pain sliders and labels." />
            <div class="shot-caption">Track pain, tingling, spasms, and activity in seconds.</div>
          </div>

          <div class="shot">
            <img src="images/screenshot-history.png" alt="Recoverly History view with calendar and recent days." />
            <div class="shot-caption">Spot good days, tough days, and patterns in your calendar.</div>
          </div>

          <div class="shot">
            <img src="images/screenshot-insights.png" alt="Recoverly Insights view showing weekly trends for pain and mobility." />
            <div class="shot-caption">Simple weekly trends for pain, mobility, and nerve activity.</div>
          </div>

          <div class="shot">
            <img src="images/screenshot-pdf.png" alt="Recoverly PDF export preview with charts and stats." />
            <div class="shot-caption">Export a detailed PDF report for your care team.</div>
          </div>
        </div>
      </section>

      <!-- FOOTER -->
      <footer>
        <div>© <span id="year"></span> Recoverly — Back &amp; Nerve Recovery Tracker</div>
        <div class="footer-links">
          <a href="https://richr44.github.io/recoverly-privacy/">Privacy policy</a>
          <span>·</span>
          <a href="mailto:getrecoverly@gmail.com">Support: getrecoverly@gmail.com</a>
        </div>
      </footer>

    </main>
  </div>

  <script>
    // Set current year in footer
    document.getElementById('year').textContent = new Date().getFullYear();
  </script>
</body>
</html>
