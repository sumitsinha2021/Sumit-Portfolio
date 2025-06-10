# Sumit-Portfolio
Portfolio

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Creative Portfolio</title>
  <style>
    :root {
      --color-bg: #ffffff;
      --color-text-primary: #111827;
      --color-text-secondary: #6b7280;
      --color-accent: #000000;
      --color-accent-hover: #333333;
      --color-card-bg: #f9fafb;
      --border-radius: 0.75rem;
      --shadow-light: 0 6px 12px rgba(0, 0, 0, 0.08);
      --font-heading: 'Poppins', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      --font-body: 'Inter', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      --max-width: 1200px;
      --spacing-vertical: 4rem;
      --spacing-horizontal: 1.5rem;
      --transition-speed: 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    }

    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: var(--font-body);
      background: var(--color-bg);
      color: var(--color-text-secondary);
      font-size: 18px;
      line-height: 1.6;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
    }

    a {
      color: var(--color-accent);
      text-decoration: none;
      transition: color var(--transition-speed);
    }
    a:hover,
    a:focus {
      color: var(--color-accent-hover);
      outline: none;
    }

    img {
      display: block;
      max-width: 100%;
      border-radius: var(--border-radius);
      height: auto;
    }

    /* Container for layout */
    .container {
      max-width: var(--max-width);
      margin-left: auto;
      margin-right: auto;
      padding-left: var(--spacing-horizontal);
      padding-right: var(--spacing-horizontal);
    }

    /* Header */
    header {
      position: sticky;
      top: 0;
      background: var(--color-bg);
      box-shadow: 0 2px 6px rgba(0,0,0,0.05);
      z-index: 1000;
    }
    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem var(--spacing-horizontal);
      max-width: var(--max-width);
      margin: 0 auto;
    }
    .logo {
      font-family: var(--font-heading);
      font-weight: 700;
      font-size: 1.5rem;
      color: var(--color-accent);
      user-select: none;
    }
    .nav-links {
      display: flex;
      gap: 2rem;
      font-weight: 600;
      font-size: 1rem;
      color: var(--color-text-secondary);
    }
    .nav-links a {
      position: relative;
      padding-bottom: 4px;
    }
    .nav-links a::after {
      content: "";
      position: absolute;
      bottom: 0;
      left: 0;
      width: 0%;
      height: 2px;
      background: var(--color-accent);
      border-radius: 2px;
      transition: width var(--transition-speed);
    }
    .nav-links a:hover::after,
    .nav-links a:focus::after {
      width: 100%;
    }

    /* Hero Section */
    .hero {
      padding: var(--spacing-vertical) 0 3rem;
      text-align: center;
    }
    .hero-title {
      font-family: var(--font-heading);
      font-weight: 800;
      font-size: 3.75rem;
      color: var(--color-text-primary);
      max-width: 900px;
      margin: 0 auto 1rem;
      line-height: 1.1;
    }
    .hero-subtitle {
      max-width: 600px;
      margin: 0 auto 3rem;
      font-size: 1.25rem;
      color: var(--color-text-secondary);
      font-weight: 500;
    }
    .btn-primary {
      background-color: var(--color-accent);
      color: white;
      font-weight: 700;
      font-size: 1.25rem;
      padding: 1rem 3rem;
      border: none;
      border-radius: var(--border-radius);
      cursor: pointer;
      box-shadow: var(--shadow-light);
      transition: background-color var(--transition-speed), transform var(--transition-speed);
      user-select: none;
      display: inline-block;
    }
    .btn-primary:hover,
    .btn-primary:focus {
      background-color: var(--color-accent-hover);
      outline: none;
      transform: scale(1.05);
    }

    /* About Section */
    section {
      padding-top: var(--spacing-vertical);
      padding-bottom: var(--spacing-vertical);
    }
    .about {
      max-width: var(--max-width);
      margin: 0 auto;
      text-align: center;
      padding-left: var(--spacing-horizontal);
      padding-right: var(--spacing-horizontal);
    }
    .about h2 {
      font-family: var(--font-heading);
      font-weight: 700;
      font-size: 2.75rem;
      margin-bottom: 2rem;
      color: var(--color-text-primary);
    }
    .about p {
      margin: 0 auto 1.5rem;
      max-width: 700px;
      font-size: 1.15rem;
      font-weight: 500;
      color: var(--color-text-secondary);
    }

    /* Skills Grid */
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit,minmax(200px,1fr));
      gap: 1.5rem;
      margin-top: 3rem;
      max-width: 900px;
      margin-left: auto;
      margin-right: auto;
    }
    .skill-card {
      background: var(--color-card-bg);
      border-radius: var(--border-radius);
      box-shadow: var(--shadow-light);
      padding: 2rem 1.5rem;
      transition: box-shadow var(--transition-speed);
      cursor: default;
      color: var(--color-text-primary);
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 1rem;
    }
    .skill-card:hover,
    .skill-card:focus-within {
      box-shadow: 0 12px 20px rgba(0,0,0,0.15);
      transform: translateY(-6px);
      transition: box-shadow 0.25s ease, transform 0.25s ease;
      outline: none;
    }

    /* Simple line-icons using SVG inline */
    .skill-icon {
      width: 48px;
      height: 48px;
      fill: none;
      stroke: var(--color-accent);
      stroke-width: 2;
      stroke-linecap: round;
      stroke-linejoin: round;
    }
    .skill-title {
      font-weight: 700;
      font-size: 1.1rem;
    }

    /* Projects Section */
    .projects {
      max-width: var(--max-width);
      margin: 0 auto;
      padding-left: var(--spacing-horizontal);
      padding-right: var(--spacing-horizontal);
    }
    .projects h2 {
      font-family: var(--font-heading);
      font-weight: 700;
      font-size: 2.5rem;
      margin-bottom: 3rem;
      color: var(--color-text-primary);
      text-align: center;
    }
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit,minmax(280px,1fr));
      gap: 2rem;
    }
    .project-card {
      background: var(--color-card-bg);
      padding: 1.75rem 1.5rem;
      border-radius: var(--border-radius);
      box-shadow: var(--shadow-light);
      transition: box-shadow var(--transition-speed);
      cursor: pointer;
      color: var(--color-text-primary);
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }
    .project-card:hover,
    .project-card:focus-within {
      box-shadow: 0 12px 24px rgba(0,0,0,0.17);
      transform: translateY(-4px);
      outline: none;
    }
    .project-title {
      font-family: var(--font-heading);
      font-size: 1.25rem;
      font-weight: 700;
      margin: 0;
    }
    .project-desc {
      font-size: 1rem;
      color: var(--color-text-secondary);
      flex-grow: 1;
    }
    .project-link {
      font-weight: 600;
      color: var(--color-accent);
      align-self: flex-start;
      transition: color var(--transition-speed);
    }
    .project-link:hover,
    .project-link:focus {
      color: var(--color-accent-hover);
      outline: none;
    }

    /* Contact Section */
    .contact {
      max-width: 600px;
      margin: 0 auto;
      padding-left: var(--spacing-horizontal);
      padding-right: var(--spacing-horizontal);
      color: var(--color-text-primary);
    }
    .contact h2 {
      font-family: var(--font-heading);
      font-weight: 700;
      font-size: 2rem;
      margin-bottom: 2rem;
      text-align: center;
    }
    form {
      display: flex;
      flex-direction: column;
      gap: 1.5rem;
    }
    label {
      font-weight: 600;
      color: var(--color-text-secondary);
      font-size: 0.875rem;
      user-select: none;
    }
    input,
    textarea {
      padding: 0.75rem 1rem;
      font-family: var(--font-body);
      font-size: 1rem;
      border-radius: var(--border-radius);
      border: 1px solid #d1d5db;
      resize: vertical;
      color: var(--color-text-primary);
      transition: border-color var(--transition-speed), box-shadow var(--transition-speed);
      width: 100%;
      box-sizing: border-box;
    }
    input:focus,
    textarea:focus {
      outline: none;
      border-color: var(--color-accent);
      box-shadow: 0 0 8px rgba(0, 0, 0, 0.1);
    }
    button[type="submit"] {
      align-self: center;
      background-color: var(--color-accent);
      color: white;
      font-weight: 700;
      font-size: 1.125rem;
      padding: 0.75rem 3rem;
      border: none;
      border-radius: var(--border-radius);
      cursor: pointer;
      box-shadow: var(--shadow-light);
      transition: background-color var(--transition-speed), transform var(--transition-speed);
      user-select: none;
      width: auto;
    }
    button[type="submit"]:hover,
    button[type="submit"]:focus {
      background-color: var(--color-accent-hover);
      outline: none;
      transform: scale(1.05);
    }

    /* Footer */
    footer {
      text-align: center;
      color: var(--color-text-secondary);
      font-size: 0.875rem;
      padding: 3rem 1rem;
      user-select: none;
    }

    /* Responsive */
    @media (max-width: 767px) {
      .nav-links {
        display: none;
      }
      .hero-title {
        font-size: 2.8rem;
      }
      .about h2 {
        font-size: 2rem;
      }
      .projects h2 {
        font-size: 2rem;
      }
    }
  </style>
</head>
<body>
  <header>
    <nav aria-label="Primary navigation">
      <div class="logo" tabindex="0">CreativePortfolio</div>
      <div class="nav-links" role="navigation" aria-label="Main navigation links">
        <a href="#about" tabindex="0">About</a>
        <a href="#projects" tabindex="0">Projects</a>
        <a href="#contact" tabindex="0">Contact</a>
      </div>
    </nav>
  </header>

  <main>
    <section class="hero" role="banner" aria-label="Introduction">
      <div class="container">
        <h1 class="hero-title">Crafting Beautiful Digital Experiences</h1>
        <p class="hero-subtitle">
          I'm a creative frontend developer passionate about turning ideas into stunning, user-friendly websites using modern web technologies.
        </p>
        <a href="#contact" class="btn-primary" role="button">Get In Touch</a>
      </div>
    </section> 
    <section id="about" class="about" aria-labelledby="about-title" tabindex="0">
      <h2 id="about-title">About Me</h2>
      <p>I am SUMIT KUMAR SINHA. I am 21 years old, and I am from Ramgarh, Jharkhand. I have completed BTECH in Computer science engineering from MIT, Meerut, UP</p>
      <p>I bring a unique blend of creativity and technical expertise to every project. With a deep love for clean design and intuitive interfaces, I aim to create digital experiences that not only look great but feel natural to use.</p>
      <p>My journey began with a curiosity for how websites worked, leading me to master the core technologies: HTML, CSS, and Google Analytics. I continuously improve by exploring new frameworks and design principles to stay at the forefront of the industry.</p>
      <p>Apart from coding, I enjoy sketching ideas, photography, and exploring places — all fueling my creative process.</p>

      <div class="skills-grid" role="list" aria-label="Skills and Technologies">
        <article class="skill-card" role="listitem" tabindex="0">
          <svg class="skill-icon" viewBox="0 0 24 24" aria-hidden="true" focusable="false"><circle cx="12" cy="12" r="10"/><path d="M8 12l2 2 4-4"/></svg>
          <div class="skill-title">HTML5 &amp; CSS3</div>
        </article>
        <article class="skill-card" role="listitem" tabindex="0">
          <svg class="skill-icon" viewBox="0 0 24 24" aria-hidden="true" focusable="false"><rect x="3" y="3" width="18" height="18" rx="2"/></svg>
          <div class="skill-title">Responsive Design</div>
        </article>
        <article class="skill-card" role="listitem" tabindex="0">
          <svg class="skill-icon" viewBox="0 0 24 24" aria-hidden="true" focusable="false"><path d="M12 12c2-2 4-4 4-6a4 4 0 0 0-8 0c0 2 2 4 4 6z"/></svg>
          <div class="skill-title">UI/UX Design</div>
        </article>
        <article class="skill-card" role="listitem" tabindex="0">
          <svg class="skill-icon" viewBox="0 0 24 24" aria-hidden="true" focusable="false"><path d="M6 18L18 6M6 6l12 12"/></svg>
          <div class="skill-title">Version Control (Git)</div>
        </article>
      </div>
    </section>

    <section id="projects" class="projects" aria-labelledby="projects-title" tabindex="0">
      <h2 id="projects-title">Projects</h2>
      <div class="projects-grid">
        <article class="project-card" tabindex="0" aria-label="Project Portfolio Website">
          <h3 class="project-title">Portfolio Website</h3>
          <p class="project-desc">A showcase of my work built with modern HTML, CSS Grid, and accessibility best practices.</p>
          <a href="#" class="project-link" tabindex="0">View project</a>
        </article>
        <article class="project-card" tabindex="0" aria-label="Project E-commerce UI Design">
          <h3 class="project-title">E-commerce UI</h3>
          <p class="project-desc">A sleek and responsive shopping interface focusing on user engagement and conversion.</p>
          <a href="#" class="project-link" tabindex="0">View project</a>
        </article>
        <article class="project-card" tabindex="0" aria-label="Project Blog Platform">
          <h3 class="project-title">Blog Platform</h3>
          <p class="project-desc">Minimalistic and user-friendly blog platform emphasizing content readability.</p>
          <a href="#" class="project-link" tabindex="0">View project</a>
        </article>
      </div>
    </section>

    <section id="contact" class="contact" aria-labelledby="contact-title" tabindex="0">
      <h2 id="contact-title">Contact Me</h2>
      <form aria-label="Contact Form" novalidate>
        <label for="name">Name</label>
        <input id="name" name="name" type="text" placeholder="Your full name" required aria-required="true" />

        <label for="email">Email</label>
        <input id="email" name="email" type="email" placeholder="you@example.com" required aria-required="true" />

        <label for="message">Message</label>
        <textarea id="message" name="message" rows="5" placeholder="Write your message here..." required aria-required="true"></textarea>

        <button type="submit">Send Message</button>
      </form>
    </section>
  </main>

  <footer>
    &copy; 2025 CreativePortfolio. All rights reserved.
  </footer>
</body>
</html>


