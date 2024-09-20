---
layout: page
title: Staff
description: A listing of all the course staff members.
---

# Staff



## Instructor

{% assign instructors = site.staffers | where: 'role', 'Instructor' %}
{% for staffer in instructors %}
{{ staffer }}
{% endfor %}

{% assign teaching_assistants = site.staffers | where: 'role', 'Teaching Assistant' %}
{% assign num_teaching_assistants = teaching_assistants | size %}
{% if num_teaching_assistants != 0 %}

## Teaching Assistants

{% for staffer in teaching_assistants %}
{{ staffer }}
{% endfor %}
{% endif %}

{% assign peer_mentors = site.staffers | where: 'role', 'Peer Mentor' %}
{% assign num_peer_mentors = peer_mentors | size %}
{% if num_peer_mentors != 0 %}

## Peer Mentors

{% for staffer in peer_mentors %}
{{ staffer }}
{% endfor %}
{% endif %}
