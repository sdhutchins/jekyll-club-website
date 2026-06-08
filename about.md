---
layout: page
title: About
subtitle: Learn more about our organization.
permalink: /about/
---

## Mission

<!-- Replace this with your organization's mission statement. -->

Our club was founded to foster a community for students and trainees interested
in [your field] through professional development, social activities, and
community service.

## History

<!-- Replace this with your organization's history. -->

Founded in [year], our organization has grown to include members from diverse
disciplines. Over the years, we have organized workshops, hackathons, seminars,
and social events that bring together students passionate about [your field].

## Previous Presidents

<!-- Update this list with your organization's leadership history. -->

- First President (2020-2022)
- Second President (2022-2024)
- Current President (2024-Present)

{% if site.data.alumni.size > 0 %}

## Previous Executive Board Members

<div class="columns is-multiline alumni-grid">
{% for member in site.data.alumni %}
  <div class="column is-half-tablet is-one-third-desktop reveal">
    <div class="alumni-card">
      <div class="alumni-card-top">
        <div>
          <p class="title is-5 mb-1">{{ member.name }}</p>
          <p class="alumni-role mb-0">{{ member.role }}</p>
        </div>
        <span class="alumni-years">{{ member.years }}</span>
      </div>
      {% if member.current_position %}
      <p class="alumni-current-position">{{ member.current_position }}</p>
      {% endif %}
      {% if member.github or member.linkedin or member.bluesky or member.website %}
      <div class="alumni-links">
        {% if member.github %}
        <a href="https://github.com/{{ member.github }}" target="_blank" rel="noopener" aria-label="{{ member.name }} GitHub">
          <span class="icon"><i class="fab fa-github"></i></span>
        </a>
        {% endif %}
        {% if member.linkedin %}
        <a href="https://linkedin.com/in/{{ member.linkedin }}" target="_blank" rel="noopener" aria-label="{{ member.name }} LinkedIn">
          <span class="icon"><i class="fab fa-linkedin"></i></span>
        </a>
        {% endif %}
        {% if member.bluesky %}
        <a href="https://bsky.app/profile/{{ member.bluesky }}" target="_blank" rel="noopener" aria-label="{{ member.name }} Bluesky">
          <span class="icon"><i class="fab fa-bluesky"></i></span>
        </a>
        {% endif %}
        {% if member.website %}
        <a href="{{ member.website }}" target="_blank" rel="noopener" aria-label="{{ member.name }} Website">
          <span class="icon"><i class="fas fa-globe"></i></span>
        </a>
        {% endif %}
      </div>
      {% endif %}
    </div>
  </div>
{% endfor %}
</div>
{% endif %}
