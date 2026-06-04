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

<ul>
{% for member in site.data.alumni %}
  <li>
    <strong>{{ member.name }}</strong> &mdash; {{ member.role }} ({{ member.years }})
    {% if member.current_position %}<br><em>{{ member.current_position }}</em>{% endif %}
    {% if member.github %}
      <a href="https://github.com/{{ member.github }}" target="_blank" rel="noopener"><i class="fab fa-github"></i></a>
    {% endif %}
    {% if member.linkedin %}
      <a href="https://linkedin.com/in/{{ member.linkedin }}" target="_blank" rel="noopener"><i class="fab fa-linkedin"></i></a>
    {% endif %}
    {% if member.bluesky %}
      <a href="https://bsky.app/profile/{{ member.bluesky }}" target="_blank" rel="noopener"><i class="fab fa-bluesky"></i></a>
    {% endif %}
    {% if member.website %}
      <a href="{{ member.website }}" target="_blank" rel="noopener"><i class="fas fa-globe"></i></a>
    {% endif %}
  </li>
{% endfor %}
</ul>
{% endif %}
