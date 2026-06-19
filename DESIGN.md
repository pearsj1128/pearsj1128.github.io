<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <title>pearsj1128 | Chemistry Portfolio</title>

  <style>
    :root {
      --bg: #f6fbff;
      --surface: #ffffff;
      --surface-soft: #eef7ff;
      --text: #102033;
      --muted: #5b6b7f;
      --primary: #006d77;
      --primary-dark: #004f56;
      --accent: #83c5be;
      --accent-warm: #ffddd2;
      --border: #d7e7ef;
      --shadow: 0 18px 45px rgba(16, 32, 51, 0.12);
      --radius-lg: 28px;
      --radius-md: 18px;
      --max-width: 1080px;
    }

    * {
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      margin: 0;
      font-family: Arial, Helvetica, sans-serif;
      background:
        radial-gradient(circle at top left, rgba(131, 197, 190, 0.28), transparent 32rem),
        radial-gradient(circle at bottom right, rgba(255, 221, 210, 0.55), transparent 30rem),
        var(--bg);
      color: var(--text);
      line-height: 1.65;
    }

    a {
      color: var(--primary);
    }

    .skip-link {
      position: absolute;
      left: -999px;
      top: 12px;
      background: var(--primary);
      color: white;
      padding: 10px 14px;
      border-radius: 10px;
      z-index: 1000;
    }

    .skip-link:focus {
      left: 12px;
    }

    header {
      position: sticky;
      top: 0;
      z-index: 50;
      background: rgba(255, 255, 255, 0.88);
      backdrop-filter: blur(14px);
      border-bottom: 1px solid var(--border);
    }

    .nav {
      max-width: var(--max-width);
      margin: 0 auto;
      padding: 16px 22px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 18px;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 10px;
      font-weight: 800;
      letter-spacing: -0.02em;
      color: var(--primary-dark);
      text-decoration: none;
    }

    .brand-mark {
      width: 34px;
      height: 34px;
      border-radius: 50%;
      background: linear-gradient(135deg, var(--primary), var(--accent));
      display: grid;
      place-items: center;
      color: white;
      font-weight: 900;
    }

    nav {
      display: flex;
      flex-wrap: wrap;
      justify-content: flex-end;
      gap: 14px;
      font-size: 14px;
      font-weight: 700;
    }

    nav a {
      color: var(--text);
      text-decoration: none;
    }

    nav a:hover {
      color: var(--primary);
    }

    main {
      max-width: var(--max-width);
      margin: 0 auto;
      padding: 36px 22px 70px;
    }

    .hero {
      min-height: 74vh;
      display: grid;
      grid-template-columns: 1.15fr 0.85fr;
      gap: 34px;
      align-items: center;
      padding: 34px 0 56px;
    }

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      margin: 0 0 14px;
      padding: 8px 12px;
      border-radius: 999px;
      background: var(--surface-soft);
      color: var(--primary-dark);
      font-size: 13px;
      font-weight: 800;
      letter-spacing: 0.04em;
      text-transform: uppercase;
      border: 1px solid var(--border);
    }

    .dot {
      width: 9px;
      height: 9px;
      border-radius: 50%;
      background: var(--primary);
    }

    h1 {
      margin: 0;
      font-size: clamp(42px, 7vw, 78px);
      line-height: 0.98;
      letter-spacing: -0.07em;
    }

    .hero-text {
      margin: 20px 0 0;
      max-width: 680px;
      color: var(--muted);
      font-size: 19px;
    }

    .hero-text strong {
      color: var(--text);
    }

    .buttons {
      margin-top: 28px;
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
    }

    .button {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      padding: 12px 18px;
      border-radius: 999px;
      border: 1px solid var(--primary);
      text-decoration: none;
      font-weight: 800;
      color: var(--primary);
      background: white;
    }

    .button.primary {
      background: var(--primary);
      color: white;
    }

    .button:hover {
      transform: translateY(-1px);
      box-shadow: 0 10px 22px rgba(0, 109, 119, 0.18);
    }

    .profile-panel {
      background: linear-gradient(160deg, rgba(255, 255, 255, 0.96), rgba(238, 247, 255, 0.92));
      border: 1px solid var(--border);
      border-radius: var(--radius-lg);
      box-shadow: var(--shadow);
      padding: 24px;
      position: relative;
      overflow: hidden;
    }

    .profile-panel::before,
    .profile-panel::after {
      content: "";
      position: absolute;
      border-radius: 50%;
      border: 1px solid rgba(0, 109, 119, 0.2);
    }

    .profile-panel::before {
      width: 160px;
      height: 160px;
      right: -54px;
      top: -54px;
    }

    .profile-panel::after {
      width: 110px;
      height: 110px;
      left: -40px;
      bottom: -34px;
    }

    .profile-image-wrap {
      position: relative;
      z-index: 1;
      width: min(260px, 80%);
      margin: 0 auto 20px;
      padding: 10px;
      background: white;
      border-radius: 50%;
      border: 1px solid var(--border);
    }

    .profile-image {
      display: block;
      width: 100%;
      aspect-ratio: 1 / 1;
      object-fit: cover;
      border-radius: 50%;
      background: var(--surface-soft);
    }

    .profile-panel h2 {
      position: relative;
      z-index: 1;
      margin: 0;
      text-align: center;
      font-size: 28px;
    }

    .profile-panel p {
      position: relative;
      z-index: 1;
      margin: 8px 0 0;
      text-align: center;
      color: var(--muted);
    }

    .quick-facts {
      position: relative;
      z-index: 1;
      display: grid;
      gap: 10px;
      margin-top: 20px;
    }

    .fact {
      padding: 12px 14px;
      background: rgba(255, 255, 255, 0.78);
      border: 1px solid var(--border);
      border-radius: 14px;
    }

    .fact span {
      display: block;
      color: var(--muted);
      font-size: 12px;
      font-weight: 800;
      text-transform: uppercase;
      letter-spacing: 0.05em;
    }

    .fact strong {
      display: block;
      margin-top: 2px;
    }

    section {
      margin-top: 26px;
      padding: 32px;
      background: rgba(255, 255, 255, 0.88);
      border: 1px solid var(--border);
      border-radius: var(--radius-lg);
      box-shadow: 0 12px 32px rgba(16, 32, 51, 0.07);
    }

    .section-heading {
      display: flex;
      align-items: end;
      justify-content: space-between;
      gap: 20px;
      margin-bottom: 22px;
    }

    h2 {
      margin: 0;
      font-size: clamp(28px, 4vw, 42px);
      letter-spacing: -0.04em;
      line-height: 1.05;
    }

    .section-note {
      max-width: 460px;
      margin: 0;
      color: var(--muted);
      font-size: 15px;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 16px;
    }

    .card {
      padding: 22px;
      border: 1px solid var(--border);
      border-radius: var(--radius-md);
      background: white;
    }

    .card h3 {
      margin: 0 0 10px;
      font-size: 20px;
    }

    .card p {
      margin: 0;
      color: var(--muted);
    }

    .tag-list {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-top: 14px;
    }

    .chip {
      padding: 6px 10px;
      border-radius: 999px;
      background: var(--surface-soft);
      color: var(--primary-dark);
      font-size: 12px;
      font-weight: 800;
      border: 1px solid var(--border);
    }

    .resume-layout {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 18px;
    }

    .resume-box {
      padding: 22px;
      border-radius: var(--radius-md);
      border: 1px solid var(--border);
      background: white;
    }

    .resume-box ul {
      margin: 12px 0 0;
      padding-left: 20px;
      color: var(--muted);
    }

    .course-list {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 14px;
    }

    .course {
      padding: 18px;
      border-radius: var(--radius-md);
      border: 1px solid var(--border);
      background: linear-gradient(180deg, white, var(--surface-soft));
    }

    .course strong {
      display: block;
      margin-bottom: 4px;
    }

    .course span {
      color: var(--muted);
    }

    .ai-box {
      background: #0f2f35;
      color: white;
      border-radius: var(--radius-md);
      padding: 22px;
    }

    .ai-box h3 {
      margin-top: 0;
    }

    .ai-box p,
    .ai-box li {
      color: rgba(255, 255, 255, 0.82);
    }

    .ai-box code {
      background: rgba(255, 255, 255, 0.12);
      color: white;
      padding: 2px 6px;
      border-radius: 6px;
    }

    .contact {
      display: grid;
      grid-template-columns: 1.1fr 0.9fr;
      gap: 18px;
      align-items: stretch;
    }

    .contact-card {
      padding: 24px;
      border-radius: var(--radius-md);
      border: 1px solid var(--border);
      background: white;
    }

    .contact-card p {
      margin: 8px 0;
      color: var(--muted);
    }

    footer {
      max-width: var(--max-width);
      margin: 0 auto;
      padding: 28px 22px 44px;
      color: var(--muted);
      text-align: center;
      font-size: 14px;
    }

    @media (max-width: 840px) {
      .nav {
        align-items: flex-start;
        flex-direction: column;
      }

      nav {
        justify-content: flex-start;
      }

      .hero {
        grid-template-columns: 1fr;
        min-height: auto;
      }

      .profile-panel {
        max-width: 520px;
      }

      .grid,
      .resume-layout,
      .course-list,
      .contact {
        grid-template-columns: 1fr;
      }

      section {
        padding: 24px;
      }

      .section-heading {
        align-items: flex-start;
        flex-direction: column;
      }
    }

    @media (max-width: 520px) {
      main {
        padding: 22px 14px 50px;
      }

      .nav {
        padding: 14px;
      }

      section {
        padding: 20px;
        border-radius: 22px;
      }

      .buttons {
        flex-direction: column;
      }

      .button {
        width: 100%;
      }
    }
  </style>
</head>

<body>
  <a class="skip-link" href="#main">Skip to main content</a>

  <header>
    <div class="nav">
      <a class="brand" href="#top" aria-label="Go to top of page">
        <span class="brand-mark">P</span>
        <span>pearsj1128</span>
      </a>

      <nav aria-label="Main navigation">
        <a href="#about">About</a>
        <a href="#projects">Projects</a>
        <a href="#resume">Resume</a>
        <a href="#courses">Courses</a>
        <a href="#ai-usage">AI Usage</a>
        <a href="#contact">Contact</a>
      </nav>
    </div>
  </header>

  <main id="main">
    <section class="hero" id="top">
      <div>
        <p class="eyebrow"><span class="dot"></span> Chemistry Major Portfolio</p>
        <h1>Hello, I’m pearsj1128.</h1>
        <p class="hero-text">
          I am a <strong>Chemistry major</strong> interested in laboratory work,
          scientific data interpretation, and clear science communication.
          This website is a static personal portfolio built with HTML and CSS
          and deployed through GitHub Pages.
        </p>

        <div class="buttons">
          <a class="button primary" href="#projects">View Projects</a>
          <a class="button" href="assets/cv.pdf">Open CV</a>
          <a class="button" href="#contact">Contact</a>
        </div>
      </div>

      <aside class="profile-panel" aria-label="Profile summary">
        <div class="profile-image-wrap">
          <img class="profile-image" src="assets/profile.png" alt="Profile image for pearsj1128" />
        </div>

        <h2>pearsj1128</h2>
        <p>Student · Chemistry Major · Scientific Learner</p>

        <div class="quick-facts">
          <div class="fact">
            <span>Major</span>
            <strong>Chemistry</strong>
          </div>
          <div class="fact">
            <span>Interests</span>
            <strong>Lab work, analysis, science communication</strong>
          </div>
          <div class="fact">
            <span>Website</span>
            <strong>Hosted on GitHub Pages</strong>
          </div>
        </div>
      </aside>
    </section>

    <section id="about">
      <div class="section-heading">
        <h2>About Me</h2>
        <p class="section-note">
          A brief introduction focused on chemistry, learning, and academic growth.
        </p>
      </div>

      <p>
        I am a Chemistry major building a foundation in molecular structure,
        chemical reactions, analytical reasoning, and experimental thinking.
        I enjoy connecting classroom concepts with real observations and
        explaining scientific ideas in a clear, organized way.
      </p>

      <p>
        Through this GitHub Pages project, I practiced building a simple
        personal website, organizing content for an academic portfolio, and
        using AI tools responsibly to improve structure, wording, and design.
      </p>
    </section>

    <section id="projects">
      <div class="section-heading">
        <h2>Projects & Activities</h2>
        <p class="section-note">
          Academic and personal work related to chemistry, communication, and web publishing.
        </p>
      </div>

      <div class="grid">
        <article class="card">
          <h3>Chemistry Learning Portfolio</h3>
          <p>
            Organized key chemistry concepts into a readable portfolio format,
            focusing on clarity, structure, and scientific accuracy.
          </p>
          <div class="tag-list">
            <span class="chip">Chemistry</span>
            <span class="chip">Study Notes</span>
          </div>
        </article>

        <article class="card">
          <h3>Data Interpretation Practice</h3>
          <p>
            Practiced interpreting experimental-style results and summarizing
            observations in a concise, evidence-based way.
          </p>
          <div class="tag-list">
            <span class="chip">Analysis</span>
            <span class="chip">Reasoning</span>
          </div>
        </article>

        <article class="card">
          <h3>GitHub Pages Website</h3>
          <p>
            Built and deployed this static personal website using HTML, CSS,
            GitHub repository management, and GitHub Pages.
          </p>
          <div class="tag-list">
            <span class="chip">HTML</span>
            <span class="chip">CSS</span>
            <span class="chip">GitHub Pages</span>
          </div>
        </article>
      </div>
    </section>

    <section id="resume">
      <div class="section-heading">
        <h2>CV / Resume</h2>
        <p class="section-note">
          A downloadable PDF resume is linked from the repository assets folder.
        </p>
      </div>

      <div class="resume-layout">
        <div class="resume-box">
          <h3>Resume File</h3>
          <p>
            The CV is available as a PDF file in the website repository.
          </p>
          <div class="buttons">
            <a class="button primary" href="assets/cv.pdf">Download CV PDF</a>
          </div>
        </div>

        <div class="resume-box">
          <h3>Current Focus</h3>
          <ul>
            <li>Building chemistry fundamentals</li>
            <li>Improving scientific writing and explanation</li>
            <li>Practicing data interpretation and structured reporting</li>
            <li>Learning how to present academic work online</li>
          </ul>
        </div>
      </div>
    </section>

    <section id="courses">
      <div class="section-heading">
        <h2>Courses I Plan to Take</h2>
        <p class="section-note">
          Courses that match my Chemistry major and future academic interests.
        </p>
      </div>

      <div class="course-list">
        <div class="course">
          <strong>Organic Chemistry</strong>
          <span>Reaction mechanisms, molecular structure, and synthesis.</span>
        </div>

        <div class="course">
          <strong>Analytical Chemistry</strong>
          <span>Measurement, data quality, and chemical analysis methods.</span>
        </div>

        <div class="course">
          <strong>Physical Chemistry</strong>
          <span>Thermodynamics, kinetics, and molecular-level reasoning.</span>
        </div>

        <div class="course">
          <strong>Biochemistry</strong>
          <span>Chemical principles in biological systems.</span>
        </div>
      </div>
    </section>

    <section id="ai-usage">
      <div class="section-heading">
        <h2>AI Usage</h2>
        <p class="section-note">
          Transparent record of how AI assistance was used for this assignment.
        </p>
      </div>

      <div class="ai-box">
        <h3>Tool Used</h3>
        <p>
          I used ChatGPT as an AI assistant to plan the page structure,
          revise the content for a Chemistry major, and improve the HTML/CSS
          layout while keeping the site compatible with GitHub Pages.
        </p>

        <h3>Example Prompts</h3>
        <ul>
          <li>
            <code>Build a static personal website for GitHub Pages using assets/profile.png and assets/cv.pdf.</code>
          </li>
          <li>
            <code>Make the portfolio fit a Chemistry major and include About, Projects, Resume, Courses, AI Usage, and Contact sections.</code>
          </li>
          <li>
            <code>Improve the design so it looks clean, responsive, and suitable for academic submission.</code>
          </li>
        </ul>

        <h3>Human Edits</h3>
        <p>
          I checked that the major is Chemistry, reviewed the section content,
          and confirmed that the website is deployed through GitHub Pages.
        </p>
      </div>
    </section>

    <section id="contact">
      <div class="section-heading">
        <h2>Contact</h2>
        <p class="section-note">
          Basic contact information for this personal academic portfolio.
        </p>
      </div>

      <div class="contact">
        <div class="contact-card">
          <h3>Email</h3>
          <p>pearsj1128@snu.ac.kr</p>
          <p>
            If this email is not correct, replace it before final submission.
          </p>
        </div>

        <div class="contact-card">
          <h3>GitHub</h3>
          <p>
            <a href="https://github.com/pearsj1128">github.com/pearsj1128</a>
          </p>
          <p>
            Website URL:
            <a href="https://pearsj1128.github.io">pearsj1128.github.io</a>
          </p>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <p>© 2026 pearsj1128. Chemistry portfolio hosted on GitHub Pages.</p>
  </footer>
</body>
</html>
