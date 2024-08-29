---
layout: single
title: "Fair Incentive Mechanisms for Differentiated Services in a Public Electric Vehicle Charging Station"
showTitle: true
excerpt: #"Urgency-aware Routing in Single Origin-destination Itineraries through Artificial Currencies"
permalink: /evcharging/
classes: wide
sidebar:
  title: "Research"
  nav: sidebar-evcharging
tags:
  - artificial currencies
  - fairness
  - EV charging
date: "2024-08-29"
last_modified_at: "2024-08-29"
---

## Short abstract
A major barrier to electric vehicle (EV) adoption is the lack of affordable and **accessible public chargers**. This thesis proposes **a fair incentive mechanism** for operating a public EV charging station with access to renewable energy, **prioritizing users** without home-based chargers, and **minimizing grid power usage**. This mechanism is based on an **artificial currency**, rather than monetary plug-in fees or differential electricity prices, which effectively eliminates income-based discrimination. The framework is applied to and validated for the **use-case** of a charging station at the University of California, Merced. The results show that the pricing design effectively steers the decision of **selfish users** toward the **societal optimum**.
{: .text-justify}

## Source code

A **MATLAB** implementation of the methods and simulations presented in this paper are openly available in an **open-source repository** available at <a href="https://github.com/fish-tue/ev-charging-station" target="blank">github.com/fish-tue/ev-charging-station</a>. The code is **thoroughly commented** and is **easy to follow and modify**.
{: .text-justify}

The source code can also be **downloaded** directly <a href="https://github.com/fish-tue/ev-charging-station/releases">here</a>.

See below for **step-by-step** instructions on how the **illustrative numerical results** in [[1, Section V]](#references) were obtained from the source code made available.
{: .text-justify}

## Simulation Results

### Generate Illustrative Example

Generate model for UC Merced use-case. Set parameters and define discomfort function.
{: .text-justify}

```text
>> initialization
```

Find optimal allocation as described in Section III [1] using ```optimize_x.m```.

```text
>> optimize_x
Sys. opt. allocation priority (xp_star) = 	[0.0000, 0.0681, 0.0319, 0.0000, 0.0000]
Sys. opt. allocation non-priority (xnp_star) = 	[0.2855, 0.0000, 0.0681, 0.0461, 0.0003]
Discomfort at sys. opt. priority (dp_star) = 	[1.2000, 0.0102, 0.2956, 0.3985, 1.0000]
Discomfort at sys. opt. non-priority (dnp_star) = 	[0.6000, 0.0102, 0.2956, 0.3985, 1.0000]
```

<img src="/assets/img/research/evcharging/05_OptimalX.svg" style="width:60%">

Compute the resource prices according to [[1, Section IV]](#references), use ``pricing.m``.

```text
>> prices
Prices priority (p_p) = 	[0, 9, -18, 0, 0]
Prices non-priority (p_np) = 	[-3, 100, 20, 14, 100]
```

Simulate the daily Nash equilibrium and user decisions without incentive mechanism using ```simulation_baseline.m```
```text
>> simulation_baseline
```

<img src="/assets/img/research/evcharging/05_baseline.svg" style="width:60%">

Simulate the daily Nash equilibrium and user decisions with incentive mechanism using ```simulation_AC.m```
```text
>> simulation_AC
```

<img src="/assets/img/research/evcharging/05_decision-bounded.svg" style="width:60%">

<div class="row">
  <div class="column">
    <img src="/assets/img/research/evcharging/05_decision_xp-bounded.svg" style="width:100%">
  </div>
  <div class="column">
    <img src="/assets/img/research/evcharging/05_decision_xnp-bounded.svg" style="width:100%">
  </div>
</div>

<div class="row">
  <div class="column">
    <img src="/assets/img/research/evcharging/05_simulationX-bounded.svg" style="width:100%">
  </div>
  <div class="column">
    <img src="/assets/img/research/evcharging/05_cost.svg" style="width:100%">
  </div>
</div>

##  Conclusions

- The proposed incentive mechanism design **minimizes energy from the grid** and **prioritizes access to priority users**.
- The **system’s optimum is achieved** with the prices designed for priority and non-priority users.
- The **societal cost is significantly lower** in comparison to a mechanism without artificial currency.

### Future work

Once UC Merced implements the artificial incentive scheme for their chargers, they would need an application in which users can select their charging resources, i.e., time slots. The storyboard below illustrates how this would work with an artificial currency incentive scheme.

<img src="/assets/img/research/evcharging/EAEV storyboard.pdf" style="width:100%">

## Citing

If you use this repository, **please reference the publication below**.

L. Hollander, L. Pedroso, R. De Castro and M. Salazar, **Fair Incentive Mechanisms for Differentiated Services in a Public Electric Vehicle Charging Station**, *Eindhoven University of Technology*, 2024.

```bib
@mastersthesis{HollanderPedrosoEtAl2024,
author = {L. Hollander and L. Pedroso and R. {De Castro} and M. Salazar},
title = {Fair Incentive Mechanisms for Differentiated Services in a Public Electric Vehicle Charging Station},
year = {2024},
school = {Eindhoven University of Technology}
}
```

## References

[1] L. Hollander, L. Pedroso, R. De Castro and M. Salazar, **Fair Incentive Mechanisms for Differentiated Services in a Public Electric Vehicle Charging Station**, *Eindhoven University of Technology*, 2024.
{: .text-justify}
