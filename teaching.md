---
layout: page
permalink: /teaching/
title: ""
---


{% include image.html url="../images/beyoglu.png" caption="road to the house in tomtom, april 18,  photo by me" width="800px" align="middle" %}

---

# Invited Lectures

{% for t in site.data.cv.invitedlect %}
**{{t.topic}}** <br />
*{{t.title}}* {% if t.prof %}*by {{t.prof}}*{% endif %}<br />
*{{t.date}} at {{t.school}}*

{% endfor %}


# Teaching Assistant

## University of Maryland

{% for t in site.data.cv.teachingumd %}
**{{t.title}}** {% if t.prof %}*by {{t.prof}}*{% endif %}<br />
*{{t.popul}} students in {{t.date}} at {{t.school}}*  <br />
{% if t.syl %}[[syllabus]({{t.syl}})]{% endif %}{% if t.url %} | [[web]({{t.url}})]{% endif %}<br />
{% if t.notes %}*{{t.notes}}*{% endif %}

{% endfor %}

##  Bogazici University

{% for t in site.data.cv.teaching %}
**{{t.title}}** {% if t.prof %}*by {{t.prof}}*{% endif %}<br />
*{{t.popul}} students in {{t.date}} at {{t.school}}*  <br />
{% if t.syl %}[[syllabus]({{t.syl}})]{% endif %}{% if t.url %} | [[web]({{t.url}})]{% endif %}<br />
{% if t.notes %}*{{t.notes}}*{% endif %}

{% endfor %}
