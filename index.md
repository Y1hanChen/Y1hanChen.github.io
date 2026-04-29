---
layout: default
---

<div class="home">
  <div class="profile-section">
    <div class="profile-image">
      <img src="{{ '/assets/img/profile.jpg' | relative_url }}" alt="{{ site.author.name }}">
    </div>
    <div class="profile-info">
      <h1 class="profile-name">{{ site.author.name }}</h1>
      <p class="profile-position">{{ site.author.position }}</p>
      <p class="profile-institution">
        {{ site.author.institution }}<br>
        {{ site.author.university }}
      </p>
      <p class="profile-advisor">Advisor: {{ site.author.advisor }}</p>
      
      <div class="contact-info">
        <p><i class="fas fa-envelope"></i> <a href="mailto:{{ site.email }}">{{ site.email }}</a></p>
      </div>

      <div class="social-links-home">
        {% if site.github_username %}
        <a href="https://github.com/{{ site.github_username }}" target="_blank" title="GitHub">
          <i class="fab fa-github"></i>
        </a>
        {% endif %}
        {% if site.scholar_userid %}
        <a href="https://scholar.google.com/citations?user={{ site.scholar_userid }}" target="_blank" title="Google Scholar">
          <i class="fas fa-graduation-cap"></i>
        </a>
        {% endif %}
        {% if site.linkedin_username %}
        <a href="https://linkedin.com/in/{{ site.linkedin_username }}" target="_blank" title="LinkedIn">
          <i class="fab fa-linkedin"></i>
        </a>
        {% endif %}
      </div>
    </div>
  </div>

  <section class="about-section">
    <h2>About Me</h2>
    <p>
      I am a Master's student at the <strong>Institute of Software, Chinese Academy of Sciences (ISCAS)</strong> 
      and <strong>University of Chinese Academy of Sciences (UCAS)</strong>, advised by Prof. Ben He (何苯). 
      My research focuses on <strong>Large Language Models (LLMs)</strong>, 
      <strong>Retrieval-Augmented Generation (RAG)</strong>, and <strong>Responsible AI</strong>.
    </p>
  </section>

  <section class="research-interests">
    <h2>Research Interests</h2>
    <ul class="interests-list">
      <li><strong>Large Language Models (LLMs)</strong></li>
      <li><strong>Retrieval-Augmented Generation (RAG)</strong></li>
      <li><strong>Responsible AI</strong></li>
    </ul>
  </section>

  <section class="education-section">
    <h2>Education</h2>
    <div class="education-item">
      <div class="edu-header">
        <h3>University of Chinese Academy of Sciences (UCAS)</h3>
        <span class="edu-date">2024.09 - 2027.06</span>
      </div>
      <p class="edu-degree">Master of Engineering in Electronic Information</p>
      <p class="edu-detail">Chinese Information Processing Laboratory, ISCAS</p>
    </div>

    <div class="education-item">
      <div class="edu-header">
        <h3>Nankai University</h3>
        <span class="edu-date">2020.09 - 2024.06</span>
      </div>
      <p class="edu-degree">Bachelor of Engineering in Software Engineering</p>
    </div>
  </section>

  <section class="news-section">
    <h2>Recent News</h2>
    <ul class="news-list">
      <li><strong>[2026.03]</strong> Our paper "CoCoNUTS" has been accepted to ACL 2026 Main Conference!</li>
      <li><strong>[2024.09]</strong> Started my Master's program at ISCAS/UCAS.</li>
    </ul>
  </section>
</div>
