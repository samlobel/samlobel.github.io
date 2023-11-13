---
layout: page
permalink: /research/
title: Research
---


## Peer reviewed publications

{% assign thumbnail="right" %}

{% for pub in site.data.cv.publications %}
<!-- {% if pub.image %}
{% include image.html url=pub.image caption="" height="80px" align=thumbnail %}
{% endif %} -->
{{pub.author}}<br />
**{{pub.title}}**<br />
*{{pub.journal}}*
{% if pub.note %} *({{pub.note}})*
{% endif %} *{{pub.year}}*  {% if pub.url %}[<a href="{% if pub.internal %}{{pub.url | prepend: site.baseurl}}{% else %}{{pub.url}}{% endif %}" target="_blank">web</a>]{% endif %} {% if pub.doi %}[[doi]({{pub.doi}})]{% endif %} {% if pub.pdf %}[<a href="{{pub.pdf}}" target="_blank">pdf</a>]{% endif %} {% if pub.code %}[<a href="{{pub.code}}" target="_blank">code</a>]{% endif %} {% if pub.presentation %}[<a href="{{pub.presentation}}" target="_blank">video</a>]{% endif %}{% if pub.second_pub_note %}<br />{{pub.second_pub_note}} [<a href="{{pub.second_pub_pdf}}" target="_blank">pdf</a>]
{% endif %}
{% endfor %}

<!-- -----

## Doctoral thesis

**Algorithms & perceptual analysis for interactive free viewpoint image-based navigation** [[web]({{ "/research/thesis/" | prepend: site.baseurl}})]<br />
*Adviser: [George Drettakis](http://www-sop.inria.fr/members/George.Drettakis)* <br />
[INRIA](http://www.inria.fr/sophia), 2014

------

## Media coverage

{% for pub in site.data.cv.publications %}
{% if pub.media %}
- {{pub.title}} ({{pub.note}}, {{pub.year}}){% for article in pub.media %}
    - [{{article.url}}]({{article.url}}){% endfor %}
{% endif %}

{% endfor %}

------

## Professional service

- Grant proposals{% for review in site.data.cv.reviews.grants %}
    - {{review.title}} {% for y in review.years %} [{% if review.url %}[{{y.year}}]({{review.url}}){% else %}{{y.year}}{% endif %}] {% endfor %}<br />{% endfor %}

- Conference reviews{% for review in site.data.cv.reviews.conference %}
    - {{review.title}} {% for y in review.years %} [{% if y.url %}[{{y.year}}]({{y.url}}){% else %}{{y.year}}{% endif %}] {% endfor %}<br />{% endfor %}

- Journal reviews{% for review in site.data.cv.reviews.journal %}
    - {{review.title}} {% for y in review.years %} [{% if review.url %}[{{y.year}}]({{review.url}}){% else %}{{y.year}}{% endif %}] {% endfor %}<br />{% endfor %} -->
