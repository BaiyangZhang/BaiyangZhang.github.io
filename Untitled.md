To understand why $\phi_H(x) \ket{\Omega}$ in an interacting theory is not a pure single-particle state, but rather a superposition of many-particle states, let's delve into some foundational concepts and derivations.

### Heisenberg Equation of Motion

In the Heisenberg picture, field operators obey the Heisenberg equation of motion:
$$
\frac{d}{dt}\phi_H(t, \vec{x}) = i[H, \phi_H(t, \vec{x})],
$$
where $H$ is the full Hamiltonian of the theory, including all interactions. The exact form of $\phi_H$ generally cannot be solved explicitly in interacting theories, but we know it must incorporate all the dynamics and effects of the interactions.

### Vacuum State and Field Operator

The vacuum state $\ket{\Omega}$ in an interacting theory is the ground state of the Hamiltonian $H$. This state is highly non-trivial as it includes all the quantum corrections and fluctuations due to interactions.

### Action of Field Operator on Vacuum

When $\phi_H(x)$ acts on the vacuum state $\ket{\Omega}$, the result is:
$$
\phi_H(x) \ket{\Omega}.
$$
We need to understand the nature of this state. In free theory, this would simply create a single-particle state localized at $x$. In an interacting theory, however, the interpretation is not straightforward.

### Decomposition into Particle States

In QFT, states can be expanded in terms of eigenstates of the free particle number operator, although in interacting theories, these are not the eigenstates of the full Hamiltonian. The state $\phi_H(x) \ket{\Omega}$ can be formally expressed as:
$$
\phi_H(x) \ket{\Omega} = \sum_n \int d^3p_1 \ldots d^3p_n \psi_n(p_1, \ldots, p_n; x) \ket{p_1, \ldots, p_n},
$$
where $\ket{p_1, \ldots, p_n}$ are $n$-particle states and $\psi_n$ are complex functions characterizing the amplitude for finding such $n$-particle states when $\phi_H(x)$ acts on the vacuum.

### Spectral Decomposition (Lehmann Representation)

A more rigorous approach uses the spectral representation of the field operator. The two-point function in the vacuum state, also known as the propagator, is given by:
$$
\langle \Omega | \phi_H(x) \phi_H(y) | \Omega \rangle.
$$
Using translational invariance, this can be rewritten in terms of the spectral function $ \rho(p^2) $ as:
$$
\int d^4p \, e^{-ip \cdot (x-y)} \rho(p^2) \frac{1}{p^2 - m^2 + i\epsilon}.
$$
Here, $ \rho(p^2) $ encodes the distribution of mass and momentum in the state created by $\phi_H(x)$, revealing that it includes contributions from all sorts of particle states, not just a single particle.

### Conclusion

In interacting theories, $\phi_H(x) \ket{\Omega}$ is not simply a single-particle state but a complex superposition involving potentially multiple particles. This complexity arises from the interactions encoded in the Hamiltonian and manifests in the non-trivial structure of the vacuum and the field operator's action on it.