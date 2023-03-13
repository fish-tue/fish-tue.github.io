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
The presence of self-interested users in **shared resource allocation settings** leads to usage patters that **inefficient** compared with the system's optimum. Specifically, within mobility systems, the presence of self-interested commuters leads to aggregate routing patterns that are far from the societal optimum that could be achieved by centrally controlling the user's mobility patters. With the FISH project we strive to develop **human-centered fair incentive mechanisms** through **artificial currencies** so that the selfish behavior of the users aligns with the societally-optimal aggregate behaviour.
{: .text-justify}

***

People
=====
{% for author in site.data.authors %} {{author.name}}<sup>{{author.affiliation}}</sup> | {% if author.website %}<a itemprop="sameAs" target="_blank" content="{{author.website}}" href="{{author.website}}" target="blank" rel="me noopener noreferrer" style="vertical-align:top;"><img src="/assets/img/emoji/link_1f517.png" style="width:1em;margin-right:.5em;" alt="Website"></a>{%endif%}{% if author.orcid %}<a itemprop="sameAs" target="_blank" content="{{author.orcid}}" href="{{author.orcid}}" target="orcid.widget" rel="me noopener noreferrer" style="vertical-align:top;"><img src="https://orcid.org/sites/default/files/images/orcid_16x16.png" style="width:1em;margin-right:.5em;" alt="ORCID iD icon"></a>{%endif%}{% if author.googlescholar %}<a target="_blank" itemprop="sameAs" href="{{author.googlescholar}}" style="vertical-align:top;"><img src="https://upload-icon.s3.us-east-2.amazonaws.com/uploads/icons/png/17520148421579517848-512.png" style="width:1em;margin-right:.5em;"></a>{%endif%}{% if author.github %}<a itemprop="sameAs" target="_blank" content="{{author.github}}" href="{{author.github}}" rel="me noopener noreferrer" style="vertical-align:top;"><img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" style="width:1em;margin-right:.5em;" alt="GitHub icon"></a>{%endif%}<br>{% endfor %}

{% for affiliation in site.data.author-affiliation %} <sup>{{affiliation.superscript}}</sup>{{affiliation.affiliation}}{%endfor%}

***

Contact
=====
The FISH repositories are currently mantained by Leonardo Pedroso (<a href = "mailto: l.pedroso@tue.nl">l.pedroso@tue.nl</a>).
