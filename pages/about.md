---
title: About
permalink: /about/
layout: single
classes: wide
sidebar:
  title: "About"
  nav: sidebar-about
---
About
=====
When users **access shared resources in a selfish manner**, the resulting societal cost and perceived users' cost is often higher than what would result from a centrally coordinated optimal allocation. While several contributions in **mechanism design** manage to steer the aggregate users choices to the desired optimum by using **monetary tolls**, such approaches bear the inherent drawback of **discriminating against users with a lower income**. Against this backdrop, with the FISH project, we aim to **design incentive schemes** based on **artificial currencies** with the goal of achieving a **system-optimal resource allocation** that is also **fair**.
{: .text-justify}

***

People
=====
{% for author in site.data.authors %} {{author.name}}<sup>{{author.affiliation}}</sup> | {% if author.website %}<a itemprop="sameAs" target="_blank" content="{{author.website}}" href="{{author.website}}" target="blank" rel="me noopener noreferrer" style="vertical-align:top;"><img src="/assets/img/emoji/link_1f517.png" style="width:1em;margin-right:.5em;" alt="Website"></a>{%endif%}{% if author.orcid %}<a itemprop="sameAs" target="_blank" content="{{author.orcid}}" href="{{author.orcid}}" target="orcid.widget" rel="me noopener noreferrer" style="vertical-align:top;"><img src="https://orcid.org/sites/default/files/images/orcid_16x16.png" style="width:1em;margin-right:.5em;" alt="ORCID iD icon"></a>{%endif%}{% if author.googlescholar %}<a target="_blank" itemprop="sameAs" href="{{author.googlescholar}}" style="vertical-align:top;"><img src="https://upload-icon.s3.us-east-2.amazonaws.com/uploads/icons/png/17520148421579517848-512.png" style="width:1em;margin-right:.5em;"></a>{%endif%}{% if author.github %}<a itemprop="sameAs" target="_blank" content="{{author.github}}" href="{{author.github}}" rel="me noopener noreferrer" style="vertical-align:top;"><img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" style="width:1em;margin-right:.5em;" alt="GitHub icon"></a>{%endif%}<br>{% endfor %}

{% for affiliation in site.data.author-affiliation %} <sup>{{affiliation.superscript}}</sup>{{affiliation.affiliation}}{%endfor%}

***

Contact
=====
The FISH repositories are currently maintained by Leonardo Pedroso (<a href = "mailto: l.pedroso@tue.nl">l.pedroso@tue.nl</a>).
