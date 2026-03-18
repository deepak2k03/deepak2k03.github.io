---
layout: null
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600&display=swap');

  :root {
    --bg: #fdf6f1;
    --text: #2f3454;
    --muted: #7d85a3;
    --accent: #f2a55f;
  }

  html,
  body {
    margin: 0;
    padding: 0;
    background: var(--bg);
    color: var(--text);
    font-family: 'Poppins', sans-serif;
  }

  .container {
    max-width: 920px;
    min-height: 100vh;
    margin: 0 auto;
    padding: 2.1rem 1.2rem 1.3rem;
    display: flex;
    flex-direction: column;
  }

  .topbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 1rem;
    flex-wrap: wrap;
  }

  .links,
  .social {
    list-style: none;
    margin: 0;
    padding: 0;
    display: flex;
    align-items: center;
    gap: 1.3rem;
  }

  .links a,
  .social a {
    text-decoration: none;
    color: var(--text);
    font-size: 1.05rem;
  }

  .links a.active {
    border-bottom: 3px solid var(--accent);
    padding-bottom: 0.08rem;
  }

  .content {
    margin-top: 3.2rem;
    flex: 1;
  }

  .section-title {
    margin: 0 0 0.8rem;
    color: var(--text);
    font-size: 1.15rem;
    font-weight: 600;
  }

  .blog-row {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    gap: 1rem;
    color: var(--text);
    text-decoration: none;
    padding: 0.5rem 0;
  }

  .blog-title {
    display: flex;
    gap: 0.8rem;
    align-items: center;
    font-size: 2.2rem;
    line-height: 1.25;
  }

  .arrow {
    color: var(--muted);
    font-size: 1.35rem;
  }

  .date {
    color: var(--muted);
    font-style: italic;
    font-size: 0.95rem;
    white-space: nowrap;
  }

  .footer {
    text-align: center;
    color: var(--muted);
    margin-top: 2rem;
    font-size: 1.65rem;
  }

  .heart {
    color: #e05d5d;
  }

  @media (max-width: 720px) {
    .blog-row {
      flex-direction: column;
      align-items: flex-start;
    }

    .blog-title {
      font-size: 1.55rem;
    }
  }
</style>

<div class="container">
  <nav class="topbar" aria-label="Main navigation">
    <ul class="links">
      <li><a href="index.html">Home</a></li>
      <li><a class="active" href="blogs.html">Blogs</a></li>
      <li><a href="projects.html">Projects</a></li>
    </ul>

    <ul class="social">
      <li><a href="https://github.com/deepak2k03" target="_blank" rel="noopener noreferrer">GitHub</a></li>
      <li><a href="https://www.linkedin.com/in/deepak-singh-1b8590257/" target="_blank" rel="noopener noreferrer">Linkedin</a></li>
    </ul>
  </nav>

  <main class="content">
    <h2 class="section-title">Blogs</h2>
    <a class="blog-row" href="blogs/blog1.html">
      <span class="blog-title"><span class="arrow">&raquo;</span> GSoC Final Report</span>
      <span class="date">Aug 23, 2024</span>
    </a>
  </main>

  <footer class="footer">Made with <span class="heart">&hearts;</span></footer>
</div>
