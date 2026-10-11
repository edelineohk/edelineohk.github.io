
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Edeline Ohk</title>
    <style>
      * {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
      }

      html, body {
        font-family: -apple-system, BlinkMacSystemFont, "JetBrains Mono", "Inter", JetBrains Mono;
        background: #FDFBDQ;
        color: #1a1a1a;
      }

      body {
        min-height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 40px 20px;
      }

      .container {
        width: 100%;
        max-width: 900px;
      }

      .header {
        text-align: center;
        margin-bottom: 50px;
      }

      .name {
        font-size: clamp(3.5rem, 6vw, 5.5rem);
        font-weight: 600;
        letter-spacing: -0.05em;
        line-height: 1;
        margin-bottom: 30px;
      }

      .nav {
        display: flex;
        justify-content: center;
        gap: 12px;
        flex-wrap: wrap;
        margin-bottom: 50px;
      }

      .nav-btn {
        padding: 10px 20px;
        background: transparent;
        border: 1px solid #ddd;
        border-radius: 4px;
        font-size: 16px;
        cursor: pointer;
        transition: all 0.2s ease;
        color: #1a1a1a;
        font-family: inherit;
      }

      .nav-btn.active {
        background: #7bb8f0;
        border-color: #7bb8f0;
        color: white;
      }

      .nav-btn:hover {
        border-color: #999;
      }

      .content {
        max-width: 700px;
        margin: 0 auto;
      }

      .section {
        display: none;
      }

      .section.active {
        display: block;
        animation: fadeIn 0.3s ease;
      }

      @keyframes fadeIn {
        from {
          opacity: 0;
          transform: translateY(10px);
        }
        to {
          opacity: 1;
          transform: translateY(0);
        }
      }

      h2 {
        font-size: 2rem;
        margin-bottom: 20px;
        font-weight: 500;
      }

      p {
        font-size: 1.1rem;
        line-height: 1.7;
        margin-bottom: 16px;
        color: #333;
      }

      .links {
        margin-top: 30px;
        display: flex;
        flex-direction: column;
        gap: 10px;
      }

      a {
        color: #1a1a1a;
        text-decoration: none;
        font-size: 1.1rem;
        padding-bottom: 2px;
        border-bottom: 1px solid transparent;
        width: fit-content;
        transition: border-color 0.2s ease;
      }

      a:hover {
        border-bottom-color: #1a1a1a;
      }

      @media (max-width: 600px) {
        body {
          padding: 30px 20px;
        }

        .name {
          font-size: 2.8rem;
        }

        .nav {
          gap: 8px;
        }

        .nav-btn {
          padding: 8px 16px;
          font-size: 15px;
        }

        h2 {
          font-size: 1.6rem;
        }

        p {
          font-size: 1rem;
        }
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="header">
        <div class="name">Edeline Ohk</div>

        <div class="nav">
          <button class="nav-btn active" data-section="about">About</button>
          <button class="nav-btn" data-section="projects">Projects</button>
          <button class="nav-btn" data-section="writing">Writing</button>
          <button class="nav-btn" data-section="resume">Resume</button>
        </div>
      </div>

      <div class="content">
        <div class="section active" id="about">
          <h2>About</h2>
          <p>
            Hi, I'm Edeline! I study Politics and International Relations at the University of Melbourne. Alongside university, I’ve worked across the Australian Government in Canberra and Washington, D.C., with experience in public administration, trade and economic security.
          </p>
          <p>
I’m curious about how politics, institutions and ideas shape public life, especially where different fields and perspectives overlap. I like asking questions, learning quickly, and following an interesting idea further than I probably need to.            
Here you’ll find some of my work, projects and experience. Thanks for stopping by!
          </p>
          <div class="links">
            <a href="https://github.com" target="_blank">GitHub</a>
            <a href="https://linkedin.com" target="_blank">LinkedIn</a>
            <a href="mailto:hello@edeline.dev">Email</a>
          </div>
        </div>

        <div class="section" id="projects">
          <h2>Projects</h2>
          <p>
            Here are some projects I've worked on:
          </p>
          <ul style="margin-left: 20px; margin-bottom: 20px;">
            <li style="margin-bottom: 10px;">
              <strong>Project One</strong> - A cool web application
            </li>
            <li style="margin-bottom: 10px;">
              <strong>Project Two</strong> - An interesting tool or library
            </li>
            <li style="margin-bottom: 10px;">
              <strong>Project Three</strong> - Something creative
            </li>
          </ul>
        </div>

        <div class="section" id="writing">
          <h2>Writing</h2>
          <p>
            I occasionally write about tech, design, and building. Check out my latest posts:
          </p>
          <div class="links">
            <a href="#">Blog Post One</a>
            <a href="#">Blog Post Two</a>
            <a href="#">Blog Post Three</a>
          </div>
        </div>

        <div class="section" id="resume">
          <h2>Resume</h2>
          <p>
            I'm experienced in web development, software engineering, and building full-stack applications.
          </p>
          <p>
            <strong>Skills:</strong> JavaScript, React, Python, Full-stack development, UI/UX
          </p>
          <p>
            <strong>Education:</strong> [Your degree/school]
          </p>
          <div class="links">
            <a href="#">Download Resume (PDF)</a>
          </div>
        </div>
      </div>
    </div>

    <script>
      const navBtns = document.querySelectorAll(".nav-btn");
      const sections = document.querySelectorAll(".section");

      navBtns.forEach((btn) => {
        btn.addEventListener("click", () => {
          // Remove active class from all
          navBtns.forEach((b) => b.classList.remove("active"));
          sections.forEach((s) => s.classList.remove("active"));

          // Add active to clicked
          btn.classList.add("active");
          const sectionId = btn.getAttribute("data-section");
          document.getElementById(sectionId).classList.add("active");
        });
      });
    </script>
  </body>
</html>
