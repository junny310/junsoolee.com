---
layout: page
permalink: /research/
title: Research Projects
description: Ongoing research in the Dynamics and Control Lab, organized into control theory, numerical study, and hardware.
nav: true
nav_order: 3
toc:
  sidebar: left
---

<style>
  .research-figs { display: flex; flex-wrap: wrap; gap: 1rem; margin: 0.75rem 0 1.25rem; }
  .research-figs figure { margin: 0; text-align: center; }
  .research-figs img { max-height: 200px; width: auto; border-radius: 8px; border: 1px solid var(--global-divider-color); background: #fff; }
  .research-figs figcaption { font-size: 0.85rem; color: var(--global-text-color-light); margin-top: 0.35rem; }
</style>

The Dynamics and Control Lab develops the mathematical foundations of dynamical systems and control and applies them to autonomous and networked systems. Our work spans three areas: **control theory**, **numerical study**, and **hardware**.

## Control Theory

### Semistability analysis

Many engineered and natural networks settle not to a single equilibrium but to one of a continuum of equilibria selected by the initial conditions — for instance, the common value reached by a consensus protocol. Semistability is the appropriate stability notion for such systems. We develop Lyapunov and geometric conditions for asymptotic, finite-time, and fixed-time semistability of nonlinear discrete-time systems, and apply them to multiagent coordination and network consensus.

*Related publications:* [IEEE TAC 2022](/publications/#lee2022semistability), [Automatica 2022](/publications/#lee2022lyapunov), [SCL 2024](/publications/#lee2024geometric), [book chapter 2025](/publications/#lee2025smartercps).

### Stochastic stability

Real systems operate under noise — sensor errors, random communication dropouts, and environmental disturbances. We extend Lyapunov stability and semistability theory to discrete-time stochastic dynamical systems, establishing theorems for stability, semistability, and ultimate boundedness in probability, with application to network consensus under random communication noise.

*Related publications:* [Automatica 2022](/publications/#lee2022lyapunov), [IEEE TAC 2023](/publications/#lee2023stochastic), [Automatica 2024](/publications/#lee2024fixedstochastic), [IFAC 2025](/publications/#lee2025ultimately).

### Finite- and fixed-time stability

Classical asymptotic stability only guarantees convergence as time tends to infinity. For time-critical autonomy we study finite-time stability — convergence within a settling time that depends on the initial state — and fixed-time stability, in which the settling-time bound is uniform and independent of initialization. We develop both the stability tests and the optimal feedback controllers that achieve these guarantees for nonlinear, hybrid, and stochastic discrete-time systems.

*Related publications:* [Automatica 2020](/publications/#lee2020finitetime), [IEEE TAC 2022](/publications/#lee2022finitetimestab), [IEEE TAC 2023](/publications/#lee2023stochastic), [IJC 2023](/publications/#lee2023fixedtime), [Automatica 2024](/publications/#lee2024fixedstochastic).

### Nontangency analysis

Certifying convergence and (semi)stability for nonlinear systems with a continuum of equilibria is difficult using classical strict-Lyapunov arguments alone. We develop nontangency-based tests — geometric conditions on how the system's motion approaches the set of equilibria — that establish convergence and stability in discrete-time dynamical systems, complementing and in some cases relaxing standard Lyapunov requirements.

*Related publications:* [SIADS 2025](/publications/#lee2025nontangency), [ACC 2023](/publications/#lee2023accnontangency), [ACC 2025](/publications/#lee2025accstability).

## Numerical Study

### Thermodynamic particle swarm optimization

We design particle swarm optimization (PSO) algorithms grounded in thermodynamic and dynamical-systems principles for swarm robotics across ground and aerial platforms. Treating the swarm as a multiagent dynamical system yields distributed rendezvous, reconnaissance, and search behaviors with convergence guarantees, including operation in unknown or confined environments.

*Related publications:* [MECC 2025](/publications/#bojappa2025tpso), [IEEE/CAA JAS 2025](/publications/#bojappa2025pso).

### Long-term autonomous missions

Sustained autonomy over hours or days requires reasoning at multiple timescales. Inspired by Dual Process Theory (DPT) from cognitive science — fast, reactive decision-making paired with slow, deliberative planning — we develop layered decision architectures for agents that must act reliably over long-horizon missions.

### Tether modeling

Tethered multirotor UAVs (TMUAVs) trade some mobility for effectively unlimited flight time and a secure, high-bandwidth data link, but the tether's dynamics strongly shape vehicle stability and control. We model the tether — its sag, tension, and coupling to the airframe — to enable accurate simulation and robust control design for tethered and retractable-tether platforms.

*Related publications:* [Dynamics 2025](/publications/#handrick2025tethered).

## Hardware

### Swarm system using Thymio Wireless

We validate swarm-intelligence and PSO algorithms on physical multi-robot testbeds built from Thymio wireless robots, closing the gap between numerical study and real hardware that is subject to limited sensing, communication, and energy.

<div class="research-figs">
  <figure>
    <img src="{{ '/assets/img/research/thymio-swarm.jpg' | relative_url }}" alt="Wireless Thymio robot" loading="lazy">
    <figcaption>Wireless Thymio</figcaption>
  </figure>
</div>

*Related publications:* [MECC 2025](/publications/#bojappa2025tpso), [IEEE/CAA JAS 2025](/publications/#bojappa2025pso).

### Battery-degradation–aware long-term agent

Battery capacity fades with use, changing what a long-duration mission can accomplish. We build hardware agents whose planning and control explicitly account for battery degradation, sustaining continuous field operation — such as long-term monitoring — as the onboard energy budget evolves.

### Tethered MUAV & retractable TMUAV

We develop tethered multirotor UAV platforms, including retractable-tether systems, that combine the endurance and bandwidth of a physical tether with the agility of a multirotor, together with the robust control frameworks required to fly them reliably.

*Related publications:* [Dynamics 2025](/publications/#handrick2025tethered).

### Human-mountable fixed-wing UAV launcher

We design a flywheel-based, human-mountable launcher that stores and releases the energy needed to hand-launch a fixed-wing UAV, enabling rapid field deployment without a runway or fixed catapult.
