<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Recoverly — Back &amp; Nerve Recovery Tracker</title>

  <style>
    :root {
      --bg: #050810;
      --card-bg: #0e111a;
      --accent: #3b82f6;
      --accent-soft: rgba(59,130,246,0.14);
      --text-main: #f9fafb;
      --text-muted: #9ca3af;
      --pill-bg: rgba(15,23,42,0.9);
      --shadow-soft: 0 18px 45px rgba(0,0,0,0.65);
      --radius-lg: 24px;
      --radius-pill: 999px;
      --max-width: 960px;
    }

    * { box-sizing: border-box; }
    body {
      margin: 0;
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "SF Pro Text",
                   -webkit-system-font, sans-serif;
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
      box-shadow: var(--shadow-soft);
      border-radius: var(--radius-lg);
      background: linear-gradient(145deg, #020617 0%, #020617 52%, #020308 100%);
      border: 1px solid rgba(148,163,184,0.30);
      overflow: hidden;
    }

    header.hero {
      display: grid;
      grid-template-columns: minmax(0, 1.2fr) minmax(0, 1fr);
      gap: 32px;
      align-items: center;
      padding: 28px 24px 8px;
    }

    @media (max-width: 840px) {
      header.hero {
        grid-template-columns: minmax(0,1fr);
        padding: 24px 20px 12px;
      }
    }

    .hero-kicker {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 6px 12px;
      border-radius: var(--radius-pill);
      background: linear-gradient(90deg, rgba(37,99,235,0.20), rgba(59,130,246,0));
      border: 1px solid rgba(148,163,184,0.35);
      font-size: 12px;
      color: var(--text-muted);
      letter-spacing: 0.08em;
      text-transform: uppercase;
    }

    .dot {
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
      margin: 0 0 18px;
    }

    .hero-meta {
      display: flex;
      flex-wrap: wrap;
      gap: 10px 18px;
      align-items: center;
      font-size: 13px;
      color: var(--text-muted);
    }

    .hero-meta span.badge {
      padding: 4px 10px;
      border-radius: 999px;
      background: rgba(15,23,42,0.95);
      border: 1px solid rgba(148,163,184,0.40);
      font-size: 11px;
      letter-spacing: 0.08em;
      text-transform: uppercase;
    }

    .cta-row {
      display: flex;
      flex-wrap: wrap;
      gap: 10px 14px;
      margin-top: 20px;
    }

    .cta-primary {
      border-radius: 16px;
      padding: 10px 18px;
      border: none;
      background: linear-gradient(135deg, #3b82f6, #22c55e);
      color: #0b1020;
      font-weight: 600;
      font-size: 14px;
      cursor: pointer;
      display: inline-flex;
      align-items: center;
      gap: 8px;
      box-shadow: 0 14px 35px rgba(37,99,235,0.45);
    }

    .cta-secondary {
      border-radius: 999px;
      padding: 9px 16px;
      font-size: 13px;
      color: var(--text-muted);
      border: 1px solid rgba(148,163,184,0.45);
      background: rgba(15,23,42,0.9);
    }

    main {
      display: grid;
      grid-template-columns: minmax(0,1fr) minmax(0,0.9fr);
      gap: 24px;
      padding: 12px 24px 24px;
    }

    @media (max-width: 840px) {
      main {
        grid-template-columns: minmax(0,1fr);
        padding: 0 20px 20px;
      }
    }

    section {
      background: radial-gradient(circle at top, #111827 0, #020617 70%);
      border-radius: 20px;
      padding: 16px 16px 14px;
      border: 1px solid rgba(148,163,184,0.30);
    }

    section h2 {
      font-size: 16px;
      margin: 0 0 6px;
    }

    section p {
      margin: 0 0 10px;
      font-size: 13px;
      line-height: 1.6;
      color: var(--text-muted);
    }

    ul.feature-list {
      list-style: none;
      padding: 0;
      margin: 8px 0 0;
      font-size: 13px;
      color: var(--text-muted);
    }

    ul.feature-list li {
      display: flex;
      align-items: flex-start;
      gap: 8px;
      margin-bottom: 6px;
    }

    .check {
      width: 14px;
      height: 14px;
      border-radius: 999px;
      background: rgba(34,197,94,0.12);
      border: 1px solid #22c55e;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      font-size: 10px;
      color: #22c55e;
      flex-shrink: 0;
      margin-top: 2px;
    }

    footer {
      padding: 10px 24px 18px;
      font-size: 11px;
      color: #6b7280;
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      justify-content: space-between;
      align-items: center;
    }

    footer a {
      color: #9ca3af;
      text-decoration: none;
      border-bottom: 1px dashed rgba(156,163,175,0.6);
    }

    footer a:hover {
      color: var(--accent);
      border-bottom-style: solid;
    }
  </style>
</head>

<body>
  <div class="page">
    <div class="shell">
      <header class="hero">
        <div>
          <div class="hero-kicker">
            <span class="dot"></span>
            <span>Built for spine &amp; nerve recovery</span>
          </div>
          <h1>
            Recovery you can <span class="accent">see</span> —
            without guessing what’s “normal”.
          </h1>
          <p class="tagline">
            Recoverly helps you track back pain, leg nerve symptoms, and daily
            activity so you can understand your recovery after lumbar or nerve
            surgery and bring clear data to your follow-up visits.
          </p>

          <div class="hero-meta">
            <span class="badge">Post-surgery friendly</span>
            <span class="badge">No account required</span>
            <span>Designed by a real spine-surgery patient.</span>
          </div>

          <div class="cta-row">
            <button class="cta-primary" type="button">
              Coming soon on the App Store
            </button>
            <button class="cta-secondary" type="button">
              Get email updates (coming soon)
            </button>
          </div>
        </div>

        <div>
          <section>
            <h2>Why Recoverly?</h2>
            <p>
              The first weeks after surgery blur together. Was today better than
              last Tuesday? Are tingling and spasms easing up, or just moving
              around? Recoverly turns those “I think so…” answers into clear
              trends.
            </p>
            <ul class="feature-list">
              <li>
                <span class="check">✓</span>
                <span>Built around common lumbar and nerve symptoms:
                  back pain, hip/glute pain, leg nerve pain, tingling,
                  and spasms.</span>
              </li>
              <li>
                <span class="check">✓</span>
                <span>Track walking and sitting tolerance so you can see how
                  activity changes week to week.</span>
              </li>
              <li>
                <span class="check">✓</span>
                <span>Designed to be used once a day in under a minute.</span>
              </li>
            </ul>
          </section>
        </div>
      </header>

      <main>
        <section>
          <h2>Understand your days, not just your pain score.</h2>
          <p>
            Recoverly doesn’t try to replace your surgeon or physical therapist.
            It gives you a simple way to see:
          </p>
          <ul class="feature-list">
            <li>
              <span class="check">✓</span>
              <span>Which days felt like “overdoing it” and what you did
                beforehand.</span>
            </li>
            <li>
              <span class="check">✓</span>
              <span>How pain and nerve symptoms compare to last week.</span>
            </li>
            <li>
              <span class="check">✓</span>
              <span>Your walking and sitting trends over time.</span>
            </li>
          </ul>
        </section>

        <section>
          <h2>Share a clean report with your care team.</h2>
          <p>
            When you’re ready for a follow-up, Recoverly can generate a clear
            PDF summary of your symptoms and activity to bring to your visit.
          </p>
          <ul class="feature-list">
            <li>
              <span class="check">✓</span>
              <span>Weekly charts for pain, nerve symptoms, and activity.</span>
            </li>
            <li>
              <span class="check">✓</span>
              <span>Plain-language summaries you can review together.</span>
            </li>
            <li>
              <span class="check">✓</span>
              <span>Designed for laminectomy, discectomy, fusion, and other
                lumbar procedures.</span>
            </li>
          </ul>
        </section>
      </main>

      <footer>
        <span>© <span id="year"></span> Recoverly. All rights reserved.</span>
        <span>
          Privacy policy:
          <a href="https://richr44.github.io/recoverly-privacy/" target="_blank" rel="noopener">
            richr44.github.io/recoverly-privacy
          </a>
        </span>
      </footer>
    </div>
  </div>

  <script>
    document.getElementById("year").textContent = new Date().getFullYear();
  </script>
</body>
</html>
