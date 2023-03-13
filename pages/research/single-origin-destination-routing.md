---
layout: single
title: "Urgency-aware Routing in Single Origin-destination Itineraries through Artificial Currencies"
showTitle: true
excerpt: #"Urgency-aware Routing in Single Origin-destination Itineraries through Artificial Currencies"
permalink: /single-origin-destination-routing/
classes: wide
sidebar:
  title: "Research"
  nav: sidebar-single-origin-destination-routing
tags:
  - mobility
  - karma
  - artificial currencies
  - routing
date: "2023-03-13"
last_modified_at: "2023-03-13"
---

## Short abstract
Within **mobility systems**, the presence of **self-interested users** can lead to aggregate routing patterns that are far from the **societal optimum**. We design a **fair incentive mechanism so that the selfish behavior of the users aligns with the societally-optimal aggregate routing**. The proposed mechanism is based on an **artificial currency** that cannot be traded or bought, but is only used when traveling. Specifically, we consider a parallel-arc network with a single origin and destination node whereby each user chooses from one of the available arcs to reach their destination on a daily basis. Taking faster routes comes at a cost, whereas taking slower routes is incentivized by a reward. Our numerical simulations show that it is possible to **achieve a near-optimal solution** whilst significantly **reducing the users’ perceived discomfort**.
{: .text-justify}

{:refdef: style="display: block; margin-left: auto; margin-right: auto; width: 50%;"}
![single-origin-destination-routing](/assets/img/research/single-origin-destination-routing/teaser.webp){:class="img-responsive"}
{: refdef}

## Source code

A **MATLAB** implementation of the methods and simulations presented in this paper are openly available in an **open-source repository** available at [https://github.com/fish-tue/single-origin-destination-routing](https://github.com/fish-tue/single-origin-destination-routing). The code is **thoroughly commented** and is **easy to follow and modify**.
{: .text-justify}

The source code can also be **downloaded** directly [here](/) (X Kb).

See below for **step-by-step** instructions on how the **illustrative numerical results** in [[1, Section V.I ]](#references) were obtained from the source code made available.
{: .text-justify}

## Simulation Results

### Generate Illustrative Network

To generate an illustrative network use the ```generate_network.m``` script, where the parameters regarding the network ($n$,$\mathbf{d}(\mathbf{x})$, $c(\mathbf{x})$), the population ($M$, $s_{\mathrm{min}}$, $\bar{s}$, $s_{\mathrm{max}}$, $P_\mathrm{home}$, $T$) can be set.
{: .text-justify}

```text
>> generate_network
System opt. flows (x_star):	0.138707 0.133566 0.131482 0.170298 0.375947
System opt. disc. (d_star):	0.116706 0.321068 0.321317 0.323368 0.414719
System opt. cost:		0.541656
```
###  Compute Near-optimal Arcs' Prices
To compute the arcs' prices according to the method proposed in [[1, Section V.I]](#references), use the ```n_arcs_pricing.m``` script.

```text
>> n_arcs_pricing
---------------------------------------------------------------------
Diagnostic information:
Fitness function: @(p)c(n_arcs_stationary_flows(d_star,T,p',s_max,s_bar,s_min,P_go,P_home))
5 Variable(s)
5 Integer variable(s)
6 Linear inequality constraint(s)
1 Linear equality constraint(s)

Options:
CreationFcn:       @CustomCreationFcn
CrossoverFcn:      @crossoverlaplace
SelectionFcn:      @selectiontournament
MutationFcn:       @mutationpower
StallGenLimit:     3
Display:           'diagnose'
End of diagnostic information.

                                  Best          Mean         Stall
Generation      Func-count     Penalty         Penalty    Generations
    1              100          0.5777          0.7856        0
    2              147          0.5647          0.7537        0
    3              194          0.5643          0.7166        0
    4              241          0.5563          0.7211        0
    5              288          0.5563          0.7513        1
    6              335          0.5522          0.6837        0
    7              382          0.5522          0.7205        1
    8              429          0.5522          0.7001        2
    9              476          0.5522          0.7422        3
Optimization terminated: average change in the penalty fitness value less than options.FunctionTolerance
and constraint violation is less than options.ConstraintTolerance.
---------------------------------------------------------------------
Genetic alg. prices:		76 1 0 -1 -28  
```
###  Pot Decision Landscape

The decision landscape with the selected prices at the system's optimum can be plotted using the ```draw_decision_landscape.m``` script.
{: .text-justify}

```text
>> draw_decision_landscape.m
```

{:refdef: style="display: block; margin-left: auto; margin-right: auto; width: 50%;"}
![single-origin-destination-routing](/assets/img/research/single-origin-destination-routing/decision-landscape.webp){:class="img-responsive"}
{: refdef}

###  Simulate Evolution

The simulation is carried out by computing the daily Nash equilibrium and the decisions of each user. It can be carried out using the ```simulation.m``` script.

```text
>> simulation
```

<div class="row">
  <div class="column">
    <img src="/assets/img/research/single-origin-destination-routing/decision.webp" style="width:100%">
  </div>
  <div class="column">
    <img src="/assets/img/research/single-origin-destination-routing/karma.webp" style="width:100%">
  </div>
</div>
<div class="row">
  <div class="column">
    <img src="/assets/img/research/single-origin-destination-routing/cost.webp" style="width:100%">
  </div>
  <div class="column">
    <img src="/assets/img/research/single-origin-destination-routing/sensitivity.webp" style="width:100%">
  </div>
</div>


###  Conclusions

- When the Karma levels are very **high**, the users behave as if the pricing scheme **were not implemented**
- The **system's optimum is achieved** with the selected prices
- The **perceived discomfort** is significantly lower in comparison to a optimal but urgency-unaware policy


## Citing

If you use this repository, **please reference the publication below**.

L. Pedroso, W. P. M. H. Heemels, and M. Salazar, “**Urgency-aware optimal routing in repeated games through artificial currencies**” [*not published yet*]

```bib
@article{PedrosoHeemelsEtAl2023,
  title={Urgency-aware Routing in Single Origin-destination Itineraries through Artificial Currencies},
  author={Pedroso, L. and Heemels, W. P. M. H. and Salazar, M.},
  year={2023}
}
```



## References

[1] L. Pedroso, W. P. M. H. Heemels, and M. Salazar, “**Urgency-aware optimal routing in repeated games through artificial currencies**” [*not published yet*]
{: .text-justify}
