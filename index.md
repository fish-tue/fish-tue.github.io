---
layout: splash
title: "FISH"
entries_layout: grid
excerpt: "Fair Incentive Mechanism Design using Artificial Currencies"
description: "Research project on fair incentive mechanism design using artificial currencies at TU Eindhoven"
header:
  overlay_image: assets/img/splash.webp
  overlay_filter: 0.1
  text_color: "#ffffff"
  text_outline_color: "#99999"


AC-weighted-eqt-eql:
  - image_path: /assets/img/research/AC-weighted-eqt-eql/teaser.webp
    alt: "AC-weighted-eqt-eql"
    title: "Fair Artificial Currency Incentives in Repeated Weighted Congestion Games: Equity vs. Equality"
    excerpt: "Incentive schemes utilizing artificial currencies have been explored to achieve a system-optimal resource allocation that is also fair, contrarily to state-of-the-art monetary schemes. This paper delves into the comprehensive notion of fairness by meticulously optimizing for the societal metrics of equity and equality."
    url: "AC-weighted-eqt-eql/"
    btn_label: "Read More"
    btn_class: "btn--warning"

single-origin-destination-routing:
  - image_path: /assets/img/research/single-origin-destination-routing/teaser.webp
    alt: "single-origin-destination-routing"
    title: "Urgency-aware Routing in Single Origin-destination Itineraries through Artificial Currencies"
    excerpt: "Within mobility systems, the presence of self-interested users can lead to aggregate routing patterns that are far from the societal optimum that could be achieved by centrally controlling the user's choices. We design an urgency-aware fair incentive mechanism through artificial currencies so that the selfish behavior of the users aligns with the societally-optimal aggregate routing for single origin-destination inteneraries."
    url: "single-origin-destination-routing/"
    btn_label: "Read More"
    btn_class: "btn--warning"

---

<h2>👋🏻 Welcome </h2>

When users **access shared resources in a selfish manner**, the resulting societal cost and perceived users' cost is often higher than what would result from a centrally coordinated optimal allocation. While several contributions in **mechanism design** manage to steer the aggregate users choices to the desired optimum by using **monetary tolls**, such approaches bear the inherent drawback of **discriminating against users with a lower income**. Against this backdrop, with the FISH project, we aim to **design incentive schemes** based on **artificial currencies** with the goal of achieving a **system-optimal resource allocation** that is also **fair**.
{: .text-justify}


<h2>📣 Featured News & Events </h2>
{% include news.html limit=site.data.settings.news.news_limit%}

<h2>🧪 Featured Research</h2>
{% include feature_row id="AC-weighted-eqt-eql" type="left" %}
{% include feature_row id="single-origin-destination-routing" type="left" %}
