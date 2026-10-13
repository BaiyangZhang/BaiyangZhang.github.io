\label{ap}
\end{gather}
The Abelian projection has three key features. First, $\hA_\mu$ leaves the Abelian direction invariant under parallel transport, making $\hn$ covariantly constant. Second, it consists of two distinct parts: the non-topological (Maxwellian) potential $\cA_\mu$, which describes the color-neutral gluon (the nuron), and the topological (Diracian) potential $\cC_\mu$, which characterizes non-Abelian topological configurations \cite{prl80}. Third, the decomposition is gauge-independent. Rotating $\hn$ to any other direction yields the identical physical decomposition.

From (\ref{ap}), the restricted field strength tensor is
\begin{gather}
\hF_\mn = (F_\mn+ H_\mn)\hn, \nn\\
F_\mn = \pd_\mu A_\nu-\pd_\nu A_\mu,   \nn\\
H_\mn =-\frac1g \n \cdot (\pd_\mu \n \times \pd_\nu \n) = \pd_\mu C_\nu-\pd_\nu C_\mu, \nn\\
C_\mu \simeq -\frac{1}{g} \hn_1 \cdot \pd_\mu \hn_2.
\label{rf} 
\end{gather} 
Here $C_\mu$ is determined up to a $U(1)$ gauge transformation that leaves $\hn$ invariant. This shows two things: first, $\hF_\mn$ points purely along the Abelian direction $\hn$; second, $\hF_\mn$ inherits the dual structure of $\hA_\mu$, composed of the non-topological part $F_\mn$ and the topological part $H_\mn$.

We recover the full QCD potential by adding the gauge-covariant colored valence potential $\X_\mu$, which describes colored gluons (chromons) \cite{prd80,prl81}:
\begin{gather}
\A_\mu = \hA_\mu + \X_\mu,  \hn \cdot \X_\mu=0.
\label{adec}
\end{gather}
Thus, the full gluon potential is decomposed gauge-independently into the non-topological Maxwellian potential $\cA_\mu$ (color-neutral nuron), the topological Diracian potential $\cC_\mu$, and the colored valence potential $\X_\mu$ (chromon). This formulation is known as the Cho, Cho-Duan-Ge, or Cho-Faddeev-Niemi decomposition \cite{fadd,shab,zucc,kondo}.

Under the infinitesimal gauge transformation
\begin{gather}
\delta \A_\mu=\oneg  D_\mu \vec \alpha, 
~~~\delta \hn_i= -\vec \alpha \times \hn_i, 
\label{agt0}
\end{gather} 
the component fields transform as
\begin{gather}
\delta A_\mu = \oneg \n \cdot \pd_\mu \valpha,
~~~\delta \hA_\mu=\dfrac1g \hD_\mu \vec \alpha, \nn\\
\delta \X_\mu = - \valpha \times \X_\mu,
\label{agt1}
\end{gather}
where $\hD_\mu=\pd_\mu+g\hA_\mu \times$. This shows that $\hA_\mu$ retains the full $SU(2)$ gauge symmetry, even though it is restricted. Furthermore, $\X_\mu$ transforms covariantly. This occurs because the space of gauge connections is affine: any connection can be reached from the Abelian connection by adding a gauge-covariant vector field.

Crucially, the decomposition (\ref{adec}) is gauge-independent. Once $\hn$ is specified, the decomposition follows automatically, regardless of the gauge choice. In particular, isolating the monopole potential is completely gauge-independent \cite{prd80,prl81}.

Using the restricted potential, we construct restricted QCD (RCD), which retains the full non-Abelian gauge symmetry while remaining simpler than full QCD:
\begin{gather} 
\cL_{RCD} =-\frac14 \hF^2_\mn 
=-\frac14 (F_\mn +H_\mn)^2  \nn\\
=-\frac14 F_\mn^2 
+\frac1{2g} F_\mn \hn \cdot (\pd_\mu \hn \times \pd_\nu \hn) \nn\\
-\frac1{4g^2} (\pd_\mu \hn \times \pd_\nu \hn)^2.
\label{rcd}
\end{gather}
This Lagrangian describes the Abelian subdynamics of QCD. It contains two Abelian potentials: the non-topological Maxwellian potential $A_\mu$ and the topological Diracian potential $C_\mu$.

From (\ref{adec}), the full field strength tensor is
\begin{gather}
\F_\mn =\hF_\mn + \hD _\mu \X_\nu -\hD_\nu \X_\mu 
+ g\X_\mu \times \X_\nu  \nn\\
=(F_\mn +H_\mn + X_\mn) \n 
+\hD _\mu \X_\nu -\hD_\nu \X_\mu,   \nn\\
X_\mn= g \n \cdot (\X_\mu \times \X_\nu). 
\end{gather} 
The full QCD Lagrangian can then be expressed as
\begin{gather} 
{\cL}_{ECD} = -\frac14 \F^2_\mn   \nn\\
=-\frac14 \hF_\mn^2
-\frac14 (\hD_\mu\X_\nu-\hD_\nu\X_\mu)^2 
-\frac{g}{2} {\hF}_\mn \cdot (\X_\mu \times \X_\nu)  \nn\\
-\frac{g^2}{4} (\X_\mu \times \X_\nu)^2 \nn\\
=-\frac14 (F_\mn +H_\mn + X_\mn)^2  \nn\\
-\frac14 (\hD_\mu\X_\nu-\hD_\nu\X_\mu)^2. 
\label{ecd} 
\end{gather}
This formulation is called extended QCD (ECD). It shows that QCD can be regarded as RCD coupled to $\X_\mu$ as a colored source—a structure hidden in the standard formulation.

Varying the Lagrangian (\ref{ecd}) yields the equations of motion for $SU(2)$ QCD:
\begin{gather}
\pd_\mu (F_\mn +H_\mn)  \nn\\
= -g\n \cdot \big[\X_\mu \times (\hD_\mu\X_\nu-\hD_\nu\X_\mu) 
+\pd_\mu (\X_\mu \times \X_\nu) \big], \nn\\
\hD_\mu (\hD_\mu\X_\nu-\hD_\nu\X_\mu) \nn\\
= g (F_\mn +H_\mn +X_\mn)~\n \times \X_\mu.
\label{ecdeq}
\end{gather}
This should be compared with the standard Yang-Mills equation,
\begin{gather}
D_\mu \F_\mn =0.
\label{qcdeq}
\end{gather} 
Remarkably, Eq.~(\ref{ecdeq}) separates Eq.~(\ref{qcdeq}) into two coupled equations: one for the nuron $A_\mu$ and one for the chromon $\X_\mu$. The first equation resembles Maxwell's equations in QED, while the second shows that the chromon acts as a colored source for the restricted potential $\hA_\mu$. This indicates that the nuron plays the role of the photon in QCD, whereas the chromon $\X_\mu$ acts as a colored source and represents the constituent gluon \cite{prd80,prl81}.

The decomposition also abelianizes QCD in a gauge-independent way \cite{prd80,prl81}. To see this, we express the valence potential $\X_\mu$ in terms of a complex vector field $X_\mu$:
\begin{gather}
\X_\mu =X^1_\mu \hn_1 + X^2_\mu \hn_2,
~~X_\mu =\frac{1}{\sqrt 2} (X^1_\mu+ i X^2_\mu).
\end{gather}
The Lagrangian (\ref{ecd}) then becomes
\begin{gather}
\cL =-\frac14 (F_\mn + H_\mn)^2 
-\frac12 |\hD_\mu X_\nu-\hD_\nu X_\mu|^2  \nn\\
+ ig G_\mn X_\mu^* X_\nu 
-\frac{g^2}{2} \Big[(X_\mu^*X_\mu)^2
-(X_\mu^*)^2 (X_\nu)^2 \Big] \nn\\
= -\frac14 (F_\mn +H_\mn + X_\mn)^2
-\frac12 |\hD_\mu X_\nu -\hD_\nu X_\mu|^2, 
\label{abqcd}
\end{gather}
where
\begin{gather}
\hD_\mu X_\nu = \big[\pd_\mu 
+ ig (A_\mu+\tC_\mu) \big] X_\nu, \nn\\
X_\mn = - i g ( X_\mu^* X_\nu - X_\nu^* X_\mu ). \nn
\end{gather}
This resembles an Abelian gauge theory coupled to a charged vector field $X_\mu$, but with two Abelian potentials, $A_\mu$ and $\tC_\mu$. The theory becomes a dual gauge theory with gauge group $U(1)_e \otimes U(1)_m$. In this representation, the non-Abelian topology is retained through the dual structure in the magnetic potential $\tC_\mu$ \cite{prd80,prl81}.

In this form, the equations of motion (\ref{ecdeq}) read
\begin{gather}
	\pd_\mu (F_\mn +H_\mn +X_\mn ) 
	= +ig \big[X_\mu^*(\hD_\mu X_\nu
	-\hD_\nu X_\mu) \nn\\
	-X_\mu (\hD_\mu X_\nu
	-\hD_\nu X_\mu)^* \big], \nn\\
	\hD_\mu (\hD_\mu X_\nu-\hD_\nu X_\mu) 
	= ig X_\mu (F_\mn +H_\mn +X_\mn). 
	\label{ecdeq3}
\end{gather}
These equations are equivalent to (\ref{ecdeq}). They confirm that QCD contains two distinct types of gluons—the color-neutral nuron and the colored chromon—governed by different dynamical rules. Furthermore, the unit vector $\hn$ has no independent equation of motion. Because it represents a choice of gauge direction, it can be rotated arbitrarily.

This does not mean that $\hn$ is unphysical; rather, it carries the topological degrees of freedom of QCD. When $\X_\mu=0$, the RCD equation of motion is
\begin{gather}
\pd_\mu (F_\mn +H_\mn)= 0.
\label{rcdeq0}
\end{gather} 
This reveals two important points. First, the RCD equation of motion is formally identical to the source-free Maxwell equations. The only difference is the dual structure of the field strength, composed of the Maxwellian part $F_\mn$ and the topological part $H_\mn$. Second, the two gauge potentials $A_\mu$ and $C_\mu$ satisfy the linear superposition principle.

Equation~(\ref{rcdeq0}) can also be written as
\begin{gather}
\pd_\mu F_\mn = j_\nu =-\pd_\mu H_\mn,
~~~(\pd_\mu j^\mu =0).
\label{rcdeq}
\end{gather} 
Thus, RCD can be interpreted as electrodynamics where the Maxwellian field is driven by a conserved topological current $j_\nu = -\pd_\mu H_\mn$. In the absence of the nuron ($A_\mu=0$), the RCD equation $\pd_\mu H_\mn =0$ reduces to
\begin{gather}
\n \cdot \big(\pd^2 \n \times \pd_\nu \n
+\pd_\mu \n \times \pd_\mu \pd_\nu \n \big) =0. 
\label{neq}
\end{gather} 
This acts as a constraint on $\hn$ when the nuron vanishes and admits non-trivial solutions, such as the Wu-Yang monopole (\ref{wy}). Therefore, RCD describes non-trivial topological configurations even without the nuron.

When $A_\mu=0$, Eq.~(\ref{ecdeq}) becomes
\begin{gather}
\pd_\mu \big[\n \cdot (\pd_\mu \n \times \pd_\nu \n) \big] = g^2 \n \cdot \big[\X_\mu \times (\hD_\mu\X_\nu-\hD_\nu\X_\mu) \nn\\
+\pd_\mu (\X_\mu \times \X_\nu) \big], \nn\\
\hD_\mu (\hD_\mu\X_\nu-\hD_\nu\X_\mu)
=-\big[\n \cdot (\pd_\mu \n \times \pd_\nu \n)   \nn\\
-g^2 \n \cdot (\X_\mu \times \X_\nu) \big]~\n \times \X_\mu,
\label{ecdeq1}
\end{gather}
or equivalently,
\begin{gather}
	\pd_\mu (H_\mn +X_\mn) 
	=+ig \big[X_\mu^*(\hD_\mu X_\nu
	-\hD_\nu X_\mu) \nn\\
	-X_\mu (\hD_\mu X_\nu 
	-\hD_\nu X_\mu)^* \big], \nn\\
	\hD_\mu (\hD_\mu X_\nu-\hD_\nu X_\mu) 
	= ig X_\mu (H_\mn +X_\mn).   
	\label{ecdeq4}
\end{gather}
When $H_\mn=0$, this system simplifies to
\begin{gather}
\n \cdot \big[\X_\mu \times
(\pd_\mu\X_\nu-\pd_\nu\X_\mu)
+\pd_\mu (\X_\mu \times \X_\nu) \big]=0, \nn\\
\pd_\mu (\pd_\mu\X_\nu-\pd_\nu\X_\mu)
= g X_\mn~\n \times \X_\mu.
\label{ecdeq2}
\end{gather}
This confirms that the chromon possesses its own dynamical equation independent of the nuron.

Although ECD is mathematically equivalent to conventional QCD, it exposes structures hidden in the standard formulation. Strictly speaking, Eq.~(\ref{ecd}) has an enlarged gauge symmetry because the decomposition (\ref{adec}) places QCD into the background field formalism \cite{prd01}. The theory is invariant under active (classical) gauge transformations (\ref{agt1}), as well as passive (quantum) gauge transformations:
\begin{gather}
\delta\A_\mu=\frac{1}{g} D_\mu \valpha,
~~~~\delta \hn=0,
\label{pgt0}
\end{gather}
under which
\begin{gather}
\delta A_\mu=\frac{1}{g}\hn \cdot D_\mu \valpha,
~~~~\delta \hA_\mu=\frac{1}{g}
(\hn \cdot D_\mu \valpha) \hn, \nn\\
\delta \X_\mu=\frac{1}{g}[D_\mu \valpha
 -(\hn \cdot D_\mu \valpha)\hn].
\label{pgt1}
\end{gather}
This redundancy arises because a given potential $\A_\mu$ can be decomposed in different ways by selecting different directions $\hn$. Conversely, for a fixed $\hn$, different gauge-equivalent potentials $\A_\mu$ yield distinct components. The decomposition therefore introduces additional gauge freedom.

This enlarged symmetry is a standard feature of the background field method \cite{dewitt,pesk}. Because splitting a connection into background and quantum parts does not uniquely specify how gauge transformations are assigned, the formalism carries redundant gauge freedom. Consequently, quantizing ECD requires two independent gauge-fixing conditions: one for the restricted connection and one for the chromon.

To fix the active gauge symmetry (\ref{agt1}), one can choose the generalized Lorentz gauge \cite{prd01},
\begin{gather}
\pd_\mu \hA_\mu =0,
\label{agcon}
\end{gather}
or equivalently,
\begin{gather}
\pd_\mu A_\mu =0,   \nn\\
\n \times \pd^2 \n -g A_\mu \pd_\mu \n =0.
\label{agcon1}
\end{gather}
This splits the condition into the Lorentz gauge for the nuron $A_\mu$ and a constraint on the topological field $\hn$.

To fix the passive gauge symmetry (\ref{pgt1}), one can choose the background covariant gauge \cite{prd01},
\begin{gather}
\hD_\mu \X_\mu=0.
\label{pgcon}
\end{gather}
This condition removes the unphysical degrees of freedom of $\X_\mu$ while keeping the chromons massless. It ensures that ECD remains physically equivalent to standard QCD despite its enlarged symmetry.

The Abelianized theory remains non-Abelian because Eq.~(\ref{abqcd}) preserves the full non-Abelian symmetry. Decomposing the transformation parameter and the magnetic potential as
\begin{gather}
\valpha = \alpha_1~\hn_1 + \alpha_2~\hn_2 + \theta~\hn, 
~~~\alpha = \frac{1}{\sqrt 2} (\alpha_1 + i \alpha_2), \nn\\
\C_\mu = - \frac {1}{g} \hn \times \pd_\mu \hn
= - C^1_\mu \hn_1 - C^2_\mu \hn_2, \nn\\
C_\mu = \frac{1}{\sqrt 2} (C^1_\mu + i C^2_\mu),
\end{gather}
we find that Eq.~(\ref{abqcd}) is invariant under active gauge transformations,
\begin{gather} 
\delta A_\mu = \frac{1}{g} \pd_\mu \theta 
- i (C_\mu^* \alpha - C_\mu \alpha^*),
~~~\delta \tC_\mu = - \delta A_\mu, \nn\\
\delta X_\mu = 0,
\label{agt2}
\end{gather}
as well as passive gauge transformations,
\begin{gather} 
\delta A_\mu = \frac{1}{g} \pd_\mu \theta 
-i (X_\mu^* \alpha - X_\mu \alpha^*), 
~~~\delta \tC_\mu = 0, \nn\\
\delta X_\mu = \oneg \hD_\mu \alpha - i \theta X_\mu.
\label{pgt2}
\end{gather}
Hence, Abelianized QCD possesses enlarged active and passive gauge symmetries \cite{prd01}.

For our purposes, the primary advantage of the Abelian decomposition is the separation of the QCD equations of motion in (\ref{ecdeq}). This structure simplifies the search for classical solutions. In fact, Eq.~(\ref{ecdeq}) allows one to construct solutions directly without having to solve the full twelve coupled second-order Yang-Mills equations simultaneously. In the following sections, we demonstrate how this is achieved.

---

### Notes on Primary Literature Cited

1. **Y. M. Cho**, *Phys. Rev. D* **21**, 1080 (1980)[cite: 1] — Formulates restricted gauge theory and the gauge-independent Abelian projection.
2. **Y. M. Cho**, *Phys. Rev. Lett.* **46**, 302 (1981)[cite: 1] — Introduces extended QCD, the valence decomposition, and the role of the constituent gluon.
3. **L. Faddeev and A. J. Niemi**, *Phys. Rev. Lett.* **82**, 1624 (1999)[cite: 1] — Investigates partially dual variables and geometric knot/soliton configurations in $SU(2)$ gauge fields.
4. **S. V. Shabanov**, *Phys. Lett. B* **458**, 322 (1999)[cite: 1] — Analyzes independent gauge-invariant degrees of freedom and constraint structures in the Cho-Faddeev-Niemi decomposition.
5. **W. S. Bae, Y. M. Cho, and S. W. Kimm**, *Phys. Rev. D* **65**, 025005 (2001)[cite: 1, 6] — Details the active and passive gauge groups, background-field gauge fixing, and extended quantization.