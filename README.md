<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Edeline Ohk</title>

  <style>
    :root {
      --globe-cursor: url("data:image/svg+xml,%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20width%3D%2232%22%20height%3D%2232%22%20viewBox%3D%220%200%2032%2032%22%3E%3Ccircle%20cx%3D%2216%22%20cy%3D%2216%22%20r%3D%2213%22%20fill%3D%22white%22%20stroke%3D%22white%22%20stroke-width%3D%224%22%2F%3E%3Cg%20fill%3D%22none%22%20stroke%3D%22black%22%20stroke-width%3D%221.4%22%3E%3Ccircle%20cx%3D%2216%22%20cy%3D%2216%22%20r%3D%2212%22%2F%3E%3Cellipse%20cx%3D%2216%22%20cy%3D%2216%22%20rx%3D%226%22%20ry%3D%2212%22%2F%3E%3Cpath%20d%3D%22M4%2016h24M6%209q10%206%2020%200M6%2023q10-6%2020%200%22%2F%3E%3C%2Fg%3E%3C%2Fsvg%3E") 16 16;
    }

    * {
      box-sizing: border-box;
    }

    html,
    body {
      margin: 0;
      padding: 0;
    }

    body {
      background: #ffffff;
      color: #000000;
      font-family: "Lucida Sans Unicode", "Lucida Grande", sans-serif;
      font-size: 16px;
      font-weight: 400;
    }

    button {
      font: inherit;
      color: inherit;
      cursor: pointer;
    }

    a {
      color: #000000;
    }

    a:focus-visible {
      outline: 2px solid #000000;
      outline-offset: 4px;
    }

    ::selection {
      background: #dddddd;
      color: #000000;
    }

    .shell {
      max-width: 850px;
      margin: auto;
      padding: 18px 24px 70px;
    }

    .header {
      text-align: center;
    }

    h1 {
      font-size: 40px;
      line-height: 1.25;
      font-weight: 500;
      letter-spacing: 1px;
      margin: 0 0 24px;
    }

    .nav {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 16px;
    }

    main {
      max-width: 600px;
      margin: 50px auto 0;
    }

    .section[hidden] {
      display: none;
    }

    h2 {
      font-size: 24px;
      line-height: 1.3;
      font-weight: 500;
      margin: 0 0 20px;
    }

    p {
      font-size: 16px;
      line-height: 1.55;
      margin: 0 0 20px;
    }

    .links {
      display: flex;
      flex-wrap: wrap;
      gap: 16px;
      margin-top: 36px;
    }

    .resume-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 16px;
      margin: 24px 0;
    }

    /* Shared button appearance */
    .nav-btn,
    .links a,
    .resume-actions a,
    .project-details summary {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      width: fit-content;
      min-height: 44px;
      padding: 10px 16px;
      border: 3px solid #000000;
      border-radius: 4px;
      background: #ffffff;
      color: #000000;
      box-shadow: 4px 4px 0 #000000;
      font-family: inherit;
      font-size: 14px;
      font-weight: 600;
      line-height: 1.3;
      letter-spacing: 0;
      text-decoration: none;
      transition:
        transform 180ms ease,
        box-shadow 180ms ease,
        background-color 180ms ease;
    }

    .nav-btn {
      min-width: 96px;
    }

    /* Expandable project buttons */
    .project-details summary {
      list-style: none;
      cursor: pointer;
    }

    .project-details summary::-webkit-details-marker {
      display: none;
    }

    .project-details summary::after {
      content: "+";
      margin-left: 14px;
      font-size: 18px;
      line-height: 1;
    }

    .project-details[open] > summary::after {
      content: "−";
    }

    /* Selected tab and open project */
    .nav-btn[aria-selected="true"],
    .project-details[open] > summary {
      background: #eeeeee;
      transform: translate(2px, 2px);
      box-shadow: 2px 2px 0 #000000;
    }

    /* Hover: move into the shadow */
    @media (hover: hover) {
      .nav-btn:hover,
      .links a:hover,
      .resume-actions a:hover,
      .project-details summary:hover {
        background: #eeeeee;
        transform: translate(2px, 2px);
        box-shadow: 2px 2px 0 #000000;
      }
    }

    /* Click: fully press the button */
    .nav-btn:active,
    .links a:active,
    .resume-actions a:active,
    .project-details summary:active {
      transform: translate(4px, 4px);
      box-shadow: 0 0 0 #000000;
      background: #dddddd;
    }

    /* Keyboard navigation */
    .nav-btn:focus-visible,
    .links a:focus-visible,
    .resume-actions a:focus-visible,
    .project-details summary:focus-visible {
      outline: 2px dashed #000000;
      outline-offset: 6px;
    }

    .project-card {
      border: 1px solid #e5e5e5;
      border-radius: 8px;
      padding: 24px;
      box-shadow: 0 3px 8px rgba(0, 0, 0, 0.04);
      background: #ffffff;
    }

    .project-card + .project-card {
      margin-top: 24px;
    }

    .project-card h3 {
      font-size: 20px;
      line-height: 1.4;
      font-weight: 500;
      margin: 0 0 7px;
    }

    .project-card .project-date {
      color: #666666;
      font-size: 13px;
      margin: 0 0 18px;
    }

    .project-activities {
      padding-top: 24px;
    }

    .project-activities h4 {
      font-size: 16px;
      font-weight: 600;
      line-height: 1.5;
      margin: 24px 0 10px;
    }

    .project-activities h4:first-child {
      margin-top: 0;
    }

    .project-activities p:last-child {
      margin-bottom: 0;
    }

    .art-gallery {
      display: grid;
      gap: 28px;
      margin-top: 24px;
    }

    .art-gallery figure {
      margin: 0;
    }

    .art-gallery img {
      display: block;
      width: auto;
      height: auto;
      max-width: 100%;
      max-height: 560px;
      margin: 0 auto;
    }

    .art-gallery figcaption {
      font-size: 14px;
      line-height: 1.6;
      margin-top: 14px;
    }

    .resume-preview {
      display: block;
      width: 100%;
      height: 720px;
      border: 1px solid #e5e5e5;
      background: #ffffff;
    }

    /* Globe cursor */
    @media (hover: hover) and (pointer: fine) {
      html,
      body {
        cursor: var(--globe-cursor), auto;
      }

      button,
      a,
      .project-details summary {
        cursor: var(--globe-cursor), pointer;
      }
    }

    /* Respect reduced-motion preferences */
    @media (prefers-reduced-motion: reduce) {
      .nav-btn,
      .links a,
      .resume-actions a,
      .project-details summary {
        transition: none;
        transform: none !important;
      }
    }

    @media (max-width: 600px) {
      .shell {
        padding: 25px 22px 50px;
      }

      h1 {
        font-size: 34px;
      }

      .nav {
        gap: 12px;
      }

      .nav-btn {
        min-width: 86px;
        padding: 9px 12px;
      }

      main {
        margin-top: 40px;
      }

      h2 {
        font-size: 22px;
      }

      .project-card {
        padding: 20px;
      }
    }
  </style>
</head>

<body>
  <div class="shell">
    <header class="header">
      <h1>Edeline Ohk</h1>

      <nav class="nav" role="tablist" aria-label="Website sections">
        <button
          type="button"
          class="nav-btn"
          id="tab-about"
          role="tab"
          data-section="about"
          aria-controls="about"
          aria-selected="true"
        >About</button>

        <button
          type="button"
          class="nav-btn"
          id="tab-projects"
          role="tab"
          data-section="projects"
          aria-controls="projects"
          aria-selected="false"
          tabindex="-1"
        >Projects</button>

        <button
          type="button"
          class="nav-btn"
          id="tab-resume"
          role="tab"
          data-section="resume"
          aria-controls="resume"
          aria-selected="false"
          tabindex="-1"
        >Resume</button>
      </nav>
    </header>

    <main>
      <section
        class="section"
        id="about"
        role="tabpanel"
        aria-labelledby="tab-about"
        tabindex="0"
      >
        <h2>Hi, I’m Edeline!</h2>

        <p>
          I study Politics and International Affairs at the University
          of Melbourne. Before university, I worked for the Australian
          Government in Canberra and Washington, D.C., across public
          administration, trade and economic security.
        </p>

        <p>
          I’m especially interested in how Australia navigates the
          international questions shaping our time, from supply security
          in a new technological and climate era to migration, borders
          and sovereignty. Currently, when I’m not doing school work,
          I enjoy some creative labour and local history. Here you’ll
          find some of my projects and my resume. Thanks for stopping by!
        </p>

        <div class="links">
          <a
            href="https://www.linkedin.com/in/edeline-ohk111"
            target="_blank"
            rel="noopener noreferrer"
          >LinkedIn</a>

          <a href="mailto:ohkedeline@gmail.com">Email</a>
        </div>
      </section>

      <section
        class="section"
        id="projects"
        role="tabpanel"
        aria-labelledby="tab-projects"
        tabindex="0"
        hidden
      >
        <h2>Projects</h2>

        <article class="project-card">
          <h3>Returning to university life</h3>
          <p class="project-date">2027 – Ongoing</p>

          <p>
            Returning to university after full-time work has been an
            adjustment. I had forgotten, among other things, that 10AM
            can constitute an early start! Still, university has left me
            with the luxury of a little more time, which I have been
            filling with various projects, questionable commitments,
            and the occasional attempt at becoming a well-rounded person.
            Here is what I have been getting up to.
          </p>

          <details class="project-details">
            <summary>Read more</summary>

            <div class="project-activities">
              <h4>
                Marketing Director, University of Melbourne Matcha Club
              </h4>

              <p>
                The club’s Instagram has grown from zero to more than
                1,000 followers, alongside a community of over 300 members.
                What drew me in, though, was its hilariously unserious
                premise of bringing people together over a drink they love.
                An entire club whose entire ideological programme amounts
                to having a nice free drink felt like a great counterweight
                to a politics degree (satirical).
              </p>

              <h4>
                Events Officer, Young Australians in International Affairs
                (YAIYA)
              </h4>

              <p>
                I have also taken on an Events Officer role. Australia’s
                voice matters, and I want to understand more clearly what
                we ought to do with it. The role gives me the chance to
                bring together people thinking about the same questions,
                while surrounding myself with peers who care just as much
                about international affairs and what Australia can
                contribute to them.
              </p>

              <h4>Neighbourhood dog walking</h4>

              <p>
                Solomon, a Chihuahua–Jack Russell mix, and Maggie, an
                Australian Cattle Dog mix, keep me company on our
                twice-weekly, hour-long walks. They bring affection,
                enthusiasm and a rigorous peer-review process to every
                tree. Their priorities are admirably clear, and their
                approach to networking considerably more direct than mine.
              </p>

              <h4>Volunteer English Tutor, Embrace Education</h4>

              <p>
                With a little more time on my hands, I also wanted to
                use some of it to give back to the community around me.
              </p>
            </div>
          </details>
        </article>

        <article class="project-card">
          <h3>Art portfolio</h3>
          <p class="project-date">2021 – onwards</p>

          <p>
            A digital showroom of curiosities for my visual projects,
            from paintings and sketches to sculptures and photographs.
            Entirely for fun.
          </p>

          <details class="project-details">
            <summary>View artworks</summary>

            <div class="art-gallery">
              <figure>
                <a
                  href="sanso.png"
                  target="_blank"
                  rel="noopener noreferrer"
                  aria-label="Open the chopstick sculpture image"
                >
                  <img
                    src="sanso.png"
                    loading="lazy"
                    alt="Three views of a rounded sculpture made from densely arranged chopsticks."
                  >
                </a>

                <figcaption>
                  Inspired by Rosalie Gascoigne, I used chopsticks to
                  evoke the form of a Korean ancestral gravesite, or
                  <em>sanso</em> (산소).
                </figcaption>
              </figure>

              <figure>
                <a
                  href="caravaggio-fillide.png"
                  target="_blank"
                  rel="noopener noreferrer"
                  aria-label="Open the painting of Caravaggio and Fillide Melandroni"
                >
                  <img
                    src="caravaggio-fillide.png"
                    loading="lazy"
                    alt="Painting of two figures together against a dark background, with one holding a white flower."
                  >
                </a>

                <figcaption>
                  Painted Caravaggio alongside Fillide Melandroni,
                  one of his favourite muses.
                </figcaption>
              </figure>

              <figure>
                <a
                  href="politician-portrait.png"
                  target="_blank"
                  rel="noopener noreferrer"
                  aria-label="Open the portrait in the style of Egon Schiele"
                >
                  <img
                    src="politician-portrait.png"
                    loading="lazy"
                    alt="Tall painted portrait of a bespectacled figure with an exposed torso and a red lower garment."
                  >
                </a>

                <figcaption>
                  Large portraiture of a politician (produced for class)
                  in the style of Egon Schiele.
                </figcaption>
              </figure>
            </div>
          </details>
        </article>
      </section>

      <section
        class="section"
        id="resume"
        role="tabpanel"
        aria-labelledby="tab-resume"
        tabindex="0"
        hidden
      >
        <h2>Resume</h2>

        <p>
          I have some experience across government, international affairs,
          research and public administration.
        </p>

        <div class="resume-actions">
          <a
            href="resume%20(3).pdf"
            target="_blank"
            rel="noopener noreferrer"
          >View resume</a>

          <a
            href="resume%20(3).pdf"
            download="Edeline-Ohk-Resume.pdf"
          >Download resume</a>
        </div>

        <iframe
          class="resume-preview"
          src="resume%20(3).pdf#view=FitH"
          title="Edeline Ohk’s resume"
          loading="lazy"
        ></iframe>
      </section>
    </main>
  </div>

  <script>
    const tabs = [...document.querySelectorAll('[role="tab"]')];
    const panels = [...document.querySelectorAll('[role="tabpanel"]')];

    function showSection(id, updateURL = true) {
      if (!tabs.some(tab => tab.dataset.section === id)) {
        id = "about";
      }

      tabs.forEach(tab => {
        const selected = tab.dataset.section === id;
        tab.setAttribute("aria-selected", String(selected));
        tab.tabIndex = selected ? 0 : -1;
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
        showSection(tab.dataset.section);
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
        showSection(tabs[next].dataset.section);
      });
    });

    window.addEventListener("hashchange", () => {
      showSection(location.hash.slice(1), false);
    });

    showSection(location.hash.slice(1), false);
  </script>
</body>
</html>
