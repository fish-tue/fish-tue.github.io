---
layout: splash
title: "FISH"
entries_layout: grid
excerpt: "Fair Incentive mechanisms for Sustainable Human-centered mobility"
description: "Research project on fair incentive mechanisms for sustainable human-centered mobility through artificial currencies at TU Eindhoven"
header:
  overlay_image: assets/img/splash.webp
  overlay_filter: 0.1
  text_color: "#ffffff"
  text_outline_color: "#99999"

single-origin-destination-routing:
  - image_path: /assets/img/research/single-origin-destination-routing/teaser.webp
    alt: "single-origin-destination-routing"
    title: "Urgency-aware Routing in Single Origin-destination Itineraries through Artificial Currencies"
    excerpt: "Within mobility systems, the presence of self-interested users can lead to aggregate routing patterns that are far from the societal optimum that could be achieved by centrally controlling the user's choices. We design an urgency-aware fair incentive mechanism through artificial currencies so that the selfish behavior of the users aligns with the societally-optimal aggregate routing for single origin-destination inteneraries."
    url: "single-origin-destination-routing/"
    btn_label: "Read More"
    btn_class: "btn--warning"

AC-weighted-eqt-eql:
  - image_path: /assets/img/research/AC-weighted-eqt-eql/teaser.webp
    alt: "AC-weighted-eqt-eql"
    title: "Fair Artificial Currency Incentives in Repeated Weighted Congestion Games: Equity vs. Equality"
    excerpt: "Incentive schemes utilizing artificial currencies have been explored to achieve a system-optimal resource allocation that is also fair, contrarily to state-of-the-art monetary schemes. This paper delves into the comprehensive notion of fairness by meticulously optimizing for the societal metrics of equity and equality."
    url: "AC-weighted-eqt-eql/"
    btn_label: "Read More"
    btn_class: "btn--warning"
---

<h2>👋🏻 Welcome </h2>

{% comment %}
<div class="row">
  <div class="column">
  Current mobility systems face many <b>challenges</b>:<br>🔸 traffic <b>congestion</b><br>🔸 evironmental <b>pollution</b><br>🔸 user <b>dissatisfaction</b>
  </div>
  <div class="column">
  <img src = ""> </img>
  </div>
</div>
{% endcomment %}

The presence of self-interested users in **shared resource allocation settings** leads to usage patters that **inefficient** compared with the system's optimum. Specifically, within mobility systems, the presence of self-interested commuters leads to aggregate routing patterns that are far from the societal optimum that could be achieved by centrally controlling the user's mobility patters. With the FISH project we strive to develop **human-centered fair incentive mechanisms** through **artificial currencies** so that the selfish behavior of the users aligns with the societally-optimal aggregate behaviour.<br><br>
{: .text-justify}


<h2>📣 Featured News & Events </h2>
{% include news.html limit=site.data.settings.news.news_limit%}

<h2>🧪 Featured Research</h2>
{% include feature_row id="AC-weighted-eqt-eql" type="left" %}
{% include feature_row id="single-origin-destination-routing" type="left" %}
