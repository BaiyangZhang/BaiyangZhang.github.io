---
layout: post
title: Abelian Decomposition and Monopole
date: 2025-03-19
author: Baiyang Zhang
catalog: true
tags:
---

# Convention

The gauge Lie group $G$ has Lie algebra $\mathfrak{g}\in T_ {e}G$, where $e$ is the unit element of $G$. The generators $T^{a}$ of $G$ satisfy

$$
  [T^a,T^b] = i f^{ab}_ {c} T^c
$$

where $f^{abc}$ is the structure constant. The indices can be lowered or raised by the Cartan-Killing metric $g^{ab} = \text{Tr }{T^a T^b}$, for our discussion $g^{ab} = \delta^{ab}$, so it doesn't matter where we put the indices.

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

where $g^2$ is the Yang-Mills coupling constant, but $g$ is not a constant at all. The fact that it appears in the denominator instead of numerator (like in Peskin&Schroeder), is due to a rescaling of the Yang-Mills field $A$. We can reproduce the Yang-Mills action used in Peskin&Schroeder by the following substitution in our convention:

$$
A \to g A,\, F \to g\partial A -g\partial A -ig^{2}[A,A].
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
# 't Hooft-Polyakov Monopole

Magnetic Monopole solutions in Yang-Mills theory with adjoint bosons appears more naturally than in U(1) theory. Whenever the **non-abelian** gauge group is broken to its **Cartan subgroup** (Cartan subalgebra is spanned by a maximal set of Lie algebra) by adjoint Higgs bosons, we have magnetic monopoles. The **adjoint** Higgs fields have non-zero vacuum expectation values (VEV for short, denoted by $\left\langle \bullet \right\rangle$), breaking the gauge symmetry. Those gauge transformations that leave $\left\langle \phi \right\rangle$ invariant are symmetries not spontaneously broken by the Higgs bosons. Loosely speaking there are two kinds of symmetries:

- the symmetry of the Lagrangian,
- the symmetry of the vacuum.

Gauge symmetry is not really a symmetry but a redundancy, a change of basis, so here we don't count it. Sometimes, a symmetry is preserved in the Lagrangian but not the vacuum, meaning that the symmetry will change the vacuum, e.g. the double well potential in quantum mechanics, the $x \leftrightarrow -x$ symmetry doesn't change the Lagrangian, but it turn one vacuum to the other, thus it is not a symmetry of the vacuum. In this case we say this symmetry is spontaneously broken. Of course, since the spontaneously broken symmetry is still a symmetry of the Hamiltonian, it only takes one vacuum to another. In more mathematical terms, let $H$ be the broken symmetry and $\phi_ {0}$ be any vacuum configuration, the orbit of $H$ acting on $\phi_ {0}$ is the vacuum manifold, or at least a connected submanifold of vacuum. 

Why should we start with $SU(2)$ monopole? because 

- it is the simplest monopole in Yang-Mills theory, and
- $SU(2)$ monopole solution is the building block for monopole solutions in larger groups.

In $SU(2)$ Yang-Mills theory, the generator is $T^a = \frac{1}{2}\sigma^a$, where $\sigma$'s are the Pauli matrices, with inner product defined by the trace:

$$
  \left\langle T^{a} \middle\vert T^b \right\rangle  := \text{Tr }{T^a T^b} = \frac{1}{2}\delta^{ab}
$$

Besides the gauge field, let us add the triplet Higgs scalar in the adjoint representation,

$$
  \phi = \frac{\sigma^a}{2}\phi^a
$$

with convention $\left\lvert \phi \right\rvert^{2} := \phi^a \phi^a = 2\text{Tr }(\phi^a T^a)^2$. In our convention, if $\phi$ without absolute value notation is squared, we are simply squaring the matrix field itself, while if $\left\lvert \phi \right\rvert $ is squared, we are doing the module square.

The action is

$$
  S = \int d^4 x \, \left\lbrace   {-\frac{1}{2e^2}\text{Tr }F_ {\mu\nu}F^{\mu\nu}+ \frac{1}{e^2}\mathrm{Tr}\,\left\lvert D_ \mu \phi \right\rvert ^2-V(\phi)}\right\rbrace,
$$

where

$$
  V(\phi) = - \mu^2 \text{Tr }{\phi^2} + \lambda(\text{Tr }{\phi^2})^2 = -\frac{\mu^2}{2}\phi^a \phi^a +\frac{\lambda}{4}(\phi^a \phi^a )^2,
$$

the vacuum manifold is $\mathbb{S}^{2}$. To see this we can complete the square

$$
  V = \frac{\lambda}{4} \left( \phi^a\phi^a-v^2 \right)^2-\frac{\mu^4}{4\lambda}, \quad v^2 = \frac{\mu^2}{\lambda},
$$

If $v^{2}<0$, the model is in confined phase. We will assume that $v^{2}>0$, so the theory sits in the Higgs phase. One possible vacuum is obtained at

$$
  \left\langle \phi^{1} \right\rangle = \left\langle \phi^2 \right\rangle = 0,\, \left\langle \phi^3 \right\rangle = v,\, \left\langle A \right\rangle = 0.
$$

The VEV of $\vec{\phi}$ field points to the $z$-direction. Now the gauge symmetry $SU(2)$ is broken to $U(1)$, since the vacuum for the Higgs is $\left\langle \phi \right\rangle=\phi^{3}T^{3}$ and only the gauge transform given by $e^{i\theta^3 T^3}$ preserves the vacuum:

$$
SU(2) \to  U(1).
$$

It is often useful to borrow the terminologies from QED, separating the field strength into "magnetic" and "electric" part,

$$
\begin{align*}
  B_ i &= -\frac{1}{2} \epsilon_ {ijk}F_ {jk},\\
  E_ i &= F_ {0i}.
\end{align*}
$$

Note that in Yang-Mills theory, $B$ and $E$ are matrices and they are not gauge invariant as in $U(1)$ theory. It means that $B,E$ are no longer physical observables which must be gauge invariant, such as the trace of $F_ {\mu\nu}^2$ or the Wilson loops.

Since we have chosen the vacuum to be $\left\langle \phi \right\rangle = v T^3$, in the unitary gauge, the degrees of freedom are
- two massive gauge bosons, $W_ \mu^\pm = \frac{1}{\sqrt{2}}(A_ \mu^1 \pm i A_ \mu^2)$. The mass comes solely from the covariant derivative $\left\lvert D_ \mu \phi \right\rvert^2$, after shifting $\phi^3$ to $\phi^3 + v$, the coupling between A and $\phi^3$ is

$$
\frac{1}{2}\frac{v^2}{e^2}A_ \mu^a A^{a\mu}\equiv  \frac{1}{2}m_ W^2 A^2,\quad a = 1,2
$$

- $A^3$ remains massless, it is the "photon" decoupled from $\phi^3$
- $\phi^3$ particle is electrically neutral.

For the total energy to be finite, we must have that at spatial infinity the field configuration goes to a vacuum configuration fast enough:

$$
  \left\lvert \phi \right\rvert  \to v,\quad \left\lvert D_ \mu \phi \right\rvert ^2 \to 0, \quad A \to i \Omega \partial_ \mu\Omega^{-1}.
$$

Note that $\left\lvert D_ \mu \phi \right\rvert^2$ must drop to zero faster than $r^{-3/2}$ to make the energy integral finite.

The topology of the space boundary is $\mathbb{S}^2$ since $\partial \mathbb{R}^3 = \mathbb{S}^2$. The vacuum manifold of the Higgs field is also $\mathbb{S}^2$, thus the Higgs field at $r \to \infty$ is a map $\mathbb{S}^2 \to \mathbb{S}^2$, which is classified by homotopy group $\pi_ 2(S^2) = \mathbb{Z}$, where $\mathbb{Z}$ is the addition group of integers. We can use homotopy to classify topologically different solutions, labeling any finite energy Higgs configuration by an integer $n$, which counts the winding number of Higgs field at infinity. Given a $\phi$ field configuration, Let $\hat{\phi}^{i} \equiv \phi^{i} / \left\lvert \phi \right\rvert$ be the unit field vector, the winding number give by integrating the pullback of the volume in $\phi$ configuration space:

$$
\boxed{
  n = \frac{1}{8\pi}\epsilon_ {ijk} \epsilon_ {abc} \int d^2S_ i \, \hat{\phi}^{a}\partial_ {j} \hat{\phi}^{b}\partial_ {k} \hat{\phi}^{c}
  }
$$

The trivial vacuum where $\phi = \text{const}$ everywhere obviously has $n = 0$.

Consider the case winding number $n=1$. $\left\langle \phi \right\rangle$ at infinity depends on the direction. The residual U(1) symmetry of $SU(2)$ consists of the elements that commutes with $\left\langle \phi \right\rangle$, thus U(1) also depends on the direction. Recall that $A_ \mu = A_ \mu^a T^a$ as a $\mathfrak{su}(2)$-valued field, the components of $A_ {\mu}$ that commutes with $\phi$ can be projected out (in any direction) via

$$
  a_ \mu = \frac{2}{v} \text{Tr }{\phi A_ \mu},
$$

for example, if $\phi = v T^3, \, a_ \mu = A_ \mu^3$.

The unbroken U(1) component is a vector in the Lie-algebra whose direction, after choosing a $\phi$ vacuum, is parallel to $\phi$. For example, if $\phi$ vacuum is chosen to be $vT^3$, then the unbroken U(1) group is proportional to $T^3$. In the case of a monopole solution, the U(1) direction is position-dependent.

Let's look at the covariant derivative. In order to make sure that $\left\lvert D_ \mu\phi \right\rvert^{2} = \left\lvert \partial_ \mu\phi-i[A_ \mu,\phi] \right\rvert^{2} \to 0$, we need to find a corresponding $A_ \mu$ that can cancel the $\partial_ \mu \phi$, for $\phi = v \hat{\phi}$. 

The following identities might be helpful:

$$
  \phi^2 = \phi^a T^a \phi^b T^b = \frac{1}{2}\phi^a\phi^b \left\lbrace  T^a ,T^b  \right\rbrace=  \frac{v^2}{4}.
$$

For Pauli matrices we have 

$$
  \sigma^i \sigma^j = \delta^{ij} + i \epsilon^{ijk}\sigma^k.
$$

If $\phi^{2}$ is constant, we have

$$
  \partial_ \mu \phi^2 = 0 = \left\lbrace \partial_ \mu \phi,\phi \right\rbrace 
$$

thus

$$
   [\partial_ \mu \phi,\phi] = -2\phi\partial_ \mu \phi
$$


and

$$
  \left[ [\partial_ \mu \phi,\phi],\phi  \right] = v^2 \partial_ \mu \phi.
$$

Let

$$
\boxed{
 A_ \mu \to -\frac{i}{v^2} [\partial_ \mu \phi,\phi]+\frac{a_ \mu}{v}\phi,
 }
$$

then

$$
  -i [A_ \mu,\phi] = - \partial_ \mu \phi,
$$

$a_ \mu$ above is the same as the unbroken U(1) field.

Knowing the asymptotic form of the gauge field, we can work out the asymptotic form of $F_ {\mu\nu}$, however we are mostly interested in the U(1) part, that is the field strength in the same direction of $\phi$,

$$
\begin{align}
\notag
  F_ {\mu\nu} &= \partial_ \mu A_ \nu-\partial_ \nu A_ \mu-i[{A_ \mu},{A_ \nu}]\\
  &= \frac{\phi}{v}(\partial_ \mu a_ \nu - \partial_ \nu a_ \mu )+\frac{i}{v^2}[{\partial_ \mu \phi},{\partial_ \nu \phi}] + \frac{a_ \mu }{v} \partial_ \nu \phi - \frac{a_ \nu }{v} \partial_ \mu \phi
\end{align}
$$

The last two terms are orthogonal to $\phi$ thus we can discard them. Writing

$$
  F_ {\mu\nu} =  \cdots + f_ {\mu\nu}\frac{\phi}{v}
$$

where

$$
  f_ {\mu\nu} = \partial_ \mu a_ \nu - \partial_ \mu a_ \nu +\frac{2i}{v^3}\text{Tr }{\phi[{\partial_ \mu \phi},{\partial_ \nu \phi}]}
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

where n is the winding number. The $\partial_ \mu a_ \nu - \partial_ \mu a_ \nu$ term doesn't contribution to the magnetic charge since its contribution to the magnetic field is a curl, whose divergence vanishes. Such solution with a quantized U(1) magnetic charge goes by the name 't Hooft-Polyakov monopole.

- - -

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

$$
  A_ i^a(x) = a(r) \epsilon_ {aij}x_ j/er^2, \quad a(r) \to
  \begin{cases}
    1 & r \to \infty \\
    0 & r \to 0
  \end{cases}.
$$

The explicit form of $h(r)$ and $a(r)$ can be worked out by solving the equation of motion, numerically if not analytically.

The SU(N) gauge symmetry can be maximally broken to $U(1)^{N-1}$ abelian components, they are the sub Lie algebra of $\mathfrak{su}(N)$. Here we use the Gothic font to denote the Lie algebra. Consequently,

- we have N-1 different kinds of electric charges, field may have various linear combination of these charges.
- There will be monopole solutions with respect to $U(1)^{N-1}$

There are already some pretty nice references on SU(3) monopole, for example this one: https://doi.org/10.1103/PhysRevD.14.2016.

# Abelian Projection of SU(N) QCD

In studying nonperturbative effects like quark confinement in SU(N) QCD, it is often useful to extract an effective Abelian theory from QCD, which retains essential physics while simplifying computations. This approach is called the Abelian projection.

Abelian projection is a method that extracts an Abelian $U(1)^{N-1}$ theory (for gauge group $SU(N)$) from a non-Abelian gauge theory like QCD by *partially fixing the gauge* so that only the Cartan subgroup (the maximal torus group) remains unbroken.

There is strong evidence that confinement may be related to the concept of dual superconductivity, where the QCD vacuum behaves like a type-II superconductor with condensation of magnetic monopoles. In electrodynamics, magnetic charges and electric charges are treated symmetrically in Maxwell's equations. In QCD, however:

- The electric sector corresponds to the color charges carried by quarks.
- The magnetic sector involves topological objects like monopoles that arise from the non-Abelian nature of the gauge group.

The idea behind the Abelian projection is that even though QCD is a non-Abelian theory, its **long-distance behavior** might be dominated by Abelian degrees of freedom, similar to how superconductors exhibit Abelian gauge behavior.

The Abelian projection involves fixing the gauge partially, such that only the maximal Abelian subgroup (Cartan subgroup) remains unbroken.

Take $SU(3)$ QCD for example. The Lie algebra $\mathfrak{su}(3)$ consists of eight generators $T^a (a=1,…,8a = 1, \dots, 8)$, corresponding to eight gluon fields $A_ \mu^a$. Its Cartan subgroup consists of diagonal elements that form a maximal Abelian subgroup:

$$
U(1)^{N-1} \subset SU(N).
$$

For SU(3), the maximal Abelian subgroup is $U(1) \times U(1)$, generated by the two diagonal Gell-Mann matrices $T^3$ and $T^8$.

- - -

Gauge fixing means choosing a specific gauge transformation to simplify the theory while preserving essential physics. In Abelian projection, we choose a gauge-fixing condition that preserves only the Cartan subgroup.

A common choice is to diagonalize a field like the Polyakov loop $P(x)$ or the adjoint Higgs field in the fundamental representation:

$$
P(x) = \mathcal{P} \exp \left( i \int_ 0^\beta A_ 0(x, t) dt \right),
$$

where $A_0$ is the time component of the gauge field and $\mathcal{P}$ denotes path ordering. By fixing a gauge such that $P(x)$ is diagonal, the remaining gauge freedom consists only of transformations in the Cartan subgroup (because $T^{3}$ and $T^{8}$ are also diagonal), effectively reducing the theory to an Abelian gauge theory.

- - -

After Abelian projection,

1. The gauge fields decompose into **diagonal (Abelian) components** and **off-diagonal (charged) components**:
    
    $$
    A_ \mu = A_ \mu^{\text{diag}} + A_ \mu^{\text{off-diag}}.
    $$
    
    The diagonal fields behave like photons in electromagnetism, while the off-diagonal fields carry color charge.
    
2. Magnetic Monopoles Appear Naturally: The gauge fixing makes topological excitations like magnetic monopoles manifest. 
    
3. Supports the Dual Superconductor Picture: In a superconductor, electric charges form Cooper pairs that condense, leading to the **Meissner effect** (expulsion of magnetic fields). In QCD, the dual of this process suggests that **monopoles condense**, leading to the confinement of quarks via the dual Meissner effect.


# Abelian Decomposition in SU(2)

The Cho-Duan-Ge decomposition is a covariant separation of the gauge field into abelian and non-abelian components. Roughly speaking, the gauge potential is separated into
- abelian, restricted gauge potential. It is further separated into
	- topologically trivial part, or Maxwell part, or `neurons`. And
	- topological part, or Dirac part. Monopole?
- valance gauge field which describes colored gluons, or `chromons`.

For the sake of simplicity we will consider $SU(2)$ Consider The $\mathfrak{g}$-valued gauge potential is decomposed to the abelian sub-algebra, so-called Cartan subalgebra, and the rest part that is orthogonal to it. Let $\hat{n}$ be a unit vector, $\hat{n}=(\hat{n}^{1},\hat{n}^{2},\hat{n}^{3})$ and $\hat{n}^{i}\hat{n}^{i}=1$. Let's put it in the Lie algebra $\mathfrak{g}$, by assigning each component $\hat{n}^{i}$ to a basis $T^{a}\in\mathfrak{g}$, $T^{a} = \frac{\sigma^{2}}{2}$ for $SU(2)$. Let $N$ be the $\mathfrak{g}$-valued unit vector $\hat{n}$, i.e. $N:= \hat{n}^{i}T^{i}$. Now we can act the covariant derivative on $N$, just how we act covariant derivative on $\mathfrak{g}$-valued scalar fields. 

