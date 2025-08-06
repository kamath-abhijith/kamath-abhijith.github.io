---
layout: page
title: projects
permalink: /projects/
description: 
nav: true
nav_order: 3
display_categories: [unlimited sampling, inverse problems]
horizontal: false
---

<div class="projects-modern">
  {% if site.enable_project_categories and page.display_categories %}
    {% for category in page.display_categories %}
      <h2 class="category-header">{{ category }}</h2>
      <div class="projects-grid">
        {% assign categorized_projects = site.projects | where: "category", category %}
        {% assign sorted_projects = categorized_projects | sort: "importance" %}
        {% for project in sorted_projects %}
          {% include projects_modern.liquid %}
        {% endfor %}
      </div>
    {% endfor %}
  {% else %}
    <div class="projects-grid">
      {% assign sorted_projects = site.projects | sort: "importance" %}
      {% for project in sorted_projects %}
        {% include projects_modern.liquid %}
      {% endfor %}
    </div>
  {% endif %}
</div>

<style>
.projects-modern {
  margin-top: 2rem;
}

.category-header {
  color: black;
  border-bottom: 2px solid black;
  padding-bottom: 0.5rem;
  margin-bottom: 2rem !important;
  font-weight: 600;
  font-size: 1.5rem;
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
  gap: 1.5rem;
  margin-bottom: 3rem;
}

.project-card {
  display: flex;
  flex-direction: column;
  background-color: var(--global-card-bg-color);
  border: 1px solid var(--global-divider-color);
  padding: 1.5rem;
  border-radius: 12px;
  height: 100%;
  box-shadow: 0 2px 8px rgba(0,0,0,0.08);
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

.project-link {
  text-decoration: none;
  color: inherit;
  display: block;
}

.project-link:hover {
  text-decoration: none;
  color: inherit;
}

.project-card.clickable {
  cursor: pointer;
}

.project-card.clickable:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 25px rgba(0,0,0,0.15);
  border-color: var(--global-theme-color);
}

.project-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 3px;
  background: linear-gradient(90deg, var(--global-theme-color), #667eea);
  opacity: 0;
  transition: opacity 0.3s ease;
}

.project-card.clickable:hover::before {
  opacity: 1;
}

.project-header {
  display: flex;
  justify-content: flex-end;
  align-items: flex-start;
  margin-bottom: 1rem;
  height: 24px; /* Set a fixed height */
}

.project-code {
  background: linear-gradient(135deg, var(--global-theme-color), #8696fe);
  color: white;
  padding: 0.4rem 0.8rem;
  border-radius: 20px;
  font-size: 0.85rem;
  font-weight: 600;
  min-width: fit-content;
}

.project-link-icon {
  color: var(--global-text-color-light);
  opacity: 0.7;
  transition: opacity 0.2s ease;
}

.project-card.clickable:hover .project-link-icon {
  opacity: 1;
  color: var(--global-theme-color);
}

.project-content {
  flex-grow: 1;
}

.project-image-container {
  margin-bottom: 1rem;
  overflow: hidden;
  border-radius: 8px;
}

.project-image {
  width: 100%;
  height: auto;
  display: block;
  transition: transform 0.3s ease;
}

.project-card.clickable:hover .project-image {
  transform: scale(1.05);
}

.project-title {
  color: var(--global-text-color);
  font-weight: 600;
  line-height: 1.3;
  margin-bottom: 0.75rem !important;
  transition: color 0.3s ease;
}

.project-card.clickable:hover .project-title {
  color: var(--global-theme-color);
}

.project-description {
  color: var(--global-text-color-light);
  font-size: 0.95rem;
  line-height: 1.5;
  margin-bottom: 1rem !important;
}

.project-footer {
  margin-top: auto;
  padding-top: 1rem;
  border-top: 1px solid var(--global-divider-color);
  display: flex;
  justify-content: flex-end;
}

.github-button {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background-color: var(--global-bg-color);
  color: var(--global-text-color);
  padding: 0.5rem 1rem;
  border-radius: 20px;
  border: 1px solid var(--global-divider-color);
  font-weight: 500;
  font-size: 0.85rem;
  text-decoration: none !important;
  transition: all 0.3s ease;
}

.github-button:hover {
  background-color: var(--global-theme-color);
  color: white;
  border-color: var(--global-theme-color);
}

.github-button .fa-star {
  color: #ffc107;
}

@media (max-width: 768px) {
  .projects-grid {
    grid-template-columns: 1fr;
    gap: 1rem;
  }
  
  .project-card {
    padding: 1.25rem;
  }
}

html[data-theme="dark"] .project-card {
  background-color: var(--global-card-bg-color);
  border-color: var(--global-divider-color);
}

html[data-theme="dark"] .project-card.clickable:hover {
  box-shadow: 0 8px 25px rgba(255,255,255,0.1);
}

html[data-theme="dark"] .github-button {
  background-color: var(--global-card-bg-color);
  border-color: var(--global-divider-color);
}
</style>
