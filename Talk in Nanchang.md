# From the Passive Perspective to Linearized Soliton Perturbation Theory

## Quantization of Kinks and Its Challenges


# Part 0. Introduction and motivation (0–10 min)

### 0.1 The central question

Today I want to discuss a fundamental problem in quantum field theory: how do we quantize a classical soliton?

We know that perturbative quantum field theory is extremely successful when we deal with small fluctuations around a homogeneous vacuum. We construct a Fock space, introduce creation and annihilation operators, and calculate quantum corrections order by order.

However, a soliton is fundamentally different. It is a nonperturbative classical configuration, and the ordinary perturbative construction around the vacuum does not seem to be adequate for describing it.

The question is therefore:

**How do we construct a quantum state corresponding to a classical kink, and how do we develop a consistent perturbation theory around this state?**

There are several approaches to this problem. Today I will concentrate on the Hamiltonian approach, Linearized Soliton Perturbation Theory, or LSPT.

Before introducing LSPT, I want to explain three difficulties associated with the traditional construction:

1. The Hilbert-space problem.
    
2. Coleman's divergence problem.
    
3. The regularization mismatch problem.
    

These problems will motivate the formalism that I will introduce in the second half.

### 0.2 The classical kink

Let us consider a real scalar field in (1+1) dimensions, with Hamiltonian

$$
H=\int dx\left[  
\frac12\pi^2+  
\frac12(\partial_x\phi)^2+  
U(\phi)  
\right],  
$$

where

$$U(\phi)=\frac{\lambda}{4}(\phi^2-v^2)^2.  $$


We have two degenerate vacua:

[  
\phi_{\mathrm{vac}}=\pm v.  
]

The mass of small fluctuations around either vacuum is

[  
m^2=U''(\pm v)=2\lambda v^2.  
]

The theory admits a static kink solution,

[  
f(x)=v\tanh\left(\frac{mx}{2}\right).  
]

Its classical mass is

[  
Q_0=\frac{m^3}{3\lambda}.  
]

Notice something important:

[  
f(x)\sim \frac{1}{\sqrt{\lambda}}.  
]

The classical kink is inversely proportional to the square root of the coupling. It is therefore intrinsically nonperturbative in (\lambda).

This is already a warning sign. Ordinary perturbation theory is constructed by expanding around a configuration whose fluctuations are small. The kink itself is not a small fluctuation around the vacuum.

**The challenge is to find a new perturbative organization in which the kink becomes the background and the fluctuations around it become perturbative.**

---

# Part I. Three problems with traditional kink quantization

# 1. The Hilbert-space problem (10–25 min)

### 1.1 How do we construct the vacuum-sector Hilbert space?

Let me first recall the standard construction of the vacuum sector.

After shifting the field around one of the homogeneous vacua, we can expand the fluctuation field in plane waves:

[  
\eta(x)=  
\int\frac{dp}{2\pi}  
\frac{1}{\sqrt{2\omega_p}}  
\left(  
a_p e^{ipx}  
+a_p^\dagger e^{-ipx}  
\right),  
]

where

[  
\omega_p=\sqrt{p^2+m^2}.  
]

The creation and annihilation operators satisfy

[  
[a_p,a_q^\dagger]=2\pi\delta(p-q).  
]

The vacuum is defined by

[  
a_p|0\rangle=0.  
]

The vacuum-sector Fock space is constructed by acting on this vacuum with a finite number of creation operators.

Everything is straightforward.

The reason this construction works is that the field moments are small in the perturbative vacuum. We can organize calculations according to powers of the fluctuation field.

### 1.2 Why does this fail for a kink?

Now consider the kink sector.

The expectation value of the field should be approximately

[  
\langle K|\phi(x)|K\rangle=f(x).  
]

But (f(x)) is not small.

The perturbative vacuum is constructed around a homogeneous configuration, whereas the kink sector consists of configurations close to the nontrivial function (f(x)).

The natural decomposition should be

[  
\phi(x)=f(x)+\eta_K(x),  
]

where (\eta_K) represents small fluctuations around the kink.

In other words, the small quantity is not (\phi(x)), but rather

[  
\phi(x)-f(x).  
]

This suggests that we need a different Fock-space construction.

We should distinguish two sectors:

**Vacuum sector:**

{\text{vacuum and finite numbers of mesons}}.  
]

The mesons are constructed using plane-wave creation operators.

**Kink sector:**

{\text{one kink and finite numbers of mesons}}.  
]

The mesons should be constructed using normal modes around the kink.

The important point is that these are two different perturbative organizations of the quantum theory.

There is also a more fundamental mathematical issue.

In ordinary quantum mechanics, the Stone–von Neumann theorem tells us that, under the usual assumptions, irreducible representations of the finite-dimensional canonical commutation relations are unitarily equivalent.

However, in quantum field theory, we have infinitely many degrees of freedom.

The situation changes dramatically. Different representations of the canonical commutation relations need not be unitarily equivalent.

The Fock representation is only one possible representation.

The choice of representation is therefore not merely a mathematical convenience. It is related to the physical state and the dynamics that we want to describe.

This connects to Haag's theorem and the broader question of whether a single Fock representation is sufficient for describing all sectors of an interacting quantum field theory.

I do not want to go into the mathematical details of Haag's theorem today. My point is simply that we should not take the vacuum Fock space as the unique and universal starting point for every quantum state.

The kink sector requires its own appropriate perturbative construction.

**Transition:**

Now, one might argue that we can simply use a coherent state to construct the kink. Indeed, this is the traditional proposal. But this brings us to the second problem.

---

# 2. Coleman's divergence problem (25–40 min)

### 2.1 The coherent-state construction

The intuitive idea is very simple.

We want a quantum state whose expectation value of the field reproduces the classical kink profile.

In quantum mechanics, we know how to construct coherent states using displacement operators.

The same idea can be applied to quantum field theory.

Define

[  
D_f=  
\exp\left[  
-i\int dx,f(x)\pi(x)  
\right].  
]

Acting on the vacuum, we obtain

[  
|K\rangle_{\mathrm{coh}}=D_f|0\rangle.  
]

Using the canonical commutation relation, we find

[  
D_f^\dagger\phi(x)D_f=\phi(x)+f(x).  
]

Consequently,

[  
\begin{aligned}  
\langle K|\phi(x)|K\rangle  
&=  
\langle 0|D_f^\dagger\phi(x)D_f|0\rangle\  
&=  
\langle 0|\phi(x)+f(x)|0\rangle\  
&=f(x).  
\end{aligned}  
]

At least at leading order, this is exactly what we want.

The coherent state has the correct classical expectation value.

So what is wrong with it?

### 2.2 Coleman's observation

In his famous 1975 Erice lectures, Sidney Coleman pointed out that the conventional coherent-state construction works beautifully in (1+1) dimensions but encounters serious difficulties in higher dimensions.

In particular, the expectation value of the Hamiltonian density becomes ultraviolet divergent.

He challenged the community to find the correct quantum states corresponding to solitons in higher dimensions.

The important question is:

**Why does the coherent-state construction fail?**

### 2.3 The physical origin of the problem

The problem is that shifting the expectation value of the field is not enough.

A coherent state changes the one-point function of the field, but it does not change the fluctuation structure of the vacuum.

Let me explain this.

In the vacuum sector, the elementary excitations are plane waves.

However, in the kink sector, the elementary excitations are normal modes of the fluctuation operator

[  
\mathcal K=-\partial_x^2+U''(f(x)).  
]

These are different sets of modes.

The vacuum is annihilated by the plane-wave annihilation operators (a_p), whereas the correct kink ground state should be annihilated by the normal-mode annihilation operators (b_\alpha).

In general,

[  
b_\alpha\neq  
\int dp,\alpha_{\alpha p}a_p.  
]

More generally, the two sets of operators are related by a Bogoliubov transformation:

[  
b_\alpha=  
\int dp\left(  
\alpha_{\alpha p}a_p+  
\beta_{\alpha p}a_p^\dagger  
\right).  
]

The appearance of creation operators in this transformation means that the vacuum defined by (a_p) is not the vacuum defined by (b_\alpha).

This is the key point.

The coherent state gives us the correct classical background, but its fluctuations are not in the correct ground state.

### 2.4 The squeezed coherent state

A Bogoliubov transformation is implemented by a squeeze operator.

Therefore, the correct quantum state should not be an ordinary coherent state. It should be a squeezed coherent state.

Schematically,

[  
\boxed{  
|K\rangle\sim D_f S_f|0\rangle.  
}  
]

Here:

- (D_f) produces the classical kink profile.
    
- (S_f) changes the quantum fluctuations so that they are appropriate to the kink background.
    

The squeeze operator is not an arbitrary correction. It is required because the normal modes around the kink differ from plane waves.

In the (3+1)-dimensional (\phi^4) domain-wall problem, the leading squeeze is sufficient to eliminate the one-loop divergence associated with Coleman's problem.

I will return to this result later.

For now, the important lesson is:

[  
\boxed{  
\text{Correct classical background}  
\neq  
\text{Correct quantum state}.  
}  
]

We must get both the mean field and the fluctuation structure right.

**Transition:**

Even if we solve the problem of constructing the correct state, there is another issue. We still need to make sure that the kink sector and vacuum sector describe the same regularized quantum theory.

---

# 3. The regularization mismatch problem (40–53 min)

### 3.1 The classical field shift

In classical field theory, the standard procedure is straightforward.

We write

[  
\phi(x)=f(x)+\eta(x),  
]

and define a shifted Hamiltonian

[  
H'[\eta,\pi]=H[\eta+f,\pi].  
]

This is simply a change of variables.

There is no difficulty at the classical level.

But quantum field theory introduces an additional complication: ultraviolet divergences.

The Hamiltonian must be regularized.

### 3.2 Two independently regularized Hamiltonians

Suppose we regularize the vacuum Hamiltonian using a cutoff (\Lambda):

[  
H_\Lambda[\phi,\pi].  
]

We then construct the shifted Hamiltonian and regularize it independently, using another cutoff (\Lambda'):

[  
H'_{\Lambda'}[\eta,\pi].  
]

The problem is that, in general,

[  
H'_{\Lambda'}[\eta,\pi]  
\neq  
H_\Lambda[\eta+f,\pi].  
]

Why?

Because a regularization prescription need not be invariant under the field shift.

For example, normal ordering is defined with respect to a particular set of creation and annihilation operators. Changing the background changes the natural mode decomposition.

Similarly, a momentum cutoff imposed in one basis does not necessarily correspond to the same cutoff after a nontrivial change of variables.

Consequently, we have introduced two independently regulated Hamiltonians.

### 3.3 The ambiguity in the kink mass

Suppose we calculate the kink mass by subtracting the vacuum energy:

E_K(\Lambda')-E_{\mathrm{vac}}(\Lambda).  
]

The result can depend on both cutoffs.

More seriously, the limit

[  
\Lambda,\Lambda'\longrightarrow\infty  
]

can depend on the direction along which we approach infinity in the ((\Lambda,\Lambda')) plane.

This is clearly unacceptable.

The physical theory is defined by the original Hamiltonian. We should not obtain different physical masses by choosing different ways to remove two independent regulators.

The problem is not simply a freedom in the finite part of a renormalization prescription. We have not guaranteed that the two calculations correspond to the same regulated theory.

### 3.4 What do we need?

The lesson is straightforward:

**We should regularize the quantum theory only once.**

The kink Hamiltonian should be constructed from the original regularized Hamiltonian, rather than being independently regularized.

This observation will lead us directly to the displacement-operator construction of LSPT.

---

# Part II. Linearized Soliton Perturbation Theory

# 4. The passive perspective and the displacement operator (58–76 min)

This is the most important conceptual part of the talk.

I want to introduce LSPT from a slightly different perspective.

Rather than immediately treating the displacement operator as a device that creates a new quantum state, I want to interpret it as a passive transformation.

### 4.1 Active versus passive transformations

Let us first recall the distinction between active and passive transformations.

Consider ordinary quantum mechanics.

A spatial translation can be implemented by

[  
T(a)=e^{-ia\hat P}.  
]

There are two ways to interpret this transformation.

In the active interpretation, we keep the coordinate system fixed and translate the physical state.

In the passive interpretation, we keep the physical state unchanged but change the coordinate system used to describe it.

Both descriptions are mathematically equivalent, provided that we transform the relevant quantities consistently.

The same idea applies to the displacement operator in quantum field theory.

Define

[  
\boxed{  
D_f=  
\exp\left[  
-i\int dx,f(x)\pi(x)  
\right].  
}  
]

Using the canonical commutation relation,

[  
[\phi(x),\pi(y)]=i\delta(x-y),  
]

we obtain

\phi(x)+f(x).  
}  
]

Similarly,

[  
D_f^\dagger\pi(x)D_f=\pi(x).  
]

The displacement operator translates us in the space of field configurations.

It does not translate the spatial coordinate (x). Instead, it shifts the field configuration by the function (f(x)).

### 4.2 The passive interpretation

Now comes the important conceptual point.

We can interpret

[  
D_f|\psi\rangle  
]

as a new state in the original frame. This is the active interpretation.

Alternatively, we can regard it as the same physical state expressed in a different basis.

This is the passive interpretation.

For the purpose of LSPT, I prefer the passive interpretation.

Why?

Because I do not want to think that we are changing the physical theory or physically preparing a different state every time we introduce the displacement operator.

I want to think that we are changing the coordinates used to describe the same quantum state.

In other words, we are introducing a new frame in the Hilbert space.

### 4.3 Defining the kink frame

Let us make this precise.

We call the original description the defining frame.

We define the kink frame as follows:

The ket (|\psi\rangle) in the kink frame represents the physical state (D_f|\psi\rangle) in the defining frame.

In shorthand,

D_f|\psi\rangle_{\mathrm{kink}}.  
]

This is simply a change in the identification between abstract states and their ket coordinates.

The physical state has not changed.

However, because we have changed the frame, we must transform the operators as well.

For any operator (O), its representation in the kink frame is

[  
\boxed{  
O_K=D_f^\dagger O D_f.  
}  
]

The expectation value is unchanged:

[  
\begin{aligned}  
{}_{\mathrm{def}}\langle\psi|O|\psi\rangle_{\mathrm{def}}  
&=  
{}_{\mathrm{kink}}\langle\psi|  
D_f^\dagger O D_f  
|\psi\rangle_{\mathrm{kink}}\  
&=  
{}_{\mathrm{kink}}\langle\psi|O_K|\psi\rangle_{\mathrm{kink}}.  
\end{aligned}  
]

This is the essence of a passive transformation.

We have changed the representation, not the physical state.

### 4.4 Why does the Hamiltonian have to transform?

The Hamiltonian is an operator too.

Therefore, in the kink frame, it becomes

[  
\boxed{  
H_K=D_f^\dagger H D_f.  
}  
]

Let me show why this is necessary.

In the defining frame, the Schrödinger equation is

H|\Psi(t)\rangle_{\mathrm{def}}.  
]

By definition,

D_f|\psi(t)\rangle_{\mathrm{kink}}.  
]

Assuming a static kink profile, (D_f) is time-independent.

Substituting this into the Schrödinger equation gives

HD_f|\psi(t)\rangle_{\mathrm{kink}}.  
]

Multiplying by (D_f^\dagger),

D_f^\dagger HD_f  
|\psi(t)\rangle_{\mathrm{kink}}.  
}  
]

Thus,

[  
H_K=D_f^\dagger HD_f.  
]

This is not an additional Hamiltonian defining a different physical theory.

It is the original Hamiltonian expressed in the kink frame.

In particular,

[  
\operatorname{Spec}(H_K)=\operatorname{Spec}(H)  
]

whenever the transformation is implemented unitarily.

I would emphasize this point on the blackboard:

**The vacuum Hamiltonian and kink Hamiltonian are not two different physical theories. They are two descriptions of the same quantum theory in different frames.**

### 4.5 What happens to the field operator?

In the kink frame, the original physical field observable is represented by

# D_f^\dagger\phi(x)D_f

\phi(x)+f(x).  
]

It is useful to distinguish the physical field from the fluctuation field.

I will denote the fluctuation field by (\varphi(x)).

Then, in the kink frame,

[  
\Phi_K(x)=f(x)+\varphi(x).  
]

The perturbative state is constructed such that

[  
\langle\varphi(x)\rangle_K=0  
]

at leading order.

Consequently,

[  
\langle\Phi_K(x)\rangle_K=f(x).  
]

This is exactly what we want.

Notice the difference in interpretation:

- The physical field has a nonzero expectation value corresponding to the kink.
    
- The fluctuation field has a vanishing expectation value.
    

The second field is the appropriate perturbative variable.

This is analogous to shifting the origin of a coordinate system before performing a Taylor expansion.

### 4.6 A useful analogy with ordinary Taylor expansion

Suppose we want to study a function (F(x)) near a point (x=x_0).

A Taylor expansion around the origin is not necessarily useful if (x_0) is far from the origin.

Instead, we introduce a new coordinate,

[  
y=x-x_0.  
]

We have not changed the function. We have changed the coordinate system.

Now we can expand around

[  
y=0.  
]

The same thing happens in quantum field theory.

We want to study a quantum state whose field expectation value is (f(x)).

Instead of expanding in the original field (\phi), we introduce the fluctuation operator

[  
\varphi=\phi-f.  
]

More precisely, this shift is implemented by the unitary displacement operator.

We have changed the frame so that the interesting state becomes perturbative.

**This is the central idea of the passive perspective of LSPT.**

---

# 5. The two Hamiltonians and their quadratic parts (76–90 min)

Now let us examine what this transformation buys us.

We have two equivalent descriptions of the theory:

[  
H[\phi,\pi]  
]

in the defining frame, and

D_f^\dagger H[\phi,\pi]D_f  
]

in the kink frame.

For the displacement operator defined above, we can write

H[\varphi+f,\pi].  
]

Now expand the kink Hamiltonian in powers of the fluctuation field.

### 5.1 Expansion of the kink Hamiltonian

For a general scalar potential,

\int dx\left[  
\frac12\pi^2+  
\frac12(\partial_x\varphi)^2+  
U(f+\varphi)  
\right].  
]

Taylor expanding the potential,

U(f)+U'(f)\varphi  
+\frac12U''(f)\varphi^2  
+\frac{1}{3!}U'''(f)\varphi^3+\cdots.  
]

Therefore,

[  
H_K=H_0^K+H_1^K+H_2^K+\cdots.  
]

The zeroth-order term is the classical kink mass:

[  
H_0^K=Q_0.  
]

The linear term is

\int dx\left[  
-f''(x)+U'(f(x))  
\right]\varphi(x).  
]

Since (f(x)) satisfies the classical equation of motion,

[  
-f''(x)+U'(f(x))=0,  
]

we have

[  
\boxed{H_1^K=0.}  
]

The quadratic term is

\frac12\int dx  
\left[  
\pi^2+  
(\partial_x\varphi)^2+  
U''(f(x))\varphi^2  
\right].  
}  
]

Higher-order terms describe interactions among the fluctuations.

For example,

\frac{1}{3!}\int dx,U'''(f)\varphi^3,  
]

and

\frac{1}{4!}\int dx,U''''(f)\varphi^4.  
]

For the (\phi^4) model,

[  
H_3^K=\lambda\int dx,f(x)\varphi^3(x),  
]

[  
H_4^K=\frac{\lambda}{4}\int dx,\varphi^4(x).  
]

We have now achieved something important.

The kink is contained in the background, and the Hamiltonian is organized in powers of the small fluctuation field.

This is precisely what we wanted from a perturbative formalism.

### 5.2 The vacuum quadratic Hamiltonian

But there is something I want to emphasize.

We already have another quadratic Hamiltonian: the quadratic Hamiltonian in the vacuum sector.

Let us denote it by

[  
H_{2}^{\mathrm{vac}}.  
]

After shifting around a homogeneous vacuum, it has the familiar form

\frac12\int dx  
\left[  
\pi^2+  
(\partial_x\eta)^2+  
m^2\eta^2  
\right].  
}  
]

This Hamiltonian is diagonalized by plane waves.

It defines the ordinary meson operators (a_p,a_p^\dagger).

On the other hand, the kink quadratic Hamiltonian is

\frac12\int dx  
\left[  
\pi^2+  
(\partial_x\varphi)^2+  
U''(f(x))\varphi^2  
\right].  
}  
]

This Hamiltonian is diagonalized by normal modes around the kink.

It defines the kink-sector operators (b_\alpha,b_\alpha^\dagger).

We therefore have two different quadratic Hamiltonians:

[  
\boxed{  
H_2^{\mathrm{vac}}  
\qquad\text{and}\qquad  
H_2^K.  
}  
]

They correspond to two different perturbative descriptions.

They are not two terms that should be added together. They are alternative quadratic approximations of the same exact theory, organized around different backgrounds.

---

# 6. Why I choose the Schrödinger picture (90–103 min)

This is the methodological motivation that I want to make particularly clear.

### 6.1 The conventional interaction picture

Let me briefly recall how the interaction picture works.

Given a Hamiltonian,

[  
H=H_0+H_I,  
]

we identify a free Hamiltonian (H_0) and an interaction Hamiltonian (H_I).

The operators evolve according to (H_0):

[  
O_I(t)=e^{iH_0t}O_Se^{-iH_0t},  
]

while the states evolve according to the interaction Hamiltonian.

This is extremely convenient in ordinary perturbative quantum field theory.

In the vacuum sector, the choice is natural:

[  
H_0=H_2^{\mathrm{vac}}.  
]

The operators evolve as plane waves, and we can construct the usual Feynman propagators.

But now consider the kink sector.

### 6.2 Which Hamiltonian should define the interaction picture?

We now have two natural quadratic Hamiltonians:

[  
H_2^{\mathrm{vac}},  
\qquad  
H_2^K.  
]

If I choose

[  
H_0=H_2^{\mathrm{vac}},  
]

then the operators evolve according to plane waves.

This is natural in the vacuum sector, but it is not natural for perturbation theory around the kink.

If instead I choose

[  
H_0=H_2^K,  
]

then the operators evolve according to the kink normal modes.

This is natural in the kink sector, but it is not the usual vacuum-sector interaction picture.

The two choices lead to different time-dependent operators and different definitions of the interaction Hamiltonian.

We could certainly define two separate interaction pictures, one for each sector.

But then we have to be extremely careful when comparing quantities between the two descriptions. We must keep track of the change of frame, the different mode decompositions, and the corresponding transformations of operators and states.

There is no obvious reason to privilege one of these quadratic Hamiltonians as the unique free Hamiltonian for the entire problem.

This is the ambiguity I want to emphasize.

### 6.3 The connection with the passive perspective

The passive perspective makes the situation clearer.

We have

[  
H_K=D_f^\dagger H D_f.  
]

These are not two different physical Hamiltonians.

They are the same Hamiltonian represented in two different frames.

However, their quadratic expansions are different:

[  
H_2^{\mathrm{vac}}  
\quad\longleftrightarrow\quad  
\text{plane-wave fluctuations},  
]

[  
H_2^K  
\quad\longleftrightarrow\quad  
\text{kink normal-mode fluctuations}.  
]

The problem is not that one description is wrong.

Both are appropriate in their respective sectors.

The problem is that the interaction picture requires us to choose one particular free Hamiltonian to define time evolution of operators.

For this problem, that choice is not neutral.

### 6.4 Why the Schrödinger picture is more natural

This is why I eventually convinced myself to formulate the calculation in the Schrödinger picture.

In the Schrödinger picture, the canonical field and momentum operators are time-independent:

[  
\phi(x),\qquad \pi(x).  
]

All time evolution is carried by the states.

In the defining frame, the states evolve according to

[  
i\partial_t|\Psi\rangle=H|\Psi\rangle.  
]

In the kink frame, they evolve according to

[  
i\partial_t|\psi\rangle=H_K|\psi\rangle.  
]

We do not need to assign time dependence to the field operators using one of two competing quadratic Hamiltonians.

Instead, we keep the canonical operator algebra fixed and let the Hamiltonian determine the dynamics in the chosen frame.

The perturbative calculations can then be formulated as a Hamiltonian eigenvalue problem:

[  
H|\Psi\rangle=E|\Psi\rangle  
]

or, equivalently,

[  
H_K|\psi\rangle=E|\psi\rangle.  
]

We use the appropriate quadratic Hamiltonian to construct the basis for perturbation theory.

In the vacuum sector, we use plane-wave creation and annihilation operators.

In the kink sector, we use normal-mode creation and annihilation operators.

This is a much cleaner organization.

Let me stress one point: I am not claiming that the interaction picture is mathematically impossible here. One can certainly construct it after choosing a particular free Hamiltonian, or construct separate interaction pictures for the two sectors.

My point is that the Schrödinger picture avoids making an unnecessary and potentially confusing choice of a common free time evolution.

It also makes the passive interpretation of the displacement operator much more transparent.

**The central principle is: keep the canonical field operators fixed, transform the Hamiltonian when changing frames, and perform perturbation theory in the appropriate sector.**

---

# 7. Constructing the kink-sector Fock space (103–110 min)

We are now ready to construct the kink-sector Fock space.

The quadratic kink Hamiltonian is

\frac12\int dx  
\left[  
\pi^2+  
(\partial_x\varphi)^2+  
U''(f)\varphi^2  
\right].  
]

Introduce the fluctuation operator

[  
\boxed{  
\mathcal K=-\partial_x^2+U''(f(x)).  
}  
]

The normal modes satisfy

\omega_\alpha^2g_\alpha(x).  
]

This is a Sturm–Liouville eigenvalue problem.

For the (\phi^4) kink,

m^2-\frac{3m^2}{2}  
\operatorname{sech}^2\left(\frac{mx}{2}\right).  
]

There are three types of modes.

### 7.1 Zero mode

The translational zero mode satisfies

[  
\mathcal K g_B=0.  
]

It is proportional to the derivative of the kink:

[  
g_B(x)\propto f'(x).  
]

It exists because translating the kink does not change its energy.

### 7.2 Shape mode

There is also a discrete shape mode:

[  
\omega_S=\frac{\sqrt3}{2}m.  
]

It is a localized excitation bound to the kink.

### 7.3 Continuum modes

Finally, there is a continuum of scattering modes:

[  
\omega_k=\sqrt{k^2+m^2}.  
]

The normal modes form a complete basis for the fluctuations around the kink.

### 7.4 Mode expansion

We can therefore expand the fluctuation field as

\varphi_0g_B(x)  
+  
\sum_S  
\frac{1}{\sqrt{2\omega_S}}  
\left(  
b_Sg_S(x)+b_S^\dagger g_S^_(x)  
\right)  
+  
\int\frac{dk}{2\pi}  
\frac{1}{\sqrt{2\omega_k}}  
\left(  
b_kg_k(x)+b_k^\dagger g_k^_(x)  
\right).  
]

The momentum field has a corresponding expansion.

The canonical commutation relations imply

[  
[b_k,b_q^\dagger]=2\pi\delta(k-q),  
]

and analogous relations for the discrete modes.

The zero mode is special. It is not an ordinary harmonic oscillator because its frequency vanishes.

Instead, it is associated with the translational degree of freedom of the kink and must be treated as a collective coordinate or center-of-mass degree of freedom.

The resulting quadratic Hamiltonian has the schematic form

Q_0+  
\frac12\pi_0^2  
+  
\sum_S\omega_S b_S^\dagger b_S  
+  
\int\frac{dk}{2\pi},  
\omega_k b_k^\dagger b_k  
+\text{constant}.  
]

We have now constructed the kink-sector Fock space.

The perturbative excitations are mesons and internal excitations of the kink, rather than plane waves alone.

---

# 8. Returning to Coleman's problem: the squeezed coherent state (110–115 min)

Let me now return to the second problem.

We have seen that the vacuum sector is naturally described by plane-wave operators (a_p), whereas the kink sector is described by normal-mode operators (b_\alpha).

These two sets of operators are related by a Bogoliubov transformation:

\int dp\left(  
\alpha_{\alpha p}a_p+  
\beta_{\alpha p}a_p^\dagger  
\right).  
]

Because the transformation mixes creation and annihilation operators, the two vacuum states are different.

The state annihilated by the kink normal-mode operators is not simply the plane-wave vacuum.

A squeeze operator implements the Bogoliubov transformation.

Thus, in the active description, the leading kink state takes the schematic form

[  
\boxed{  
|K\rangle  
\simeq  
D_fS_f|0\rangle_{\mathrm{vac}}.  
}  
]

The displacement operator produces the classical background.

The squeeze operator adjusts the quantum fluctuations.

In the passive description, we do not need to keep writing the displacement operator in front of every ket. It has been absorbed into the definition of the kink frame.

This is another advantage of the passive perspective: the state in the kink frame is described directly using the kink-sector perturbative degrees of freedom.

The leading squeeze is then understood as the deformation required to obtain the correct quantum ground state of the normal modes.

### 8.1 The 3+1-dimensional domain wall

A particularly important application is the domain wall in the (3+1)-dimensional (\phi^4) theory.

The classical solution is

\frac{m}{\sqrt{2\lambda}}  
\tanh\left(\frac{mx_1}{2}\right).  
]

Its classical tension is

[  
\rho_0=\frac{m^3}{3\lambda}.  
]

The conventional coherent-state construction produces a logarithmically divergent one-loop contribution to the tension.

However, when the leading squeeze is included, the divergence is canceled in the calculation.

The counterterms are then fixed in the vacuum sector and used consistently in the domain-wall sector.

This provides a concrete demonstration that the quantum state must contain more information than the classical field expectation value alone.

I want to be careful about the scope of this statement: the squeeze resolves the leading divergence studied in this example; it should not be interpreted as a proof that all possible higher-order divergences disappear automatically.

---

# Part III. Conclusion and outlook (115–120 min)

Let me summarize the logic of the talk.

We started with three problems.

**First, the Hilbert-space problem.**

The ordinary vacuum Fock space is not the natural perturbative organization for a state containing a kink.

We need a kink-sector Fock space built from normal modes.

**Second, Coleman's divergence problem.**

The ordinary coherent state gives the correct classical field expectation value but the wrong quantum fluctuations.

We need a squeezed coherent state.

**Third, the regularization mismatch problem.**

Independently regularizing the vacuum and kink Hamiltonians can lead to regulator-dependent answers.

We should regularize the theory once and obtain the kink Hamiltonian through unitary conjugation.

The central construction is

[  
\boxed{  
H_K=D_f^\dagger H D_f.  
}  
]

But I want to emphasize that the most important point is not simply the introduction of a displacement operator.

It is the interpretation of this operator as a passive transformation.

The kink Hamiltonian is the original Hamiltonian expressed in a different frame.

This allows us to understand the vacuum and kink sectors as two perturbative descriptions of the same quantum theory.

It also explains why the Schrödinger picture is particularly natural: we do not have to choose a single free Hamiltonian to define the time evolution of operators when the vacuum and kink sectors have different natural quadratic Hamiltonians.

Instead, we keep the canonical operators fixed and use the appropriate Hamiltonian and perturbative basis in each frame.

Finally, this construction opens the door to systematic calculations of quantum soliton properties, including kink masses, form factors, kink-meson scattering, shape-mode excitations and higher-order quantum corrections.

The broader goal is not merely to calculate the quantum correction to a classical kink mass.

**The goal is to develop a consistent perturbative framework for the quantum dynamics of nonperturbative classical configurations.**

Thank you.

---

# Final blackboard summary

I would leave these equations on the board at the end:

**1. Classical kink**

[  
f(x)=v\tanh\left(\frac{mx}{2}\right).  
]

**2. Displacement operator**

[  
D_f=\exp\left[-i\int dx,f(x)\pi(x)\right].  
]

**3. Passive transformation**

[  
D_f^\dagger\phi D_f=\phi+f.  
]

**4. Kink Hamiltonian**

[  
H_K=D_f^\dagger HD_f.  
]

**5. Two perturbative quadratic Hamiltonians**

[  
H_2^{\mathrm{vac}}  
\quad\text{and}\quad  
H_2^K.  
]

**6. Kink fluctuation operator**

[  
\mathcal K=-\partial_x^2+U''(f).  
]

**7. Normal-mode eigenvalue equation**

[  
\mathcal K g_\alpha=\omega_\alpha^2g_\alpha.  
]

**8. Squeezed coherent state**

[  
|K\rangle\simeq D_fS_f|0\rangle_{\mathrm{vac}}.  
]

The final message should be that the displacement operator changes our frame, the normal modes provide the appropriate perturbative degrees of freedom, and the squeeze corrects the quantum fluctuations.