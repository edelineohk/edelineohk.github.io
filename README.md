<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Laura Chapman</title>
    <style>
      :root {
        --bg: #efefef;
        --browser-bg: #dadada;
        --tab-bg: #f2f2f2;
        --chrome: #e8e8e8;
        --line: #d0d0d0;
        --text: #1a1a1a;
        --muted: #4a4a4a;
        --blue: #bfe1f4;
        --tab-text: #5b5b5b;
      }

      * {
        box-sizing: border-box;
      }

      html, body {
        margin: 0;
        padding: 0;
        background: var(--bg);
        color: var(--text);
        font-family: "Georgia", "Times New Roman", serif;
      }

      body {
        min-height: 100vh;
        display: flex;
        align-items: stretch;
        justify-content: center;
      }

      .browser {
        width: 100%;
        min-height: 100vh;
        background: var(--bg);
        display: flex;
        flex-direction: column;
      }

      .topbar {
        height: 58px;
        background: var(--chrome);
        border-bottom: 1px solid var(--line);
        display: flex;
        align-items: center;
        padding: 0 18px;
        gap: 14px;
      }

      .browser-actions {
        display: flex;
        align-items: center;
        gap: 12px;
        width: 125px;
      }

      .nav-arrow {
        width: 12px;
        height: 12px;
        border: solid #5b5b5b;
        border-width: 0 2px 2px 0;
        transform: rotate(135deg);
        opacity: 0.8;
      }

      .nav-arrow.right {
        transform: rotate(-45deg);
      }

      .nav-arrow.up {
        transform: rotate(225deg);
      }

      .refresh {
        width: 18px;
        height: 18px;
        border: 2px solid #4f4f4f;
        border-right-color: transparent;
        border-radius: 50%;
        position: relative;
        opacity: 0.8;
      }

      .refresh::after {
        content: "";
        position: absolute;
        right: -5px;
        top: -2px;
        width: 0;
        height: 0;
        border-left: 6px solid #4f4f4f;
        border-top: 4px solid transparent;
        border-bottom: 4px solid transparent;
        transform: rotate(35deg);
      }

      .addressbar {
        flex: 1;
        display: flex;
        justify-content: center;
      }

      .bar {
        width: min(100%, 900px);
        height: 34px;
        background: rgba(255,255,255,0.5);
        border: 1px solid rgba(0,0,0,0.08);
        border-radius: 18px;
        display: flex;
        align-items: center;
        padding: 0 14px;
        gap: 10px;
        color: #202020;
        font-size: 15px;
        font-family: Arial, sans-serif;
      }

      .lock {
        width: 12px;
        height: 12px;
        border: 2px solid #555;
        border-radius: 2px;
        position: relative;
        opacity: 0.7;
      }

      .lock::before {
        content: "";
        position: absolute;
        width: 7px;
        height: 7px;
        border: 2px solid #555;
        border-bottom: none;
        border-radius: 8px 8px 0 0;
        left: 1px;
        top: -8px;
      }

      .url {
        font-family: Arial, sans-serif;
      }

      .toolbar-icons {
        width: 150px;
        display: flex;
        justify-content: flex-end;
        align-items: center;
        gap: 14px;
      }

      .icon {
        width: 14px;
        height: 14px;
        border-radius: 3px;
        background: #5a5a5a;
        opacity: 0.8;
      }

      .profile {
        width: 12px;
        height: 12px;
        border-radius: 50%;
        background: #5a5a5a;
      }

      .tab-row {
        height: 52px;
        background: var(--chrome);
        border-bottom: 1px solid var(--line);
        display: flex;
        align-items: flex-end;
        padding: 0 18px 0 12px;
        gap: 8px;
      }

      .tab {
        height: 40px;
        min-width: 126px;
        border: 1px solid var(--line);
        border-bottom: none;
        border-top-left-radius: 8px;
        border-top-right-radius: 8px;
        background: var(--tab-bg);
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 8px;
        color: var(--tab-text);
        font-family: Arial, sans-serif;
        font-size: 15px;
        padding: 0 14px;
      }

      .tab.active {
        background: white;
        border-bottom: 1px solid white;
      }

      .gmail-icon {
        width: 18px;
        height: 14px;
        background: #ea4335;
        border-radius: 3px;
        position: relative;
      }

      .gmail-icon::before,
      .gmail-icon::after {
        content: "";
        position: absolute;
        inset: 0;
        background: transparent;
      }

      .gmail-icon::before {
        border-left: 10px solid white;
        border-top: 6px solid transparent;
        border-bottom: 6px solid transparent;
        left: 4px;
        top: 1px;
      }

      .gmail-icon::after {
        border-right: 10px solid white;
        border-top: 6px solid transparent;
        border-bottom: 6px solid transparent;
        right: 4px;
        top: 1px;
      }

      .page {
        flex: 1;
        background: #f5f5f5;
        display: flex;
        justify-content: center;
        align-items: flex-start;
        padding-top: 38px;
      }

      .content {
        width: min(1100px, calc(100% - 80px));
        display: flex;
        justify-content: center;
      }

      .inner {
        width: 100%;
        max-width: 1030px;
        display: flex;
        flex-direction: column;
        align-items: center;
      }

      .name {
        font-size: clamp(3.1rem, 5.5vw, 6rem);
        line-height: 1;
        letter-spacing: -0.06em;
        font-weight: 400;
        margin-top: 10px;
        margin-bottom: 26px;
      }

      .nav-tabs {
        display: flex;
        gap: 8px;
        margin-bottom: 38px;
      }

      .nav-tab {
        height: 38px;
        min-width: 110px;
        display: inline-flex;
        align-items: center;
        justify-content: center;
        padding: 0 20px;
        font-family: Arial, sans-serif;
        font-size: 16px;
        color: #2f2f2f;
        background: transparent;
        border: 1px solid transparent;
      }

      .nav-tab.active {
        background: var(--blue);
        border-color: rgba(90, 164, 214, 0.15);
      }

      .bio-wrap {
        width: 100%;
        display: flex;
        justify-content: center;
        margin-top: 10px;
      }

      .bio-grid {
        width: min(100%, 920px);
        display: grid;
        grid-template-columns: 360px 1fr;
        gap: 60px;
        align-items: start;
      }

      .photo-card {
        width: 100%;
        max-width: 330px;
        height: 310px;
        margin-left: 48px;
        border-radius: 4px;
        overflow: hidden;
        box-shadow: 0 0 0 1px rgba(0,0,0,0.04);
      }

      .photo-card img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        display: block;
      }

      .bio-copy {
        padding-top: 4px;
      }

      h2 {
        font-size: clamp(2.2rem, 3vw, 3rem);
        font-weight: 400;
        margin: 0 0 24px 0;
        letter-spacing: -0.04em;
      }

      p {
        margin: 0;
        font-size: clamp(1.1rem, 1.5vw, 1.35rem);
        line-height: 1.55;
        color: #2b2b2b;
        max-width: 720px;
      }

      .links {
        margin-top: 36px;
        display: flex;
        flex-direction: column;
        gap: 0;
      }

      .links a {
        color: #1d1d1d;
        text-decoration: none;
        font-size: clamp(1.15rem, 1.5vw, 1.45rem);
        margin: 0 0 8px 0;
        width: fit-content;
        position: relative;
      }

      .links a::after {
        content: "";
        position: absolute;
        left: 0;
        bottom: -2px;
        width: 100%;
        height: 1px;
        background: rgba(0,0,0,0.35);
        transform: scaleX(0);
        transform-origin: left;
        transition: transform 0.18s ease;
      }

      .links a:hover::after {
        transform: scaleX(1);
      }

      @media (max-width: 900px) {
        .bio-grid {
          grid-template-columns: 1fr;
          gap: 26px;
          justify-items: center;
        }

        .photo-card {
          margin-left: 0;
        }

        .bio-copy {
          text-align: left;
          width: 100%;
        }

        .page {
          padding-top: 24px;
        }
      }

      @media (max-width: 620px) {
        .tab-row {
          overflow-x: auto;
          padding-bottom: 0;
        }

        .tab {
          min-width: 110px;
        }

        .content {
          width: calc(100% - 30px);
        }

        .name {
          margin-bottom: 18px;
        }

        .nav-tabs {
          flex-wrap: wrap;
          justify-content: center;
        }

        .bar {
          font-size: 13px;
        }
      }
    </style>
  </head>
  <body>
    <div class="browser">
      <div class="topbar">
        <div class="browser-actions">
          <div class="nav-arrow"></div>
          <div class="nav-arrow right"></div>
          <div class="refresh"></div>
        </div>

        <div class="addressbar">
          <div class="bar">
            <div class="lock"></div>
            <div class="url">laurachapman.github.io</div>
          </div>
        </div>

        <div class="toolbar-icons">
          <div class="icon"></div>
          <div class="profile"></div>
          <div class="icon"></div>
        </div>
      </div>

      <div class="tab-row">
        <div class="tab">
          <div class="gmail-icon"></div>
          <span>Gmail</span>
        </div>
        <div class="tab active">
          <div class="gmail-icon"></div>
          <span>Gmail</span>
        </div>
      </div>

      <div class="page">
        <div class="content">
          <div class="inner">
            <div class="name">Laura Chapman</div>

            <div class="nav-tabs">
              <div class="nav-tab active">About</div>
              <div class="nav-tab">Projects</div>
              <div class="nav-tab">Resume</div>
            </div>

            <div class="bio-wrap">
              <div class="bio-grid">
                <div class="photo-card">
                  <img
                    src="https://images.unsplash.com/photo-1544005313-94ddf0286df2?auto=format&fit=crop&w=800&q=80"
                    alt="Laura portrait"
                  />
                </div>

                <div class="bio-copy">
                  <h2>Hi, I'm Laura!</h2>

                  <p>
                   I'm currently completing my degree at the University of Melbourne.
                    I study Politics and International Affairs. When I'm not doing school work,
                    I enjoy additional creative labor — here you'll find my projects and my resume.
                    Thanks for stopping by!
                  </p>

                  <div class="links">
                    <a href="#">LinkedIn</a>
                    <a href="#">Github</a>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </body>
</html>
