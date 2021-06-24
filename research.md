---
layout: page
permalink: /research/
title: Research
---

Jump to [Publications](#publications), [Proceedings](#proceedings)[Talks](#talks), [Reviewing](#reviews)

---

## Publications

{% assign thumbnail="right" %}

{% for pub in site.data.cv.publications %}
<!-- {% if pub.image %}
{% include image.html url=pub.image caption="" height="80px" align=thumbnail %}
{% endif %} -->
{{pub.author}}<br />
**{{pub.title}}**<br />
*{{pub.journal}}*
{% if pub.note %} *({{pub.note}})*
{% endif %} *{{pub.year}}*  [[web]({% if pub.internal %}{{pub.url | prepend: site.baseurl}}{% else %}{{pub.url}}{% endif %})] {% if pub.doi %}[[doi]({{pub.doi}})]{% endif %}

{% endfor %}

-----

## Peer Reviewed Proceedings

{% for pub in site.data.cv.proceedings %}
<!-- {% if pub.image %}
{% include image.html url=pub.image caption="" height="80px" align=thumbnail %}
{% endif %} -->
{{pub.author}}<br />
**{{pub.title}}**<br />
*{{pub.journal}}*
{% if pub.note %} *({{pub.note}})*
{% endif %} *{{pub.year}}*  {% if pub.abs %}[[abstract]({{pub.abs}})]{% endif %} {% if pub.ho %}| [[handout]({{pub.ho}})]{% endif %} {% if pub.slide %}| [[slides]({{pub.slide}})]{% endif %}

{% endfor %}

-----


## Talks


{% for talk in site.data.cv.conferences %}
<!-- {% if pub.image %}
{% include image.html url=pub.image caption="" height="80px" align=thumbnail %}
{% endif %} -->
{{talk.author}}<br />
**{{talk.title}}**<br />
*{{talk.conf}}*
{% if talk.note %} *({{talk.note}})*
{% endif %} *{{talk.year}}*  [[web]({% if talk.internal %}{{talk.url | prepend: site.baseurl}}{% else %}{{talk.url}}{% endif %})] {% if talk.abstract %}[[abstract]({{talk.abstract}})]{% endif %} {% if talk.handout %}[[handout]({{talk.handout}})]{% endif %} {% if talk.poster %}[[poster]({{talk.poster}})]{% endif %} {% if talk.slides %}[[slides]({{talk.slide}})]{% endif %}

{% endfor %}

-----

## Professional service

- Conference reviews{% for review in site.data.cv.reviews.conference %}
    - {{review.title}} {% for y in review.years %} [{% if y.url %}[{{y.year}}]({{y.url}}){% else %}{{y.year}}{% endif %}] {% endfor %}<br />{% endfor %}

- Journal reviews{% for review in site.data.cv.reviews.journal %}
    - {{review.title}} {% for y in review.years %} [{% if review.url %}[{{y.year}}]({{review.url}}){% else %}{{y.year}}{% endif %}] {% endfor %}<br />{% endfor %}
