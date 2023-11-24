---
layout: post
title: " Hamiltonian Truncation in 3D"
subtitle: 
date: 2023-11-24
author: Baiyang Zhang
header-img: img/background1.jpg
catalog: true
tags:
---

### The basic idea

In classical field theory, the Hamiltonian formalism provides an alternative to the Lagrangian formalism for deriving the equations of motion. The process involves defining the Hamiltonian of the system and using it to derive the field equations.

To make the transition from Lagrangian to Hamiltonian formalism in field theory, we first define the canonical momenta $\pi_i$ conjugate to each field $\phi_i$ by
$$ \pi_i = \frac{\partial \mathcal{L}}{\partial (\partial_t \phi_i)}, $$
where $\mathcal{L}$ is the Lagrangian density and $\partial_t \phi_i$ is the time derivative of the field.

The Hamiltonian density $\mathcal{H}$ is then given by
$$ \mathcal{H} = \sum_i \pi_i \partial_t \phi_i - \mathcal{L}, $$
where the sum runs over all fields in the theory.

The equations of motion in the Hamiltonian formalism for field theory are then given by Hamilton's equations, analogous to the Hamiltonian formalism in classical mechanics. These equations are
$$ \frac{\partial \phi_i}{\partial t} = \frac{\delta \mathcal{H}}{\delta \pi_i}, $$
$$ \frac{\partial \pi_i}{\partial t} = -\frac{\delta \mathcal{H}}{\delta \phi_i}, $$
where $\frac{\delta}{\delta \phi_i}$ and $\frac{\delta}{\delta \pi_i}$ represent functional derivatives with respect to the field $\phi_i$ and its conjugate momentum $\pi_i$, respectively.

These equations describe how the fields and their conjugate momenta evolve over time, analogous to how the position and momentum of a particle evolve in classical mechanics. They provide a complete description of the dynamics of the field system within the Hamiltonian framework.

$$
 \frac{\partial \phi_i}{\partial t} = \frac{\delta \mathcal{H}}{\delta \pi_i} \implies \dot{\phi}=\pi  
$$
and 
$$
 \frac{\partial \pi_i}{\partial t} = -\frac{\delta \mathcal{H}}{\delta \phi_i}\implies \frac{\partial^{2}\phi}{\partial t^{2}} =  -\frac{\delta \mathcal{H}}{\delta \phi_i}
$$
