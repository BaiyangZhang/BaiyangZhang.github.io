# Linearized Soliton Perturbation Theory: a blackboard talk


## Asymptotic perturbation theory does not determine the full observable (00--15)

A perturbative calculation gives a formal series. It does not, by itself, give a unique function of the coupling.

Write an observable as 

$$
F(\lambda)\sim\sum_{n=0}^{\infty}c_n\lambda^n.
$$

The symbol $\sim$ is important. It means that for every fixed $N$, 

$$
F(\lambda)-\sum_{n=0}^{N-1}c_n\lambda^n
=O(\lambda^N)
$$

in the specified limit and sector. It does not mean that the infinite sum converges.

Dyson's argument gives a simple reason to expect a zero radius of convergence in many theories. Consider the stable scalar potential with
positive quartic coupling. If we analytically continue $\lambda$ to negative values, the potential is unbounded below. The vacuum ceases to be stable. Therefore the exact observable cannot generally be analytic in a full neighbourhood of $\lambda=0$. This argument establishes nonanalyticity. It does not, by itself, determine the exact large-order coefficients or the location of every Borel singularity.

**Blackboard.**

$$
F(\lambda)\sim\sum_{n\geq0}c_n\lambda^n,
\qquad
\lambda\to0^+.
$$

$$
\text{Positive }\lambda:\ \text{stable quartic potential},
\qquad
\text{Negative }\lambda:\ \text{potential unbounded below}.
$$
**Spoken text.**

Suppose the coefficients grow factorially, 

$$
c_n\sim C\,\frac{n!}{A^n}.
$$

The ordinary series diverges. We can nevertheless form its Borel transform, 

$$
\mathcal B F(t)=\sum_{n=0}^{\infty}\frac{c_n}{n!}t^n.
$$

If this transform admits analytic continuation and suitable growth bounds along a ray, the Borel sum is 

$$
\mathcal S F(\lambda)
=
\frac1{\lambda}\int_0^\infty
dt\,e^{-t/\lambda}\mathcal B F(t).
$$

The location of the Borel singularities matters. A singularity on the integration ray makes the integral ambiguous. We then define lateral
sums just above and below that ray: 


$$
\mathcal S_\pm F(\lambda)
=
\frac1{\lambda}
\int_{0}^{e^{\pm i0}\infty}
dt\,e^{-t/\lambda}\mathcal B F(t).
$$

Their difference is exponentially small in $\lambda$. For a singularity at $t=A>0$, it has the schematic form 

$$
\mathcal S_+F-\mathcal S_-F
\sim i\,C_A\,\lambda^\gamma e^{-A/\lambda}.
$$


A nonperturbative sector can carry the opposite ambiguity. **The physical observable is unambiguous only after the perturbative and**
**nonperturbative sectors are combined with the correct Stokes data.** There are two qualifications. First, Dyson's instability argument alone
does not prove that a Borel singularity lies on the positive integration
ray. For stable positive-coupling $\phi^4$, the instability reached by
continuing to negative coupling is associated with the negative-coupling
direction. Second, a static kink is a soliton state, not automatically a
Euclidean instanton contribution to a vacuum observable. The kink mass
has its own semiclassical expansion beginning with $Q_0\sim1/\lambda$.
We should not identify that whole kink sector with a flat term in the
vacuum-sector expansion.

**Blackboard.**

$$
\mathcal B F(t)=\sum_{n=0}^{\infty}\frac{c_n}{n!}t^n,
\qquad
\mathcal S_\pm F(\lambda)
=
\frac1{\lambda}
\int_{0}^{e^{\pm i0}\infty}
dt\,e^{-t/\lambda}\mathcal B F(t).
$$

$$
\operatorname{Disc}\mathcal S F
=
\mathcal S_+F-\mathcal S_-F
\sim i\,C_A\lambda^\gamma e^{-A/\lambda}.
$$

$$
F_{\rm phys}
=
\mathcal S F_{\rm pert}
+
\sigma\,e^{-A/\lambda}F_1(\lambda)
+\cdots.
$$

**Spoken text.**

There is a useful mathematical way to organize this distinction. Let $U$ be a sector in the complex coupling plane with the origin at its boundary. Define $\mathscr O_{\rm sec}(U)$ to be the holomorphic functions on $U$ that obey a specified asymptotic expansion and growth condition. Restriction from $U$ to a smaller sector gives the sheaf structure.

Let $\widehat{\mathscr O}$ denote the sheaf of formal power series, and let $\mathscr F_{\rm flat}$ denote the functions whose asymptotic power series vanishes. Locally, under the hypotheses of the Borel-Ritt theorem, one has the schematic exact sequence $$
0\longrightarrow\mathscr F_{\rm flat}
\longrightarrow\mathscr O_{\rm sec}
\xrightarrow{\operatorname{Asymp}}
\widehat{\mathscr O}
\longrightarrow0.
$$

The kernel contains functions such as $e^{-A/\lambda}$ on sectors where they are exponentially small. These functions are invisible to every
coefficient of the power series.

**Blackboard.**

$$
\boxed{
0\longrightarrow\mathscr F_{\rm flat}
\longrightarrow\mathscr O_{\rm sec}
\xrightarrow{\operatorname{Asymp}}
\widehat{\mathscr O}
\longrightarrow0
}
$$

$$
e^{-A/\lambda}=o(\lambda^N)
\quad
\text{for every fixed }N
\quad
\text{in a sector with }\operatorname{Re}(A/\lambda)>0.
$$
------------------------------------------------------------------------

## Topological charge labels the sector

Consider a scalar theory with two degenerate vacua, $\phi_-$ and $\phi_+$. A finite-energy configuration in one spatial dimension approaches a vacuum at each end of space: 

$$
\phi(x)\longrightarrow\phi_\pm^{\rm end}
\qquad
(x\to\pm\infty).
$$
 The topological charge is 
 
 $$
Q_T=
\frac{\phi(+\infty)-\phi(-\infty)}
{\phi_+-\phi_-}.
$$

For the kink used here, $Q_T=1$; for the antikink, $Q_T=-1$; and for a configuration with the same vacuum at both ends, $Q_T=0$.

The charge depends only on the boundary conditions. A local observable has support in a bounded region. It cannot change the field value at
spatial infinity. Consequently, for the algebra of local observables, $$
[Q_T,\mathcal O_{\rm loc}]=0.
$$ This is the sense in which $Q_T$ labels superselection sectors.

If we deliberately construct a Hilbert space containing all sectors, it
has the schematic decomposition $$
\mathcal H=\bigoplus_{n\in\mathbb Z}\mathcal H_n,
\qquad
Q_T|_{\mathcal H_n}=n.
$$ The local observable algebra acts block-diagonally. A local operator
cannot turn a vacuum state into a one-kink state.

This direct sum is a convenient way to collect sectors. In algebraic
QFT, distinct sectors may instead be described by disjoint
representations of the same local observable algebra. We should not
assume that every sector is already a subspace of the irreducible vacuum
Fock representation.

**Blackboard.**

$$
Q_T=
\frac{\phi(+\infty)-\phi(-\infty)}
{\phi_+-\phi_-},
\qquad
Q_T\in\mathbb Z.
$$

$$
[Q_T,\mathcal O_{\rm loc}]=0.
$$

$$
\mathcal H=\bigoplus_{n\in\mathbb Z}\mathcal H_n,
\qquad
Q_T|_{\mathcal H_n}=n.
$$

**Spoken text.**

This is already different from ordinary perturbation theory. In the
vacuum sector, we expand the field in plane waves. In the one-kink
sector, the natural small fluctuations are eigenfunctions of the
differential operator obtained by linearizing about the kink.

The finite-dimensional Stone--von Neumann theorem does not settle this
issue. For a finite number of canonical pairs, under its regularity
assumptions, the irreducible representation of the canonical commutation
relations is unique up to unitary equivalence. A field theory has
infinitely many degrees of freedom. The theorem does not imply
uniqueness of the Fock representation in that setting.

Haag's theorem gives a related warning. Under the Wightman-type
assumptions used in its proof, a free field and a genuinely interacting
field cannot be related by a single global unitary transformation at a
fixed time while preserving all the required vacuum and covariance
properties. This undermines a literal, nonperturbative interaction
picture in one common free-field Fock space. It does not say that
perturbative interaction-picture calculations are useless, and it does
not by itself prove that every topological sector is disjoint from every
vacuum representation.

Constructive $\phi^4_2$ theory, developed by Glimm and Jaffe and others,
provides an explicit setting in which the interacting theory is not
simply the free-field Fock representation with a unitary change of
basis. The example is useful because it shows that the representation
issue is not restricted to solitons or to higher dimensions.

**Blackboard.**

$$
[\phi(x),\pi(y)]=i\delta(x-y).
$$

$$
\begin{array}{c}
\text{finitely many canonical pairs}\\[2pt]
\Downarrow\\[2pt]
\text{Stone--von Neumann uniqueness}
\end{array}
\qquad
\begin{array}{c}
\text{infinitely many field modes}\\[2pt]
\Downarrow\\[2pt]
\text{inequivalent representations may occur}
\end{array}
$$

**Spoken text.**

There is also a direct way to see why a kink displacement is problematic
in the vacuum Fock representation. Let $$
\mathcal D_f=
\exp\left[-i\int dx\,f(x)\pi(x)\right].
$$ For a finite-volume regulator, this is a unitary Weyl displacement.
Its coherent-state parameter in the plane-wave basis is, with the
Fourier convention used below, $$
\alpha_f(p)=\sqrt{\frac{\omega_p}{2}}\,\widetilde f(p),
\qquad
\omega_p=\sqrt{p^2+m^2}.
$$ The vacuum overlap is $$
|\langle0|\mathcal D_f|0\rangle|^2
=
e^{-\|\alpha_f\|^2},
\qquad
\|\alpha_f\|^2
=
\frac12\int\frac{dp}{2\pi}\,
\omega_p|\widetilde f(p)|^2.
$$ This formula assumes that $f$ belongs to the one-particle
displacement space. A kink approaches different constants at the two
ends of space. Its Fourier transform has a distributional zero-momentum
contribution and a $1/p$-type infrared behaviour. The norm above
therefore diverges as the volume tends to infinity. The overlap tends to
zero.

This is an infrared statement about the boundary conditions. It is not a
UV divergence. At finite volume and finite regulator the displacement is
well-defined; in the infinite-volume limit it need not be implementable
as a unitary operator on the vacuum Fock space. That distinction will
matter when I describe the passive transformation.

**Blackboard.**

$$
\alpha_f(p)=\sqrt{\frac{\omega_p}{2}}\widetilde f(p),
\qquad
\|\alpha_f\|^2=
\frac12\int\frac{dp}{2\pi}\,
\omega_p|\widetilde f(p)|^2.
$$

$$
|\langle0|\mathcal D_f|0\rangle|^2=e^{-\|\alpha_f\|^2}.
$$

$$
f(+\infty)\ne f(-\infty)
\quad\Longrightarrow\quad
\|\alpha_f\|^2\to\infty
\quad
(L\to\infty).
$$

**Transition.** There are three related problems with the naive
construction. The first is this representation issue. The second is the
divergence identified by Coleman. The third is the mismatch that can
arise if the two sectors are regulated independently.

------------------------------------------------------------------------

## The coherent displacement is not the full kink state (30--42)

**Spoken text.**

A coherent displacement gives the correct leading one-point function. It
does not generally give the correct state.

The coherent state is $$
|f\rangle=\mathcal D_f|0\rangle.
$$ Using the canonical commutator, $$
\mathcal D_f^\dagger\phi(x)\mathcal D_f=\phi(x)+f(x),
$$ and therefore $$
\langle f|\phi(x)|f\rangle=f(x)
$$ if the reference vacuum has zero one-point function.

But a Gaussian state is fixed by both its mean and its covariance. The
displacement changes the mean. It does not change the covariance. The
coherent state therefore retains the vacuum fluctuation kernel even
though the fluctuation operator is now governed by the kink background.

In the kink sector the quadratic operator is $$
\mathcal K=-\partial_x^2+V''(f(x)).
$$ The correct Gaussian covariance is controlled by $\mathcal K^{-1/2}$,
not by the vacuum operator $$
\Omega_0^{-1}=(-\partial_x^2+m^2)^{-1/2}.
$$ This is the basic reason that the kink state must be squeezed as well
as displaced.

**Blackboard.**

$$
\langle f|\phi(x)|f\rangle=f(x),
\qquad
\langle f|(\phi-f)(x)(\phi-f)(y)|f\rangle
=
\frac12\Omega_0^{-1}(x,y).
$$

$$
\mathcal K=-\partial_x^2+V''(f(x)),
\qquad
C_{\rm kink}(x,y)=\frac12\mathcal K^{-1/2}(x,y).
$$

**Spoken text.**

Coleman's observation is especially sharp in more than one spatial
dimension. In $1+1$ dimensions, normal ordering makes the coherent-state
calculation finite for the scalar theories under discussion. The
coherent state still misses the one-loop correction to the kink mass. In
$3+1$ dimensions, the unsqueezed coherent state has an
ultraviolet-divergent energy density after the vacuum subtraction. The
squeeze changes the short-distance covariance and supplies the missing
one-loop contribution.

There is a separate regulator problem. The vacuum basis is labelled by
plane-wave momentum $p$. The kink basis is labelled by a continuum mode
$k$, together with bound modes. A cutoff $|p|<\Lambda$ and a cutoff
$|k|<\Lambda'$ are not automatically the same regulator. The two bases
are related by a Bogoliubov transformation, not by a diagonal
relabelling of momenta.

The safe prescription is to define one regulated Hamiltonian and
transform that Hamiltonian. At finite regulator, the transformation is
an ordinary unitary conjugation. We then take the continuum limit while
keeping the regulator and counterterm prescription common. In the limit,
the transformation may cease to be unitarily implementable in the
original vacuum Fock representation. That does not invalidate the
regulated construction; it tells us that the limiting kink sector may
require its own representation.

The language of quantization as a functor can be a useful analogy, but
it is not a proof of this regulator statement. The Groenewold--van Hove
obstruction concerns the impossibility of preserving the full Poisson
algebra under canonical quantization in a finite-dimensional setting. It
is not, by itself, a theorem about matching plane-wave and kink-mode
cutoffs.

**Blackboard.**

$$
H_\Lambda\quad\text{one regulated Hamiltonian},
$$

$$
H_{{\rm K},\Lambda}
=
\mathcal D_{f,\Lambda}^{\dagger}
H_\Lambda
\mathcal D_{f,\Lambda}.
$$

$$
\text{Do not define }H_\Lambda
\text{ and }H_{{\rm K},\Lambda'}
\text{ independently and then guess }\Lambda'(\Lambda).
$$

**Transition.** I now want to formulate the displacement as a passive
change of frame. This separates the physical state from the coordinates
used to describe its fluctuations.

------------------------------------------------------------------------

## The displacement operator as a passive change of frame (42--60)

**Spoken text.**

Let the defining-frame canonical fields be $\Phi(x)$ and $\Pi(x)$, with
$$
[\Phi(x),\Pi(y)]=i\delta(x-y).
$$ For a real, time-independent profile $f(x)$, define $$
\mathcal D_f=
\exp\left[-i\int dx\,f(x)\Pi(x)\right].
$$

I first derive its action. Set $$
A=\int dx\,f(x)\Pi(x).
$$ Then $$
[A,\Phi(y)]=-if(y).
$$ Since this is a c-number, all higher nested commutators vanish. Hence
$$
e^{iA}\Phi(y)e^{-iA}
=
\Phi(y)+[iA,\Phi(y)]
=
\Phi(y)+f(y).
$$ Therefore $$
\mathcal D_f^\dagger\Phi(y)\mathcal D_f=\Phi(y)+f(y),
\qquad
\mathcal D_f\Phi(y)\mathcal D_f^\dagger=\Phi(y)-f(y).
$$ The momentum is unchanged: $$
\mathcal D_f^\dagger\Pi(y)\mathcal D_f=\Pi(y).
$$

The two signs are both correct. They correspond to the two inverse
conjugations. I will not switch between them without saying so.

**Blackboard.**

$$
A=\int dx\,f(x)\Pi(x),
\qquad
[A,\Phi(y)]=-if(y).
$$

$$
\boxed{
\mathcal D_f^\dagger\Phi(x)\mathcal D_f=\Phi(x)+f(x)
}
$$

$$
\boxed{
\mathcal D_f\Phi(x)\mathcal D_f^\dagger=\Phi(x)-f(x)
}
$$

$$
\mathcal D_f^\dagger\Pi(x)\mathcal D_f=\Pi(x).
$$

**Spoken text.**

There are two ways to read this transformation.

In the active reading, the operators are held fixed and the state is
displaced: $$
|K\rangle_{\rm def}=\mathcal D_f|\Omega\rangle_0.
$$ Then $$
{}_{\rm def}\langle K|\Phi(x)|K\rangle_{\rm def}
=
{}_0\langle\Omega|
\mathcal D_f^\dagger\Phi(x)\mathcal D_f
|\Omega\rangle_0
=f(x).
$$ This is the usual coherent-state construction.

In the passive reading, we do not say that the physical state has
changed. We change the frame in which it is represented. Define $$
|K\rangle_{\rm K}
=
\mathcal D_f^\dagger|K\rangle_{\rm def},
\qquad
O_{\rm K}
=
\mathcal D_f^\dagger O_{\rm def}\mathcal D_f.
$$ Then $$
{}_{\rm K}\langle K|O_{\rm K}|K\rangle_{\rm K}
=
{}_{\rm def}\langle K|O_{\rm def}|K\rangle_{\rm def}.
$$ This is the invariance of expectation values under a change of frame.

In the kink frame the physical field is represented by $$
\Phi_{\rm K}=\mathcal D_f^\dagger\Phi_{\rm def}\mathcal D_f
=\Phi_{\rm K}^{\rm fluct}+f.
$$ The canonical field $\Phi_{\rm K}^{\rm fluct}$, which I will now call
$\varphi$, has zero expectation value in the leading kink-frame state:
$$
{}_{\rm K}\langle K|\varphi(x)|K\rangle_{\rm K}=0.
$$ Equivalently, in the defining-frame algebra the same fluctuation
operator is represented by $$
\varphi_{\rm def}
=
\mathcal D_f\Phi_{\rm K}^{\rm fluct}\mathcal D_f^\dagger
=
\Phi_{\rm def}-f.
$$ This is the relation often written simply as $$
\varphi=\mathcal D_f\Phi\mathcal D_f^\dagger=\Phi-f.
$$ It is the old-frame image of the kink-frame fluctuation field. The
state and operator must be transformed together when we compare matrix
elements.

**Blackboard.**

$$
|K\rangle_{\rm K}=\mathcal D_f^\dagger|K\rangle_{\rm def},
\qquad
O_{\rm K}=\mathcal D_f^\dagger O_{\rm def}\mathcal D_f.
$$

$$
{}_{\rm K}\langle K|O_{\rm K}|K\rangle_{\rm K}
=
{}_{\rm def}\langle K|O_{\rm def}|K\rangle_{\rm def}.
$$

$$
\Phi_{\rm K}=\varphi+f,
\qquad
\langle\varphi\rangle_{\rm K}=0.
$$

$$
\varphi_{\rm def}
=
\mathcal D_f\varphi\mathcal D_f^\dagger
=
\Phi_{\rm def}-f.
$$

**Spoken text.**

The exact Hamiltonian transforms in the same way as every other
operator: $$
H_{\rm K}
=
\mathcal D_f^\dagger H_{\rm def}\mathcal D_f.
$$ In the kink frame it is the original Hamiltonian expressed in terms
of the fluctuation field plus the background: $$
H_{\rm K}=H[\varphi+f,\Pi].
$$ At finite regulator the transformation is unitary, so $$
\operatorname{Spec}(H_{\rm K})=\operatorname{Spec}(H_{\rm def}).
$$ The energy of a physical state is unchanged. Only its representation
has changed.

This is the passive perspective. The displacement is not being used as
an extra physical interaction. It is the map between two descriptions of
the same regulated theory. The active statement that $\mathcal D_f$
creates a coherent state and the passive statement that it shifts the
field coordinate are two descriptions of the same algebraic relation.

The continuum caveat remains. For a topological profile, $\mathcal D_f$
may not be a unitary operator within the original vacuum Fock
representation after the infinite-volume limit. The safe statement is
that the transformation is unitary at finite regulator and defines the
corresponding map of the regulated canonical algebra. The limiting kink
representation can be inequivalent to the vacuum representation.

**Blackboard.**

$$
\boxed{
H_{\rm K}=\mathcal D_f^\dagger H_{\rm def}\mathcal D_f
=H[\varphi+f,\Pi]
}
$$

$$
\operatorname{Spec}(H_{\rm K})=\operatorname{Spec}(H_{\rm def})
\quad\text{at finite regulator}.
$$

**Transition.** The displacement fixes the mean field. It does not fix
the covariance. To obtain the kink-sector Gaussian ground state, we must
also squeeze.

------------------------------------------------------------------------

## The kink vacuum is squeezed as well as displaced (60--75)

**Spoken text.**

Let $a_p$ denote the plane-wave annihilation operators in the defining
vacuum basis. Let $b_\alpha$ denote annihilation operators for the kink
normal modes. The label $\alpha$ includes the shape mode and the
continuum. The translational zero mode is not an oscillator and will be
treated separately.

The two oscillator bases are related by a Bogoliubov transformation. To
see the coefficients, invert the plane-wave expansion and insert the
kink-mode expansions of $\varphi$ and $\Pi$: $$
a_p=
\sum_{\alpha\ne B}\int dx\,e^{-ipx}
\left[
\frac12\left(\sqrt{\frac{\omega_p}{\omega_\alpha}}+
\sqrt{\frac{\omega_\alpha}{\omega_p}}\right)
g_\alpha(x)b_\alpha
+
\frac12\left(\sqrt{\frac{\omega_p}{\omega_\alpha}}-
\sqrt{\frac{\omega_\alpha}{\omega_p}}\right)
g_\alpha^*(x)b_\alpha^\dagger
\right].
$$ Here $\sum_\alpha$ means a sum over the shape mode plus an integral
over continuum modes. The zero mode is excluded because $\omega_B=0$ and
is represented by $q_0,p_0$, not by an oscillator. For a plane-wave mode
with $\omega_\alpha=\omega_p$, the coefficient of $b^\dagger$ vanishes.
The nonzero coefficient is the squeeze.

If the inverse kernels are denoted by $\bar U,\bar V$, the projection
above is $a=\bar U b+\bar V b^\dagger$. The forward map
$b=Ua+Va^\dagger$ and this inverse map are related by the usual
canonical inverse. The coefficients obey the canonical conditions $$
UU^\dagger-VV^\dagger=\mathbf 1,
\qquad
UV^T=VU^T.
$$ The second condition ensures that the transformed annihilation
operators commute with one another.

The kink Gaussian vacuum is defined by $$
b_\alpha|0\rangle_{\rm K}=0.
$$ It is not, in general, the plane-wave vacuum $a_p|0\rangle_0=0$.

To see the form of the new vacuum, write $$
|0\rangle_{\rm K}
=
\mathcal N
\exp\left[
\frac12\int\frac{dp}{2\pi}\frac{dq}{2\pi}
a_p^\dagger Z(p,q)a_q^\dagger
\right]|0\rangle_0.
$$ The identity $$
a_p
\exp\left(\frac12a^\dagger Za^\dagger\right)|0\rangle_0
=
\left[
\int\frac{dq}{2\pi}Z(p,q)a_q^\dagger
\right]
\exp\left(\frac12a^\dagger Za^\dagger\right)|0\rangle_0
$$ follows from $[a_p,a_q^\dagger]=2\pi\delta(p-q)$. Substituting this
ansatz into $b_\alpha|0\rangle_{\rm K}=0$ gives $$
UZ+V=0,
\qquad
Z=-U^{-1}V,
$$ when $U$ is invertible on the regulated oscillator space. The
canonical conditions imply that $Z$ is symmetric. At finite regulator,
normalizability requires the singular values of $Z$ to be smaller than
one.

The corresponding unitary squeeze operator can be written $$
S=\exp\left[
\frac12(a^\dagger\zeta a^\dagger-a\zeta^\dagger a)
\right],
$$ with the kernels and indices understood. It implements the Bogoliubov
transformation. The kink state at Gaussian order is therefore $$
\boxed{
|K\rangle_{\rm def}
=
\mathcal D_f S|0\rangle_0.
}
$$ The displacement fixes the mean. The squeeze changes the covariance.

**Blackboard.**

$$
b=Ua+Va^\dagger,
$$

$$
UU^\dagger-VV^\dagger=\mathbf1,
\qquad
UV^T=VU^T.
$$

$$
|0\rangle_{\rm K}
=
\mathcal N
\exp\left(\frac12a^\dagger Za^\dagger\right)|0\rangle_0,
\qquad
Z=-U^{-1}V.
$$

$$
S=\exp\left[\frac12(a^\dagger\zeta a^\dagger-a\zeta^\dagger a)\right],
\qquad
|K\rangle_{\rm def}=\mathcal D_fS|0\rangle_0.
$$

**Spoken text.**

The same result is visible in the Schrödinger wave functional. The
vacuum Gaussian is $$
\Psi_0[\Phi]
=
N_0\exp\left[
-\frac12\int dx\,dy\,
\Phi(x)\Omega_0(x,y)\Phi(y)
\right],
\qquad
\Omega_0=\sqrt{-\partial_x^2+m^2}.
$$ A pure displacement gives $$
\Psi_{\rm coh}[\Phi]
=
N_0\exp\left[
-\frac12\int dx\,dy\,
(\Phi-f)(x)\Omega_0(x,y)(\Phi-f)(y)
\right].
$$ It is still a Gaussian with the vacuum kernel.

The quadratic kink Hamiltonian instead has the kernel $$
\Omega_{\rm K}=\sqrt{\mathcal K},
\qquad
\mathcal K=-\partial_x^2+V''(f).
$$ Its Gaussian ground-state wave functional is $$
\Psi_{\rm K}^{(0)}[\Phi]
=
N_{\rm K}\exp\left[
-\frac12\int dx\,dy\,
(\Phi-f)(x)\Omega_{\rm K}(x,y)(\Phi-f)(y)
\right].
$$ The covariance is $$
\langle(\Phi-f)(x)(\Phi-f)(y)\rangle_{\rm K}
=
\frac12\Omega_{\rm K}^{-1}(x,y).
$$ This is the squeezed coherent state. The zero-mode eigenvalue of
$\mathcal K$ is zero, so $\Omega_{\rm K}^{-1}$ is understood on the
nonzero-mode subspace. The translational coordinate is handled
separately.

**Blackboard.**

$$
\Psi_{\rm coh}[\Phi]\propto
e^{-\frac12\langle\Phi-f,\Omega_0(\Phi-f)\rangle},
\qquad
\Omega_0=\sqrt{-\partial_x^2+m^2}.
$$

$$
\Psi_{\rm K}^{(0)}[\Phi]\propto
e^{-\frac12\langle\Phi-f,\Omega_{\rm K}(\Phi-f)\rangle},
\qquad
\Omega_{\rm K}=\sqrt{-\partial_x^2+V''(f)}.
$$

$$
C_{\rm K}(x,y)=\frac12\Omega_{\rm K}^{-1}(x,y).
$$

**Spoken text.**

The phrase "squeezed coherent state" is therefore precise. It means a
state with the classical mean profile and the Gaussian covariance
selected by the kink fluctuation operator. It is not an arbitrary extra
ansatz.

The Gaussian state is only the leading approximation. Cubic and quartic
interactions generate further corrections to the state and to its
energy. The displacement and squeeze identify the correct starting point
for perturbation theory; they do not replace the perturbative
calculation.

------------------------------------------------------------------------

## One exact Hamiltonian has two natural quadratic approximations (75--83)

**Spoken text.**

Let us distinguish four objects. There is one exact Hamiltonian in the
defining frame, $H_{\rm def}$, and its exact kink-frame representative,
$$
H_{\rm K}=\mathcal D_f^\dagger H_{\rm def}\mathcal D_f.
$$ These are unitarily related at finite regulator.

There are also two different quadratic approximations. Expanding about a
homogeneous vacuum gives $H_2^{\rm vac}$. Expanding about the kink gives
$H_2^{\rm K}$. They are not the same operator.

For the shifted $\phi^4$ potential, $$
H_{\rm K}
=
\int dx\left[
\frac12\Pi^2
+\frac12(\partial_x\varphi)^2
+V(f+\varphi)
\right].
$$ Expanding the potential, $$
V(f+\varphi)
=
V(f)+V'(f)\varphi
+\frac12V''(f)\varphi^2
+\frac1{3!}V'''(f)\varphi^3
+\frac1{4!}V''''(f)\varphi^4.
$$ After integrating the gradient term by parts, the linear term is
proportional to $$
-f''+V'(f).
$$ It vanishes because $f$ solves the classical field equation.

Thus $$
H_{\rm K}=Q_0+H_2^{\rm K}+H_3^{\rm K}+H_4^{\rm K},
$$ where $$
H_2^{\rm K}
=
\frac12\int dx\left[
\Pi^2+(\partial_x\varphi)^2+V''(f)\varphi^2
\right].
$$ For the present potential, $$
H_3^{\rm K}
=
m\sqrt{\frac{\lambda}{2}}
\int dx\,\tanh\left(\frac{mx}{2}\right):\varphi^3:,
\qquad
H_4^{\rm K}=\frac{\lambda}{4}\int dx:\varphi^4:.
$$ The normal-ordering prescription must be stated. Here it is inherited
from the common regulated theory; when we rewrite the Hamiltonian in
kink modes, the associated contractions must be included.

**Blackboard.**

$$
\begin{array}{c|c|c}
&\text{defining frame}&\text{kink frame}\\ \hline
\text{exact}&H_{\rm def}&H_{\rm K}=\mathcal D_f^\dagger H_{\rm def}\mathcal D_f\\
\text{quadratic}&H_2^{\rm vac}&H_2^{\rm K}
\end{array}
$$

$$
H_{\rm K}=Q_0+H_2^{\rm K}+H_3^{\rm K}+H_4^{\rm K},
\qquad
H_1^{\rm K}=0.
$$

$$
H_2^{\rm K}
=
\frac12\int dx
\left[
\Pi^2+(\partial_x\varphi)^2+V''(f)\varphi^2
\right].
$$

**Spoken text.**

This also explains my preference for the Schrödinger picture. In the
Schrödinger picture, the canonical fields and momenta are
time-independent. The states carry the time evolution: $$
i\partial_t|\Psi\rangle=H|\Psi\rangle.
$$ In the vacuum sector, the natural free Hamiltonian is
$H_2^{\rm vac}$. In the kink sector, the natural free Hamiltonian is
$H_2^{\rm K}$. Each defines a different convenient basis.

The interaction picture is not forbidden. One can define a separate
interaction picture in either sector. The point is that there is no
unique, sector-independent choice of $H_0$ that is equally natural for
both. The Schrödinger picture avoids choosing one of the two quadratic
approximations as the universal free time evolution. It keeps the
canonical algebra fixed and lets the Hamiltonian and the perturbative
basis carry the sector dependence.

**Blackboard.**

$$
H=H_0+H_I,
\qquad
O_I(t)=e^{iH_0t}O_Se^{-iH_0t}.
$$

$$
H_0=H_2^{\rm vac}
\quad\text{or}\quad
H_0=H_2^{\rm K}.
$$

$$
\boxed{
\text{Schrödinger picture: fixed canonical operators; states evolve.}
}
$$

------------------------------------------------------------------------

## The Pöschl--Teller modes define the kink Fock space (83--95)

**Spoken text.**

The kink normal modes solve the linearized equation. Write $$
\varphi(x,t)=g_\alpha(x)e^{-i\omega_\alpha t}.
$$ Then $$
\mathcal K g_\alpha=\omega_\alpha^2g_\alpha,
\qquad
\mathcal K=-\partial_x^2+V''(f(x)).
$$ For the $\phi^4$ kink, $$
\mathcal K
=
-\partial_x^2+m^2
-\frac{3m^2}{2}\operatorname{sech}^2\left(\frac{mx}{2}\right).
$$ This is the reflectionless Pöschl--Teller problem.

There are two bound modes and a continuum. The first bound mode is the
translational zero mode. Differentiating the family $f(x-x_0)$ with
respect to $x_0$ shows that $$
\mathcal K f'(x)=0.
$$ With the sign convention used here, $$
g_B(x)=-\frac{f'(x)}{\sqrt{Q_0}}
=
-\sqrt{\frac{3m}{8}}\,
\operatorname{sech}^2\left(\frac{mx}{2}\right).
$$ It is normalized to one.

The second bound mode is the shape mode: $$
g_S(x)=
\frac{\sqrt{3m}}{2}
\tanh\left(\frac{mx}{2}\right)
\operatorname{sech}\left(\frac{mx}{2}\right),
\qquad
\omega_S=\frac{\sqrt3}{2}m.
$$ The factor $\sqrt{3m}/2$ is required for unit normalization. It is
not $\sqrt{3m/8}$.

The continuum modes can be chosen as $$
g_k(x)=
\frac{e^{-ikx}}{\omega_k\sqrt{m^2+4k^2}}
\left[
2k^2-m^2
+\frac{3m^2}{2}\operatorname{sech}^2\left(\frac{mx}{2}\right)
-3imk\tanh\left(\frac{mx}{2}\right)
\right],
$$ with $$
\omega_k=\sqrt{k^2+m^2}.
$$ They obey $$
\int dx\,g_k^*(x)g_p(x)=2\pi\delta(k-p),
$$ and are orthogonal to the two bound modes.

**Blackboard.**

$$
\mathcal K=-\partial_x^2+m^2
-\frac{3m^2}{2}\operatorname{sech}^2\left(\frac{mx}{2}\right),
\qquad
\mathcal K g_\alpha=\omega_\alpha^2g_\alpha.
$$

$$
g_B(x)=-\sqrt{\frac{3m}{8}}\operatorname{sech}^2\left(\frac{mx}{2}\right),
\qquad \omega_B=0.
$$

$$
g_S(x)=\frac{\sqrt{3m}}{2}
\tanh\left(\frac{mx}{2}\right)\operatorname{sech}\left(\frac{mx}{2}\right),
\qquad
\omega_S=\frac{\sqrt3}{2}m.
$$

$$
\omega_k=\sqrt{k^2+m^2}.
$$

**Spoken text.**

The continuum mode is a plane wave far from the kink, but its profile is
distorted in the kink core. That distortion is what changes the
oscillator basis and produces the squeeze.

For the Fourier transform, I use $$
\widetilde g_\alpha(p)=\int dx\,e^{ipx}g_\alpha(x).
$$ The bound-mode transforms are $$
\widetilde g_B(p)
=
-\frac{\sqrt6\,\pi p}{m^{3/2}}
\operatorname{csch}\left(\frac{\pi p}{m}\right),
$$ $$
\widetilde g_S(p)
=
+\frac{2i\sqrt3\,\pi p}{m^{3/2}}
\operatorname{sech}\left(\frac{\pi p}{m}\right).
$$ For the continuum mode, the transform contains both the asymptotic
plane-wave delta function and the localized scattering contribution: $$
\widetilde g_k(p)
=
\frac{2\pi(2k^2-m^2)}
{\omega_k\sqrt{m^2+4k^2}}\delta(p-k)
+
\frac{6\pi p}
{\omega_k\sqrt{m^2+4k^2}}
\operatorname{csch}\left(\frac{\pi(p-k)}{m}\right).
$$ The two terms must be kept together. The continuum modes are
generalized eigenfunctions, so products of their Fourier transforms are
interpreted with a finite-volume or wave-packet regulator before taking
the infinite-volume limit. One must not square a delta function as an
ordinary function.

**Blackboard.**

$$
\widetilde g_B(p)
=
-\frac{\sqrt6\,\pi p}{m^{3/2}}
\operatorname{csch}\left(\frac{\pi p}{m}\right),
$$

$$
\widetilde g_S(p)
=
-\frac{2i\sqrt3\,\pi p}{m^{3/2}}
\operatorname{sech}\left(\frac{\pi p}{m}\right),
$$

$$
\widetilde g_k(p)
=
\frac{2\pi(2k^2-m^2)}
{\omega_k\sqrt{m^2+4k^2}}\delta(p-k)
+
\frac{6\pi p}
{\omega_k\sqrt{m^2+4k^2}}
\operatorname{csch}\left(\frac{\pi(p-k)}{m}\right).
$$

**Spoken text.**

Completeness gives $$
g_B(x)g_B(y)+g_S(x)g_S(y)
+\int\frac{dk}{2\pi}g_k(x)g_k^*(y)
=\delta(x-y).
$$ We can therefore expand the fluctuation field in this basis: $$
\begin{aligned}
\varphi(x)={}&q_0g_B(x)
+\frac{1}{\sqrt{2\omega_S}}
\left(b_Sg_S(x)+b_S^\dagger g_S(x)\right)\\
&+\int\frac{dk}{2\pi}\frac{1}{\sqrt{2\omega_k}}
\left(b_kg_k(x)+b_k^\dagger g_k^*(x)\right).
\end{aligned}
$$ The momentum expansion is $$
\begin{aligned}
\Pi(x)={}&p_0g_B(x)
-i\sqrt{\frac{\omega_S}{2}}
\left(b_Sg_S(x)-b_S^\dagger g_S(x)\right)\\
&-i\int\frac{dk}{2\pi}\sqrt{\frac{\omega_k}{2}}
\left(b_kg_k(x)-b_k^\dagger g_k^*(x)\right).
\end{aligned}
$$ The canonical commutators are $$
[q_0,p_0]=i,\qquad
[b_S,b_S^\dagger]=1,\qquad
[b_k,b_p^\dagger]=2\pi\delta(k-p).
$$ The zero mode is a canonical pair, not a harmonic oscillator. The
shape and continuum modes are ordinary oscillators.

**Blackboard.**

$$
g_B(x)g_B(y)+g_S(x)g_S(y)
+\int\frac{dk}{2\pi}g_k(x)g_k^*(y)=\delta(x-y).
$$

$$
[q_0,p_0]=i,
\qquad
[b_S,b_S^\dagger]=1,
\qquad
[b_k,b_p^\dagger]=2\pi\delta(k-p).
$$

$$
H_2^{\rm K}
=
Q_1+\frac12p_0^2
+\omega_Sb_S^\dagger b_S
+\int\frac{dk}{2\pi}\omega_kb_k^\dagger b_k.
$$

------------------------------------------------------------------------

## The one-loop correction is the energy of the squeeze (95--105)

**Spoken text.**

The original Hamiltonian is normal ordered with respect to the
plane-wave operators $a_p$. The kink quadratic Hamiltonian is diagonal
in the $b_\alpha$ operators. These are different normal-ordering
prescriptions.

When we rewrite the plane-wave operators in terms of the kink operators,
the transformation contains both creation and annihilation operators: $$
a_p=\sum_\alpha\left(
U_{p\alpha}b_\alpha+V_{p\alpha}b_\alpha^\dagger
\right).
$$ The $V$-term is the squeeze. It is precisely the term that would be
absent if the kink state were only a coherent displacement.

After substituting the mode transformation into the common regulated
Hamiltonian, using the kink mode equation, and normal ordering in the
kink basis, the quadratic Hamiltonian takes the form $$
H_2^{\rm K}
=
Q_1+\frac12p_0^2
+\omega_Sb_S^\dagger b_S
+\int\frac{dk}{2\pi}\omega_kb_k^\dagger b_k.
$$ The c-number $Q_1$ is the one-loop correction. It is the change in
the vacuum energy caused by the change of fluctuation basis. It is not
obtained from the displacement alone.

A compact expression for this contribution is $$
Q_1
=
-\frac14
\sum_{\alpha=B,S,\mathrm{cont}}
\int\frac{dp}{2\pi}\,
|\widetilde g_\alpha(p)|^2
\frac{(\omega_\alpha-\omega_p)^2}{\omega_p},
\qquad
\omega_p=\sqrt{p^2+m^2}.
$$ For the continuum, the mode label $\alpha=k$ is integrated with
$dk/(2\pi)$. The plane-wave delta contribution is treated with the same
finite-volume regulator as the vacuum subtraction; it is not squared
naively. The zero-mode term is obtained by setting $\omega_B=0$.

This formula makes the mechanism visible. If the kink fluctuation
frequencies and wavefunctions were the same as those of the vacuum, the
integrand would vanish. The kink potential changes the spectrum and the
mode functions, so the squeeze lowers the energy.

**Blackboard.**

$$
a_p=\sum_\alpha
\left(U_{p\alpha}b_\alpha+V_{p\alpha}b_\alpha^\dagger\right).
$$

$$
Q_1
=
-\frac14
\sum_{\alpha=B,S,\mathrm{cont}}
\int\frac{dp}{2\pi}\,
|\widetilde g_\alpha(p)|^2
\frac{(\omega_\alpha-\omega_p)^2}{\omega_p}.
$$

$$
\omega_B=0,\qquad
\omega_S=\frac{\sqrt3}{2}m,\qquad
\omega_k=\sqrt{k^2+m^2}.
$$

**Spoken text.**

For this $\phi^4$ kink, the result agrees with the
Dashen--Hasslacher--Neveu correction. In the convention $\beta=m/2$, the
result is $$
Q_1=\beta\left(\frac{1}{2\sqrt3}-\frac{3}{\pi}\right).
$$ Since the $m$ used here is $2\beta$, this is $$
\boxed{
Q_1=m\left(\frac{1}{4\sqrt3}-\frac{3}{2\pi}\right).
}
$$ The correction is finite in $1+1$ dimensions with the stated
normal-ordering prescription. The result is a useful normalization
check. It also shows why the unsqueezed coherent state is insufficient:
it gives the classical energy $Q_0$, while the squeezed state gives
$Q_0+Q_1$.

**Blackboard.**

$$
Q_{\rm kink}
=
\frac{m^3}{3\lambda}
+
m\left(\frac{1}{4\sqrt3}-\frac{3}{2\pi}\right)
+O(\lambda).
$$

$$
\beta=\frac m2,
\qquad
Q_1=\beta\left(\frac{1}{2\sqrt3}-\frac3\pi\right).
$$

**Spoken text.**

A phase-shift calculation gives the same result when the mode number is
regulated consistently. The fluctuation potential is reflectionless. Its
total scattering phase can be written, with a continuous branch chosen
to vanish at large momentum, as $$
\delta(k)=2\arctan\left(\frac{m}{2k}\right)
+2\arctan\left(\frac{m}{k}\right)
$$ up to the branch convention at $k=0$. The density-of-states
difference is proportional to $\delta'(k)$. The one-loop energy is the
sum of the bound-state zero-point contribution and the regulated
continuum density difference, together with the counterterm fixed by the
vacuum renormalization condition. The mode-overlap formula above is the
Hamiltonian version of the same spectral reorganization.

The cutoff must be imposed on the same physical spectrum in the two
sectors. If one uses a box, the mode numbers must be matched before the
box is removed. If one uses a momentum cutoff, the counterterm and the
continuum subtraction must be defined in the same scheme. The finite
answer is not obtained by subtracting two independently regulated sums
with unrelated cutoffs.

------------------------------------------------------------------------

## The zero mode is a collective coordinate, but the nonlinear coordinate is constrained (105--109)

**Spoken text.**

The translational zero mode exists because the kink can be centered
anywhere. The family of classical solutions is $f(x-x_0)$. Expanding for
small $x_0$, $$
f(x-x_0)=f(x)-x_0f'(x)+O(x_0^2).
$$ Since $$
g_B(x)=-\frac{f'(x)}{\sqrt{Q_0}},
$$ the zero-mode part of the fluctuation is $$
\varphi_B(x)=q_0g_B(x)
$$ and therefore $$
q_0\simeq\sqrt{Q_0}\,x_0.
$$ The sign is fixed by the chosen sign of $g_B$. Define $$
X=\frac{q_0}{\sqrt{Q_0}},
\qquad
P=\sqrt{Q_0}\,p_0.
$$ Then $$
[X,P]=i,
\qquad
\frac12p_0^2=\frac{P^2}{2Q_0}.
$$ At this order the kink behaves as a particle of mass $Q_0$.

There is a subtle point. The relation $q_0\simeq\sqrt{Q_0}x_0$ is the
linearized relation. In a nonlinear collective-coordinate decomposition,
$$
\Phi(x)=f(x-X)+\eta(x-X),
$$ one usually imposes an orthogonality condition such as $$
\int dx\,\eta(x)f'(x-X)=0
$$ to avoid counting the translation mode twice. The coordinate $X$ is
then a nonlinear functional of the field, and it is constrained by the
orthogonality condition. It is not automatically an independent
canonical coordinate with the naive commutator. A full
collective-coordinate treatment requires the induced symplectic form or
Dirac brackets and the associated Jacobian in the measure.

LSPT uses the linear projection onto the normalized zero mode. At this
order $q_0,p_0$ form an ordinary canonical pair. The nonlinear
collective-coordinate subtleties enter when one goes beyond the
linearized treatment.

**Blackboard.**

$$
f(x-X)=f(x)-Xf'(x)+O(X^2),
\qquad
g_B=-\frac{f'}{\sqrt{Q_0}}.
$$

$$
q_0\simeq\sqrt{Q_0}X,
\qquad
P=\sqrt{Q_0}p_0,
\qquad
[X,P]=i.
$$

$$
\frac12p_0^2=\frac{P^2}{2Q_0}.
$$

$$
\int dx\,\eta(x)f'(x-X)=0
\quad
\text{(nonlinear collective-coordinate constraint)}.
$$

**Spoken text.**

The formal state with $P=0$ is a momentum eigenstate of the kink centre.
It is not normalizable. A physical state can be a wave packet in $X$,
with a small but nonzero momentum spread. The limit of a sharply
localized momentum eigenstate is useful for computing the rest energy,
but it should be understood as a generalized state.

------------------------------------------------------------------------

## The first correction to the kink wavefunction follows from the Schrödinger equation (109--112)

**Spoken text.**

The squeeze gives the Gaussian ground state of the quadratic kink
Hamiltonian. The cubic and quartic interactions correct this state. I
will derive the first correction, because it is the cleanest way to see
what "wavefunction correction" means in LSPT.

Write $$
H_{\rm K}=Q_0+H_2^{\rm K}+\epsilon H_3+\epsilon^2H_4+\cdots,
$$ where $\epsilon$ is a bookkeeping parameter. In the present
normalization $H_3$ is proportional to $\sqrt\lambda$, while $H_4$ is
proportional to $\lambda$.

Let $|0\rangle_{\rm K}$ be the Gaussian vacuum of the nonzero kink
modes. Expand $$
|\Omega\rangle
=
|0\rangle_{\rm K}
+\epsilon|\Omega_1\rangle
+\epsilon^2|\Omega_2\rangle+\cdots,
$$ $$
E=E_0+\epsilon E_1+\epsilon^2E_2+\cdots.
$$ Substituting into $$
H_{\rm K}|\Omega\rangle=E|\Omega\rangle
$$ and collecting first-order terms gives $$
(H_2^{\rm K}-E_0)|\Omega_1\rangle
=
-(H_3-E_1)|0\rangle_{\rm K}.
$$ Choose intermediate normalization, $$
{}_{\rm K}\langle0|\Omega_1\rangle=0.
$$ Then $$
E_1={}_{\rm K}\langle0|H_3|0\rangle_{\rm K}.
$$ For a normal-ordered cubic interaction this expectation value
vanishes. Expanding in excited eigenstates $|n\rangle$ of $H_2^{\rm K}$,
we obtain $$
\boxed{
|\Omega_1\rangle
=
-\sum_{n\ne0}
|n\rangle
\frac{{}_{\rm K}\langle n|H_3|0\rangle_{\rm K}}
{E_n-E_0}.
}
$$ This is ordinary Rayleigh--Schrödinger perturbation theory, but the
intermediate states are kink normal-mode states.

**Blackboard.**

$$
H_{\rm K}=Q_0+H_2^{\rm K}+\epsilon H_3+\epsilon^2H_4+\cdots.
$$

$$
|\Omega\rangle=|0\rangle_{\rm K}+\epsilon|\Omega_1\rangle+\cdots,
\qquad
E=E_0+\epsilon E_1+\cdots.
$$

$$
(H_2^{\rm K}-E_0)|\Omega_1\rangle
=-(H_3-E_1)|0\rangle_{\rm K}.
$$

$$
|\Omega_1\rangle
=
-\sum_{n\ne0}|n\rangle
\frac{\langle n|H_3|0\rangle}{E_n-E_0}.
$$

**Spoken text.**

For the shifted $\phi^4$ potential, $$
V'''(f(x))
=
3\sqrt{2\lambda}\,m
\tanh\left(\frac{mx}{2}\right),
$$ so $$
H_3
=
\frac1{3!}\int dx\,V'''(f(x)):\varphi^3(x):
=
m\sqrt{\frac{\lambda}{2}}
\int dx\,\tanh\left(\frac{mx}{2}\right):\varphi^3(x):.
$$ Insert the normal-mode expansion of $\varphi$. Define the cubic
vertex $$
\mathcal V_{\alpha\beta\gamma}
=
\int dx\,
V'''(f(x))g_\alpha(x)g_\beta(x)g_\gamma(x).
$$ The part of $H_3$ that acts nontrivially on the Gaussian vacuum
creates three nonzero-mode quanta: $$
H_3|0\rangle_{\rm K}
=
\frac1{3!}
\sum_{\alpha\beta\gamma}'\!
\frac{\mathcal V_{\alpha\beta\gamma}}
{\sqrt{8\omega_\alpha\omega_\beta\omega_\gamma}}
b_\alpha^\dagger b_\beta^\dagger b_\gamma^\dagger
|0\rangle_{\rm K}.
$$ The prime means that the translational zero mode is not included as
an oscillator. The sum includes the shape mode and the continuum, with
continuum integrals understood.

The first wavefunction correction is therefore $$
|\Omega_1\rangle
=
-\frac1{3!}
\sum_{\alpha\beta\gamma}'\!
\frac{\mathcal V_{\alpha\beta\gamma}}
{\sqrt{8\omega_\alpha\omega_\beta\omega_\gamma}
(\omega_\alpha+\omega_\beta+\omega_\gamma)}
b_\alpha^\dagger b_\beta^\dagger b_\gamma^\dagger
|0\rangle_{\rm K}.
$$ This is the first non-Gaussian correction to the kink state. In the
Schrödinger representation, its wave functional is obtained by taking
the field-configuration matrix element of this state. It is a cubic
polynomial functional multiplying the Gaussian
$\Psi_{\rm K}^{(0)}[\varphi]$.

At higher orders, quartic vertices, repeated cubic vertices,
counterterms, and the zero-mode constraints all contribute. The
important point is that the correction is calculated in the kink
normal-mode basis. A plane-wave expansion would obscure the energy
denominators and the sector-specific intermediate states.

**Blackboard.**

$$
H_3
=
\frac1{3!}\int dx\,V'''(f):\varphi^3:,
\qquad
\mathcal V_{\alpha\beta\gamma}
=
\int dx\,V'''(f)g_\alpha g_\beta g_\gamma.
$$

$$
|\Omega_1\rangle
=
-\frac1{3!}
\sum_{\alpha\beta\gamma}'\!
\frac{\mathcal V_{\alpha\beta\gamma}}
{\sqrt{8\omega_\alpha\omega_\beta\omega_\gamma}
(\omega_\alpha+\omega_\beta+\omega_\gamma)}
b_\alpha^\dagger b_\beta^\dagger b_\gamma^\dagger
|0\rangle_{\rm K}.
$$

**Spoken text.**

The word "wavefunction" here refers to the state functional in the kink
frame. It should not be confused with the field-strength renormalization
constant $Z_\phi$. The latter is a parameter in the renormalized field
definition. The expression above is the perturbative correction to the
kink state itself.

The same expansion gives the second-order energy: $$
E_2
=
\langle0|H_4|0\rangle
-
\sum_{n\ne0}
\frac{|\langle n|H_3|0\rangle|^2}{E_n-E_0}
+
\langle0|H_{\rm ct}^{(2)}|0\rangle,
$$ with the counterterm contribution and normal-ordering conversions
fixed by the common renormalization prescription. This is the general
form. An explicit mode-integral formula depends on the spacetime
dimension and on how the wall-parallel momenta are organized. A formula
with $d^3k$ phase space must not be presented as a $1+1$-dimensional
kink formula.

**Blackboard.**

$$
E_2
=
\langle0|H_4|0\rangle
-
\sum_{n\ne0}
\frac{|\langle n|H_3|0\rangle|^2}{E_n-E_0}
+
\langle0|H_{\rm ct}^{(2)}|0\rangle.
$$

------------------------------------------------------------------------

## The $3+1$-dimensional wall: the squeeze cancels the one-loop tension divergence (112--120)

**Spoken text.**

The $1+1$-dimensional kink is the cleanest place to derive the mode
basis. The higher-dimensional wall shows why the squeeze is not
optional.

Take a flat wall in $3+1$ dimensions, with $x$ the coordinate normal to
the wall and $\mathbf y=(y,z)$ the coordinates along it. The classical
profile is still $$
f(x)=\frac{m}{\sqrt{2\lambda}}
\left[1+\tanh\left(\frac{mx}{2}\right)\right],
$$ and the classical tension per unit area is $$
\rho_0=\frac{m^3}{3\lambda}.
$$ The normal modes factorize: $$
g_{k_x,\mathbf k_\parallel}(x,\mathbf y)
=
g_{k_x}(x)e^{-i\mathbf k_\parallel\cdot\mathbf y}.
$$ Their frequencies are $$
\omega_{B,\mathbf k_\parallel}=|\mathbf k_\parallel|,
$$ $$
\omega_{S,\mathbf k_\parallel}
=
\sqrt{\frac{3m^2}{4}+\mathbf k_\parallel^2},
$$ $$
\omega_{k_x,\mathbf k_\parallel}
=
\sqrt{m^2+k_x^2+\mathbf k_\parallel^2}.
$$ The zero-mode branch is gapless along the wall. The single point
$k_x=0,\mathbf k_\parallel=0$ is the global translation mode.

The squeeze contribution to the tension is the higher-dimensional
version of the same mode-overlap expression: \[ `\rho`{=tex}\_1 =
-`\frac14`{=tex}`\left[
\sum_{\alpha=B,S}
\int\frac{d^3p}{(2\pi)^3}
\left|\widetilde g_{\alpha}(p_x)\right|^2
\frac{
\left(\omega_{\alpha,\mathbf p_\parallel}
-\omega_{\mathbf p}\right)^2
}{
\omega_{\mathbf p}
}
+
\int\frac{dk_x}{2\pi}
\int\frac{d^3p}{(2\pi)^3}
\left|\widetilde g_{k_x}(p_x)\right|^2
\frac{
\left(\omega_{k_x,\mathbf p_\parallel}
-\omega_{\mathbf p}\right)^2
}{
\omega_{\mathbf p}
}
\right]`{=tex}

\] where $$
\omega_{\mathbf p}
=
\sqrt{m^2+p_x^2+p_y^2+p_z^2}.
$$ For the continuum, the $k_x$ label is integrated. For the two bound
modes, the sum replaces that integral. The same UV regulator is used in
every term.

After the normal-mode integrals are evaluated, the logarithmic part is
$$
\rho_1
=
-\frac{3m^3}{16\pi^2}
\ln\left(\frac{\Lambda}{m}\right)
+\text{finite}.
$$ This is the one-loop energy decrease due to squeezing.

**Blackboard.**

$$
\rho_0=\frac{m^3}{3\lambda}.
$$

$$
\omega_{B,\mathbf k_\parallel}=|\mathbf k_\parallel|,
\quad
\omega_{S,\mathbf k_\parallel}
=
\sqrt{\frac{3m^2}{4}+\mathbf k_\parallel^2},
\quad
\omega_{k_x,\mathbf k_\parallel}
=
\sqrt{m^2+k_x^2+\mathbf k_\parallel^2}.
$$

$$
\rho_1
=
-\frac14\left[
\sum_{\alpha=B,S}
\int\frac{d^3p}{(2\pi)^3}
|\widetilde g_{\alpha}(p_x)|^2
\frac{(\omega_{\alpha,\mathbf p_\parallel}-\omega_{\mathbf p})^2}
{\omega_{\mathbf p}}
+
\int\frac{dk_x}{2\pi}
\int\frac{d^3p}{(2\pi)^3}
|\widetilde g_{k_x}(p_x)|^2
\frac{(\omega_{k_x,\mathbf p_\parallel}-\omega_{\mathbf p})^2}
{\omega_{\mathbf p}}
\right].
$$

$$
\boxed{
\rho_1
=
-\frac{3m^3}{16\pi^2}
\ln\left(\frac{\Lambda}{m}\right)
+\text{finite}
}
$$

**Spoken text.**

Let me separate this logarithm from the local tadpole divergence that
appears if we evaluate the unsqueezed coherent state before
renormalization.

For a vacuum Gaussian of mass $m$, $$
C_\Lambda
=
\langle0|\varphi^2(x)|0\rangle_\Lambda
=
\int_{|\mathbf p|<\Lambda}
\frac{d^3p}{(2\pi)^3}\frac1{2\sqrt{\mathbf p^2+m^2}}.
$$ The radial integral gives $$
C_\Lambda
=
\frac1{8\pi^2}
\left[
\Lambda\sqrt{\Lambda^2+m^2}
-m^2\ln\left(
\frac{\Lambda+\sqrt{\Lambda^2+m^2}}{m}
\right)
\right].
$$ At large cutoff, $$
C_\Lambda
=
\frac{\Lambda^2}{8\pi^2}
-\frac{m^2}{8\pi^2}\ln\left(\frac{2\Lambda}{m}\right)
+O(1).
$$ The factor $1/(8\pi^2)$ follows from the measure $d^3p/(2\pi)^3$ and
the factor $1/(2\omega_p)$.

In the kink background, the quadratic coefficient differs from its
vacuum value: $$
V''(f)-m^2
=
-\frac{3m^2}{2}\operatorname{sech}^2\left(\frac{mx}{2}\right).
$$ After subtracting the homogeneous vacuum contribution, the unsqueezed
Gaussian therefore leaves the local term $$
\delta\mathcal H_{\rm coh}(x)
=
\frac12[V''(f(x))-m^2]C_\Lambda
\sim
-\frac{3m^2\Lambda^2}{32\pi^2}
\operatorname{sech}^2\left(\frac{mx}{2}\right)
+\cdots.
$$ This is the local tadpole or mass-renormalization divergence. It must
be canceled by the usual local counterterms in the renormalized
Hamiltonian. It is not the logarithmic tension divergence displayed in
the previous equation. The two must not be confused.

Once the ordinary vacuum counterterms have been imposed, the
coherent-state tension still has a logarithmic divergence from
expressing the bare parameters in terms of the renormalized ones. The
squeeze contribution $\rho_1$ cancels that remaining logarithm.

**Blackboard.**

$$
C_\Lambda
=
\int_{|\mathbf p|<\Lambda}
\frac{d^3p}{(2\pi)^3}\frac1{2\sqrt{\mathbf p^2+m^2}}
$$

$$
C_\Lambda
=
\frac1{8\pi^2}
\left[
\Lambda\sqrt{\Lambda^2+m^2}
-m^2\ln\left(
\frac{\Lambda+\sqrt{\Lambda^2+m^2}}{m}
\right)
\right]
$$

$$
C_\Lambda
=
\frac{\Lambda^2}{8\pi^2}
-\frac{m^2}{8\pi^2}\ln\left(\frac{2\Lambda}{m}\right)+O(1).
$$

$$
\delta\mathcal H_{\rm coh}(x)
=
\frac12[V''(f)-m^2]C_\Lambda
\sim
-\frac{3m^2\Lambda^2}{32\pi^2}
\operatorname{sech}^2\left(\frac{mx}{2}\right).
$$

**Spoken text.**

Now write the bare parameters as $$
m_0^2=m^2-\delta m^2,
\qquad
\sqrt{\lambda_0}=\sqrt\lambda-\delta\sqrt\lambda.
$$ After the local power-divergent tadpole has been absorbed into the
vacuum mass counterterm (or subtracted by the equivalent normal-ordering
prescription), the remaining logarithmic counterterms in the cutoff
convention used for this one-loop calculation are $$
\frac{\delta m^2}{\lambda m^2}
=
-\frac{9}{8\pi^2}\ln\left(\frac{\Lambda}{m}\right)
+\text{finite},
$$ $$
\frac{\delta\sqrt\lambda}{\lambda\sqrt\lambda}
=
-\frac{9}{16\pi^2}\ln\left(\frac{\Lambda}{m}\right)
+\text{finite}.
$$ Expand the bare classical tension: $$
\frac{m_0^3}{3\lambda_0}
=
\frac{m^3}{3\lambda}
\left[
1-\frac32\frac{\delta m^2}{m^2}
+2\frac{\delta\sqrt\lambda}{\sqrt\lambda}
\right]
+\cdots.
$$ Substituting the counterterms gives $$
\rho_{\rm coh}
=
\frac{m^3}{3\lambda}
+
\frac{3m^3}{16\pi^2}
\ln\left(\frac{\Lambda}{m}\right)
+\text{finite}.
$$ This is the residual logarithm in the renormalized coherent-state
tension.

The squeeze contributes the opposite term: $$
\rho_1
=
-\frac{3m^3}{16\pi^2}
\ln\left(\frac{\Lambda}{m}\right)
+\text{finite}.
$$ Therefore $$
\rho_{\rm wall}
=
\rho_{\rm coh}+\rho_1
=
\frac{m^3}{3\lambda}+\text{finite}
$$ at this order.

The cancellation is a one-loop result in the stated scheme. It is not an
all-orders proof that every domain-wall observable is finite without
further renormalization. The local power divergence and the remaining
logarithmic tension divergence have different origins and are canceled
at different stages: the ordinary local counterterms remove the former,
while the squeeze supplies the one-loop energy correction that cancels
the latter.

**Blackboard.**

$$
m_0^2=m^2-\delta m^2,
\qquad
\sqrt{\lambda_0}=\sqrt\lambda-\delta\sqrt\lambda.
$$

$$
\frac{\delta m^2}{\lambda m^2}
=
-\frac{9}{8\pi^2}\ln\frac{\Lambda}{m}
+\text{finite},
\qquad
\frac{\delta\sqrt\lambda}{\lambda\sqrt\lambda}
=
-\frac{9}{16\pi^2}\ln\frac{\Lambda}{m}
+\text{finite}.
$$

$$
\frac{m_0^3}{3\lambda_0}
=
\frac{m^3}{3\lambda}
\left[
1-\frac32\frac{\delta m^2}{m^2}
+2\frac{\delta\sqrt\lambda}{\sqrt\lambda}
\right]+\cdots
$$

$$
\rho_{\rm coh}
=
\frac{m^3}{3\lambda}
+
\frac{3m^3}{16\pi^2}\ln\frac{\Lambda}{m}
+\text{finite},
$$

$$
\rho_1
=
-\frac{3m^3}{16\pi^2}\ln\frac{\Lambda}{m}
+\text{finite}.
$$

$$
\boxed{
\rho_{\rm wall}
=
\rho_{\rm coh}+\rho_1
=
\frac{m^3}{3\lambda}+\text{finite}
\quad\text{at one loop}.
}
$$

**Spoken text.**

The dimension matters. In $1+1$ dimensions, the squeezed correction to
the kink mass is finite with normal ordering. In $2+1$ dimensions, the
one-loop wall correction is finite and the first divergence appears at
higher order. In $3+1$ dimensions, the one-loop squeeze is required to
cancel the logarithmic tension divergence. This is why the
coherent-state approximation can be useful in low dimensions but is not
an acceptable final state for the $3+1$-dimensional wall.

------------------------------------------------------------------------

## References and source notes

1.  T. H. R. Skyrme, "A Non-Linear Theory of Strong Interactions,"
    *Proceedings of the Royal Society A* **247** (1958) 260--278.
2.  F. J. Dyson, "Divergence of Perturbation Theory in Quantum
    Electrodynamics," *Physical Review* **85** (1952) 631--632.
3.  R. Haag, "On Quantum Field Theories," *Matematisk-fysiske
    Meddelelser* **29**, no. 12 (1955); D. Hall and A. S. Wightman, "A
    Theorem on Invariant Analytic Functions with Applications to
    Relativistic Quantum Field Theory," *Matematisk-fysiske Meddelelser*
    **31**, no. 5 (1957).
4.  J. Glimm and A. Jaffe, *Quantum Physics: A Functional Integral Point
    of View*, 2nd ed., Springer (1987), for constructive $P(\phi)_2$
    theory and the $\phi^4_2$ example.
5.  S. Coleman, "Classical Lumps and Their Quantum Descendants," Erice
    lectures (1975; published in *Subnuclear Phenomena*, 1977).
6.  R. F. Dashen, B. Hasslacher, and A. Neveu, "Nonperturbative Methods
    and Extended-Hadron Models in Field Theory. II. Two-Dimensional
    Models and Extended Hadrons," *Physical Review D* **10** (1974)
    4130.
7.  J. Evslin, "Manifestly Finite Derivation of the Quantum Kink Mass,"
    arXiv:1908.06710 (2019).
8.  K. E. Cahill, A. Comtet, and R. J. Glauber, "Mass Formulas for
    Static Solitons," *Physics Letters B* **64** (1976) 283--285.
9.  J. Evslin, "Quantum Domain Walls Must Be Squeezed," *Bulgarian
    Journal of Physics* **52** (2025) 13--17,
    doi:10.55318/bgjp.2025.52.s1.013.
10. K. Ogundipe, J. Evslin, B. Zhang, and H. Guo, "A (2+1)-Dimensional
    Domain Wall at One-Loop," *Journal of High Energy Physics*
    **05** (2024) 098, arXiv:2403.14062.
11. J. Evslin, H. Guo, H. Liu, and B. Zhang, "A Finite Tension for the
    $\phi^4_4$ Domain Wall," *Physics Letters B* **864** (2025) 139457,
    arXiv:2411.05406.
12. B. Zhang, "A Passive Perspective of Linearized Soliton Perturbation
    Theory" (13 December 2025), together with the notes on kink mass
    corrections and finite-tension domain walls (2024).

------------------------------------------------------------------------

## Notes for the speaker

-   The displacement sign convention is fixed by
    $\mathcal D_f^\dagger\Phi\mathcal D_f=\Phi+f$. Its inverse is
    $\mathcal D_f\Phi\mathcal D_f^\dagger=\Phi-f$. Keep both equations
    visible when changing frames.
-   The one-loop kink mass quoted here uses $m$ as the vacuum meson mass
    and $\beta=m/2$. This avoids the factor-of-two ambiguity in formulas
    that call $\beta$ by the name $m$.
-   The normalized shape mode is $\sqrt{3m}/2\,\tanh(mx/2)\sech(mx/2)$.
    The zero mode is $-\sqrt{3m/8}\,\sech^2(mx/2)$.
-   The continuum Fourier transform contains a plane-wave delta term and
    a localized csch term. Do not omit the delta term or square it
    outside a common regulator.
-   The sheaf sequence is a local Borel--Ritt model for sectorial
    asymptotic functions. Do not present it as a theorem about the full
    observable algebra of an arbitrary QFT.
-   Haag's theorem is context for representation dependence. It does not
    prove by itself that all topological sectors are inequivalent.
-   The local $\Lambda^2$ term in the unsqueezed $3+1$-dimensional
    energy density is a tadpole/mass-renormalization divergence. The
    squeeze cancels the residual logarithmic one-loop wall-tension
    divergence after the ordinary counterterms are included.
-   The relation $q_0\simeq\sqrt{Q_0}X$ is linearized. The exact
    nonlinear collective-coordinate construction has a constraint and a
    nontrivial measure.
