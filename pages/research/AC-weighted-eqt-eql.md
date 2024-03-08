---
layout: single
title: "Fair Artificial Currency Incentives in Repeated Weighted Congestion Games: Equity vs. Equality"
showTitle: true
excerpt: #"Urgency-aware Routing in Single Origin-destination Itineraries through Artificial Currencies"
permalink: /AC-weighted-eqt-eql/
classes: wide
sidebar:
  title: "Research"
  nav: sidebar-AC-weighted-eqt-eql
tags:
  - artificial currencies
  - fairness
  - weighted congestion games
  - congestion games
date: "2024-03-08"
last_modified_at: "2024-03-08"
---

## Short abstract
When individuals access shared resources **selfishly**, the resulting societal and perceived costs often surpass those of a centrally coordinated optimal allocation. While various contributions in mechanism design aim to guide users' choices towards the desired optimum using **monetary tolls**, such approaches suffer from the inherent drawback of **discriminating against those with lower incomes**. More recently, incentive schemes utilizing **artificial currencies** have been explored to achieve a **system-optimal** resource allocation that is also **fair**. This paper delves into the comprehensive notion of fairness by meticulously optimizing for the societal metrics of **equity** and **equality**, which respectively encompass providing equal outcomes and equal opportunities.
{: .text-justify}

## Source code

A **MATLAB** implementation of the methods and simulations presented in this paper are openly available in an **open-source repository** available at <a href="https://github.com/fish-tue/AC-weighted-equity-equality" target="blank">github.com/fish-tue/AC-weighted-equity-equality</a>. The code is **thoroughly commented** and is **easy to follow and modify**.
{: .text-justify}

The source code can also be **downloaded** directly <a href="https://github.com/fish-tue/AC-weighted-equity-equality">here</a> (X MB).

See below for **step-by-step** instructions on how the **illustrative numerical results** in [[1, Section IV]](#references) were obtained from the source code made available.
{: .text-justify}

## Simulation Results

### Generate Illustrative Example

To generate an illustrative network use the ```generate_example.m``` script.
{: .text-justify}

```text
>> generate_example
System opt. flows (x_star):	0.559563 0.390437
System opt. disc. (l_star):	1.23529 2.03529
System opt. cost:		1.48588
```

###  Compute Equity and Equality maximizing prices

To compute the arcs' prices according to the methods proposed in [[1, Section III]](#references), use the ```prices.m``` script.

```text
>> prices
Prices (Equity):		p1 = 6.97753 	 p2 = -10
InEqt (Design for InEqt):	4.44815e-07
InEql (Design for InEqt):	0.256755
InEqt (Design for InEql):	0.20542
InEql (Design for InEql):	0.0688788
```


<div class="row">
  <div class="column">
    <img src="/assets/img/research/AC-weighted-eqt-eql/n1.webp" style="width:100%">
  </div>
  <div class="column">
    <img src="/assets/img/research/AC-weighted-eqt-eql/prices.webp" style="width:100%">
  </div>
</div>


###  Simulate Evolution: Equity

The simulation with the **prices designed for equity** is carried out by computing the daily Nash equilibrium and the decisions of each user. It can be carried out using the ```simulation_equity.m``` script.

```text
>> simulation_equity
```

<div class="row">
  <div class="column">
    <img src="/assets/img/research/AC-weighted-eqt-eql/decision_Eqt.webp" style="width:100%">
  </div>
  <div class="column">
    <img src="/assets/img/research/AC-weighted-eqt-eql/AC_Eqt.webp" style="width:100%">
  </div>
</div>
<div class="row">
  <div class="column">
    <img src="/assets/img/research/AC-weighted-eqt-eql/cost_Eqt.webp" style="width:100%">
  </div>
  <div class="column">
    <img src="/assets/img/research/AC-weighted-eqt-eql/sensitivity_Eqt.webp" style="width:100%">
  </div>
</div>
<div class="row">
  <div class="column">
    <img src="/assets/img/research/AC-weighted-eqt-eql/L_Eqt.webp" style="width:100%">
  </div>
  <div class="column">
    <img src="/assets/img/research/AC-weighted-eqt-eql/Unf_Eqt.webp" style="width:100%">
  </div>
</div>


###  Simulate Evolution: Equality

The simulation with the **prices designed for equality** is carried out by computing the daily Nash equilibrium and the decisions of each user. It can be carried out using the ```simulation_equality.m``` script.

```text
>> simulation_equality
```

<div class="row">
  <div class="column">
    <img src="/assets/img/research/AC-weighted-eqt-eql/decision_Eql.webp" style="width:100%">
  </div>
  <div class="column">
    <img src="/assets/img/research/AC-weighted-eqt-eql/AC_Eql.webp" style="width:100%">
  </div>
</div>
<div class="row">
  <div class="column">
    <img src="/assets/img/research/AC-weighted-eqt-eql/cost_Eql.webp" style="width:100%">
  </div>
  <div class="column">
    <img src="/assets/img/research/AC-weighted-eqt-eql/sensitivity_Eql.webp" style="width:100%">
  </div>
</div>
<div class="row">
  <div class="column">
    <img src="/assets/img/research/AC-weighted-eqt-eql/L_Eql.webp" style="width:100%">
  </div>
  <div class="column">
    <img src="/assets/img/research/AC-weighted-eqt-eql/Unf_Eql.webp" style="width:100%">
  </div>
</div>


###  Conclusions

- The **system's optimum is achieved** with the prices designed for equity and equality
- The **perceived discomfort** is significantly lower in comparison to a optimal but urgency-unaware policy
- **Perfect equity** can always be achieved
- **Perfect equality** may be not be possible to achieve

## Citing

If you use this repository, **please reference the publication below**.

L. Pedroso, A. Agazzi, W.P.M.H. Heemels and M. Salazar, **'Fair Artificial Currency Incentives in Repeated Weighted Congestion Games: Equity vs. Equality**, *arxiV preprint*, 2024.

```bib
@article{PedrosoAgazziEtAl2024,
  author = {Leonardo Pedroso and Andrea Agazzi and W. P. M. H. Heemels and Mauro Salazar},
  title = {Fair Artificial Currency Incentives in Repeated Weighted Congestion Games: Equity vs. Equality},
  journal = {arxiV preprint},
  year = {2024},
  doi = {}
}
```

## References

[1] L. Pedroso, A. Agazzi, W.P.M.H. Heemels and M. Salazar, **'Fair Artificial Currency Incentives in Repeated Weighted Congestion Games: Equity vs. Equality**, *arxiV preprint*, 2024.
{: .text-justify}
