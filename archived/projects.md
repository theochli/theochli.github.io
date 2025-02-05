---
layout: page
title: projects
permalink: /projects/
description: Current projects in my lab
nav: true
---
<style>
  .custom-card {
    width: 100%;
    max-width: 800px;
    margin: 0 auto;
  }
</style>

<div class="projects grid">
  <div class="row justify-content-center">
    {% assign sorted_projects = site.projects | sort: "importance" %}
    {% for project in sorted_projects %}
      <div class="col-lg-9">
        <div class="grid-item">
          {% if project.redirect %}
            <a href="{{ project.redirect }}" target="_blank">
          {% else %}
            <a href="{{ project.url | relative_url }}">
          {% endif %}
            <div class="card hoverable custom-card">
              {% if project.img %}
                <img src="{{ project.img | relative_url }}" alt="project thumbnail">
              {% endif %}
              <div class="card-body">
                <h2 class="card-title text-lowercase">{{ project.title }}</h2>
                <p class="card-text">{{ project.description }}</p>
                <div class="row ml-1 mr-1 p-0">
                  {% if project.github %}
                    <div class="github-icon">
                      <div class="icon" data-toggle="tooltip" title="Code Repository">
                        <a href="{{ project.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
                      </div>
                      {% if project.github_stars %}
                        <span class="stars" data-toggle="tooltip" title="GitHub Stars">
                          <i class="fas fa-star"></i>
                          <span id="{{ project.github_stars }}-stars"></span>
                        </span>
                      {% endif %}
                    </div>
                  {% endif %}
                </div>
              </div>
            </div>
          </a>
        </div>
      </div>
      {% if forloop.index == 1 %}
        </div>
        <div class="row justify-content-center">
      {% endif %}
    {% endfor %}
  </div>
</div>
