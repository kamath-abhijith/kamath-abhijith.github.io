---
layout: about
title: about
permalink: /
subtitle: PhD Student @ <a href="https://spectrum-lab-iisc.github.io" target="_blank" rel="noopener">Spectrum Lab</a>, <a href="http://iisc.ac.in" target="_blank" rel="noopener">Indian Institute of Science</a>

profile:
    align: right
    image: Abijith.jpg
    image_circular: false # crops the image to make it circular
    more_info: >

news: true # includes a list of news items
latest_posts: true # includes a list of the newest posts
selected_papers: true # includes a list of papers marked as "selected={true}"
social: false # includes social icons at the bottom of the page
---

<div class="intro-section">
    <div class="intro-content">
        <div class="intro-highlight">
            <i class="fas fa-rocket"></i>
            <span>Research Focus</span>
        </div>
        <p class="intro-text">
            <strong>I want to challenge the frontiers of computational imaging.</strong>
        </p>
        <p class="intro-description">
            I work in the intersection of sampling theory, inverse problems and machine learning for event-driven imaging &mdash; <em>with high speed and dynamic range!</em>
        </p>
        <div class="intro-background">
            <i class="fas fa-university"></i>
            <span>Previously at <a href="https://www.nitk.ac.in" target="_blank" rel="noopener">National Institute of Technology Karnataka</a>.</span>    </div>
    </div>
</div>

<style>
/* Enhanced Intro Section */
.intro-section {
  background-color: var(--global-card-bg-color);
  border: 1px solid var(--global-divider-color);
  border-radius: 12px;
  padding: 2rem;
  margin: 2rem 0;
  box-shadow: 0 2px 8px rgba(0,0,0,0.08);
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

.intro-section:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 25px rgba(0,0,0,0.15);
}

.intro-section::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 3px;
  background: linear-gradient(90deg, var(--global-theme-color), #667eea);
}

.intro-content {
  max-width: 700px;
  margin: 0 auto;
}

.intro-highlight {
  display: inline-flex;
  align-items: center;
  background: linear-gradient(135deg, #d3d3d3, #a9a9a9);
  color: #333333;
  padding: 0.4rem 0.8rem;
  border-radius: 20px;
  font-size: 0.85rem;
  font-weight: 600;
  margin-bottom: 1.5rem;
}

.intro-highlight i {
  margin-right: 0.5rem;
}

.intro-text {
  font-size: 1.3rem;
  line-height: 1.4;
  color: var(--global-text-color);
  margin-bottom: 1.2rem;
}

.intro-description {
  font-size: 1.1rem;
  line-height: 1.6;
  color: var(--global-text-color-light);
  margin-bottom: 1.5rem;
}

.intro-background {
  display: flex;
  align-items: center;
  font-size: 0.95rem;
  color: var(--global-text-color-light);
  padding: 0.8rem 1rem;
  background-color: var(--global-bg-color);
  border: 1px solid var(--global-divider-color);
  border-radius: 8px;
}

.intro-background i {
  margin-right: 0.5rem;
  color: var(--global-theme-color);
}

/* Dark mode compatibility */
html[data-theme="dark"] .intro-section {
  background-color: var(--global-card-bg-color);
  border-color: var(--global-divider-color);
}

html[data-theme="dark"] .intro-section:hover {
  box-shadow: 0 8px 25px rgba(255,255,255,0.1);
}

html[data-theme="dark"] .intro-background {
  background-color: var(--global-card-bg-color);
  border-color: var(--global-divider-color);
}

/* Responsive design */
@media (max-width: 768px) {
  .intro-section {
    padding: 1.5rem;
    margin: 1.5rem 0;
  }
  
  .intro-text {
    font-size: 1.2rem;
  }
  
  .intro-description {
    font-size: 1rem;
  }
}

@media (max-width: 600px) {
  .intro-section {
    padding: 1.25rem;
  }
  
  .intro-text {
    font-size: 1.1rem;
  }
  
  .intro-description {
    font-size: 0.95rem;
  }
}
</style>
