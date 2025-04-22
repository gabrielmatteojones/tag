---
layout: default
title: Homepage di esempio
description: Questo è un esempio di homepage con utilizzo del componente "hero"
lang: it
ref: homepage
permalink: /
order: 1
---

<div class="container my-4">
  <div class="row">
    {% for post in site.posts %}
      <div class="col-md-6 mb-4">
        <div class="card shadow-sm">
          <div class="card-body">
            <h5 class="card-title">
              <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
            </h5>
            {% if post.dipartimento %}
              <p class="card-subtitle text-muted mb-2">{{ post.dipartimento }}</p>
            {% endif %}
            <p class="card-text">
              {{ post.content | strip_html | truncate: 150 }}
            </p>
            <a href="{{ post.url | relative_url }}" class="btn btn-sm btn-outline-primary">Leggi di più</a>
          </div>
        </div>
      </div>
    {% endfor %}
  </div>
</div>
