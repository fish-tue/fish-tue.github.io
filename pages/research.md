---
layout: single
classes: wide
title: "Research"
permalink: /research/
sidebar:
  title: "Research"
  nav: sidebar-research
author_profile: false

single-origin-destination-routing:
  - image_path: /assets/img/research/single-origin-destination-routing/teaser.webp
    alt: "single-origin-destination-routing"
    title: "Urgency-aware Routing in Single Origin-destination Itineraries through Artificial Currencies"
    excerpt: "Within mobility systems, the presence of self-interested users can lead to aggregate routing patterns that are far from the societal optimum that could be achieved by centrally controlling the user's choices. We design an urgency-aware fair incentive mechanism through artificial currencies so that the selfish behavior of the users aligns with the societally-optimal aggregate routing for single origin-destination inteneraries."
    url: "single-origin-destination-routing/"
    btn_label: "Read More"
    btn_class: "btn--warning"

AC-weighted-eqt-eql:
  - image_path: /assets/img/research/AC-weighted-eqt-eql/teaser-square.webp
    alt: "AC-weighted-eqt-eql"
    title: "Fair Artificial Currency Incentives in Repeated Weighted Congestion Games: Equity vs. Equality"
    excerpt: "Incentive schemes utilizing artificial currencies have been explored to achieve a system-optimal resource allocation that is also fair, contrarily to state-of-the-art monetary schemes. This paper delves into the comprehensive notion of fairness by meticulously optimizing for the societal metrics of equity and equality."
    url: "AC-weighted-eqt-eql/"
    btn_label: "Read More"
    btn_class: "btn--warning"

evcharging:
  - image_path: /assets/img/research/evcharging/teaser.svg
    alt: "evcharging"
    title: "Fair Incentive Mechanisms for Differentiated Services in a Public Electric Vehicle Charging Station"
    excerpt: "A major barrier to electric vehicle (EV) adoption is the lack of affordable and accessible public chargers. This thesis proposes a fair incentive mechanism for operating a public EV charging station with access to renewable energy, prioritizing users without home-based chargers, and minimizing grid power usage."
    url: "evcharging/"
    btn_label: "Read More"
    btn_class: "btn--warning"

---
<h1>Research</h1>
<h2>Posts</h2>
<h3>2024</h3>
{% include feature_row id="evcharging" type="left" %}
{% include feature_row id="AC-weighted-eqt-eql" type="left" %}
<h3>2023</h3>
{% include feature_row id="single-origin-destination-routing" type="left" %}


<h2>Publications</h2>
{% include publications.html list=site.data.publications %}
