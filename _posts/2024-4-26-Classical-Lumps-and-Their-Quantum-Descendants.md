---
layout: post
title: Note on Classical Lumps and Their Quantum Descendants
subtitle: 
date: 2024-04-26
author: Baiyang Zhang
header-img: 
catalog: true
tags:
  - Duality
  - QFT
  - Notes
---

# Classical lumps
## Solitonic waves

The waves in real world usually dissipate over time. As the energy propagates to infinite far in the form of waves, the energy density goes to zero uniformly in spacetime. The same is true for the solutions of wave equations, except for some singular solutions at least. We give a more rigorous definition for dissipation: a solution of the classical equations of motion is dissipative if 

$$
\lim_{ t \to \infty } \text{max } \mathcal{E}(\mathbf{x},t)=0,
$$

where $\mathcal{E}(\mathbf{x},t)$ is the energy density. 

The interesting thing is that there exists wave functions that allows for non-singular, non-dissipative solutions. In the most striking and simplest case, the solution is time-independent. Somehow, lumps of energy hold themselves together by their own self-interaction. 

- - - 

### Some time-independent example in one space dimension

First some conventions. The metric is taken to be $g = \text{diag}(1,-1,-1,\cdots)$, $i,j, \dots$ denote space dimensions, $a,b, \dots$ denotes internal symmetry. 

Let us consider the simplest relativistic example: theories of a single scalar field in one space and one time dimension, with non-derivative interactions. The dynamics of such a theory are describe by the Lagrangian density

$$
\mathcal{L} = \frac{1}{2} \partial _ {\mu}\phi \partial ^{\mu}\phi - U(\phi).
$$

The energy is given by a Legendre transformation $H = L - p\dot{q}$, we get 

$$
H = \int d x \,  \left[  \frac{1}{2}(\partial _ {0}\phi)^{2}+\frac{1}{2} (\partial _ {1}\phi)^{2}+U(\phi) \right].
$$

We sometimes write the total energy as the sum of kinetic and potential energy,

$$
E = T+V
$$

where $T$ is the term quadratic in *time derivatives*, and $V$ is the term involving no time derivatives. 

- - -

There are two models we will consider here. First let's take a look at the phi-fourth theory. There are two degenerate vacua, corresponding to the two directions of the boundary of the space. The potential energy is 

$$
U = \frac{\lambda}{2} (\phi^{2}-a^{2})^{2}.
$$

The vacuum configuration is clearly given by $\phi = \pm a$ a constant in spacetime. In a different form $a$ is written as $a = \mu^{2} / \lambda$. 

Next let's consider the sine-Gordon potential, 

$$
U = \frac{\alpha}{\beta^{2}} (1-\cos \beta \phi).
$$

The ground states have infinite degeneracy. 

We want to find the time-independent solutions of the equations of motion. We need to find the stationary point of the energy function, which is very similar to finding the stationary point of the action, with one difference: the sign of the potential term. Mathematically, looking for the time-independent solution is the same as looking for the motion of a particle of unit mass in a potential equal to **minus** $U(x)$. 

To emphasize, **we can turn a static problem of finding the time-independent solution that minimizes the Hamiltonian, to a dynamical problem of finding the motion of a particle (of unit mass) in a reversed potential.** The latter allows us to make use of our intuition and imagination, and helps to visualize the solution.

Every motion of the particle in the potential corresponds to a time-independent solution of the field equations, but not all of them are of finite energy. For the energy integral to converge, the energy density must go to zero at space infinity. In terms of the particle problem, this boundary conditions fixes the possible initial and final positions. 

In the example of the phi-fourth theory, the potential takes the form of double-well. The minus version of the potential is of the form double hill. It would be helpful to draw some picture here but I am too lazy, interested readers should just read Coleman's book. The lump solution corresponds to the motion that the particle starts off from one of the hills and rolls over the valley and reaches the other hill and stays there.

By convention, we call the solution for which $\phi$ is monotone increasing `lumps` and those for which it is monotone decreasing `antilumps`.

To find the exact expression of the solution, let's adopt the dynamic picture of a moving particle. The potential is now $-U(x)$ where $x$ is identified with $\phi$ in the static problem. The total energy is conserved to zero during the whole motion, thus 

$$
\frac{1}{2} \left( \frac{dx}{dt} \right)^{2} - U(x) = 0.
$$

We can translate this back into field language by substitution $x\to \phi$ and the solution can be read off instantly in the integral form,

$$
\phi(x) = \pm\int d x \,[2U(\phi(x))]^{1/2}
$$

or 

$$
x = \pm\int_ {\phi_ {0}}^{\phi} d\phi \,  [2U(\phi')]^{- 1/2}.
$$


Note that the solutions enjoys the translation symmetry, meaning the center of the lump can be translated to anywhere. 

These equation also enables us to simplify the expression for the energy of a lump, thanks to the fact that a lump satisfies the equation of motion. 

For phi-fourth theory, we find for the form of the lump

$$
\phi = a \tanh(\mu x).
$$

The energy of the lump is given by 

$$
E = \frac{4\mu^{3}}{3\lambda}.
$$

The lumps of $\phi^{4}$ theory is frequently called `kinks` in the literature.

For the sine-Gordon theory, we find 

$$
\phi = \frac{4}{\beta} \tan^{-1} \exp(\alpha^{1/2}x)
$$

where which branch of the inverse tangent we choose determines which two zeros we move between. The energy of the lump is 

$$
E = \frac{8\alpha^{1/2}}{\beta^{2}}.
$$

The lumps of sine-Gordon theory are frequently called `solitons` in the literature. In both cases the antilumps are obtained simply by multiplying by minus one.

A few words on the stability of the kink solution. We know that the equation of motion in the kink background has solutions called normal modes, each with a eigen value corresponding to the energy. The kink is stable under fluctuation if all the eigen values are non-negative, otherwise the perturbation in the direction of the negative-eigenvalue normal mode would decrease the energy indefinitely, hence making the kink unstable. Hence, if we can prove that there exists no normal modes with negative eigen values, we can prove that the kink is stable. To do this, we need two ingredients:  zero mode and the node theorem. Zero mode is a result of translation symmetry of the model, or rather the breaking of it. Zero mode is a constant solution with no nodes, and the node theorem says that for 1-dimensional Schrodinger equation, the lowest wave function has zero node, the first excitation wave function has one nodes, etc. Then the zero mode is the lowest energy state, with energy zero! Hence there exists no negative eigen value.

A kink in $\phi^{4}$ theory can be very well regarded as a almost-localized classical particle, with one major difference: the condition for patching adjacent kink solutions together must be ...kink-antikink-kink..., otherwise it would not be a solution to the equation of motion. 


## With gauge field

Let $\phi$ be a vector of scalar field with gauge group $G$ and gauge field $A$. The covariant derivative and field strength are defined in the usual way, you can pick your favorite convention. Let $\phi=\phi_ {0}$, $A =0$ be the ground state. Due to the gauge invariance (or more precisely, gauge redundancy), there might exist a subset $H$ of $G$ such that it leaves $\phi=\phi_ {0},A=0$ unchanged. It is usually written as $H<G$, then for any $h\in H$ we have $h\phi_ {0}=\phi_ {0}$, $H$ is the little group of $\phi_ {0}$, $\phi_ {0}$ is the fixed point of $H$. If we study the fluctuation near $\phi_ {0}$, we find that the gauge fields associated with the generators of $H$ remains massless. The vacuum manifold would be the coset space $G/H$, for reasons that I have no time to explain here. This is under the assumption that the vacuum manifold is connected and on which the gauge group acts transitively. This excludes both the case of accidental degeneracy and existence of ordinary (non-gauge) symmetry. Accidental degeneracy refers to a situation where two or more energy levels have the same energy not due to an obvious symmetry of the system, but rather due to a more subtle or hidden symmetry, or as a result of a specific mathematical coincidence, such as the accidental degeneracy in the hydrogen atom. This differs from the usual degeneracy associated with the symmetries of the system's Hamiltonian, such as those arising from rotational or translational invariance. 

We can wrap the vacuum manifold, namely the coset space, around the space boundary, this gives a homotopy group. This homotopy group classifies topologically different field configurations the theory admits. 

The rest of Coleman's lecture goes to a involved discussion of homotopy groups and short exact sequence, we will not note it here. Instead, we will directly dive into the quantum lumps. But before going there, I can't resist to say that Sidney Coleman's illustration of the map 

$$
\pi_ {2}(G) \to \pi_ {1}(H)
$$

is brilliant! I strongly recommend section 3.7 to everyone. I've learnt about homotopy groups from other places, mostly from a pure mathematical perspective, and I've learnt how to use the short exact sequence to evaluate the homotopy group, but Coleman's introduction is more intuitive and straightforward. It serves as a pretty good supplement to short exact sequence argument. Coleman's section 3.7 can be regarded as a special case of Theorem. 22.27 in Frankel's textbook.

- - -

# Quantum lumps
## Power expansion of the time-independent lumps

The quantization of kink is a fascinating topic. We start from the classical solution and consider the small perturbations about it, order by order. 

Consider the sine-Gordon Lagrangian:

$$
\boxed{ 
\mathcal{L} = \frac{1}{2} (\partial \phi)^{2} + \frac{\alpha}{\beta^{2}} (\cos \beta \phi-1),
}
$$

where under the $\cos$ function, $\beta$ cancels the dimension of $\phi$ and renders $\beta \phi$ dimensionless. 

We can rescale field such that the parameter $\beta$ factors out of the Lagrangian. Since $\beta \phi$ appears together under $\cos$ function, let's define 

$$
\widetilde{\phi} := \phi \beta
$$

then the Lagrangian in term it reads

$$
\mathcal{L} = \frac{1}{\beta^{2}} \left[ \frac{1}{2}(\partial \widetilde{\phi})^{2}+\alpha(\cos \widetilde{\phi}-1) \right].
$$

If you write down the equation of motion corresponding to the above Lagrangian, you'll find that $\beta$ does not enter the equation *at all*! Since classically all the info is given by the equation of motion, it is safe to say that $\beta$ drops out from the classical theory. Of course when you are calculating Hamiltonian, which is just the Legendre transform of the Lagrangian, $\beta$ appears again, but the dependence is trivial. It is similar to study the motion of a point object in gravitational force only, $\beta$ would be similar to the mass of the object, the mass does not change the motion, only trivially changes the gravitational potential. 

However when we quantize it, things will be different. Follow the path of path integral, recall that the stuff that decides all the physics is the partition function 

$$
Z = \int D\phi \, \exp \left\lbrace \frac{i}{\hbar} \int \mathcal{L(\phi)} \,   \right\rbrace
= \int D\phi \, \exp \left\lbrace \frac{i}{\boxed{ \hbar \beta^{2}}} \int \mathcal{L(\widetilde{\phi})} \,   \right\rbrace,
$$

note that $\beta^{2}$ always appears together with $\hbar$, and $\hbar\to 0$ corresponds to the classical limit, so $\beta\to 0$ also corresponds to the classical limit! I will not talk too much about it here for this matter is addressed in more details in my other notes. we just mention that the same argument goes for the phi-4th theory with the replacement $\beta^{2}\to \lambda$. A quote from Coleman:

>These manipulations are trivial, but they teach us something important: if there are particles in the quantum theory that correspond to classical lumps, they are most likely to resemble their classical ancestors for weakly coupled theories. (Conversely, there is no more reason to trust classical analysis for strongly coupled theories than there is to trust the Born approximation.) This suggests that the most direct way to construct quantum lumps is by an expansion in powers of the coupling constant. The leading term in such an expansion should give the classical results, appropriately reinterpreted in quantum language, and the higher terms should give quantum corrections

The canonical momentum (density) associated to $\widetilde{\phi}$ is 

$$
\widetilde{\pi} := \frac{\partial \mathcal{L}}{\partial (\partial_ {0}\widetilde{\phi})} = \frac{\partial_ {0}\widetilde{\phi}}{\beta^{2}},
$$

and the Hamiltonian is

$$
\begin{align*}
\beta^{2}\mathcal{H}(\tilde{\phi}) &= \widetilde{\pi} \, \partial_ {0}\widetilde{\phi}-\mathcal{L}(\widetilde{\phi}) = \int dx \, \left( \frac{\beta^{4}\widetilde{\pi}^{2}}{2} + V[\widetilde{\phi}] \right) \\
&\equiv \int dx \,  \frac{1}{2}(\partial_ {0}\widetilde{\phi})^{2}+\frac{1}{2}(\partial _ {i} \widetilde{\phi})^{2} + V(\widetilde{\phi})
\end{align*}
$$

Let $\widetilde{f}(x-b)$ be a kink solution, and $\widetilde{E}_ {0}$ be the rescaled classical (leading-order) kink energy,

$$
\widetilde{E}_ {0} := \beta^{2} V(\widetilde{f}(x)).
$$

Note that all the quantities with a tilde on it are rescaled quantities, constructed so that they are independent of $\beta$. 

The peculiar thing with $\beta^{2}\mathcal{H}$ is that, in terms of $\widetilde{\pi}$, the small quantity $\beta$ multiplies the kinetic term, namely $\beta^{4}\widetilde{\pi}^{2}$, while leaving the potential untouched. This is opposite to the Lagrangian with a small coupling! Sidney Coleman compared it with the case in diatomic molecules, where the kinetic term is also perturbatively small, reduced by a factor of $\frac{1}{M}$, where $M$ is the nuclear reduced mass. The same perturbation method is adopted to calculate the correction to energy eigen value and eigen states. The final result is divergent, maybe not surprisingly, since we have not introduced any renormalization techniques yet. 

- - -

## Coherent-state variational method for time-independent lumps

Another non-relativistic quantum mechanical method we can use to study the quantum lumps is the variational method, with some trial states. The `Rayleigh-Ritz` method is based on the variational principle, which states that for a given Hamiltonian $H$ and a trial wave function $\psi$, the expectation value of the Hamiltonian, $\langle \psi \rvert H \lvert \psi \rangle$, provides an **upper bound** to the ground state energy of the system. The goal is to *choose a trial wave function that minimizes this expectation value*, which then approximates the ground state energy as closely as possible. To do that, we first choose a set of basis functions $\lbrace \phi_ 1, \phi_ 2, \dots, \phi_ n \rbrace$ that are believed to closely resemble the true wave functions of the system. These can be functions that satisfy boundary conditions or other physical considerations of the problem. Then we construct a trial wave function $\psi$ as a linear combination of these basis functions:
  
$$
   \psi = \sum_ {i=1}^n c_ i \phi_ i
$$
  
where $c_ i$ are coefficients to be determined. We can calculate the matrix elements of the Hamiltonian in the basis of the chosen functions. Each element $H_ {ij}$ of the matrix is given by:

$$
  H_ {ij} = \langle \phi_ i \rvert  H \lvert \phi_ j \rangle
$$

The variational principle leads to the matrix equation

$$
   H\mathbf{c} = E\mathbf{c}
$$

where $H,E$ are now regarded as matrices, $\mathbf{c}$ is the vector of coefficients $c_i$, and $E$ is the energy eigenvalue. Solving this eigenvalue problem gives us the approximate energy levels and the corresponding coefficients for the wave functions.

As a quick example, consider a particle in a one-dimensional box of length $L$, with infinitely high walls at $x = 0$ and $x = L$. The Hamiltonian for this system is

$$
H = -\frac{\hbar^2}{2m} \frac{d^2}{dx^2}
$$

with boundary conditions $\psi(0) = \psi(L) = 0$.

We choose sine functions that satisfy the boundary conditions as basis functions:

$$
\phi_ n(x) = \sqrt{\frac{2}{L}} \sin\left(\frac{n\pi x}{L}\right), \quad n = 1, 2, 3, \dots
$$


We could start with a simple trial function using the first two basis functions

$$
\psi(x) = c_ 1 \phi_ 1(x) + c_ 2 \phi_2(x)
$$

to calculate elements $H_{ij}$

$$
H_ {ij} = \frac{\hbar^2}{2m} \left(\frac{n\pi}{L}\right)^2 \delta_ {ij}
$$

For this simplified example, since the Hamiltonian matrix is diagonal (due to orthogonality and the properties of sine functions), the energy eigenvalues are directly given by:

$$
E_ n = \frac{\hbar^2}{2m} \left(\frac{n\pi}{L}\right)^2
$$

- - -

Coleman talked about one advantage of 1+1 dimensional scalar theory: it is `locally Fock`, meaning that when put in a finite box, the exact energy eigenstates are in ordinary Fock space, and this is connected to the mild UV divergence in 2D. How come? If this were true then this indeed facilitates the variational method, since all the trial states are also in Fock space.

Another advantage is that in 2D we can write the Hamiltonian in terms of finite parameters (renormalized parameters) alone, in closed form. This avoids us writing the final results in bare parameters. 

Consider the Hamiltonian (with canonical fields $\phi$, nor rescaled field $\widetilde{\phi}$) 

$$
\mathcal{H} = \frac{1}{2} \pi^{2} + \frac{1}{2}(\partial_ {x}\phi)^{2} + U(\phi),
$$

There is only one type of divergence: the diagrams with one loop and one internal line (propagator) only. Thus we need only one condition to cancel it: the normal ordering of the Hamiltonian. 

We will go on with our calculation of variational method in the Schrodinger picture, where the wave functions are time dependent while the operator are not. In Schrodinger picture the Hamiltonian is not given in $\phi$ and $\dot{\phi}$, but $\phi$ and $\pi$, there is no such thing as $\dot{\phi}$. 

We are all familiar with the time ordering in interaction picture, however here we are talking about normal ordering in Schrodinger picture. The generalization is trivial: we just forget about the time parameter $t$ in interaction picture. We **define** the creation and annihilation part of $\phi$ and $\pi$ as if they are free operators, since the interaction evolves the states not the operators:

$$
\phi^{\pm }(x) := \frac{1}{2} \left[ \phi(x) \mp  \frac{i}{\sqrt{ -\nabla^{2}+m^{2} }}\pi(x) \right]
$$

and 

$$
\pi^{\pm }(x) := \mp i\sqrt{ -\nabla^{2}+m^{2} }\phi^{\pm }(x),
$$

where $\phi^{+}$ is the creation part and $\phi^{-}$ the annihilation part, the same for $\pi$. We then define the normal-ordered version of any function of these operators as the function rearranged with all the creation operators on the left and all the annihilation operators on the right. Here $m$ is to be regarded as a free parameter, we should choose the most convenient value of it, usually the pole mass. Different choice of $m$ represents different choice of renormalization condition. 

We can use Wick's theorem to perform the normal ordering. In Coleman's textbook the normal ordering depends on $m$, but in our work it also depends on which sector we are working in. 

Take the simplest case for an instructive example. Consider the perversely defined Hamiltonian

$$
\mathcal{H} = \mathcal{N}_ {m}\left\lbrace \mathcal{H}_ {0} + \frac{1}{2} M^{2}\phi^{2} \right\rbrace ,
$$

perversely in the sense that the mass parameter of the field is clearly $M$ but we are normal-ordering with respect to $m$, and $m\neq M$. This is a free field model so exactly solvable, and serves as a good test ground for our method. 

Yet we introduce a third mass-parameter $\mu$, which is used to define the vacuum. Assume that the vacuum is such that annihilated by the field with mass $\mu$,

$$
\phi^{-}(x,\mu) \left\lvert{0,\mu}\right\rangle = \pi^{-}(x,\mu)\left\lvert{0,\mu}\right\rangle =0.
$$

Then in order to find the Hamiltonian density, we need to normal-order the Hamiltonian in terms of $\mu$, and a change from $\mathcal{N}_ {m}$ to $\mathcal{N}_ {\mu}$ can be again achieved by Wick's theorem. We'll skip the details and just present the final result. Eventually the Hamiltonian will look like 

$$
\mathcal{H} = \mathcal{N}_ {\mu}\left\lbrace \cdots  \right\rbrace  + f(\mu,M,m)
$$

where $f(\mu,M,m)$ is a scalar function of $\mu,M$ and $m$, which is the non-zero Hamiltonian density.

This completes the first step of the `Rayleigh-Ritz` method, the computation of the expectation value of $H$ in the trial state $\left\lvert{0,\mu}\right\rangle$. The next step is to differentiate this with respect to the variational parameter $\mu$, find the minimum. I'll again skip the details, just mention that it indeed gives the correct answer, saying that the best trial state is $\left\lvert{0,M}\right\rangle$. 

- - -

If we adopt exactly the same method to sine-Gordon model, something strange happens: The energy vev of the trial state is not bounded from below for $\beta^{2}>8\pi$. The variational method always gives a rigorous upper bound on the ground-state energy; in this case the upper bound is minus infinity. Thus we conclude that *the energy of the sine-Gordon theory is unbounded below if* $\beta^{2}>8\pi$.

- - -

We have been working with the vacuum states as the trial state, of course it is not gonna be enough, especially when classic kink background is involved. We need to consider trial states where the vev of $\phi$ is not zero. They are called `coherent states`.

What are coherent states? Consider the familiar harmonic oscillator,

$$
H = \frac{1}{2}(p^{2}+q^{2})
$$

where $q$ is the general coordinate and we have set $\omega,m,\hbar$ to be identity. The ladder operators (raising and lower operators) are constructed as 

$$
\begin{align*}
a &= \frac{1}{\sqrt{ 2 }}(q+ip), \\
a^{\dagger} &= \frac{1}{\sqrt{ 2 }}(q-ip).
\end{align*}
$$

A coherent state is labeled by a complex number $z$ and constructed from the ground state as 

$$
\left\lvert{z}\right\rangle  = D(z)\left\lvert{0}\right\rangle = e^{ - z^{\ast }z/2 } e^{ za^{^{\dagger}} }\left\lvert{0}\right\rangle = e^{ - z^{\ast }z/2 } \sum_ {n\geq 0} \frac{z^{n}}{\sqrt{ n! }}\left\lvert{n}\right\rangle   .
$$

It is most of all the (normalized) eigen vector of the lower operator,

$$
a\left\lvert{z}\right\rangle  = z\left\lvert{z}\right\rangle ,\quad  \left\langle{z}\right\rvert a^{\dagger}=\left\langle{z}\right\rvert z^{\ast }.
$$

Due to this property, coherent states are extremely convenient to deal with normal-ordered functions, since normal ordering ensures that $a^{\dagger}$ always acts on $\left\langle{z}\right\rvert$ from the right and $a$ acts on $\left\lvert{z}\right\rangle$ from left. Let $f(p,q)$ be a normal ordered function of $p$ and $q$, we have 

$$
\left\langle : f(p,q) : \right\rangle = f(\left\langle p \right\rangle,\left\langle q \right\rangle),
$$

where $\left\langle p \right\rangle$ is $\left\langle{z}\right\rvert \;p \left\lvert{z}\right\rangle$, the same for $q$. 

Now we can generalize it to the scalar quantum field theory. In scalar quantum field theory, fields themselves are treated as quantum mechanical operators. In Schrodinger picture one can consider a scalar field $\phi(x)$ is similar to $x$ in the quantum mechanical example above. A coherent state $\lvert\alpha \rangle$ in the field theory context is characterized by: 

$$
a(f) \lvert \alpha \rangle = \alpha(f) \lvert\alpha \rangle
$$

for all test functions $f$, where $a(f)$ is the annihilation operator *smeared with* $f$, and $\alpha(f)$ is a function defining the coherent state. The smeared annihilation operator is given by:

$$
a(f) = \int dx \, f(x) a(x)
$$

where $a(x)$ is the annihilation operator at position $x$, and it relates to the field operators as:

$$
a(x) = \sqrt{\frac{1}{2}} \phi(x) + \frac{i}{\sqrt{2}} \pi(x).
$$

Here, $\omega$ is a characteristic frequency, which can be thought of as a parameter from the dispersion relation of the field.

Just like in quantum mechanics, the coherent states in QFT are superpositions of the eigenstates of the field Hamiltonian, which represent different quantum states of the field. Coherent states in QFT are used to describe states of the field that behave in a manner closest to classical fields. This is because they minimize the uncertainty relations between field operators and their conjugate momenta, akin to the minimum uncertainty states of quantum harmonic oscillators.

Next we can use the coherent states as trial states. I'll not go into details here, interested readers can refer to Coleman's original writings. 

