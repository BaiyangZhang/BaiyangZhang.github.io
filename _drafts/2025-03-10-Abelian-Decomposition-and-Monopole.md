---
layout: post
title: Abelian Decomposition and Monopole
date: 2025-02-25
author: Baiyang Zhang
catalog: true
tags:
---

# Monopole

The gauge Lie group $G$ has an underlying Lie algebra $\mathfrak{g}$, whose generator satisfies

$$
  [T^a,T^b] = i f^{ab}_ {c} T^c
$$

where the indices can be lowered or raised by the Cartan-Killing metric $g^{ab} = \text{Tr }{T^a T^b}$, but for our discussion $g^{ab} = \delta^{ab}$ so it doesn't matter where we put the indices.

The generators in the fundamental representations satisfy normalization condition

$$
  \text{Tr }{T^a T^b} = \frac{1}{2} \delta^{ab}.
$$

Gauge field is a $\mathfrak{g}$-valued field,

$$
 A_ \mu = A_ \mu^a T^a, \, T^a \in \mathfrak{g}.
$$

The $\mathfrak{g}$-valued field strength is

$$
  F_ {\mu\nu} = \partial_ \mu A_ \nu - \partial_ \nu A_ \mu -i[A_ \mu, A_ \nu],
$$

our convention for covariant derivative acting on a field in the fundamental representation is

$$
  D_ {\mu}\psi := \partial_ \mu \psi -i A_ \mu \psi,
$$

while acting on a field in the adjoint representation is

$$
  D_ {\mu}\phi \equiv \partial_ \mu \phi -i [A_ {\mu},\phi],
$$

and

$$
\begin{align*}
[D_ {\mu},D_ {\nu}] \psi &= -iF_ {\mu \nu}\psi,\\
[D_ {\mu},D_ {\nu}]\phi &= -i[F_ {\mu \nu},\phi].
\end{align*}
$$

where again $\psi,\phi$ are fields in the fundamental and adjoint representation respectively.

The gauge transformation for various fields are


- **gauge field**: $A_ \mu \to \Omega (A_ \mu + i \partial_ \mu) \Omega^\dagger,\, \Omega=e^{i \omega^i T^i} \in SU(N)$
- **fundamental scalar field**: $\phi \to \Omega \phi$
- **fundamental spinor field**: $\psi \to \Omega \psi$
- **adjoint scalar field**: $\phi \to \Omega \phi \Omega^\dagger$

It is sometimes useful to know the infinitesimal form of gauge transformation. In such case

$$
  \Omega = 1 + i\omega^a(x) T^a
$$

and the infinitesimal change of the gauge field is

$$
  \delta A = \partial_ \mu \omega - i [A_ \mu,\omega] = D_ \mu \omega
$$

where $\omega = \omega^a T^a$ is a matrix, a $\mathfrak{g}$-valued term. And the infinitesimal change of the field strength is

$$
 \delta F_ {\mu\nu} = i [\omega,F_ {\mu \nu}].
$$

Another useful identity is 

$$
\boxed{
  \delta F_ {\mu\nu} = D_ \mu \delta A_ \nu - (\mu \leftrightarrow \nu)
}.
$$


The action for pure Yang-Mills field is

$$
  S_ {YM} = - \frac{1}{2g^2} \int d^4 x\, \text{Tr }{F_ {\mu\nu}F^{\mu\nu}},
$$

where $g^2$ is the Yang-Mills coupling constant, but $g$ is not a constant at all. The fact that it appears in the denominator instead of numerator (like in Peskin&Schroeder), is due to a rescaling of the Yang-Mills field $A$. We can reproduce the Yang-Mills action used in Peskin&Schroeder by substitution

$$
A \to A/g,\, F\to \partial A -\partial A -ig[A,A].
$$

The advantage of putting the coupling in the front of action is that $g$ is factored out from the Lagrangian, and sits where $\hbar$ does, it implies that in the weak coupling limit, the paths that contribute most to the path integral are the solution to the classical equation of motion, we have the classical limit. If $g\to \infty$, then all path contribute almost equally, we would be living in an entirely quantum world.

Introduce the Hodge star operator on the field strength,

$$
 \star F_ {\mu\nu} = \frac{1}{2} \epsilon_ {\mu\nu\rho\sigma}F^{\rho\sigma},
$$

We have Bianchi identity

$$
 d\star F=0.
$$

- - -

Magnetic Monopole solutions in Yang-Mills theory with adjoint bosons appears more naturally than in U(1) theory. The **adjoint** Higgs fields have non-zero vacuum expectation values (VEV for short, denoted by $\left\langle \bullet \right\rangle$), breaking the gauge symmetry. Those gauge transformations that leave $\left\langle \phi \right\rangle$ invariant are symmetries not spontaneously broken by the Higgs bosons. Loosely speaking there are two kinds of symmetries:


- the symmetry of the Lagrangian, and
- the symmetry of the vacuum.

Gauge symmetry is not really a symmetry but a redundancy, a change of basis, so here we don't count it. Sometimes, a symmetry is preserved in the Lagrangian but not the vacuum, meaning that the symmetry will change the vacuum, e.g. the double well potential in quantum mechanics, the $x \leftrightarrow -x$ symmetry doesn't change the Lagrangian, but it turn one vacuum to the other, thus it is not a symmetry of the vacuum. In this case we say this symmetry is spontaneously broken. Of course, since the spontaneously broken symmetry is still a symmetry of the Hamiltonian, it only takes one vacuum to another. In more mathematical terms, let $H$ be the broken symmetry and $\phi_ {0}$ be any vacuum configuration, the orbit of $H$ acting on $\phi_ {0}$ is the vacuum manifold, or at least a connected submanifold of vacuum. 

Why should we start with SU(2) monopole? because 

- it is the simplest monopole in Yang-Mills theory, and
- $SU(2)$ monopole solution is the building block for monopole solutions in larger groups.

In SU(2) Yang-Mills theory, the generator is $T^a = \frac{1}{2}\sigma^a$, where $\sigma$'s are the Pauli matrices, with inner product defined by the trace:

$$
  \left\langle T^{a} \middle\vert T^b \right\rangle  := \text{Tr }{T^a T^b} = \frac{1}{2}\delta^{ab}
$$

Besides the gauge field, we need to add the triplet Higgs scalar in the adjoint representation,

$$
  \phi = \frac{\sigma^a}{2}\phi^a
$$

with convention $\left\lvert \phi \right\rvert^{2} := \phi^a \phi^a = 2\text{Tr }(\phi^a T^a)^2$. In our convention, if $\phi$ without absolute value notation is squared, we are simply squaring the matrix field itself, while if $|\phi|$ is squared, we are doing the module square.

The Lagrangian is

$$
  \mathcal{L} = \int d^4 x \, \left\lbrace   {-\frac{1}{2e^2}\text{Tr }F_ {\mu\nu}F^{\mu\nu}+ \frac{1}{e^2}\mathrm{Tr}\,\left\lvert D_ \mu \phi \right\rvert ^2-V(\phi)}\right\rbrace,
$$

where

$$
  V(\phi) = - \mu^2 \text{Tr }{\phi^2} + \lambda(\text{Tr }{\phi^2})^2 = -\frac{\mu^2}{2}\phi^a \phi^a +\frac{\lambda}{4}(\phi^a \phi^a )^2,
$$

the vacuum manifold is $\mathbb{S}^{2}$. To see this we can complete the square

$$
  V = \frac{\lambda}{4} \left( \phi^a\phi^a-v^2 \right)^2-\frac{\mu^4}{4\lambda}, \quad v^2 = \frac{\mu^2}{\lambda}.
$$

Fix the vacuum to be

$$
  \left\langle \phi^{1} \right\rangle = \left\langle \phi^2 \right\rangle = 0,\, \left\langle \phi^3 \right\rangle = v,\, \left\langle A \right\rangle = 0.
$$

i.e. the VEV of $\bm{\phi}$ field points to the z-direction.
The gauge symmetry SU(2) is broken to $U(1)$, since only $e^{i\theta^3 T^3}$ preserves the vacuum.

It is often useful to separate the field strength into ``magnetic'' and ``electric'' part,
\begin{align}
  B_ i &= -\frac{1}{2} \epsilon_ {ijk}F_ {jk},\\
  E_ i &= F_ {0i}.
\end{align}
Note that in Yang-Mills theory, B and E are not gauge invariant as they are in U(1) theory. It means that they are no longer physical observables. In Yang-Mills theory, the physical observables are gauge invariant objects, such as the trace of $F_ {\mu\nu}^2$ or the Wilson loops.

Since we have chosen the vacuum to be $\vev{\phi} = v T^3$, the quanta of the theory are
\begin{itemize}
  \item two massive gauge bosons, $W_ \mu^\pm = \frac{1}{\sqrt{2}}(A_ \mu^1 \pm i A_ \mu^2)$.
      The mass comes solely from the covariant derivative $|D_ \mu \phi|^2$, after shifting $\phi^3$ to $\phi^3 + v$, the coupling between A and $\phi^3$ is
      \[
      \frac{1}{2}\frac{(\phi^3)^2}{e^2}A_ \mu^a A^{a\mu}\equiv  \frac{1}{2}m_ W^2 A^2,\quad a = 1,2
      \]
  \item $A^3$ will remain massless, it is the ``photon'' decoupled from $\phi^3$
  \item $\phi^3$ particle is electrically neutral.
\end{itemize}

For the total energy to be finite, we must have at spacial infinity,
$$
  |\phi| \to v,\quad |D_ \mu \phi|^2 \to 0, \quad A \to i \Omega \partial_ \mu\Omega^{-1}
$$
$|D_ \mu \phi|^2$ must drop to zero faster than $r^{-3/2}$ to make the energy integral finite.

The topology of the space boundary is $S^2$ i.e. $\partial \mathbb{R}^3 = S^2$, the vacua of the Higgs field is also $S^2$, the Higgs field at $r \to \infty$ is a map $S^2 \to S^2$, which is classified by homotopy group $\pi_ 2(S^2) = \mathbb{Z}$, where $\mathbb{Z}$ is the addition group of integers. Hence the a finite energy Higgs configuration can be labeled by an integer n, which counts if we go through the spacial boundary, how many times the $\phi$ vacua winds around. Given a $\phi$ field configuration, the winding number is given by
$$
\boxed{
  n = \frac{1}{8\pi}\epsilon_ {ijk} \epsilon_ {abc} \int d^2S_ i \, \hat{\phi}^{a}\partial_ {j} \hat{\phi}^{b}\partial_ {k} \hat{\phi}^{c}
  }
$$
where $\hat{\phi}^{i} \equiv \phi^{i} / |\phi|$ is the unit field vector.
The trivial vacuum where $\phi = \text{const}$ everywhere clearly has $n = 0$.

Let us look at what happens at $n=1$. $\vev{\phi}$ would depend on the direction. The unbroken U(1) of SU(2) is that commutes with $\vev{\phi}$, hence is also position-dependent, which can be written in a gauge invariant form
$$
  a_ \mu = \frac{2}{v} \text{Tr }{\phi A_ \mu},
  \label{eq:amu}
$$
for example, if $\phi = v T^3, \, a_ \mu = A_ \mu^3$.

\begin{rmk}
  Regard $A_ \mu = A_ \mu^a T^a$ as a $\mathfrak{su}(2)$-valued field, the unbroken U(1) component is a vector in the Lie-algebra whose direction, after choosing a $\phi$ vacuum, is parallel to $\phi$. For example, if $\phi$ vacuum is chosen to be $vT^3$, then the unbroken U(1) group is proportional to $T^3$. In the case of a monopole solution, the U(1) direction is position-dependent.
\end{rmk}

Let's look at the covariant derivative. In order to make sure $|D_ \mu\phi| = |\partial_ \mu\phi-i[A_ \mu,\phi]| \to 0$, we need to find a corresponding $A_ \mu$ that can cancel the $\partial_ \mu \phi$, for $\phi = v \hat{\phi}$. Note that
$$
  \phi^2 = \phi^a T^a \phi^b T^b = \frac{1}{2}\phi^a\phi^b \anticom{T^a}{T^b} =  \frac{v^2}{4}
$$
where we have used the relation that
$$
  \sigma^i \sigma^j = \delta^{ij} + i \epsilon^{ijk}\sigma^k.
$$
We have
$$
  \partial_ \mu \phi^2 = 0 = \anticom{\partial_ \mu \phi}{\phi}
$$
thus
$$
  \com{\partial_ \mu \phi}{\phi} = -2\phi\partial_ \mu \phi
$$
and
$$
  \com{\com{\partial_ \mu \phi}{\phi}}{\phi} = v^2 \partial_ \mu \phi.
$$
Letting
$$
\boxed{
 A_ \mu \to -\frac{i}{v^2} \com{\partial_ \mu \phi}{\phi}+\frac{a_ \mu}{v}\phi,
 }
$$
then
$$
  -i \com{A_ \mu}{\phi} = - \partial_ \mu \phi,
$$
$a_ \mu$ above is the same as that in Eq.\eqref{eq:amu}, namely $a_ \mu \phi$ is the unbroken U(1) field.

Knowing the asymptotic form of the gauge field, we can work out the asymptotic form of $F_ {\mu\nu}$, however we are mostly interested in the U(1) part, that is the field strength in the same direction of $\phi$,
\begin{align}
\notag
  F_ {\mu\nu} &= \partial_ \mu A_ \nu-\partial_ \nu A_ \mu-i\com{A_ \mu}{A_ \nu}\\
  &= \frac{\phi}{v}(\partial_ \mu a_ \nu - \partial_ \nu a_ \mu )+\frac{i}{v^2}\com{\partial_ \mu \phi}{\partial_ \nu \phi} + \frac{a_ \mu }{v} \partial_ \nu \phi - \frac{a_ \nu }{v} \partial_ \mu \phi
\end{align}
The last two terms are orthogonal to $\phi$ thus we can discard them.
Writing
$$
  F_ {\mu\nu} =  \cdots + f_ {\mu\nu}\frac{\phi}{v}
$$
where
$$
  f_ {\mu\nu} = \partial_ \mu a_ \nu - \partial_ \mu a_ \nu +\frac{2i}{v^3}\text{Tr }{\phi\com{\partial_ \mu \phi}{\partial_ \nu \phi}}
$$
is the U(1) field strength. The corresponding magnetic field is
$$
  B_ i = -\frac{1}{2} \epsilon_ {ijk}f_ {jk} = \cdots + \frac{1}{2v^3}\epsilon_ {ijk}\epsilon_ {abc}\phi^a \partial_  j \phi^{b}\partial_ {k} \phi^{c}
$$
The last term is a surprise since it comes from the non-abelian part, whose contribution to the magnetic charge is proportional to the topological charge
$$
  m = \int d^2S_ i\, B_ i = \frac{1}{2} \int d^2S_ i\,
  \epsilon_ {ijk}\epsilon_ {abc}\hat{\phi}^a \partial_  j \hat{\phi}^{b}\partial_ {k} \hat{\phi}^{c} = 4\pi n
$$
where n is the winding number.
The $\partial_ \mu a_ \nu - \partial_ \mu a_ \nu$ term doesn't contribution to the magnetic charge since its contribution to the magnetic field is a curl term, whose divergence vanishes.
Such solution with a quantized U(1) magnetic charge goes by the name 't Hooft-Polyakov monopole.

\subsection{Monopole Solutions}

Above we have given a general analyses, to find the explicit monopole solution, we introduce the hedgehog ansatz for winding number $n = 1$, a natural guess for the solution for $\phi$:
$$
  \phi^i = v \hat{x}^i h(r), \quad h(r) \to
  \begin{cases}
    1 & r \to \infty \\
    0 & r \to 0
  \end{cases}.
$$
We can find corresponding $A_ \mu$ at spacial infinity by solving
$$
  D_ i \phi = 0 \implies \partial_ i \hat{x}^a + \epsilon_ {abd}A_ \mu^b \hat{x}^c = 0
$$
by multiplying both sides by $x_ j \epsilon_ {adj}$. The final results is
\be
  A_ i^a(x) = a(r) \epsilon_ {aij}x_ j/er^2, \quad a(r) \to
  \begin{cases}
    1 & r \to \infty \\
    0 & r \to 0
  \end{cases}.
$$
The explicit form of $h(r)$ and $a(r)$ can be worked out by solving the equation of motion, numerically if not analytically.

Question: is this form of $A$ a pure gauge, meaning $A_ \mu = i\Omega \partial_ \mu \Omega^{-1}$ for some $\Omega$? It looks to me that it differs from pure gauge by an extra term.

\section{Generalization to SU(N)}

The SU(N) gauge symmetry can be maximally broken to $U(1)^{N-1}$ abelian components, they are the sub Lie algebra of $\mathfrak{su}(N)$. Here we use the Gothic font to denote the Lie algebra. Consequently,
\begin{itemize}
  \item we have N-1 different kinds of electric charges, field may have various linear combination of these charges.
  \item There will be monopole solutions with respect to $U(1)^{N-1}$
\end{itemize}
There are already some pretty nice references on SU(3) monopole\footnote{DOI:https://doi.org/10.1103/PhysRevD.14.2016}.



# The Gist of the Theory

In QCD, the $\mathfrak{g}$-valued gauge potential is decomposed to the abelian sub-algebra, so-called Cartan subalgebra, and the rest. 