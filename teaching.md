---
layout: page
permalink: /teaching/
title: "Teaching"
---

## As a Teaching Assistant

{% for t in site.data.cv.teaching %}
<!-- {% if pub.image %}
{% include image.html url=pub.image caption="" height="80px" align=thumbnail %}
{% endif %} 
{{t.role}}<br />
-->
**{{t.title}}** {% if t.prof %}*by {{t.prof}}*{% endif %}<br />
*{{t.popul}} students in {{t.date}} at {{t.school}}*  <br />
{% if t.syl %}[[syllabus]({{t.syl}})]{% endif %}{% if t.url %} | [[web]({{t.url}})]{% endif %}<br />
{% if t.notes %}*{{t.notes}}*{% endif %}

{% endfor %}