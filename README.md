---
layout: null
permalink: /
---

<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="theme-color" content="#f4f5f3">
  <title>Edeline Ohk</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Nunito+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">

  <script>
    try {
      if (localStorage.getItem("edeline-theme") === "night") {
        document.documentElement.dataset.theme = "night";
      }
    } catch {}
  </script>

  <style>
    :root {
      color-scheme: light;
      --background: #f4f5f3;
      --text: #656c74;
      --link: #3159a3;
      --button: #e5e7eb;
      --highlight: #e2e8e2;
      --border: #cdd4cf;
      --accent: #bac8bd;
      --font: "Nunito Sans", sans-serif;
    }

    :root[data-theme="night"] {
      color-scheme: dark;
      --background: #1c2230;
      --text: #d9dfdc;
      --link: #cad4ce;
      --button: #363d45;
      --highlight: #303b34;
      --border: #394052;
      --accent: #bac8bd;
    }

    * { box-sizing: border-box; }

    html, body {
      margin: 0;
      padding: 0;
      background: var(--background);
      color: var(--text);
      font-family: var(--font);
    }

    body {
      min-height: 100vh;
      transition: background .3s, color .3s;
    }

    button {
      font: inherit;
      color: inherit;
      cursor: pointer;
    }

    a { color: var(--link); }

    button:focus-visible, a:focus-visible {
      outline: 2px solid var(--text);
      outline-offset: 5px;
    }

    ::selection { background: var(--highlight); }

    .skip {
      position: absolute;
      top: -80px;
      left: 16px;
      padding: 12px;
      background: var(--background);
      z-index: 10;
    }

    .skip:focus { top: 12px; }

    .shell {
      width: 100%;
      max-width: 1060px;
      margin: auto;
      padding: 38px 50px 28px;
    }

    .hero {
      text-align: center;
      padding: 67px 0 36px;
    }

    h1 {
      font-size: clamp(3.2rem, 7vw, 5.1rem);
      line-height: 1.1;
      font-weight: 700;
      letter-spacing: -.055em;
      margin: 0 0 30px;
    }

    .nav {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 8px;
    }

    .nav-btn {
      position: relative;
      border: 0;
      border-radius: 7px;
      background: transparent;
      color: var(--text);
      padding: 10px 18px;
      font-size: 14px;
      transition: background .2s, transform .25s;
    }

    .nav-btn:hover {
      background: var(--button);
      transform: translateY(-2px);
    }

    .nav-btn[aria-selected="true"] {
      background: var(--button);
      color: var(--text);
    }

    .nav-btn[aria-selected="true"]::after {
      content: "";
      position: absolute;
      bottom: -7px;
      left: calc(50% - 2px);
      width: 4px;
      height: 4px;
      border-radius: 50%;
      background: var(--text);
    }

    main { margin: 30px 0 68px; }

    .section {
      max-width: 660px;
      margin: auto;
      animation: arrive .35s ease;
    }

    .section[hidden] { display: none; }

    @keyframes arrive {
      from { opacity: 0; transform: translateY(7px); }
      to { opacity: 1; transform: translateY(0); }
    }

    h2 {
      font-size: 28px;
      line-height: 1.25;
      font-weight: 700;
      letter-spacing: -.035em;
      margin: 0 0 24px;
    }

    p {
      font-size: 17px;
      line-height: 1.85;
      margin: 0 0 21px;
    }

    .greeting {
      position: relative;
      display: inline-block;
      isolation: isolate;
    }

    .greeting::after {
      content: "";
      position: absolute;
      left: -2px;
      right: -2px;
      bottom: 1px;
      height: 7px;
      border-radius: 50%;
      background: var(--highlight);
      z-index: -1;
    }

    .contact-links {
      display: flex;
      gap: 26px;
      margin-top: 30px;
    }

    .text-link {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      font-size: 14px;
      text-decoration: none;
    }

    .text-link span:first-child {
      border-bottom: 1px solid var(--border);
      padding-bottom: 3px;
    }

    .arrow {
      display: inline-block;
      transition: transform .35s cubic-bezier(.22, 1.7, .5, 1);
    }

    .text-link:hover .arrow {
      transform: translateX(4px) scaleX(1.25) scaleY(.8);
    }

    .simple-section { min-height: 315px; }

    .empty-note {
      margin-top: 28px;
      padding-top: 22px;
      border-top: 1px solid var(--border);
      font-size: 14px;
    }

    .small-label {
      display: block;
      margin-bottom: 8px;
      font-size: 10px;
      letter-spacing: .1em;
      text-transform: uppercase;
    }

    footer {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 20px;
      border-top: 1px solid var(--border);
      padding-top: 21px;
      font-size: 11px;
    }

    .footer-mark {
      color: var(--accent);
      margin-right: 7px;
    }

    .footer-tools {
      display: flex;
      align-items: center;
      gap: 16px;
    }

    .clock { font-variant-numeric: tabular-nums; }

    .theme-toggle {
      display: grid;
      place-items: center;
      width: 30px;
      height: 30px;
      padding: 0;
      border: 1px solid var(--border);
      border-radius: 50%;
      background: transparent;
    }

    .theme-toggle svg {
      width: 19px;
      height: 19px;
      transition: transform .6s;
    }

    .theme-toggle:hover svg { transform: rotate(35deg); }

    .moon { display: none; }
    [data-theme="night"] .sun { display: none; }
    [data-theme="night"] .moon { display: block; }

    @media (max-width: 800px) {
      .shell { padding: 28px 28px 24px; }
      .hero { padding-top: 50px; }
    }

    @media (max-width: 620px) {
      .shell { padding: 22px 23px; }
      .hero { padding: 45px 0 24px; }
      h1 { font-size: 3.2rem; }
      .nav-btn { padding: 10px 13px; }
      main { margin-top: 24px; margin-bottom: 42px; }
      p { font-size: 16px; }
      footer { font-size: 9px; gap: 12px; }
      .simple-section { min-height: 250px; }
    }

    @media (prefers-reduced-motion: reduce) {
      *, *::before, *::after {
        animation: none !important;
        transition: none !important;
      }
    }
  </style>
</head>

<body>
  <a class="skip" href="#main">Skip to content</a>

  <div class="shell">
    <div class="hero">
      <h1>Edeline Ohk</h1>

      <nav class="nav" role="tablist" aria-label="Explore my website">
        <button type="button" class="nav-btn" id="tab-about"
          role="tab" data-section="about" aria-controls="about"
          aria-selected="true">About</button>

        <button type="button" class="nav-btn" id="tab-projects"
          role="tab" data-section="projects" aria-controls="projects"
          aria-selected="false" tabindex="-1">Projects</button>

        <button type="button" class="nav-btn" id="tab-writing"
          role="tab" data-section="writing" aria-controls="writing"
          aria-selected="false" tabindex="-1">Writing</button>

        <button type="button" class="nav-btn" id="tab-resume"
          role="tab" data-section="resume" aria-controls="resume"
          aria-selected="false" tabindex="-1">Resume</button>
      </nav>
    </div>

    <main id="main">
      <section class="section" id="about" role="tabpanel"
        aria-labelledby="tab-about" tabindex="0">
        <h2><span class="greeting">Hi, I’m Edeline!</span></h2>

        <p>
          I study Politics and International Relations at the University
          of Melbourne. Alongside university, I’ve worked across the
          Australian Government in Washington, D.C., at the Australian
          Embassy, and in Canberra, where I’m from.
        </p>

        <p>
          I’m especially interested in how Australia navigates the
          international questions shaping our time, from supply security
          in a new technological and climate era to migration, borders
          and sovereignty. Currently, when I’m not doing school work,
          I enjoy some creative labour and local history. Here you’ll
          find some of my projects and my resume. Thanks for stopping by!
        </p>

        <div class="contact-links">
          <a class="text-link"
            href="https://www.linkedin.com/in/edeline-ohk111"
            target="_blank" rel="noopener noreferrer">
            <span>LinkedIn</span>
            <span class="arrow" aria-hidden="true">↗</span>
          </a>

          <a class="text-link" href="mailto:ohkedeline@gmail.com">
            <span>Email</span>
            <span class="arrow" aria-hidden="true">↗</span>
          </a>
        </div>
      </section>

      <section class="section simple-section" id="projects"
        role="tabpanel" aria-labelledby="tab-projects"
        tabindex="0" hidden>
        <h2>Projects</h2>
        <p>Here are some projects I've worked on:</p>
        <p class="empty-note">Project details coming soon.</p>
      </section>

      <section class="section simple-section" id="writing"
        role="tabpanel" aria-labelledby="tab-writing"
        tabindex="0" hidden>
        <h2>Writing</h2>
        <p>I occasionally write about politics, history and international affairs.</p>
        <p class="empty-note">Writing will be added here soon.</p>
      </section>

      <section class="section simple-section" id="resume"
        role="tabpanel" aria-labelledby="tab-resume"
        tabindex="0" hidden>
        <h2>Resume</h2>
        <p>
          My experience spans government, international affairs,
          research and public administration.
        </p>
        <p>
          <span class="small-label">Education</span>
          University of Melbourne
        </p>
        <p class="empty-note">
          For a copy of my resume, please get in touch.
        </p>
        <a class="text-link"
          href="mailto:ohkedeline@gmail.com?subject=Resume%20enquiry">
          <span>Request my resume</span>
          <span class="arrow" aria-hidden="true">↗</span>
        </a>
      </section>
    </main>

    <footer>
      <span>
        <span class="footer-mark" aria-hidden="true">✳</span>
        Edeline Ohk
      </span>

      <div class="footer-tools">
        <span>
          Melbourne
          <time class="clock" aria-label="Current time in Melbourne"></time>
        </span>

        <button class="theme-toggle" type="button"
          aria-label="Switch to night mode">
          <svg class="sun" viewBox="0 0 24 24" fill="none"
            stroke="currentColor" stroke-width="1.5" aria-hidden="true">
            <circle cx="12" cy="12" r="4"/>
            <path d="M12 1v3m0 16v3M1 12h3m16 0h3M4.2 4.2l2.1 2.1m11.4 11.4l2.1 2.1M4.2 19.8l2.1-2.1M17.7 6.3l2.1-2.1"/>
          </svg>

          <svg class="moon" viewBox="0 0 24 24" fill="none"
            stroke="currentColor" stroke-width="1.5" aria-hidden="true">
            <path d="M21 14A9 9 0 0 1 10 3a9 9 0 1 0 11 11Z"/>
            <path d="M18 2v6m-3-3h6"/>
          </svg>
        </button>
      </div>
    </footer>
  </div>

  <script>
    const tabs = [...document.querySelectorAll('[role="tab"]')];
    const panels = [...document.querySelectorAll('[role="tabpanel"]')];

    function selectSection(id, updateURL = true) {
      if (!tabs.some(tab => tab.dataset.section === id)) {
        id = "about";
      }

      tabs.forEach(tab => {
        const active = tab.dataset.section === id;
        tab.setAttribute("aria-selected", String(active));
        tab.tabIndex = active ? 0 : -1;
      });

      panels.forEach(panel => {
        panel.hidden = panel.id !== id;
      });

      if (updateURL) {
        history.replaceState(null, "", "#" + id);
      }
    }

    tabs.forEach((tab, index) => {
      tab.addEventListener("click", () => {
        selectSection(tab.dataset.section);
      });

      tab.addEventListener("keydown", event => {
        let next;

        if (event.key === "ArrowRight") {
          next = (index + 1) % tabs.length;
        } else if (event.key === "ArrowLeft") {
          next = (index + tabs.length - 1) % tabs.length;
        } else if (event.key === "Home") {
          next = 0;
        } else if (event.key === "End") {
          next = tabs.length - 1;
        } else {
          return;
        }

        event.preventDefault();
        tabs[next].focus();
        selectSection(tabs[next].dataset.section);
      });
    });

    window.addEventListener("hashchange", () => {
      selectSection(location.hash.slice(1), false);
    });

    selectSection(location.hash.slice(1), false);

    const themeButton = document.querySelector(".theme-toggle");

    function updateThemeLabel() {
      const night = document.documentElement.dataset.theme === "night";
      themeButton.setAttribute(
        "aria-label",
        night ? "Switch to day mode" : "Switch to night mode"
      );
    }

    updateThemeLabel();

    themeButton.addEventListener("click", () => {
      const theme =
        document.documentElement.dataset.theme === "night"
          ? "day"
          : "night";

      document.documentElement.dataset.theme = theme;

      document.querySelector('meta[name="theme-color"]').content =
        theme === "night" ? "#1c2230" : "#f4f5f3";

      try {
        localStorage.setItem("edeline-theme", theme);
      } catch {}

      updateThemeLabel();
    });

    function updateClock() {
      const now = new Date();
      const clock = document.querySelector(".clock");

      clock.textContent = new Intl.DateTimeFormat("en-AU", {
        timeZone: "Australia/Melbourne",
        hour: "2-digit",
        minute: "2-digit",
        hour12: false
      }).format(now);

      clock.dateTime = now.toISOString();
    }

    updateClock();
    setInterval(updateClock, 60000);
  </script>
</body>
</html>
