---
layout: post
title: Bare Minimum of Abelian Decomposition
date: 2025-11-07
author: Baiyang Zhang
catalog: true
tags:
---

# Convention

The gauge Lie group $G$ has Lie algebra $\mathfrak{g}\in T_ {e}G$, where $e$ is the unit element of $G$. The generators $T^{a}$ of $G$ satisfy

$$
  [T^a,T^b] = i {f^{ab}}_ {c} T^c
$$

where $f^{abc}$ is the structure constant. The indices can be lowered or raised by the Cartan-Killing metric $g^{ab} = \text{Tr }{T^a T^b}$, for our discussion $g^{ab} = \delta^{ab}$, so it doesn't matter where we put the indices.

The generators in the fundamental representation satisfy normalization condition

$$
  \text{Tr }{T^a T^b} = \frac{1}{2} \delta^{ab}.
$$

Gauge field is a $\mathfrak{g}$-valued field,

$$
 A_ \mu = A_ \mu^a T^a, \, T^a \in \mathfrak{g}.
$$

The $\mathfrak{g}$-valued field strength is ($g$ is the coupling)

$$
  F_ {\mu\nu} = \partial_ \mu A_ \nu - \partial_ \nu A_ \mu -ig[A_ \mu, A_ \nu].
$$

The advantage of using commutators is that we can avoid using the explicit matrix form of generators in the adjoint representation, which is $(N^{2}-1)\times(N^{2}-1)$ dimensional. 

Our convention for covariant derivative acting on a field in the fundamental representation is

$$
  D_ {\mu}\psi := \partial_ \mu \psi -i g A_ \mu \psi,
$$

while acting on a field in the adjoint representation is

$$
  D_ {\mu}\phi \equiv \partial_ \mu \phi -i g[A_ {\mu},\phi],
$$

and

$$
\begin{align*}
[D_ {\mu},D_ {\nu}] \psi &= -igF_ {\mu \nu}\psi,\\
[D_ {\mu},D_ {\nu}]\phi &= -ig[F_ {\mu \nu},\phi].
\end{align*}
$$

where again $\psi,\phi$ are fields in the fundamental and adjoint representation respectively.

The gauge transformation for various fields are

- **gauge field**: $A_ \mu \to \Omega \left( A_ \mu + \frac{i}{g} \partial_ \mu \right) \Omega^\dagger,\, \Omega=e^{i \omega^i T^i} \in SU(N)$
- **fundamental scalar field**: $\phi \to \Omega \phi$
- **fundamental spinor field**: $\psi \to \Omega \psi$
- **adjoint scalar field**: $\phi \to \Omega \phi \Omega^\dagger$

It is sometimes useful to know the infinitesimal form of gauge transformation. In such case

$$
  \Omega = 1 + i\omega^a(x) T^a
$$

and the infinitesimal change of the gauge field is

$$
  \delta A =\frac{1}{g} \partial_ \mu \omega - i [A_ \mu,\omega] =\frac{1}{g} D_ \mu \omega
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
  S_ {YM} = - \frac{1}{2} \int d^4 x\, \text{Tr }{F_ {\mu\nu}F^{\mu\nu}},
$$

Introduce the Hodge star operator on the field strength,

$$
 \star F_ {\mu\nu} = \frac{1}{2} \epsilon_ {\mu\nu\rho\sigma}F^{\rho\sigma},
$$

We have Bianchi identity

$$
 d\star F=0.
$$

# 't Hooft-Polyakov Monopole

In this section we temporarily absorb the coupling $g$ into the gauge field $A$.

Magnetic Monopole solutions in $SU(2)$ Yang-Mills theory with adjoint bosons appears more naturally than that in U(1) theory. Whenever the **non-abelian** gauge group is broken to its **Cartan subgroup** (Cartan subalgebra is spanned by a maximal mutual-commuting basis of Lie algebra) by adjoint Higgs bosons, we have magnetic monopoles. The **adjoint** Higgs fields have non-zero vacuum expectation values (VEV for short, denoted by $\left\langle \bullet \right\rangle$), breaking the gauge symmetry. Those gauge transformations that leave $\left\langle \phi \right\rangle$ invariant are symmetries not broken by the Higgs bosons. 

Loosely speaking there are two kinds of symmetries:

- the symmetry of the Lagrangian,
- the symmetry of the vacuum.

What about gauge symmetry? Gauge symmetry is not really a symmetry, rather it is a redundancy, corresponds to the freedom of a change of basis. 

Sometimes, a symmetry is preserved in the Lagrangian but not the vacuum, meaning that the symmetry will change the vacuum, e.g. the double well potential in quantum mechanics, the $x \leftrightarrow -x$ transformation doesn't change the Lagrangian, but it turns one vacuum to the other, thus it is not a symmetry of the vacuum. In this case we say this symmetry is spontaneously broken. Of course, since the spontaneously broken symmetry is still a symmetry of the Hamiltonian, it preserves the energy and only takes one vacuum (minimal energy) to another. In more mathematical terms, let $H$ be the broken symmetry and $\phi_ {0}$ be any vacuum configuration, the orbit of $H$ acting on $\phi_ {0}$ is the vacuum manifold, or at least a connected submanifold of vacuum. 

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

with convention $\left\lvert \phi \right\rvert^{2} := \phi^a \phi^a = 2\text{Tr }(\phi^2)$. In our convention, if $\phi$ without absolute value notation is squared, we are simply squaring the matrix field itself, while if $\left\lvert \phi \right\rvert$ is squared, we are doing the module square.

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

The VEV of $\vec{\phi}$ field points to the $z$-direction. Now the gauge symmetry $SU(2)$ is broken to $U(1)$, since the vacuum for the Higgs is $\left\langle \phi \right\rangle=\phi^{3}T^{3}$ and only the gauge transformation given by $e^{i\theta^3 T^3}$ preserves the vacuum:

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

Note that in Yang-Mills theory, $B$ and $E$ are matrices and they are not gauge invariant, in contrast to $U(1)$ theory. It means that $B,E$ are no longer physical observables (which must be gauge invariant), such as the trace of $F_ {\mu\nu}^2$ or the Wilson loops.

Since we have chosen the vacuum to be $\left\langle \phi \right\rangle = v T^3$, in the unitary gauge, the degrees of freedom are
- two massive gauge bosons, $W_ \mu^\pm = \frac{1}{\sqrt{2}}(A_ \mu^1 \pm i A_ \mu^2)$. The mass comes solely from the covariant derivative $\left\lvert D_ \mu \phi \right\rvert^2$, after shifting $\phi^3$ to $\phi^3 + v$, the coupling between A and $\phi^3$ is

$$
\frac{1}{2}\frac{v^2}{e^2}A_ \mu^a A^{a\mu}\equiv  \frac{1}{2}m_ W^2 A^2,\quad a = 1,2
$$

- $A^3$ remains massless, it is the "photon" decoupled from $\phi^3$
- $\phi^3$ particle is electrically neutral.

For the total energy to be finite, it must be that at spatial infinity, the field configuration goes to a vacuum configuration fast enough:

$$
  \left\lvert \phi \right\rvert  \to v,\quad \left\lvert D_ \mu \phi \right\rvert ^2 \to 0, \quad A \to i \Omega \partial_ \mu\Omega^{-1}.
$$

Note that $\left\lvert D_ \mu \phi \right\rvert^2$ must drop to zero faster than $r^{-3/2}$ to make the total energy finite.

The topology of the space boundary is $\mathbb{S}^2$ since $\partial \mathbb{R}^3 = \mathbb{S}^2$. The vacuum manifold of the Higgs field is also $\mathbb{S}^2$, thus the Higgs field at $r \to \infty$ is a map $\mathbb{S}^2 \to \mathbb{S}^2$, which is classified by homotopy group $\pi_ 2(S^2) = \mathbb{Z}$, where $\mathbb{Z}$ is the addition group of integers. We can use homotopy to classify topologically different solutions, labeling any finite energy Higgs configuration by an integer $n$, which counts the winding number of Higgs field at infinity. Given a $\phi$ field configuration, Let $\hat{\phi}^{i} \equiv \phi^{i} / \left\lvert \phi \right\rvert$ be the unit field vector, the winding number is give by integrating the *pullback* of the volume in $\phi$ configuration space:

$$
\boxed{
  n = \frac{1}{8\pi}\epsilon_ {ijk} \epsilon_ {abc} \int d^2S_ i \, \hat{\phi}^{a}\partial_ {j} \hat{\phi}^{b}\partial_ {k} \hat{\phi}^{c}
  }
$$

The trivial vacuum where $\phi = \text{const}$ everywhere obviously has $n = 0$.

Consider the case where the winding number $n=1$. $\left\langle \phi \right\rangle$ at infinity depends on the direction. The residual U(1) symmetry of $SU(2)$ consists of the elements that commutes with $\left\langle \phi \right\rangle$, thus the unbroken $U(1)$ direction also depends on the position. Recall that $A_ \mu = A_ \mu^a T^a$ as a $\mathfrak{su}(2)$-valued field, the components of $A_ {\mu}$ that commutes with $\phi$ can be projected out (in any direction) via

$$
  a_ \mu = \frac{2}{v} \text{Tr }{\phi A_ \mu},
$$

for example, if $\phi = v T^3, \, a_ \mu = A_ \mu^3$.

The unbroken U(1) component can be regarded as a vector in the Lie-algebra whose direction, after choosing a vacuum $\phi_ {0}$, is parallel to $\phi_ {0}$. For example, if $\phi_ {0}$ is chosen to be $vT^3$, then the unbroken U(1) group is proportional to $T^3$. Again, in the case of a monopole solution, the U(1) direction is position-dependent.

Let's look at the covariant derivative. In order to make sure that $\left\lvert D_ \mu\phi \right\rvert^{2} = \left\lvert \partial_ \mu\phi-i[A_ \mu,\phi] \right\rvert^{2} \to 0$, we need to find a corresponding $A_ \mu$ that can cancel the $\partial_ \mu \phi$, for $\phi = v \hat{\phi}$. 

The following identities might be helpful:

$$
  \phi^2 = \phi^a T^a \phi^b T^b = \frac{1}{2}\phi^a\phi^b \left\lbrace  T^a ,T^b  \right\rbrace= \boxed{  \frac{v^2}{4}=\phi^{2}}.
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
 A_ \mu = -\frac{i}{v^2} [\partial_ \mu \phi,\phi]+\frac{a_ \mu}{v}\phi,
 }
$$

then

$$
  -i [A_ \mu,\phi] = - \partial_ \mu \phi,
$$

$a_ \mu$ above is the same as the unbroken U(1) field. We see that $A_ {\mu}$ is the asymptotic gauge field.

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

The Abelian projection involves fixing the gauge partially, such that only the maximal Abelian subgroup (Cartan subgroup) remains unbroken. Take $SU(3)$ QCD for example. The Lie algebra $\mathfrak{su}(3)$ consists of eight generators $T^a (a=1,…,8)$, corresponding to eight gluon fields $A_ \mu^a$. Its Cartan subgroup consists of diagonal elements that form a maximal Abelian subgroup:

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

## Decomposition into $\mathcal{A},\mathcal{C}$ and $X$

The Cho-Duan-Ge decomposition is a covariant separation of the gauge field into abelian and non-abelian components. Roughly speaking, the gauge potential is separated into
- abelian, restricted gauge potential. It is further separated into
	- topologically trivial part, or Maxwell part, or `neurons`. And
	- topological part, or Dirac part. Similar to the monopole scalar solution.
- valance gauge field which describes colored gluons, or `chromons`.

For the sake of simplicity we will begin with $SU(2)$. Take The $\mathfrak{g}$-valued gauge potential, let's decompose it to the abelian sub-algebra, namely the Cartan subalgebra, and the rest of the gauge field that is orthogonal to the Cartan component. Introduce a **right-handed orthonormal frame** $(\hat{n}^{1},\hat{n}^{2},\hat{n}^{3})$ with $\hat{n}^{i}\hat{n}^{i}=1$. Choose the third component to be the so-called abelian direction, denoted it by $\hat{n}:=\hat{n}^{3}$. This notation is a bit confusing, but it was used in the original papers. 

Next, let's put the vectors into Lie algebra space $\mathfrak{g}$, by assigning to each component $\hat{n}^{i}$ a basis $T^{a}\in\mathfrak{g}$, $T^{a} = \frac{\sigma^{a}}{2}$ for $SU(2)$. In order to follow the convention that fraktur letters denote $\mathfrak{g}$-valued stuff, let's write $\mathfrak{n}$ for the $\mathfrak{g}$-valued unit vector $\hat{n}$, i.e. $\mathfrak{n}:= \hat{n}^{i}T^{i}$. Now we can treat $\mathfrak{n}$ as a static adjoint field, and act the covariant derivative on $\mathfrak{n}$, just as how we act covariant derivative on $\mathfrak{g}$-valued scalar fields. Furthermore, similar to what we did at the presence of a monopole, we can decompose the gauge field into two parts, that satisfies $D_ {\mu}\mathfrak{n}=0$ and that does not. With the help of the following matrix identities:

$$
\mathfrak{n}^{2}=\mathfrak{n}\cdot \mathfrak{n}=\hat{n}^{a}\hat{n}^{b}T^{a}T^{b}=\frac{1}{4}\mathbb{1}_ {2},\quad  T:=\frac{1}{2}\sigma
$$

and consequently

$$
\partial \mathfrak{n}^{2}=0=(\partial \mathfrak{n})\mathfrak{n}+\mathfrak{n}\partial \mathfrak{n}\implies \partial \mathfrak{n} \mathfrak{n} = -\mathfrak{n}\partial \mathfrak{n},
$$

we can solve the $\mathfrak{g}$-valued equation $D_ {\mu}\mathfrak{n}=0$ for $A_ {\mu}$, like we did for the $SU(2)$ monopole in the previous chapter. Expand the covariant derivative,

$$
D_ {\mu}\mathfrak{n} = (\partial_ {\mu}-ig[A,-])\mathfrak{n} = \partial_ {\mu}\mathfrak{n}-ig[A_ {\mu},\mathfrak{n}]=0,
$$

the solution comprises of the abelian part that is proportional to $\mathfrak{n}$, and the non-abelian part that is perpendicular to $\mathfrak{n}$. We have the identity 

$$
[[\partial_ {\mu}\mathfrak{n},\mathfrak{n}],\mathfrak{n}] = \partial_ {\mu}\mathfrak{n},
$$

thus the non-trivial part of the solution for $A_ {\mu}$, call it $\mathcal{C}_ {\mu}$, reads 

$$
\boxed{ 
\mathcal{C}_ {\mu} = \frac{i}{g} [\mathfrak{n},\partial_ {\mu} \mathfrak{n}] .
}
$$

This is a $\mathfrak{g}$-valued quantity, in basis $T^{a}$ it can be written as a cross product between 3-vectors, 

$$
\boxed{ 
\mathcal{C}_ {\mu} = - \frac{1}{g} \hat{n} \times (\partial_ {\mu}\hat{n}) \text{ in }\mathfrak{g} .
}
$$

Given a solution for $A$, we can add to it any thing proportional to $\mathfrak{n}$ and it still is a solution, since the commutator gives the same result, hence the solutions contains a trivial part that is proportional to $\mathfrak{n}$, call it $\mathcal{A}$: 

$$
\boxed{ 
\mathcal{A}_ {\mu} =  a_ {\mu} \mathfrak{n},\quad a_ {\mu}\in \mathbb{R}.
}
$$

Put together, the total solution $\hat{A}$ is called the `restricted gauge field` or `restricted gauge potential`, 

$$
\hat{A}=\mathcal{A}+\mathcal{C}, \quad \mathcal{A} = a \mathfrak{n}\text{ and }\mathcal{C}=\frac{i}{g}[\mathfrak{n},\partial \mathfrak{n}], 
$$

where we have omitted the spacetime index $\mu$, it can be put back whenever needed. 

If the symmetry is broken to the subgroup $N$ induced by $\mathfrak{n}$, then $\mathcal{A}$ corresponds to the massless $U(1)$ component that can propagate for long distance. Geometrically, $\hat{A}$ is the component of the connection that leaves $\mathfrak{n}$ invariant during parallel transport. 

One way to remember that $\mathcal{C}$ comes with a factor of $1/g$ is that, it resembles the topological soliton solution such as the monopole, which always comes with a factor of $1/g$. 

- - -

Next we carry on to study the field strength $\hat{F}$ corresponding to the restricted field $\hat{A}$. We can see that $\hat{F}$ is proportional to $\mathfrak{n}$, since from $D_ {\mu}\mathfrak{n}=0$ we have

$$
[\hat{D}_ {\mu},\hat{D}_ {\nu}]\mathfrak{n} =-\frac{i}{g}[\hat{F}_ {\mu \nu},\mathfrak{n} ]=0,
$$

where $\hat{D}_ {\mu}$ is the covariant derivative with respect to $\hat{A}$, $\hat{D}=\partial-ig[\hat{A},-]$. This means that $\hat{F}$ must be proportional to $\mathfrak{n}$. 

The following identities are helpful (hold for $SU(2)$):

$$
\begin{align*}
\mathfrak{n} \mathfrak{n} = \hat{n}^{a}\hat{n}^{b}\frac{1}{2}\sigma^{a} \frac{1}{2}\sigma^{b} &= \frac{1}{4}\mathbb{1}_ {2}, \\
[\mathfrak{n} ,[\mathfrak{n} ,\partial_ {\mu}\mathfrak{n} ]] &= \partial_ {\mu}\mathfrak{n}, \\
[[\mathfrak{n},\partial_ {\nu}\mathfrak{n}  ],[\mathfrak{n} ,\partial_ {\mu}\mathfrak{n} ]] &= - \partial_ {\nu}\mathfrak{n} \partial_ {\mu}\mathfrak{n} .
\end{align*}
$$

We have 

$$
\begin{align*}
\hat{F}:= & \partial_ {\mu}\hat{A}_ {\nu}-\partial_ {\nu}\hat{A}_ {\mu}-ig[\hat{A}_ {\mu},\hat{A}_ {\nu}]\\
=& (\partial_ {\mu}a_ {\nu}-\partial_ {\nu}a_ {\mu})\mathfrak{n} + \frac{i}{g}[\partial_ {\mu}\mathfrak{n} ,\partial_ {\nu}\mathfrak{n} ]\\
=&: f_ {\mu \nu}\mathfrak{n} +H_ {\mu \nu}\mathfrak{n} .
\end{align*}
$$

It is not obvious that $[\partial_ {\mu}\mathfrak{n},\partial_ {\nu}\mathfrak{n}]$ is proportional to $\mathfrak{n}$. But after some derivation we find 

$$
[\partial_ {\mu}\mathfrak{n},\partial_ {\nu}\mathfrak{n}] = -(\partial_ {\mu}\hat{n})^{a}(\partial_ {\nu}\hat{n})^{b}\epsilon^{abc}T^{c},
$$

which in $\mathfrak{g}$ is just $-(\partial_ {\mu}\hat{n})\times(\partial_ {\nu}\hat{n})$. Since $\partial \hat{n}$ is orthogonal to $\hat{n}$, their cross product is aligned with $\hat{n}$. So indeed $\hat{F}$ is aligned with $\mathfrak{n}$. 

$H_ {\mu \nu}\mathfrak{n}$ is in matrix form, if we want to "project out" the components $H_ {\mu \nu}$, we can write 

$$
H_ {\mu \nu} \mathfrak{n}  =\frac{1}{g} \partial_ {\mu} (i\mathfrak{n} \partial_ {\nu} \mathfrak{n}) -(\mu \leftrightarrow \nu),
$$

This form is similar to $F_ {\mu \nu}=\partial_ {\mu}A_ {\mu}-(\mu\leftrightarrow \nu)$. In fact, in the case of $SU(2)$, we can simplify it further to give an explicit expression for $H_ {\mu \nu}$ (without $\mathfrak{n}$). The final expression will be in terms of $\hat{n}_ {1,2}$. Recall that $\hat{n}_ {1}, \hat{n}_ {2}, \hat{n}$ form a right-handed orthogonal basis, let $\mathfrak{n}_ {1,2}$ be the $\mathfrak{g}$-valued counterparts of $\hat{n}_ {1,2}$. It is easily verified that 

$$
[\mathfrak{n}_ {i},\mathfrak{n} _ {j}] = i\epsilon^{ijk}\mathfrak{n}_ {k} .
$$

Since $\partial \hat{n}$ is perpendicular to $\hat{n}$ (since $\hat{n}$ has fixed length), $\partial \hat{n}=(\cdots)\hat{n}_ {1}+(\cdots)\hat{n}_ {2}$. In $\mathfrak{g}$-space we have the same. Write 

$$
\begin{align*}
\partial_ {\mu}\mathfrak{n}  =& k_ {1}\mathfrak{n} _ {1}+k_ {2}\mathfrak{n} _ {2}, \\
\partial_ {\nu}\mathfrak{n} =& k'_ {1}\mathfrak{n} _ {1}+k'_ {2}\mathfrak{n} _ {2}, 
\end{align*}
$$

then 

$$
H_ {\mu \nu}\mathfrak{n}  = (k_ {2}k_ {1}'-k_ {1}k_ {2}')\mathfrak{n},
$$

where $k_ {1}k_ {2}'$ is actually the $\mu \longleftrightarrow\nu$ replaced $k_ {2}k_ {1}'$. What are the $k$'s? Well, we can project them from $\partial \mathfrak{n}$, giving 

$$
\begin{align*}
k_ {1} =& \hat{n}_ {1} \cdot (\partial_ {\mu}\hat{n}) = \hat{n}_ {1}\cdot\partial_ {\mu}(\hat{n}_ {1}\times \hat{n}_ {2}) = \hat{n}_ {1}\cdot (\partial_ {\mu}\hat{n}_ {1}\times \hat{n}_ {2}), \\
k_ {2} =& \hat{n}_ {2}\cdot(\partial_ {\mu} \hat{n}) = \hat{n}_ {2}\cdot \partial_ {\mu} (\hat{n}_ {1} \times \hat{n}_ {2}) = \hat{n}_ {2}\cdot(\hat{n}_ {1}\times  \partial_ {\mu}\hat{n}_ {2}).
\end{align*}
$$

Note the change of notation between $\hat{n}$ and $\mathfrak{n}$. The expression for $k'$ is just that of $k$ but with $\mu$ and $\nu$ interchanged. Then,

$$
\begin{align*}
k_ {2}k_ {1}' =& \hat{n}_ {2}\cdot( \partial_ {\mu}\hat{n}) \; \hat{n}_ {1}\cdot(\partial_ {\nu}\hat{n})\\
=& (\partial_ {\mu }\hat{n}_ {2})\cdot \hat{n} \; (\partial_ {\nu}\hat{n}_ {1})\cdot \hat{n},
\end{align*}
$$

in the last line we have exploited the fact that $\hat{n}_ {1,2}$ and $\hat{n}$ are orthodox. Since $\hat{n}_ {2}$ has unit length, its derivative is orthodox to itself, 

$$
\partial_ {\mu}\hat{n}_ {2} = (\cdots) \hat{n}_ {1} + (\cdots)\hat{n}.
$$

Similarly for $\partial_ {\nu}\hat{n}_ {1}$. Then, since $\hat{n}_ {1}$ is orthodox to $\hat{n}_ {2}$, we have 

$$
\begin{align*}
k_ {2}k_ {1}'=& (\partial_ {\mu }\hat{n}_ {2})\cdot \hat{n} \; (\partial_ {\nu}\hat{n}_ {1})\cdot \hat{n}\\
=& (\partial_ {\mu}\hat{n}_ {2})\cdot(\partial_ {\nu}\hat{n}_ {1}).
\end{align*}
$$

As a result, 

$$
\begin{align*}
H_ {\mu \nu} &= \frac{1}{g}(\partial_ {\mu}\hat{n}_ {2})\cdot(\partial_ {\nu}\hat{n}_ {1}) - (\mu \leftrightarrow \nu) \\
&=\frac{1}{g} \partial_ {\mu} (\hat{n}_ {2}\cdot\partial_ {\nu}\hat{n}_ {1}) - (\mu\leftrightarrow \nu)\\
&=: \partial_ {\mu} C_ {\nu} - \partial_ {\nu} C_ {\mu}.
\end{align*}
$$

where 

$$
C_ {\mu} := \frac{1}{g} \hat{n}_ {2} \cdot \partial_ {\mu} \hat{n}_ {1}.
$$

In summary, we have 

$$
\begin{align*}
\hat{F} &= f_ {\mu \nu}\mathfrak{n} +H_ {\mu \nu}\mathfrak{n} ,\\
f_ {\mu \nu} &= \partial_ {\mu}a_ {\nu}-\partial_ {\nu}a_ {\mu},\\
H_ {\mu \nu} \mathfrak{n}  &=\frac{i}{g} [\partial_ {\mu}\mathfrak{n} ,\partial_ {\nu}\mathfrak{n} ],\\
H_ {\mu \nu} &= \partial_ {\mu}C_ {\nu}-\partial_ {\nu}C_ {\mu}, \; C_ {\mu}:= \frac{1}{g}\hat{n}_ {2}\cdot \partial_ {\mu}\hat{n}_ {1}.
\end{align*}
$$

- - -

We have talked about the monopole-like background $\mathcal{C}$ and the $U(1)$ field $\mathcal{A}$. The rest of the total $SU(N)$ gauge field can be symbolically denoted as $X$, thus we can separate the total gauge field $A$ into the following three parts, 

$$
A = \mathcal{A}+\mathcal{C}+X, \quad  [X,\mathfrak{n} ]\neq0
$$

where 

- $A$ is the total $SU(N)$ field. This is sometimes denoted $\vec{A}$ when the gauge group is $SU(2)$.
- $\mathcal{A}$ is the free, massless $U(1)$ gauge field, so-called neuron.
- $\mathcal{C}$ is the monopole-like background field defined(fixed) by $\hat{n}$, where $\hat{n}$ for example can be chosen as the hedgehog-form, similar to the monopole field configuration. Possible singularity points are allowed. It do not fluctuated and has no dynamics.
- $X$ is the rest of $A$. I'd like to think of it as the non-abelian fluctuation about the background $\mathcal{C}$, but of course this is only a perturbative perspective.

- - -

$\hat{n}$ may not be globally defined. Let $\hat{n}_ {\infty}$ be the asymptotic field configuration at the spatial boundary $\partial\mathbb{R}^{3}=\mathbb{S}^{2}$. Since $\hat{n}$ takes value in all unit-norm vectors in all directions, the collection of all $\hat{n}$ is homeomorphic to $\mathbb{S}^{2}$, think of it as the set of the end points of all possible $\hat{n}$. Thus,

$$
\hat{n}_ {\infty}: \mathbb{S}^{2} \to  \mathbb{S}^{2}.
$$

If the winding number of $\hat{n}_ {\infty}$ is nonzero, then it can not be continuously deformed into a unit map. Then $\hat{n}$ can not be well-defined everywhere, there must be at least one singularity, where the direction of $\hat{n}$ is not defined. If $\hat{n}$ were a scalar field, we usually let it go to zero to avoid this problem, like with vortices. 

## Gauge transformation

If we fix the $\mathfrak{n}(x)$ field, then gauge group is broken to $SU(2)\to U(1)$, where $U(1)$ is the little group of $\mathfrak{n}(x)$, which depends on the position $x$. The unbroken $U(1)$ symmetry corresponds to the massless "photon" that survives at long distance. What if we do not fix $\mathfrak{n}(x)$, and allow it to gauge-transform freely? Then, under gauge transformation $\mathfrak{n}$ will rotate in a $x$-dependent way. 

To keep our notation in agree with others, let's denote the gauge transformation matrix as $\Omega=e^{ i\alpha }$, where $\alpha=\alpha^{a}T^{a}$ is a $\mathfrak{g}$-valued **infinitesimal** vector. The gauge field $A$ transforms as 

$$
A \to A+ \frac{1}{g} D\alpha,\quad  D_ {\mu}=\partial_ {\mu}-ig[A_ {\mu},-].
$$

What about $\mathfrak{n}=\hat{n}^{a}T^{a}$? This $\mathfrak{g}$-valued field is not a part of the original Yang-Mills Lagrangian so it is not clear how it should transform under gauge transform, or if it should transform at all. For example at the beginning I thought that since $\hat{n}$ is a vector in physical space, why should it be affected by gauge transformation? Then again, since $\mathfrak{n}$ plays a similar rule to the Higgs boson, maybe it should transform as an adjoint scalar. That is what was adopted by Cho and other people, so I'll stick to it. 

The Higgs-like field $\mathfrak{n}$ transforms under an infinitesimal gauge transformation as

$$
\mathfrak{n}  \to  \mathfrak{n} +i[\alpha,\mathfrak{n} ] = \mathfrak{n} -\vec{\alpha}\times \hat{n}{\Large\mid}_ {\mathfrak{g} }.
$$

The notation $\vec{\alpha}\times \hat{n}{\Large\mid}_ {\mathfrak{g}}$ means that $\vec{\alpha}\times \hat{n}$ is a vector in Lie algebra.

- - -

The background $\mathcal{C}$ together with $\mathcal{A}$ constitute the so-called restricted gauge field $\hat{A}$ that is bonded to the field $\mathfrak{n}$, in the sense that $\hat{A}$ is given by the solution of $D\mathfrak{n}=0$. After a gauge transformation, $\mathfrak{n}\to\mathfrak{n}'$ and $\hat{A}\to\hat{A}'$, but we would like the equation to hold independent of the gauge transformation, that is, after an arbitrary gauge transformation we want

$$
D'\mathfrak{n} ' := (\partial-ig [\hat{A}',-])\,\mathfrak{n}' =\partial \mathfrak{n}' -ig [\hat{A}',\mathfrak{n}' ]=0.
$$

This is guaranteed if we set $\hat{A}$ to transform as a regular gauge field

$$
\hat{A}\to \hat{A}'=\Omega\left( \hat{A}+\frac{i}{g}\partial \right)\Omega ^{\dagger}.
$$

while let $\mathfrak{n}$ transform as a adjoint scalar, $$
\mathfrak{n}  =\to  \mathfrak{n'=\Omega \mathfrak{n} }  \Omega ^{\dagger}.
$$
Now, as we wanted, $\hat{A}$ is the solution to $\mathcal{D}_ {\mu}\mathfrak{n}=0$ in a **gauge independent** way: If $\hat{A}$ is a solution, after gauge transform, the transformed field $\hat{A}'$ still is a solution to $D'_ {\mu}\mathfrak{n}'=0$.

We also would like the decomposition of $\hat{A}$ to be gauge independent, that is after gauge transformation

$$
\hat{A}' = \mathcal{A}'  + \mathcal{C}'.
$$

Let's focus on $\mathcal{A}$ first. It is the $\mathfrak{n}$-direction projection of $\hat{A}$, that is

$$
\mathcal{A}=a\mathfrak{n} , \quad A = 2\mathrm{Tr}\,(\mathfrak{n} \hat{A}) \equiv \hat{n} \cdot \hat{A},
$$

the factor of $2$ is due to the normalization $\mathrm{Tr}\,T^{a}T^{b}=\frac{1}{2}\delta^{ab}$. **This should be treated as the definition of $\mathcal{a}$, and this definition better be gauge independent**, hence after gauge transformation we want

$$
\mathcal{a}'=2\mathrm{Tr}\,(\mathfrak{n} '\hat{A}').
$$

This will fix the gauge transformation rule for $\mathcal{A}$. We have 

$$
a' = a + \frac{2i}{g}\mathrm{Tr}\,\left\lbrace \mathfrak{n} \partial U^{\dagger}U \right\rbrace .
$$

Let the gauge transformation be given by $\Omega=e^{ i\alpha }$ where $\alpha=\alpha^{a}T^{a}$, then the infinitesimal form reads

$$
a \to \mathcal{A}' = a+\frac{2}{g}\mathrm{Tr}\,(\mathfrak{n}\partial \alpha )\equiv a + \frac{1}{g}\hat{n}\cdot \partial \vec{\alpha}.
$$

Note that it is no longer a total derivative, but the projection of a total derivative in $\hat{n}$ direction. It is not simply

$$
\mathcal{A}\to \Omega \mathcal{A}\Omega ^{\dagger},\quad \mathcal{C}\to \Omega(\mathcal{C}+i\partial)\Omega ^{\dagger}.
$$

- - -

To determine the gauge transform of $\mathcal{C}$, starting from the definition: 

$$
\mathcal{C} = \frac{i}{g} [\mathfrak{n} ,\partial \mathfrak{n} ] = \frac{2i}{g} \mathfrak{n}  \partial \mathfrak{n}. 
$$

Under a gauge transform, $\mathfrak{n}\to \mathfrak{n}'=\Omega \mathfrak{n}\Omega ^{\dagger}$, consequently the transform of $\mathcal{C}$ in terms of $\mathfrak{n}$ should be

$$
g\mathcal{C} \to g\mathcal{C}'=2i \mathfrak{n}' \partial (\mathfrak{n}') = 2i\Omega \mathfrak{n} \Omega ^{\dagger}\partial(\Omega \mathfrak{n}  \Omega ^{\dagger}).
$$

Note that the right-hand-side of the above equation is only equal to $\Omega(\mathcal{C}+i\partial)\Omega ^{\dagger}$ when they are both under a trace, otherwise they are not equal to each other. 

Regarding $X$ in $A = \mathcal{A}+\mathcal{C}+X$. $X$ also transforms as a adjoint scalar,

$$
X\to \Omega X \Omega ^{\dagger}.
$$

How the field transforms tells us what gauge invariant terms we could construct to be included into the Lagrangian, for instance, we know that $\left\lvert D_ {\mu}X \right\rvert^{2}$ is gauge invariant, so they could appear in the Lagrangian. 

- - -

Another possible gauge symmetry reads

$$
\begin{align*}
\delta \hat{n} &=0, \quad \delta A_ {\mu} = \frac{1}{g} \hat{n}\cdot D_ {\mu}\vec{\alpha},\\
\delta \hat{A}_ {\mu} &= \frac{1}{g}(\hat{n}\cdot D_ {\mu}\hat{\alpha})\hat{n},\\
\delta \vec{X}_ {\mu} &= \frac{1}{g}[D_ {\mu}\vec{\alpha}-(\hat{n}\cdot D_ {\mu} \vec{\alpha})\hat{n}],
\end{align*}
$$

where $A_ {\mu}:=\hat{n}\cdot \vec{A}_ {\mu}$. 

In general, given an arbitrary $\hat{n}$, there exists different decomposition of gauge transformation that preserves the defining equation $D\mathfrak{n}=0$ besides the standard one. 

- - -

The `generalized Lorentz gauge` condition is defined to be 

$$
\partial_ {\mu}\hat{A}_ {\mu}=0,
$$

substitute the definition $\hat{A}=\mathcal{A}+\mathcal{C}$, we have 

$$
\begin{align*}
(\partial_ {\mu} a_ {\mu} )\mathfrak{n} =& 0 , \\
a_ {\mu} \partial_ {\mu}\mathfrak{n} +i[\mathfrak{n} ,\partial^{2}\mathfrak{n} ]=&0.
\end{align*}
$$


## Lagrangian of Restricted and Extended QCD

The `restricted QCD`, `RCD` for short, is the self-energy of restricted gauge field $\hat{A}$, 

$$
\mathcal{L}_ {\text{RCD}} = - \frac{1}{2} \mathrm{Tr}\,\hat{F}_ {\mu \nu}^{2}.
$$

Substitute in 

$$
\begin{align*}
\hat{F} &= f_ {\mu \nu}\mathfrak{n} +H_ {\mu \nu}\mathfrak{n} ,\\
f_ {\mu \nu} &= \partial_ {\mu}a_ {\nu}-\partial_ {\nu}a_ {\mu},\\
H_ {\mu \nu} \mathfrak{n}  &=\frac{i}{g} [\partial_ {\mu}\mathfrak{n} ,\partial_ {\nu}\mathfrak{n} ].
\end{align*}
$$

we have 

$$
\begin{align*}
\mathcal{L}_ {\text{RCD}} =& - \frac{1}{4}f_ {\mu \nu}^{2} - \frac{1}{2}\mathrm{Tr}\,H^{2} - \mathrm{Tr}\,f_ {\mu \nu}H^{\mu \nu}\\
=& - \frac{1}{4} (\partial_ {\mu}a_ {\nu}-\partial_ {\nu}a_ {\mu})^{2}\\
& - \frac{1}{4g^{2}}(\partial_ {\mu}\hat{n}\times \partial_ {\nu}\hat{n})^{2}\\
&+ \frac{1}{2g} \epsilon^{abc}f_ {\mu \nu}\hat{n}^{a}\partial^{\mu}\hat{n}^{b}\partial^{\nu}\hat{n}^{c}
\end{align*}.
$$

OK, now let's include the final piece, the non-abelian fluctuation $X$. The total field strength $F_ {\mu \nu}$ is 

$$
\boxed{ 
F_ {\mu \nu} = \hat{F}_ {\mu \nu}+\hat{D}_ {\mu}X_ {\nu}-\hat{D}_ {\nu}X_ {\mu}-ig [X_ {\mu},X_ {\nu}].
}
$$

Substitute the above expression into the total gauge potential $-\frac{1}{2}\mathrm{Tr}\,F^{2}$, we get what Cho (and probably other people) call Extended QCD, ECD for short. However it is just the SU(2) Yang-Mills theory, separated into different components. 

To simplify the extended QCD Lagrangian, recall that $\mathfrak{n}$ is orthogonal to $X$ by construction, namely $\mathrm{Tr}\,\mathfrak{n}X_ {\mu}=0$ for all $\mu$, then we have 

$$
\partial \mathrm{Tr}\,\mathfrak{n} X=0=\mathrm{Tr}\,(\partial \mathfrak{n} X+\mathfrak{n} \partial X)\implies \mathrm{Tr}\,\partial \mathfrak{n} X=-\mathrm{Tr}\,\mathfrak{n}\partial X. 
$$

Note that this "exchange the derivative and change the sign" operation is only valid under the trace. 

Also take into consideration the cyclic property of trace, we can simplify the following term:

$$
\begin{align*}
\mathrm{Tr}\,\left\lbrace \hat{F}_ {\mu \nu} \hat{D}_ {\mu}X_ {\nu} \right\rbrace =& (f_ {\mu \nu}+H_ {\mu \nu}) \mathrm{Tr}\,\left\lbrace \mathfrak{n}(\partial_ {\mu}X_ {\nu}-ig [\hat{A}_ {\mu},X_ {\nu}])  \right\rbrace \\
=& (f_ {\mu \nu}+H_ {\mu \nu}) \mathrm{Tr}\,\left\lbrace \mathfrak{n} \partial_ {\mu}X_ {\nu}-\mathfrak{n} ig (\hat{A}_ {\mu}X_ {\nu}-X_ {\nu}\hat{A}_ {\mu}) \right\rbrace \\
=& (f_ {\mu \nu}+H_ {\mu \nu})\mathrm{Tr}\,\left\lbrace -\partial_ {\mu}\mathfrak{n}X_ {\nu} -ig\mathfrak{n} \hat{A}_ {\mu}X_ {\nu}+ig\mathfrak{n} X_ {\nu}\hat{A}_ {\mu} \right\rbrace \\
=& (f_ {\mu \nu}+H_ {\mu \nu})\mathrm{Tr}\,\left\lbrace -(\partial_ {\mu}\mathfrak{n} X_ {\nu} -ig \hat{A}_ {\mu}\mathfrak{n} X_ {\nu}+ig \mathfrak{n} \hat{A}_ {\mu}X_ {\nu})\right\rbrace \\
=& (f_ {\mu \nu}+H_ {\mu \nu})\mathrm{Tr}\,\left\lbrace -(\partial_ {\mu}\mathfrak{n} -ig (\hat{A}_ {\mu}\mathfrak{n} -\mathfrak{n} \hat{A}_ {\mu})X_ {\nu}) \right\rbrace \\
=& (f_ {\mu \nu}+H_ {\mu \nu})\mathrm{Tr}\,\left\lbrace -(\partial_ {\mu}\mathfrak{n} -ig[\hat{A}_ {\mu},\mathfrak{n} ])X_ {\nu} \right\rbrace \\
=&(f_ {\mu \nu}+H_ {\mu \nu}) \mathrm{Tr}\,\left\lbrace -(\hat{D}_ {\mu}\mathfrak{n} )X_ {\nu} \right\rbrace \\
=&0.
\end{align*}
$$

This holds for not only $\hat{F}$ but really anything that is proportional to $\mathfrak{n}$, which certainly includes the term proportional to $\mathrm{Tr}\,\left\lbrace [X_ {\mu},X_ {\nu}]\hat{D}X \right\rbrace$.

With this great simplification, the extended Lagrangian reads

$$
\begin{align*}
\mathcal{L}_ {\text{ECD}} =& - \frac{1}{2}\mathrm{Tr}\,F^{2} \\
=& - \frac{1}{2}\mathrm{Tr}\,\left\lbrace \hat{F}^{2}-2ig \hat{F}_ {\mu \nu}[X_ {\mu},X_ {\nu}]+(\hat{D}_ {\mu}X_ {\nu}-\hat{D}_ {\nu}X_ {\mu})^{2}  -g^{2} [X_ {\mu},X_ {\nu}]^{2}\   \right\rbrace. 
\end{align*}
$$

In $SU(2)$, the Lie-algebra space is a three dimensional vector space, since $X_ {\mu}$ is orthogonal to $\hat{n}$, $X_ {\mu}\times X_ {\nu}$ is aligned with $\hat{n}$. In terms of matrices, $[X_ {\mu},X_ {\nu}]\propto \mathfrak{n}$. Thus we can separate the $\mathfrak{n}$-factor from the commutator and define $X_ {\mu \nu}$ as 

$$
\boxed{ 
X_ {\mu \nu} \mathfrak{n} := -ig [X_ {\mu},X_ {\nu}],
}
$$

then the Lagrangian reads

$$
\boxed{ 
\begin{align*}
\mathcal{L}_ {\text{ECD}} =& - \frac{1}{2}\mathrm{Tr}\,\left\lbrace (\hat{F}+X_ {\mu \nu}\mathfrak{n} )^{2}+(\hat{D}_ {\mu}X_ {\nu}- \mu\leftrightarrow \nu)^{2} \right\rbrace \\
=& - \frac{1}{4}[(f_ {\mu \nu}+H_ {\mu \nu}+X_ {\mu \nu})^{2}+(\hat{D}_ {\mu}\vec{X}_ {\nu}-\mu \leftrightarrow \nu)^{2}]
\end{align*}
}
$$

where we have used the convention in Schwartz's QFT textbook that we do not distinct the upper indices and lower indices when summed. In the second line we have got ridden of the trace sign. Recall that 

$$
(\hat{D}\vec{X})^{i} = \partial X^{i} +\epsilon^{ijk}\hat{A}^{j}X^{k}.
$$

## Equations of Motion

The Euler-Lagrange equation for $a_ {\mu}$ reads 

$$
\frac{ \partial \mathcal{L} }{ \partial a_ {\mu} }  = \partial_ {\nu} \frac{ \partial \mathcal{L} }{ \partial(\partial_ {\nu}a_ {\mu}) } .
$$

We have 

$$
\begin{align*}
-2\frac{ \partial \mathcal{L} }{ \partial a_ {\mu} }  =& -2ig \mathrm{Tr}\,\left\lbrace [\mathfrak{n} ,X_ {\nu}](\hat{D}_ {\mu}X_ {\nu}-\hat{D}_ {\nu}X_ {\mu}) \right\rbrace \\
=& g \hat{n}\cdot(\vec{X}_ {\nu}\times \hat{D}_ {\mu}\vec{X}_ {\nu}) - g\hat{n}\cdot(\vec{X}_ {\nu}\times \hat{D}_ {\nu}\vec{X}_ {\mu}),
\end{align*}
$$

where $\hat{D}_ {\mu}\vec{X}_ {\nu} =(\hat{D}_ {\mu}X_ {\nu})^{a}T^{a}$, $T^{a}$ is the generator (basis) of $\mathfrak{su}(2)$. The right-hand side of the Euler-Lagrange equation reads

$$
\begin{align*}
-2\partial_ {\nu}\frac{ \partial \mathcal{L} }{ \partial(\partial_ {\nu}a_ {\mu})  } 
=& \frac{1}{4} \mathrm{Tr}\,\left\lbrace \frac{ \partial  }{ \partial(\partial_ {\nu}a_ {\mu}) } (f_ {\alpha \beta}+H_ {\alpha \beta}+X_ {\alpha \beta})^{2} \mathbb{1}_ {2\times 2} \right\rbrace    \\
=& \partial_ {\nu}(f_ {\nu \mu}+H_ {\nu \mu}+X_ {\nu \mu}).
\end{align*}
$$

Putting them together we get the equation of motion for $a_ {\mu}$:

$$
\boxed{ 
\begin{align*}
\partial_ {\mu}(f_ {\mu \nu}+H_ {\mu \nu}+X_ {\mu \nu}) 
&= g\hat{n}\cdot(\vec{X}_ {\mu}\times \hat{D}_ {\nu}\vec{X}_ {\mu}) - g\hat{n}\cdot(\vec{X}_ {\mu}\times \hat{D}_ {\mu}\vec{X}_ {\nu})\\
&= -g\hat{n}\cdot [\vec{X}_ {\mu}\times (\hat{D}_ {\mu}\vec{X}_ {\nu}-\hat{D}_ {\nu}\vec{X}_ {\mu})].
\end{align*}
}
$$

When $a_ {\mu}=0$, we have

$$

$$

- - -

Next we move on to the equation of motion for $X^{i}_ {\mu}$. To simplify the notation let's temporarily define part of $F_ {\mu \nu}$ to be $\Gamma_ {\mu \nu}$ (since notational-wise $\Gamma$ is written as part of $F$ ):

$$
\boxed{
\Gamma_ {\mu \nu} := f_ {\mu \nu} + H_ {\mu \nu} + X_ {\mu \nu}, \quad  F = \Gamma \mathfrak{n} +\hat{D}X-\hat{D}X.
} 
$$

We have 

$$
\begin{align*}
-2 \frac{ \partial \mathcal{L} }{ \partial X^{i}_ {\alpha} }  
=& \mathrm{Tr}\,\left\lbrace 2\Gamma_ {\mu \nu}\mathfrak{n}(-ig)\frac{ \partial  }{ \partial X_ {\alpha}^{i} } [X_ {\mu},X_ {\nu}] + 2g\hat{D}_ {\mu}X_ {\nu} (\pi)\frac{ \partial  }{ \partial X^{i}_ {\alpha} } [\hat{A},X_ {\nu}] \right\rbrace  \\
=& g(\Gamma_ {\alpha \nu}X_ {\nu}^{j}-\Gamma_ {\mu \alpha}X_ {\mu}^{j})\epsilon^{ijk}\hat{n}^{k} - g\epsilon^{ijk}\hat{A}^{j}(\hat{D}_ {\mu}X_ {\alpha})^{k}\\
=& 2g(\Gamma_ {\alpha \mu} X_ {\mu}^{j}\hat{n}^{k}\epsilon^{ijk}) + 2g\epsilon^{ijk}\hat{A}_ {\mu}^{j}(\hat{D}_ {\alpha}X_ {\mu}-\hat{D}_ {\mu}X_ {\alpha})^{k},
\end{align*}
$$

where since $\hat{A} = \mathcal{A}+\mathcal{C}$ is proportional to $\mathfrak{n}$, we have $\hat{A}^{i} = a \hat{n}^{i}+C\hat{n}^{i}$, where $\mathcal{C} =:C\mathfrak{n}$, namely $C$ is the component in $\mathfrak{n}$ direction of script C.

We have 

$$
-2 \partial_ {\beta}\frac{ \partial \mathcal{L} }{ \partial (\partial_ {\beta}X_ {\alpha}^{i})  }  = 2\partial_ {\beta}((\hat{D}_ {\beta}X_ {\alpha})^{i} - (\hat{D}_ {\alpha}X_ {\beta})^{i}).
$$

Put everything together, we have 

$$
g\epsilon^{ijk}(f_ {\alpha \mu}+H_ {\alpha \mu}+X_ {\alpha \mu})X_ {\mu}^{j}\hat{n}^{k} = \partial_ {\mu}(\hat{D}_ {\mu}X_ {\alpha}-\hat{D}_ {\alpha}X_ {\mu})^{i} + g\epsilon^{ijk}\hat{A}_ {\mu}^{j}(\hat{D}_ {\mu}X_ {\alpha}-\hat{D}_ {\alpha}X_ {\mu})^{k}.
$$

In a more concise notation we could also write the right hand side as the $i$-th component of $\hat{D}_ {\mu}(\hat{D}_ {\mu}X_ {\alpha}-\hat{D}_ {\alpha}X_ {\mu})$. Or equivalently

$$
\hat{D}_ {\mu}(\hat{D}_ {\mu}\vec{X}_ {\alpha}-\hat{D}_ {\alpha}\vec{X}_ {\mu}) = g (f_ {\alpha \mu}+H_ {\alpha \mu}+X_ {\alpha \mu})\vec{X}_ {\mu} \times \hat{n} 
$$

- - -

## Complex gauge field $\chi$

We will use two different notations for indices associated to different basis, to be specific we will adopt Greek indices in parenthesis with basis $\hat{n}$：

$$
\vec{X} = X^{i} T^{i} = X^{(\alpha)}\hat{n}_ {\alpha},
$$

where the Greek letters take value in only $\left\lbrace 1,2 \right\rbrace$, since in terms of $\hat{n}_ {i}$, $X$ only has $\hat{n}_ {1}$ and $\hat{n}_ {2}$ components. Write 

$$
X_ {\mu} = X_ {\mu}^{(1)} \mathfrak{n}_ {1}  + X_ {\mu}^{(2)}\mathfrak{n}_ {2}, \text{ where }  \mathfrak{n}_ {1,2} := \hat{n}_ {1,2}\cdot \vec{T}.
$$

Define

$$
\chi_ {\mu} :=  \frac{1}{\sqrt{2}}(X_ {\mu}^{(1)}+iX_ {\mu}^{(2)}),
$$

then 

$$
X^{(1)} = \frac{1}{\sqrt{2}} (\chi + \chi ^\ast ),\quad  X^{(2)} = \frac{1}{i\sqrt{2}}(\chi-\chi ^\ast )
$$

and

$$
X_ {\mu \nu} = X_ {\mu}^{(1)}X_ {\nu}^{(2)}-X_ {\nu}^{(1)}X_ {\mu}^{(2)} = i(\chi_ {\mu}\chi_ {\nu}^\ast-\chi_ {\mu}^\ast \chi_ {\nu}) .
$$

To rewrite the Lagrangian in terms of $\chi$, we also need to express $\hat{D}_ {\mu}X_ {\nu}-(\mu \leftrightarrow \nu)$ in $\chi$. It is more convenient to adopt the following expression in vector notation,

$$
\hat{D} \vec{X} = \partial_ {\mu}\vec{X} + g\hat{A}\times \vec{X}.
$$

Regarding the covariance derivative. In general, covariant derivative encodes information about the curvature of the underlying space. If we are dealing with the $\hat{n}$-basis which is curvilinear, that is, spacetime dependent then the covariant derivative should be able to reflect this fact. We find that

$$
\begin{align*}
\hat{D}_ {\mu} \vec{X}_ {\nu} 
=& \hat{n}_ {\alpha}\partial_ {\mu} X_ {\nu}^{(\alpha)}+(\partial_ {\mu}\hat{n}_ {\alpha}) X_ {\nu}^{(\alpha)} + g a_ {\mu} \epsilon_ {\alpha\beta}\hat{n}_ {\beta} X_ {\nu}^{(\alpha)} + \hat{n}(\hat{n}_ {\alpha}\cdot \partial_ {\mu} \hat{n})X_ {\nu}^{(\alpha)}\\
=& \hat{n}_ {\alpha} (\partial_ {\mu} X_ {\nu}^{(\alpha)} - g a_ {\mu} \epsilon_ {\alpha \beta} X_ {\nu}^{(\beta)}) + (\partial_ {\mu}\hat{n}_ {\alpha}) X_ {\nu}^{(\alpha)} + \hat{n}(\hat{n}_ {\alpha}\cdot \partial_ {\mu} \hat{n})X_ {\nu}^{(\alpha)}.
\end{align*}
$$

where $\epsilon_ {\alpha \beta}$ is the Levi-Civita symbol (not tensor), defined as $\epsilon_ {\alpha\beta}=\epsilon^{\alpha\beta}=1$ for even permutation $\alpha, \beta=1,2$ and $-1$ for odd permutation. The last two terms in the last line reads

$$
\begin{align*}
&(\partial_ {\mu}\hat{n}_ {\alpha}) X_ {\nu}^{(\alpha)} + \hat{n}(\hat{n}_ {\alpha}\cdot \partial_ {\mu} \hat{n})X_ {\nu}^{(\alpha)} \\
=& X_ {\nu}^{(\alpha)}\left\lbrace \hat{n}(\hat{n}\cdot \partial_ {\mu}\hat{n}_ {\alpha}+\hat{n}_ {\alpha}\cdot \partial_ {\mu} \hat{n}) + \hat{n}_ {\beta}\cdot \partial_ {\mu}\hat{n}_ {\alpha} \left\lvert \epsilon_ {\alpha \beta}\right\rvert \hat{n}_ {\beta}  \right\rbrace \\
=& X_ {\nu}^{(\alpha)}\left\lbrace \hat{n}\partial_ {\mu}(\hat{n}\cdot \hat{n}_ {\alpha}) + \hat{n}_ {\beta}\cdot \partial_ {\mu}\hat{n}_ {\alpha} \left\lvert \epsilon_ {\alpha \beta} \right\rvert \hat{n}_ {\beta} \right\rbrace \\
=& X_ {\nu}^{(\alpha)}\left\lbrace \hat{n}_ {\beta}\cdot \partial_ {\mu}\hat{n}_ {\alpha} \left\lvert \epsilon_ {\alpha \beta} \right\rvert \hat{n}_ {\beta} \right\rbrace,
\end{align*}
$$

where the role of $\left\lvert \epsilon_ {\alpha \beta} \right\rvert$ is simply to switch between indices $1$ and $2$ without a sign change, the summation rule is not activated. We can write 

$$
\begin{align*}
\hat{D}_ {\mu} \vec{X}_ {\nu} 
&= \hat{n}_ {\alpha} (\partial_ {\mu} X_ {\nu}^{(\alpha)} - g a_ {\mu} \epsilon_ {\alpha \beta} X_ {\nu}^{(\beta)})
+\hat{n}_ {\beta} \left\lvert \epsilon_ {\alpha \beta} \right\rvert \hat{n}_ {\beta}\cdot \partial_ {\mu}\hat{n}_ {\alpha} X_ {\nu}^{(\alpha)} \\
&=  \hat{n}_ {\alpha}[\partial_ {\mu}X_ {\nu}^{(\alpha)}-(g a_ {\mu}\epsilon_ {\alpha \beta}-\left\lvert \epsilon_ {\alpha \beta} \right\rvert \hat{n}_ {\alpha} \cdot \partial_ {\mu} \hat{n}_ {\beta})X_ {\nu}^{(\beta)}].
\end{align*}
$$

Notice that there is no $\hat{n}$ component, only $\hat{n}_ {1}$ and $\hat{n}_ {2}$. Substitute $\chi,\chi ^\ast$ for $X^{(1,2)}$, let $\alpha=1$, $\beta=2$ we have

$$
\partial_ {\mu}X_ {\nu}^{(1)}-(g a_ {\mu}\epsilon_ {12}-\left\lvert \epsilon_ {12} \right\rvert \hat{n}_ {1} \cdot \partial_ {\mu} \hat{n}_ {2})X_ {\nu}^{(2)} =: \frac{1}{\sqrt{2}}(D_ {\mu}\chi_ {\nu}+(D_ {\mu}\chi_ {\nu})^\ast)
$$

where the covariant derivative acting on $\chi$ is defined by 

$$
D_ {\mu}\chi := \partial_ {\mu} \chi_ {\nu} +i(g a_ {\mu}-\hat{n}_ {1}\cdot \partial_ {\mu}\hat{n}_ {2})\chi_ {\nu}.
$$

Similarly, let $\alpha,\beta=2,1$ we have 

$$
\partial_ {\mu}X_ {\nu}^{(2)}-(g a_ {\mu}\epsilon_ {21}-\left\lvert \epsilon_ {21} \right\rvert \hat{n}_ {2} \cdot \partial_ {\mu} \hat{n}_ {1})X_ {\nu}^{(1)} = - \frac{i}{\sqrt{2}}(D_ {\mu}\chi_ {\nu}-\text{c.c.}).
$$

Substitute this to the term in the Lagrangian, we have 

$$
\begin{align*}
 &(\hat{D}_ {\mu}\vec{X}_ {\nu}-(\mu \leftrightarrow \nu))^{2}\\
 &= \sum_ {\alpha=1,2}\left\lbrace [\partial_ {\mu}X_ {\nu}^{(\alpha)}-(a_ {\mu}\epsilon_ {\alpha \beta}-\left\lvert \epsilon_ {\alpha \beta} \right\rvert \hat{n}_ {\alpha} \cdot \partial_ {\mu} \hat{n}_ {\beta})X_ {\nu}^{(\beta)}] -(\mu \leftrightarrow \nu) \right\rbrace ^{2}\\
 &= 2\left\lvert D_ {\mu}\chi_ {\nu}-D_ {\nu}\chi_ {\mu} \right\rvert ^{2}.
\end{align*}
$$

This simplification is quite impressive.

We can also write 

$$
D_ {\mu}\chi = \partial_ {\mu} \chi +ig B_ {\mu} \chi
$$

where $B$ is a new field defined as 

$$
B_ {\mu} := a_ \mu + C_ {\mu}, \quad  \hat{F}_ {\mu \nu} = \partial_ {\mu}B_ {\nu} - \partial_ {\nu}B_ {\mu}.
$$

- - -

Next let's consider a special case just to verify our result above. *If $\hat{n}$ is independent of spacetime,* then without loss of generality we can assume that $\hat{n}$ lies in the $T^{3}$ direction, $\hat{n}_ {1}$ in $T^{1}$ and $\hat{n}_ {2}$ in $T^{2}$ respectively in $\mathfrak{su}(2)$. $X=X^{1}\mathfrak{n}_ {1}+X^{2}\mathfrak{n}_ {2}$ becomes $X=X^{1}T^{1}+X^{2}T^{2}$. $\hat{A}=a_ {\mu}T^{3}$ since $\mathcal{C}$ vanishes, and as a consequence so does $H_ {\mu \nu}$.

We can write down the three components of $\hat{D}_ {\mu}\vec{X}_ {\nu}$ easily:

$$
\begin{align*}
\text{1-component=}&  \partial_ {\mu}X_ {\nu}^{1} - g\hat{A}_ {\mu}^{3}X_ {\nu}^{2}, \\
\text{2-component=}& \partial_ {\mu}X_ {\nu}^{2} + g\hat{A}_ {\mu}^{3}X_ {\nu}^{1},  \\
\text{3-component=}& 0.
\end{align*}
$$

The last one is zero since $\hat{A}^{1,2}=0$. Thus

$$
\begin{align*}
 &(\hat{D}_ {\mu}\vec{X}_ {\nu}-(\mu \leftrightarrow \nu))^{2}\\
=& \text{1-component}^{2}+\text{2-component}^{2}\\
=& \text{1-component}^{2}-(i\times \text{2-component})^{2}\\
=& (\text{1-compnent}+i\times \text{2-compnent})(\text{1-compnent}-i\times \text{2-compnent}) \\
=& [(\partial_ {\mu}X_ {\nu}^{1}+\partial_ {\mu}iX_ {\nu}^{2}+ig\hat{A}_ {\mu}^{3}(X_ {\nu}^{1}+iX_ {\nu}^{2}))-(\mu \leftrightarrow \nu)]\\
=& 2[\partial_ {\mu}\chi_ {\nu}+ig\hat{A}_ {\mu}^{3}\chi_ {\nu}-(\mu \leftrightarrow \nu)] [\partial_ {\mu}\chi ^\ast _ {\nu}-ig\hat{A}_ {\mu}^{3}\chi ^\ast _ {\nu}-(\mu \leftrightarrow \nu)]\\
=& 2[\partial_ {\mu}\chi_ {\nu}+ig\hat{A}_ {\mu}^{3}\chi_ {\nu}-(\mu \leftrightarrow \nu)]\times (\text{h.c.})
\end{align*}
$$

Recall that $\hat{A}^{3}=a$. Define the hatted covariant derivative for $\chi$ as 

$$
\hat{D}_ {\mu} \chi_ {\nu} := \partial_ {\mu}\chi_ {\nu} +i g a_ {\mu}\chi_ {\nu}
$$

we have 

$$
(\hat{D}_ {\mu}\vec{X}_ {\nu}-(\mu \leftrightarrow \nu))^{2} = 2\left\lvert \hat{D}_ {\mu}\chi_ {\nu}-\hat{D}_ {\nu}\chi_ {\mu} \right\rvert ^{2}.
$$

Finally, in the special case where $(\hat{n}_ {1},\hat{n}_ {2},\hat{n})=(T^{1},T^{2},T^{3})$, the Lagrangian for extended QCD now reads (in terms of  $\chi$):

$$
\begin{align*}
\mathcal{L}_ {\text{ECD}} =& - \frac{1}{4}(f_ {\mu \nu}+H_ {\mu \nu}+X_ {\mu \nu})^{2} 
- \frac{1}{2} \left\lvert \hat{D}_ {\mu}\chi_ {\nu}-\hat{D}_ {\nu}\chi_ {\mu} \right\rvert ^{2}
\end{align*}
$$

- - -

The equations of motion in terms of $\chi$ can be straightforwardly obtained. We can write $\hat{D}_ {\mu}\vec{X}_ {\nu}-\hat{D}_ {\nu}\vec{X}_ {\mu}$ in terms of $\chi$, explicitly expanded in basis $\hat{n}_ {1}$ and $\hat{n}_ {2}$,

$$
\begin{align*}
\hat{D}_ {\mu}\vec{X}_ {\nu}-\hat{D}_ {\nu}\vec{X}_ {\mu} &= \hat{n}_ {1} \left[ \frac{1}{\sqrt{2}}(\hat{D}_ {\mu}\chi_ {\nu}-\hat{D}_ {\nu}\chi_ {\mu})+\text{h.c.} \right] \\
&\quad\;\, + \hat{n}_ {2}\left( -\frac{i}{\sqrt{2}} \right)[(\hat{D}_ {\mu}\chi_ {\nu} - \hat{D}_ {\nu}\chi_ {\mu}) - \text{h.c.}]
\end{align*}
$$

We have 

$$
\boxed{
\partial_ {\mu}\Gamma_ {\mu \nu} = ig [\chi_ {\mu} ^\ast (\hat{D}_ {\mu}\chi_ {\nu}-\hat{D}_ {\nu}\chi_ {\mu}) - \text{h.c.}], \quad  \Gamma_ {\mu \nu} := f_ {\mu \nu}+H_ {\mu \nu}+X_ {\mu \nu}.
} 
$$


Define $K := (\hat{D}_ {\mu}\chi_ {\nu}-\hat{D}_ {\nu}\chi_ {\mu})/\sqrt{2}$ we have

$$
\begin{align*}
\hat{D}_ {\mu} (\hat{D}_ {\mu}\vec{X}_ {\nu}-\hat{D}_ {\nu}\vec{X}_ {\mu}) 
&= (\partial_ {\mu}+g \hat{A}_ {\mu}\times )(\hat{D}X-\hat{D}X)\\
&= \hat{n}_ {1}(-i\hat{n}_ {1}\cdot \partial_ {\mu}\hat{n}_ {2} + ig a_ {\mu} + \partial_ {\mu})(K-K^\ast )\\
& \quad \;\, + \hat{n}_ {2}(-\hat{n}_ {1}\cdot \partial_ {\mu}\hat{n}_ {2} + g a_ {\mu} -i \partial_ {\mu})(K-K^\ast )\\
&= \hat{n}_ {1}\hat{D}_ {\mu} (K-K^\ast ) + \hat{n}_ {2}(-i) \hat{D}_ {\mu} (K-K^\ast ).
\end{align*}
$$

By comparing the components, we have the following EoM:

$$
\boxed{
\hat{D}_ {\mu}(\hat{D}_ {\mu}\chi_ {\nu}-\hat{D}_ {\nu}\chi_ {\mu}) = ig \Gamma_ {\mu \nu} \, \chi_ {\mu}, \quad  \Gamma_ {\mu \nu} := f_ {\mu \nu}+H_ {\mu \nu}+X_ {\mu \nu}.
}
$$

If $X=0$ and $a=0$, then the EoM becomes $\partial_ {\mu}H_ {\mu \nu}=0$, in terms of $\hat{n}$ it reads

$$
\hat{n}\cdot(\partial^{2}\hat{n}\times \partial_ {\nu}\hat{n}+\partial_ {\mu}\hat{n}\times (\partial_ {\mu}\partial_ {\nu}\hat{n})) = 0.
$$

This is the constraint for $\hat{n}$ in the absence of other fields.




# Appendix

Below is a dictionary of notations. The left hand side is the notation used in this note, the right hand side that in the paper.

$$
\begin{align*}
S=\frac{1}{g^{2}}\int d^{d}x \,  \mathcal{L} \longrightarrow & S = \int d^{d}x \,  \mathcal{L}, \\
A_ {\mu} \longrightarrow & g\vec{A}_ {\mu}, \\
\mathcal{C}_ {\mu} \longrightarrow &  \mathcal{C}_ {\mu},\\
\mathcal{A} \longrightarrow & g\mathcal{A},\\
a_ {\mu}  \longrightarrow &  g A_ {\mu}
\end{align*}
$$

but if $\mathcal{C}$ appears alone, we have $\mathcal{C}_ {\mu} \longrightarrow \frac{1}{g} \mathcal{C}_ {\mu}$.

Upon those substitutes, we recover the expressions in the paper. The reason why $\mathcal{C}\to\mathcal{C} /g$ is that, when solving for the restricted field, we write the solution as $\hat{A}=\mathcal{A}+\mathcal{C}$, then going to the paper's notation we get $g\hat{A}_ {\text{paper}} = g\mathcal{A}_ {\text{paper}}+\mathcal{C}$, but in the paper the definition reads $\hat{A}_ {\text{paper}}=\mathcal{A}_ {\text{paper}}+\mathcal{C}_ {\text{paper}}$, which implies $\mathcal{C}_ {\text{paper}}=\mathcal{C} /g$. 

- - -

Introduce a **right-handed orthonormal frame** $(\hat{n}^{1},\hat{n}^{2},\hat{n}^{3})$ with $\hat{n}^{i}\hat{n}^{i}=1$. Choose the third component to be the so-called abelian direction, denoted it by $\hat{n}:=\hat{n}^{3}$.

The following identities might be helpful (For $SU(2)$):

$$
\begin{align*}
\mathfrak{n} \mathfrak{n} = \hat{n}^{a}\hat{n}^{b}\frac{1}{2}\sigma^{a} \frac{1}{2}\sigma^{b} &= \frac{1}{4}, \\
[\mathfrak{n} ,[\mathfrak{n} ,\partial_ {\mu}\mathfrak{n} ]] &= \partial_ {\mu}\mathfrak{n}, \\
[[\mathfrak{n},\partial_ {\nu}\mathfrak{n}  ],[\mathfrak{n} ,\partial_ {\mu}\mathfrak{n} ]] &= - \partial_ {\nu}\mathfrak{n} \partial_ {\mu}\mathfrak{n} .
\end{align*}
$$

Let $d^{abc}$ be the total symmetric tensor of $SU(N)$ defined by 

$$
\left\lbrace T^{a},T^{b} \right\rbrace  = \frac{\delta^{ab}}{N} \mathbb{1} + d^{abc}T^{c},
$$

equivalently 

$$
d^{abc} = 2\mathrm{Tr}\,(\left\lbrace T^{a},T^{b} \right\rbrace T^{c})
$$

below are some useful identities about $SU(N)$ group:

$$
\begin{align*}
\mathrm{Tr}\,(T^{a}T^{b}T^{c}) =& \frac{1}{4}(d^{abc}+if^{abc}).
\end{align*}
$$

- - -

the total gauge field $A$ into the following three parts, 

$$
A = \mathcal{A}+\mathcal{C}+X, \quad  [X,\mathfrak{n} ]\neq0.
$$

The restricted gauge field $\hat{A}$ is the solution for:

$$
\hat{D}_ {\mu}\mathfrak{n}  = (\partial_ {\mu}-i[\hat{A}_ {\mu},-])\mathfrak{n} =0.
$$

$\mathcal{C}_ {\mu}$ is the non-trivial part of the solution for $D_ {\mu}\mathfrak{n} =0$,

$$
\boxed{ 
\mathcal{C}_ {\mu} = i[\mathfrak{n},\partial_ {\mu} \mathfrak{n}] .
}
$$

This is a $\mathfrak{g}$-valued quantity, in terms of components in basis $T^{a}$ it can be written as 

$$
\boxed{ 
\mathcal{C}_ {\mu} = -\hat{n} \times (\partial_ {\mu}\hat{n}) \text{ in }\mathfrak{g} .
}
$$

The trivial part of the solution that is proportional to $\mathfrak{n}$, call it $\mathcal{A}$, is given by 

$$
\boxed{ 
\mathcal{A}_ {\mu} =  a_ {\mu} \mathfrak{n},\quad a_ {\mu}\in \mathbb{R}.
}
$$

We have

$$
\hat{A}=\mathcal{A}+\mathcal{C}, \quad \mathcal{A}\propto \mathfrak{n}\text{ and }\mathcal{C}=i[\mathfrak{n},\partial \mathfrak{n}].
$$

Define

$$
\begin{align*}
\hat{F}:= & \partial_ {\mu}\hat{A}_ {\nu}-\partial_ {\nu}\hat{A}_ {\mu}-i[\hat{A}_ {\mu},\hat{A}_ {\nu}]\\
=& (\partial_ {\mu}a_ {\nu}-\partial_ {\nu}a_ {\mu})\mathfrak{n} +i[\partial_ {\mu}\mathfrak{n} ,\partial_ {\nu}\mathfrak{n} ]\\
=&: f_ {\mu \nu}\mathfrak{n} +H_ {\mu \nu}\mathfrak{n} .
\end{align*}
$$

We have 

$$
\begin{align*}
f_ {\mu \nu} &= \partial_ {\mu}a_ {\nu}-\partial_ {\nu}a_ {\mu},\\
H_ {\mu \nu} \mathfrak{n}  &=i[\partial_ {\mu}\mathfrak{n} ,\partial_ {\nu}\mathfrak{n} ],\\
H_ {\mu \nu} &= \partial_ {\mu}C_ {\nu}-\partial_ {\nu}C_ {\mu}, \; C_ {\mu}:= \hat{n}_ {2}\cdot \partial_ {\mu}\hat{n}_ {1}.
\end{align*}
$$

The total field strength $F_ {\mu \nu}$ is 

$$
\boxed{ 
F_ {\mu \nu} = \hat{F}_ {\mu \nu}+\hat{D}_ {\mu}X_ {\nu}-\hat{D}_ {\nu}X_ {\mu}-i[X_ {\mu},X_ {\nu}].
}
$$

Define

$$
\boxed{ 
X_ {\mu \nu} \mathfrak{n} := -i[X_ {\mu},X_ {\nu}],
}
$$

then the Lagrangian reads

$$
\boxed{ 
\begin{align*}
\mathcal{L}_ {\text{ECD}} =& - \frac{1}{2g^{2}}\mathrm{Tr}\,\left\lbrace (\hat{F}+X_ {\mu \nu}\mathfrak{n} )^{2}+(\hat{D}_ {\mu}X_ {\nu}- \mu\leftrightarrow \nu)^{2} \right\rbrace \\
=& - \frac{1}{2g^{2}}\mathrm{Tr}\,\left\lbrace \hat{F}^{2}-2i\hat{F}_ {\mu \nu}[X_ {\mu},X_ {\nu}]+(\hat{D}_ {\mu}X_ {\nu}-\hat{D}_ {\nu}X_ {\mu})^{2}  - [X_ {\mu},X_ {\nu}]^{2}\   \right\rbrace \\
=& - \frac{1}{4g^{2}}[(f_ {\mu \nu}+H_ {\mu \nu}+X_ {\mu \nu})^{2}+(\hat{D}_ {\mu}\vec{X}_ {\nu}-\mu \leftrightarrow \nu)^{2}]
\end{align*}
}
$$
