---
layout: default
title: Home
---

<section class="hero-section">
    <h1>Hi, I'm Shaheen Kabir 👋</h1>
    <p class="tagline">Data Science Enthusiast | R & Python Developer | Researcher in Biology</p>
</section>

<section class="quick-nav">
    <a href="{{ "/projects/" | relative_url }}" class="nav-button primary">
        <i class="fas fa-chart-line"></i> View Interactive Projects
    </a>
    <a href="{{ "/blog/" | relative_url }}" class="nav-button">
        <i class="fas fa-feather-alt"></i> Read Articles
    </a>
    <a href="{{ "/about/" | relative_url }}" class="nav-button">
        <i class="fas fa-id-card"></i> About Me
    </a>
</section>

<section class="latest-content">
    <h2>Latest Articles</h2>
    <ul>
      {% for post in site.posts limit:5 %}
        <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> — {{ post.date | date: "%Y-%m-%d" }}</li>
      {% endfor %}
    </ul>
</section>

<section class="contact-cta">
    <p>Ready to collaborate or chat about research?</p>
    <a href="mailto:shaheenkabir098@gmail.com" class="cta-button">
        Get in Touch
    </a>
</section>