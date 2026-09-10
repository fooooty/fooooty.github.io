---
layout: about
title: about
permalink: /
subtitle: M.S. Student at <a href="https://ami.kaist.ac.kr/">AMI Lab, KAIST</a>

profile:
  align: right
  image: jiyeon-son.jpeg
  image_circular: false # crops the image to make it circular
  more_info:

selected_papers: false
social: false # social links are placed directly below the introduction

announcements:
  enabled: false
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

<style>
  .post-title {
    font-weight: 700;
  }

  .about-intro {
    font-size: 1.05rem;
    line-height: 1.8;
    margin: 0 0 1.25rem;
  }

  .intro-socials {
    display: flex;
    gap: 1rem;
    margin: 1rem 0 3rem;
  }

  .intro-socials a {
    color: var(--global-text-color);
    font-size: 1.35rem;
    transition: color 0.2s ease, transform 0.2s ease;
  }

  .intro-socials a:hover {
    color: var(--global-theme-color);
    transform: translateY(-2px);
  }

  .about-section {
    margin-top: 3rem;
    scroll-margin-top: 5rem;
  }

  .about-section > h2 {
    border-bottom: 1px solid var(--global-divider-color);
    margin-bottom: 1.5rem;
    padding-bottom: 0.65rem;
  }

  .profile-entry,
  .publication-entry {
    margin-bottom: 2rem;
  }

  .entry-title {
    font-size: 1.08rem;
    font-weight: 600;
    line-height: 1.5;
    margin-bottom: 0.35rem;
  }

  .entry-role,
  .entry-authors {
    line-height: 1.65;
    margin-bottom: 0.25rem;
  }

  .entry-authors .author-link {
    color: var(--global-text-color);
  }

  .entry-authors .author-link:hover {
    color: var(--global-theme-color);
  }

  .entry-meta {
    color: var(--global-text-color-light);
    line-height: 1.6;
  }

  .publication-group {
    margin-top: 2rem;
  }

  .publication-group h3 {
    border-left: 4px solid var(--global-theme-color);
    font-size: 1.2rem;
    font-weight: 700;
    margin-bottom: 1.4rem;
    padding: 0.2rem 0 0.2rem 0.75rem;
  }
</style>

<script>
  document.addEventListener("DOMContentLoaded", () => {
    const navigation = document.querySelector("#navbarNav .navbar-menu-list");
    if (!navigation || navigation.querySelector("[data-profile-shortcut]")) return;

    const themeToggle = navigation.querySelector(".toggle-container");
    const shortcuts = [
      { label: "Publications", href: "{{ '/' | relative_url }}#publications" },
      { label: "CV", href: "{{ '/assets/pdf/Jiyeon_Son_CV.pdf' | relative_url }}", newTab: true },
    ];

    shortcuts.forEach(({ label, href, newTab }) => {
      const item = document.createElement("li");
      item.className = "nav-item";
      item.dataset.profileShortcut = label.toLowerCase();

      const link = document.createElement("a");
      link.className = "nav-link";
      link.href = href;
      link.textContent = label;
      if (newTab) {
        link.target = "_blank";
        link.rel = "noopener noreferrer";
      }

      item.appendChild(link);
      navigation.insertBefore(item, themeToggle);
    });
  });
</script>

<div class="about-intro">
  <p>
    I am an M.S. student in Computer Science at KAIST and a member of the
    <a href="https://ami.kaist.ac.kr/">Advanced Machine Intelligence Lab (AMI Lab)</a>, advised by
    <a href="https://pure.kaist.ac.kr/en/persons/tae-hyun-oh/">Prof. Tae-Hyun Oh</a>.
  </p>
  <p>I am interested in multimodal perception.</p>
</div>

<div class="intro-socials" aria-label="Contact links">
  <a href="mailto:daiisy7@kaist.ac.kr" aria-label="Email" title="Email"><i class="fa-solid fa-envelope"></i></a>
  <a href="https://github.com/fooooty" aria-label="GitHub" title="GitHub"><i class="fa-brands fa-github"></i></a>
  <a href="https://www.linkedin.com/in/daisyson01/" aria-label="LinkedIn" title="LinkedIn"><i class="fa-brands fa-linkedin"></i></a>
</div>

<section class="about-section">
  <h2>Experience</h2>
  <div class="profile-entry">
    <div class="entry-title">KT</div>
    <div class="entry-role">AI Research Intern</div>
    <div class="entry-meta">July 2026 – August 2026 · Seoul, South Korea</div>
  </div>
</section>

<section class="about-section">
  <h2>Education</h2>
  <div class="profile-entry">
    <div class="entry-title">Korea Advanced Institute of Science and Technology (KAIST)</div>
    <div class="entry-role">M.S. in Computer Science · <a href="https://ami.kaist.ac.kr/">Advanced Machine Intelligence Lab</a></div>
    <div class="entry-meta">September 2025 – August 2027 (expected)</div>
  </div>
  <div class="profile-entry">
    <div class="entry-title">Hanyang University</div>
    <div class="entry-role">B.S. in Materials Science and Engineering</div>
    <div class="entry-meta">February 2020 – August 2025</div>
  </div>
</section>

<section class="about-section" id="publications">
  <h2>Publications</h2>
  <div class="entry-meta">* Equal contribution</div>

  <div class="publication-group">
    <h3>Conference Papers</h3>
    <div class="publication-entry">
      <div class="entry-title"><a href="{{ '/projects/igg/' | relative_url }}">IGG: A Benchmark for Interactive GUI Grounding under Visibility Constraints</a></div>
      <div class="entry-authors"><a class="author-link" href="https://www.linkedin.com/in/ks-kim/">Kyeongseon Kim*</a>, <strong>Jiyeon Son*</strong>, Tae-Hyun Oh</div>
      <div class="entry-meta">EMNLP 2026 · Main Conference</div>
    </div>
  </div>

  <div class="publication-group">
    <h3>Workshop Papers</h3>
    <div class="publication-entry">
      <div class="entry-title"><a href="https://openreview.net/pdf/879ebea95a8b126a2c27d04cd7567b9d4b2019f1.pdf">Spatially Stable GUI Grounding via Zoom Consistency Loss</a></div>
      <div class="entry-authors">Ye-Bin Moon, <strong>Jiyeon Son</strong>, Tae-Hyun Oh</div>
      <div class="entry-meta">2nd Workshop on Compositional Learning: Safety, Interpretability, and Agents · ICML 2026</div>
    </div>
  </div>
</section>
