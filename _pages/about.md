---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<section id="about-me" class="home-section intro-section">
  <p class="intro__eyebrow">Second-year Ph.D. student &middot; Emory University</p>
  <h1 class="intro__title">Shengbo Gong</h1>
  <p class="intro__statement">Data-efficient learning for language models and graphs.</p>
  <p class="intro__lead">
    I am a second-year Ph.D. student in Computer Science and Informatics at Emory University,
    co-advised by Prof. <a href="https://www.cs.emory.edu/~wjin30/" target="_blank" rel="noopener">Wei Jin</a>
    and Prof. <a href="https://www.cs.emory.edu/~jyang71/" target="_blank" rel="noopener">Carl Yang</a>.
    Before joining Emory, I worked with Prof. <a href="https://en.bme.sjtu.edu.cn/show-33-130.html" target="_blank" rel="noopener">Yifei Yao</a>
    at Shanghai Jiao Tong University and Prof. <a href="http://xuanqi-net.com/" target="_blank" rel="noopener">Qi Xuan</a>
    at Zhejiang University of Technology.
  </p>

  <div class="research-focus" aria-label="Research interests">
    <span class="research-focus__label">Research interests</span>
    <ul>
      <li>Data-Efficient LLMs</li>
      <li>Graph Learning</li>
      <li>Data-Centric AI</li>
    </ul>
  </div>

  <div class="intro__actions">
    <a class="action-link action-link--primary" href="{{ '/files/Shengbo_Gong_CV.pdf' | relative_url }}" target="_blank">
      <i class="fas fa-file-pdf" aria-hidden="true"></i> View CV
    </a>
    <a class="action-link" href="{{ site.author.googlescholar }}" target="_blank" rel="noopener">
      <i class="fas fa-graduation-cap" aria-hidden="true"></i> Google Scholar
    </a>
  </div>

  <p class="intro__personal">
    Outside research, I enjoy swimming, hiking, climbing, tabletop games, strategy games, films, and books.
  </p>
</section>

<section id="citations" class="home-section citations-section">
  <div class="section-heading">
    <p class="section-heading__kicker">01 / Research impact</p>
    <h2>Google Scholar Citations</h2>
  </div>

  <div class="citation-panel">
    <div class="citation-panel__summary">
      <div>
        <span class="citation-panel__label">Total citations</span>
        <strong>{{ site.data.citations.total }}</strong>
      </div>
      <p>
        Static snapshot from
        <a href="{{ site.data.citations.source }}" target="_blank" rel="noopener">Google Scholar</a>.
        Data through <time datetime="{{ site.data.citations.as_of_iso }}">{{ site.data.citations.as_of }}</time>.
      </p>
    </div>

    <div class="citation-chart">
      <div class="citation-chart__axis" aria-hidden="true">
        <span>150</span>
        <span>100</span>
        <span>50</span>
        <span>0</span>
      </div>
      <ol class="citation-chart__bars" aria-label="Citations by year">
        {% for citation in site.data.citations.years %}
          <li aria-label="{{ citation.year }}: {{ citation.count }} citations">
            <div class="citation-chart__track">
              <span class="citation-chart__value" style="bottom: calc({{ citation.height }}% + 0.45rem);">{{ citation.count }}</span>
              <span class="citation-chart__bar" style="height: {{ citation.height }}%;"></span>
            </div>
            <span class="citation-chart__year">{{ citation.year }}</span>
          </li>
        {% endfor %}
      </ol>
    </div>
    <p class="citation-panel__note">2026 is year-to-date. Earlier citations are included in the total but are outside the profile's displayed annual chart.</p>
  </div>
</section>

<section id="news" class="home-section">
  <div class="section-heading">
    <p class="section-heading__kicker">02 / Latest</p>
    <h2>News</h2>
  </div>
  <ul class="news-list">
    <li><time>2026.04</time><span>Our work on <a href="https://arxiv.org/abs/2508.02435" target="_blank" rel="noopener">efficient RAG</a> was accepted to ACL Findings 2026.</span></li>
    <li><time>2025.11</time><span>Our work on <a href="https://arxiv.org/abs/2502.17614" target="_blank" rel="noopener">efficient graph condensation</a> was accepted to KDD 2026.</span></li>
    <li><time>2025.10</time><span>Received NeurIPS travel funding.</span></li>
    <li><time>2025.09</time><span><a href="https://arxiv.org/abs/2406.16715" target="_blank" rel="noopener">GC4NC</a> was accepted to NeurIPS 2025.</span></li>
    <li><time>2025.05</time><span>Presented graph reduction research at the SDM Doctoral Forum and received NSF travel funding.</span></li>
    <li><time>2025.01</time><span>Our co-first-author work on graph heterophily was accepted to TPAMI.</span></li>
    <li><time>2024.11</time><span>Received a Google Cloud Research Credits Award.</span></li>
    <li><time>2024.04</time><span>Our graph reduction survey was accepted to IJCAI 2024.</span></li>
  </ul>
</section>

<section id="publications" class="home-section">
  <div class="section-heading">
    <p class="section-heading__kicker">03 / Research</p>
    <h2>Selected Publications</h2>
  </div>
  <p class="section-intro">Representative work spanning data-efficient LLMs, graph learning, and data-centric AI.</p>

  <div class="publication-list">
    {% for publication in site.data.publications %}
      <article class="publication-card">
        <figure class="publication-card__figure">
          <a href="{{ publication.paper }}" target="_blank" rel="noopener" aria-label="Open {{ publication.title }}">
            <img src="{{ publication.image | relative_url }}" alt="{{ publication.image_alt }}" loading="lazy">
          </a>
          <figcaption>{{ publication.figure_caption }}</figcaption>
        </figure>
        <div class="publication-card__content">
          <div class="publication-card__meta">
            <span class="venue venue--{{ publication.topic }}">{{ publication.venue }} {{ publication.year }}</span>
          </div>
          <h3><a href="{{ publication.paper }}" target="_blank" rel="noopener">{{ publication.title }}</a></h3>
          <p class="publication-card__authors">{{ publication.authors }}</p>
          <div class="publication-card__links">
            <a class="action-link action-link--small" href="{{ publication.paper }}" target="_blank" rel="noopener">
              <i class="fas fa-file-alt" aria-hidden="true"></i> Paper
            </a>
            {% if publication.code %}
              <a class="action-link action-link--small" href="{{ publication.code }}" target="_blank" rel="noopener">
                <i class="fab fa-github" aria-hidden="true"></i> Code
              </a>
            {% endif %}
          </div>
        </div>
      </article>
    {% endfor %}
  </div>
  <p class="publication-note"><sup>*</sup> Equal contribution.</p>
</section>

<section id="internships" class="home-section">
  <div class="section-heading">
    <p class="section-heading__kicker">04 / Experience</p>
    <h2>Internships</h2>
  </div>
  <div class="experience-row">
    <time>May-Aug 2026</time>
    <div>
      <h3>Applied Scientist Intern <span>Amazon</span></h3>
      <p>Worked on foundation models for event streams and causal inference.</p>
    </div>
  </div>
</section>

<section id="presentations" class="home-section">
  <div class="section-heading">
    <p class="section-heading__kicker">05 / Speaking</p>
    <h2>Public Presentations</h2>
  </div>
  <div class="presentation-row">
    <time>Dec 2023</time>
    <p>ICDM Workshop on Blockchain: <a href="https://arxiv.org/abs/2310.00856" target="_blank" rel="noopener">Multi-triplet Feature Augmentation for Ponzi Scheme Detection in Ethereum</a>.</p>
  </div>
</section>
