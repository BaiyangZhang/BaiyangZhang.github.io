### The Ansatz

Follow the previous derivation of equation of motion for monopoles with various ansatz. Now adopt the new ansatz:

$$
\begin{align*}
\hat{A}_ {\mu} &= - \frac{1}{g} \hat{r}_ {n} \times \partial_ {\mu} \hat{r} _ {n} \\
\vec{X}_ {\mu} &= \frac{f_ {n} (r)}{g}\hat{r}_ {n} \times \partial_ {\mu}\hat{r}_ {n} + \frac{g_ {n} (r)}{g}\partial_ {\mu}\hat{r}_ {n} \\
\hat{r}_ {n} &= 
\begin{pmatrix}
\sin \alpha _ {n} (\theta)\cos (n\varphi) \\
\sin \alpha _ {n} (\theta)\sin (n\varphi) \\ 
\cos \alpha _ {n} (\theta)
\end{pmatrix}
\end{align*}
$$

and get the equation of motion by taking them to the equation of extended QCD.

### The Equation of Motion

We need to substitute it into the Extended QCD (ECD) field equations. There are two equations of motion, the nuron (abelian) Equation: 

$$
\nabla_\mu \Gamma^{\mu\nu} = -g \hat{r}_n \cdot \left[\vec{X}_\mu \times \hat{G}^{\mu\nu}\right],\quad \Gamma:= F + H + X,
$$

where $\Gamma$ is the $\hat{n}$ direction contributions in the Lagrangian. And the chromon (valence) equation read: 

$$
\hat{D}_\mu \hat{G}^{\mu\nu} = g \Gamma^{\nu\mu} (\hat{r}_n \times \vec{X}_\mu).
$$

Define the local orthonormal frame $(\hat{n}_1 , \hat{n}_2 , \hat{r}_n)$ in color space:
  

$$\hat{n}_1  = \begin{pmatrix} \cos\alpha_n(\theta)\cos(n\varphi) \\ \cos\alpha_n(\theta)\sin(n\varphi) \\ -\sin\alpha_n(\theta) \end{pmatrix}, \qquad \hat{n}_2  = \begin{pmatrix} -\sin(n\varphi) \\ \cos(n\varphi) \\ 0 \end{pmatrix}, \qquad \hat{r}_n = \hat{n}_1  \times \hat{n}_2 $$

The spacetime derivatives of $\hat{r}_n$ and the cross product $\hat{r}_n \times \partial_\mu \hat{r}_n$ expand in this basis as:

  $$\partial_\mu \hat{r}_n = \dot{\alpha}_n \partial_\mu \theta \, \hat{n}_1  + n \sin\alpha_n \partial_\mu \varphi \, \hat{n}_2 ,$$
$$\hat{r}_n \times \partial_\mu \hat{r}_n = \dot{\alpha}_n \partial_\mu \theta \, \hat{n}_2  - n \sin\alpha_n \partial_\mu \varphi \, \hat{n}_1 $$

where $\dot{\alpha}_n = \frac{d\alpha_n}{d\theta}$.

The restricted connection is $\hat{A}_\mu = \mathcal{C}_\mu = -\frac{1}{g} \hat{r}_n \times \partial_\mu \hat{r}_n$ (with $A_\mu = 0$) and since $\hat{D}_\mu \hat{r}_n = 0$, $\hat{D}_\mu$ commutes with the angular basis vectors in the sense that:

$$\hat{D}_\mu(\partial_\nu \hat{r}_n) - \hat{D}_\nu(\partial_\mu \hat{r}_n) = g \hat{F}_{\mu\nu} \times \hat{r}_n = 0$$
$$\hat{D}_\mu(\hat{r}_n \times \partial_\nu \hat{r}_n) - \hat{D}_\nu(\hat{r}_n \times \partial_\mu \hat{r}_n) = 0$$

Recall that $\hat{G}_{\mu\nu} \equiv \hat{D}_\mu \vec{X}_\nu - \hat{D}_\nu \vec{X}_\mu$, the derivative acts only on the radial functions $f_n(r)$ and $g_n(r)$:

  $$\hat{G}_{\mu\nu} = \frac{1}{g}\left(\partial_\mu f_n \hat{r}_n \times \partial_\nu \hat{r}_n - \partial_\nu f_n \hat{r}_n \times \partial_\mu \hat{r}_n\right) + \frac{1}{g}\left(\partial_\mu g_n \partial_\nu \hat{r}_n - \partial_\nu g_n \partial_\mu \hat{r}_n\right).$$

In spherical coordinates $(r, \theta, \varphi)$, the non-vanishing components of $\hat{G}_{\mu\nu}$ are (similar to the calculation before):

$$\hat{G}_{r\theta} = \frac{1}{g}\left(f_n' \hat{r}_n \times \partial_\theta \hat{r}_n + g_n' \partial_\theta \hat{r}_n\right) = \frac{\dot{\alpha}_n}{g}\left(f_n' \hat{n}_2  + g_n' \hat{n}_1 \right),$$$$\hat{G}_{r\varphi} = \frac{1}{g}\left(f_n' \hat{r}_n \times \partial_\varphi \hat{r}_n + g_n' \partial_\varphi \hat{r}_n\right) = \frac{n\sin\alpha_n}{g}\left(-f_n' \hat{n}_1  + g_n' \hat{n}_2 \right).$$
Meanwhile the topological magnetic field strength $H_{\mu\nu} = -\frac{1}{g} \hat{r}_n \cdot (\partial_\mu \hat{r}_n \times \partial_\nu \hat{r}_n)$ has only the $\theta\varphi$ component:

$$H_{\theta\varphi} = -H_{\varphi\theta} = -\frac{n}{g} \sin\alpha_n \, \dot{\alpha}_n.$$

For the chromon self-interaction $X_{\mu\nu} = g \hat{r}_n \cdot (\vec{X}_\mu \times \vec{X}_\nu)$, we have

$$\vec{X}_\mu \times \vec{X}_\nu = \frac{f_n^2 + g_n^2}{g^2} (\partial_\mu \hat{r}_n \times \partial_\nu \hat{r}_n)$$

hence $\vec{X}_\mu$ is obtained from $\frac{1}{g}\partial_\mu \hat{r}_n$ by combining a scaling of $\sqrt{f_n^2 + g_n^2}$ and a rotation in the $(\hat{n}_1 , \hat{n}_2 )$ plane. Projecting onto $\hat{r}_n$ gives:

$$X_{\mu\nu} = -(f_n^2 + g_n^2) H_{\mu\nu}$$

So the total Abelian field strength $F_{\mu\nu} + H_{\mu\nu} + X_{\mu\nu}$ (with $F_{\mu\nu} = 0$) is:
  
$$H_{\theta\varphi} + X_{\theta\varphi} = \left(1 - f_n^2 - g_n^2\right) H_{\theta\varphi} = -\frac{n}{g} \sin\alpha_n \, \dot{\alpha}_n \left(1 - f_n^2 - g_n^2\right).$$

- - -

On the right-hand side of the nuron equation, $\hat{G}^{\mu\nu}$ is only non-zero when one index is $r$ and the other is angular, whereas $\vec{X}_r = 0$. Thus, for $\nu = \theta$ or $\varphi$, the sum $\vec{X}_\mu \times \hat{G}^{\mu\nu}$ collapses to $\vec{X}_r \times \hat{G}^{r\nu} = 0$. For $\nu = r$, $\vec{X}_\theta \times \hat{G}^{\theta r} + \vec{X}_\varphi \times \hat{G}^{\varphi r}$ is proportional to $(f_n f_n' + g_n g_n') \hat{r}_n$,

$$-g \hat{r}_n \cdot \left(\vec{X}_\theta \times \hat{G}^{\theta r} + \vec{X}_\varphi \times \hat{G}^{\varphi r}\right) = -\frac{f_n f_n' + g_n g_n'}{g r^2} \left(\dot{\alpha}_n^2 + \frac{n^2 \sin^2\alpha_n}{\sin^2\theta}\right)$$

However, the left-hand side for $\nu = r$ vanishes identically ($\nabla_\mu \Gamma^{\mu r} = 0$) because $\Gamma^{\mu\nu}$ only has $\theta\varphi$ components. For $\nu = \varphi$, the right-hand side is zero, and the left-hand side gives the angular equation for $\alpha_n(\theta)$:

$$\nabla_\theta \Gamma^{\theta\varphi} = \frac{1}{r^4 \sin\theta} \partial_\theta \left(\sin\theta \, g^{\theta\theta} g^{\varphi\varphi} \Gamma_{\theta\varphi}\right) = -\frac{n(1 - f_n^2 - g_n^2)}{g r^4 \sin\theta} \frac{d}{d\theta}\left(\frac{\sin\alpha_n}{\sin\theta}\dot{\alpha}_n\right) = 0$$

Expanding the derivative yields the angular equation:

$$\ddot{\alpha}_n + \frac{\cos\alpha_n}{\sin\alpha_n}\dot{\alpha}_n^2 - \frac{\cos\theta}{\sin\theta}\dot{\alpha}_n = 0.$$

**This is  exactly the equation we were talking about in the last email. Integrating this twice with the boundary conditions $\alpha_n(0) = 0$ and $\alpha_n(\pi) = \pi$ gives the unique smooth solution $\alpha_n(\theta) = \theta+2\pi N$.**

- - -

Next let's go to the chromon equation. For the left-hand side $\hat{D}_\mu \hat{G}^{\mu\nu}$, only $\mu = r$ contributes since $\hat{G}_{\theta\varphi} = 0$ and $\hat{A}_r = 0$, we have

$$\hat{D}_\mu \hat{G}^{\mu\theta} = \frac{1}{r^2} \partial_r \left(r^2 g^{rr} g^{\theta\theta} \hat{G}_{r\theta}\right) = \frac{1}{g r^2}\left(f_n'' \hat{r}_n \times \partial_\theta \hat{r}_n + g_n'' \partial_\theta \hat{r}_n\right),$$
$$\hat{D}_\mu \hat{G}^{\mu\varphi} = \frac{1}{r^2} \partial_r \left(r^2 g^{rr} g^{\varphi\varphi} \hat{G}_{r\varphi}\right) = \frac{1}{g r^2 \sin^2\theta}\left(f_n'' \hat{r}_n \times \partial_\varphi \hat{r}_n + g_n'' \partial_\varphi \hat{r}_n\right).$$

On the right-hand side, using $\hat{r}_n \times \vec{X}_\mu = \frac{f_n}{g} \hat{r}_n \times (\hat{r}_n \times \partial_\mu \hat{r}_n) + \frac{g_n}{g} \hat{r}_n \times \partial_\mu \hat{r}_n = -\frac{f_n}{g}\partial_\mu \hat{r}_n + \frac{g_n}{g}\hat{r}_n \times \partial_\mu \hat{r}_n$, and noting the identities:

$$\partial_\varphi \hat{r}_n = \frac{n \sin\alpha_n}{\dot{\alpha}_n} (\hat{r}_n \times \partial_\theta \hat{r}_n), \qquad \hat{r}_n \times \partial_\varphi \hat{r}_n = -\frac{n \sin\alpha_n}{\dot{\alpha}_n} \partial_\theta \hat{r}_n$$

we find for $\nu = \theta$ and $\nu = \varphi$ respectively,

$$f_n'' + \frac{n^2 \sin^2\alpha_n}{r^2 \sin^2\theta} f_n \left(1 - f_n^2 - g_n^2\right) = 0, \qquad g_n'' + \frac{n^2 \sin^2\alpha_n}{r^2 \sin^2\theta} g_n \left(1 - f_n^2 - g_n^2\right) = 0,$$

and
$$f_n'' + \frac{\dot{\alpha}_n^2}{r^2} f_n \left(1 - f_n^2 - g_n^2\right) = 0, \qquad g_n'' + \frac{\dot{\alpha}_n^2}{r^2} g_n \left(1 - f_n^2 - g_n^2\right) = 0.$$

It seems that, **When $\vert{}n\vert{} > 1$, the $\theta$ and $\varphi$ vector components yield different angular prefactors ($\frac{n^2\sin^2\alpha_n}{\sin^2\theta}$ vs. $\dot{\alpha}_n^2$)  as before. It is not consistent.**

### Variational Method (can be skipped)

because higher-winding monopoles are axially symmetric rather than spherically symmetric. To obtain a self-consistent radial equation for arbitrary $n$ under a spherically symmetric radial profile, we substitute the ansatz into the ECD Lagrangian

$$\mathcal{L}_{\text{ECD}} = -\frac{1}{4}(H_{\mu\nu} + X_{\mu\nu})^2 - \frac{1}{4}(\hat{D}_\mu \vec{X}_\nu - \hat{D}_\nu \vec{X}_\mu)^2$$

and integrate over the angles $(\theta, \varphi)$:

$$S_{\text{eff}}[f_n, g_n, \alpha_n] = -\frac{\pi}{g^2} \int dt \, dr \, d\theta \, \sin\theta \left[ \left(\dot{\alpha}_n^2 + \frac{n^2 \sin^2\alpha_n}{\sin^2\theta}\right)\left((f_n')^2 + (g_n')^2\right) + \frac{n^2 \sin^2\alpha_n \, \dot{\alpha}_n^2}{r^2 \sin^2\theta}\left(1 - f_n^2 - g_n^2\right)^2 \right]$$

Setting $\alpha_n(\theta) = \theta$ (as fixed by the nuron equation) and integrating over $\theta \in [0, \pi]$ gives the 1D effective action:

$$S_{\text{eff}}[f_n, g_n] = -\frac{2\pi}{g^2} \int dt \, dr \left[ (1 + n^2)\left((f_n')^2 + (g_n')^2\right) + \frac{n^2}{r^2}\left(1 - f_n^2 - g_n^2\right)^2 \right]$$

Varying $S_{\text{eff}}$ with respect to $f_n(r)$ and $g_n(r)$ yields the coupled radial equations of motion:  

$$\begin{aligned} f_n'' + \frac{2n^2}{1 + n^2} \frac{f_n}{r^2}\left(1 - f_n^2 - g_n^2\right) &= 0 \\ g_n'' + \frac{2n^2}{1 + n^2} \frac{g_n}{r^2}\left(1 - f_n^2 - g_n^2\right) &= 0 \end{aligned}$$

Notice that $f_n'' g_n - g_n'' f_n = 0 \implies (f_n' g_n - g_n' f_n)' = 0$. With the boundary conditions $f_n(0) = g_n(0) = 0$, $g_n(r) = c \, f_n(r)$ is simply a constant global $U(1)$ dual rotation of $f_n(r)$ and can be rotated to $g_n(r) = 0$ without loss of generality, reducing the system to:
  

$$f_n'' + \frac{2n^2}{1 + n^2} \frac{f_n}{r^2}\left(1 - f_n^2\right) = 0$$
### Some More Thinkings

I guess (I could be wrong) for topological winding number $\vert{}n\vert{} > 1$, **spherically symmetric solutions do not exist in $SU(2)$ gauge theory. Adding more purely radial profile functions $f_k(r)$ cannot fix the contradiction in the equations of motion**.

In a gauge theory, a field configuration is spherically symmetric if a spatial rotation generated by $\vec{L}$ plus spin $\vec{S}$ can be compensated by an internal $SU(2)$ isospin rotation $\vec{T}$, meaning the configuration is invariant under a combined generator

$$\vec{K} = \vec{L} + \vec{S} + \vec{T}$$

For the unit monopole ($n = 1$), the internal direction is $\hat{n} = \hat{r}$, which transforms under the $j = 1$ representation of $SO(3)$. Because the $SU(2)$ adjoint generators $\vec{T}$ also carry $j = 1$, $\vec{L} + \vec{T}$ annihilates $\hat{r}$:

  

$$[L_i + T_i, \hat{r}_a] = 0$$

When $\vert{}n\vert{} > 1$, the topological map $\hat{r}_n = (\sin\alpha(\theta)\cos(n\varphi), \sin\alpha(\theta)\sin(n\varphi), \cos\alpha(\theta))^T$ winds $n$ times around the $z$-axis. Under spatial rotations around the $z$-axis, the azimuthal components carry angular momentum $L_z = \pm n$, whereas an $SU(2)$ adjoint triplet only has internal magnetic quantum numbers $T_3 = 0, \pm 1$. You cannot cancel a spatial rotation of weight $n$ with an $SU(2)$ gauge rotation of weight $1$.

Instead, only the axial generator $K_z = L_z + n T_3$ annihilates $\hat{r}_n$:

$$\left(-i\frac{\partial}{\partial\varphi} + n T_3\right)\hat{r}_n = 0$$

This is the classical theorem proved by **Weinberg and Guth (1976): in $SU(2)$, no spherically symmetric monopole configuration exists for $\vert{}n\vert{} > 1$.**
