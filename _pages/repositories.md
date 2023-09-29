---
layout: page
permalink: /repositories/
title: repositories
description: 
nav: true
nav_order: 3
---

Public datasets available through my work at ARL and UCSC.

- **ARL Creative Visual Storytelling Anthology** is a collection of 100 author responses to an improved creative visual storytelling exercise. Each item contains four facet entries, corresponding to Entity, Scene, Narrative, and Title. The ARL Creative Visual Storytelling Anthology was collected on Amazon Mechanical Turk.
- **PersonaBank** is a collection of 108 personal stories from weblogs that have been annotated with their Story Intention Graphs, a deep representation of the fabula of a story.
- **Sarcasm Corpus V1** is a subset of the Internet Argument Corpus, including response text from quote-response pairs annotated for sarcasm.
- **Persuasion and Personality Corpus** is a subset of user-generated dialogs from the Internet Argument Corpus exploring the role of affect in persuasive arguments, 637 subjects profiled for the Big Five personality traits and prior beliefs about socio-political issues, and the subjects' response after exposure to user-generated, factual vs. emotional dialogic exchanges compared to the effects on belief change to balanced, curated arguments.

{% if site.data.repositories.github_users %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.html username=user %}
  {% endfor %}
</div>

---

{% if site.repo_trophies.enabled %}
{% for user in site.data.repositories.github_users %}
  {% if site.data.repositories.github_users.size > 1 %}
  <h4>{{ user }}</h4>
  {% endif %}
  <div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% include repository/repo_trophies.html username=user %}
  </div>

  ---

{% endfor %}
{% endif %}
{% endif %}

## GitHub Repositories

{% if site.data.repositories.github_repos %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %}
