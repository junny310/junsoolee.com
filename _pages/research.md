---
layout: page
permalink: /research/
title: Research Projects
description: Ongoing research in the Dynamics and Control Lab, organized into control theory, numerical study, hardware, and quantum sensing.
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

The Dynamics and Control Lab develops the mathematical foundations of dynamical systems and control and applies them to autonomous, networked, and sensing systems. Our work spans four areas: **control theory**, **numerical study**, **hardware**, and **quantum sensing**.

## Control Theory

### Semistability analysis

Many engineered and natural networks settle not to a single equilibrium but to one of a continuum of equilibria selected by the initial conditions — for instance, the common value reached by a consensus protocol. Semistability is the appropriate stability notion for such systems. We develop Lyapunov and geometric conditions for asymptotic, finite-time, and fixed-time semistability of nonlinear discrete-time systems, and apply them to multiagent coordination and network consensus.

*Related publications:* [IEEE TAC 2022](/publications/#lee2022semistability), [Automatica 2022](/publications/#lee2022lyapunov), [SCL 2024](/publications/#lee2024geometric), [MED 2022](/publications/#lee2022consensusmed), [book chapter 2025](/publications/#lee2025smartercps).

### Stochastic stability

Real systems operate under noise — sensor errors, random communication dropouts, and environmental disturbances. We extend Lyapunov stability and semistability theory to discrete-time stochastic dynamical systems, establishing theorems for stability, semistability, and ultimate boundedness in probability, with application to network consensus under random communication noise.

*Related publications:* [Automatica 2022](/publications/#lee2022lyapunov), [IEEE TAC 2023](/publications/#lee2023stochastic), [Automatica 2024](/publications/#lee2024fixedstochastic), [MED 2021](/publications/#lee2021lyapunovmed), [IFAC 2025](/publications/#lee2025ultimately).

### Finite- and fixed-time stability

Classical asymptotic stability only guarantees convergence as time tends to infinity. For time-critical autonomy we study finite-time stability — convergence within a settling time that depends on the initial state — and fixed-time stability, in which the settling-time bound is uniform and independent of initialization. We develop both the stability tests and the optimal feedback controllers that achieve these guarantees for nonlinear, hybrid, and stochastic discrete-time systems. Most recently we study their **digital realization**: implicit- and consistent-discretization schemes that preserve exact finite- and fixed-time convergence under sampling, avoiding the chattering and loss of convergence that naïve discretization introduces.

*Related publications:* [Automatica 2020](/publications/#lee2020finitetime), [IEEE TAC 2022](/publications/#lee2022finitetimestab), [IJC 2023](/publications/#lee2023fixedtime), [Automatica 2024](/publications/#lee2024fixedstochastic), [AIMS Math. 2021](/publications/#lee2021hybrid), [MECC 2026 (implicit)](/publications/#lee2026implicit), [MECC 2026 (consistent)](/publications/#lee2026consistent).

### Nontangency analysis

Certifying convergence and (semi)stability for nonlinear systems with a continuum of equilibria is difficult using classical strict-Lyapunov arguments alone. We develop nontangency-based tests — geometric conditions on how the system's motion approaches the set of equilibria — that establish convergence and stability in discrete-time dynamical systems, complementing and in some cases relaxing standard Lyapunov requirements. We are extending these tests along two lines: **arc-length–based** conditions that certify convergence from summable displacements, and a unified taxonomy of convergence mechanisms for discrete-time **network systems** with continua of equilibria (such as consensus manifolds), aimed at protocols that enforce a favorable convergence mechanism by design rather than certifying it after the fact.

<div class="research-figs">
  <figure>
    <img src="{{ '/assets/img/research/nontangency.jpg' | relative_url }}" alt="Nontangency of a trajectory to the set of equilibria" loading="lazy">
    <figcaption>Nontangency of a trajectory to the equilibria set (SIADS 2025).</figcaption>
  </figure>
</div>

*Related publications:* [SIADS 2025](/publications/#lee2025nontangency), [ACC 2023](/publications/#lee2023accnontangency), [ACC 2025](/publications/#lee2025accstability), [CDC 2026](/publications/#lee2026arclength).

## Numerical Study

### Thermodynamic particle swarm optimization

We design particle swarm optimization (PSO) algorithms grounded in thermodynamic and dynamical-systems principles for swarm robotics across ground and aerial platforms. Treating the swarm as a multiagent dynamical system yields distributed rendezvous, reconnaissance, and search behaviors with convergence guarantees. Recent work extends the framework from distributed rendezvous to **target search in unknown, obstacle-filled environments**, combining thermal-diffusion consensus, obstacle repulsion, and temperature-modulated Lévy-flight exploration, with the exploration–exploitation balance grounded in an entropy-based (thermodynamic) consensus theory.

*Related publications:* [MECC 2025](/publications/#bojappa2025tpso), [IEEE/CAA JAS 2025](/publications/#bojappa2025pso), [IMECE 2026](/publications/#sill2026tpsosearch).

### Long-term autonomous missions

Sustained autonomy over hours or days requires reasoning at multiple timescales. Inspired by Dual Process Theory (DPT) from cognitive science — fast, reactive decision-making paired with slow, deliberative planning — we develop layered decision architectures for agents that must act reliably over long-horizon missions. We also study **resource-aware** long-horizon autonomy, coupling battery state-of-health with the decision layers so that mission planning adapts as usable capacity fades over season-long deployments.

*Related publications:* [AIAA SciTech 2027](/publications/#jadhav2027battery).

### Learning-based motion planning

Autonomous vehicles must plan safe motion through cluttered, partially unknown environments. We study reinforcement-learning approaches to quadrotor motion planning that produce collision-free trajectories in unknown obstacle fields, complementing the lab's model-based control and planning work.

*Related publications:* [IJCAS 2025](/publications/#park2025motion).

### Tether modeling

Tethered multirotor UAVs (TMUAVs) trade some mobility for effectively unlimited flight time and a secure, high-bandwidth data link, but the tether's dynamics strongly shape vehicle stability and control. We model the tether — its sag, tension, unilateral slack-to-taut behavior, and coupling to the airframe — including **retractable** tethers whose reel dynamics and length-dependent stiffness change in flight, to enable accurate simulation and robust control design.

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

*Related publications:* [MECC 2025](/publications/#bojappa2025tpso), [IEEE/CAA JAS 2025](/publications/#bojappa2025pso), [IMECE 2026](/publications/#sill2026tpsosearch).

### Battery-degradation–aware long-term agent

Battery capacity fades with use, changing what a long-duration mission can accomplish. We build hardware agents whose planning and control explicitly account for battery degradation, sustaining continuous field operation — such as long-term monitoring — as the onboard energy budget evolves.

*Related publications:* [AIAA SciTech 2027](/publications/#jadhav2027battery).

### Tethered MUAV & retractable TMUAV

We develop tethered multirotor UAV platforms, including retractable-tether systems, that combine the endurance and bandwidth of a physical tether with the agility of a multirotor. We design the robust and adaptive **geometric controllers** that fly these platforms with elastic, compliant cables — establishing closed-loop tracking guarantees despite the loss of differential flatness — and characterize their **certified performance envelopes** (bounds on payload swing and tracking error as the tether reels in and out) so that a mission planner can treat tether length as a first-class decision variable. Supporting simulation code and datasets are being released as an open, reproducible benchmark for tethered aerial autonomy (RTMUAV-Bench).

*Related publications:* [Dynamics 2025](/publications/#handrick2025tethered).

### Human-mountable fixed-wing UAV launcher

We design a flywheel-based, human-mountable launcher that stores and releases the energy needed to hand-launch a fixed-wing UAV, enabling rapid field deployment without a runway or fixed catapult. A first-principles energy-transfer analysis — modeling the friction drive as an inelastic momentum exchange — sets the efficiency ceilings and the binding design constraints, and is being validated on a benchtop testbed.

## Quantum Sensing

### NV-diamond quantum magnetometry

In collaboration with USC's quantum sensing group, we develop room-temperature quantum magnetometers based on optically detected magnetic resonance (ODMR) of nitrogen-vacancy (NV) center ensembles in diamond. A confocal fluorescence system with microwave delivery sweeps the NV spin resonances, and a spectral-fitting pipeline reconstructs the full three-dimensional magnetic-field vector from a single compact sensor head by exploiting the four crystallographic NV orientations — calibration-free vector magnetometry referenced to the fundamental NV gyromagnetic ratio.

### Geomagnetically induced currents & grid resilience

Severe geomagnetic storms induce quasi-DC geomagnetically induced currents (GICs) that can saturate high-voltage transformers and threaten the power grid. We develop the estimation and systems pipeline that turns magnetic-field measurements into grid-resilience assessments — mapping the surface geoelectric field through Earth-conductivity and grounded transmission-network models to per-transformer GIC and transformer-vulnerability scores — and study sensing architectures, from ground magnetometers to satellite-based NV-magnetometer concepts, for timely, spatially resolved nowcasting of geomagnetic disturbance.

*Related publications:* [AIAA SciTech 2027](/publications/#handrick2027nvgrid).
