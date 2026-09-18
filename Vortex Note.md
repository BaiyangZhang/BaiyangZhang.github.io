### Vortex solution

Recall the EoM w.r.t. $a_ {\mu}$:

$$
\partial_ {\mu}(f_ {\mu \nu}+H_ {\mu \nu} ) = -g \hat{n} \cdot [\vec{X}_ {\mu}\times (\hat{D}_ {\mu}\vec{X}_ {\nu}-\hat{D}_ {\nu}\vec{X}_ {\mu}) + \partial_ {\mu}(\vec{X}_ {\mu}\times \vec{X}_ {\nu}) ]
$$

and that w.r.t. $X_ {\mu}$:

$$
\hat{D}_ {\mu}(\hat{D}_ {\mu}\vec{X}_ {\nu}-\hat{D}_ {\nu}\vec{X}_ {\mu}) = g(f_ {\mu \nu}+H_ {\mu \nu}+ X_ {\mu \nu})\hat{n}\times \vec{X}_ {\mu}.
$$

Now let us consider a string that connects a monopole-antimonopole pair, the vortex solution. Take the cylindrical coordinate $(t,r,\varphi,z)$ and suppose the string streches in the z direction. Take the time-dependent ansatz for the gauge field:

$$
f=0, \quad  \hat{A} = \mathcal{C} =  -\frac{1}{g} \hat{n}\times d\hat{n},
$$
$$
 \vec{X} = \frac{f(r)}{g} e^{-i(\omega t-kz)} \hat{n}\times d\hat{n} = -f(r) e^{-i(\omega t-kz)} \mathcal{C}
$$
where 

$$
\hat{n}=(\cos n\varphi, \sin n\varphi, 0)^{T}.
$$

Take this ansatz to the equation of motion should results in an equation of motion for $f(r)$. Now let's dive into it.

From the definition of $\hat{n}$ we have $d\hat{n}=nd\varphi(-\sin n\varphi, \cos n\varphi,0)^{T}$, hence 

$$
\hat{n}\times d\hat{n} = \hat{z}nd\varphi.
$$

Note two things, it is in $z$ direction and it only has $d\varphi$ component. As a result, 

$$
\begin{align}
\mathcal{C} &= -\frac{1}{g} n\times d n = -\frac{n}{g} d\varphi T^{3}, \\
X &= \frac{nf(r)}{g} e^{-i(\omega t-kz)} d\varphi T^{3}.
\end{align}
$$

Since both $\hat{A}=\mathcal{C}$ and $X$ lie along the same direction, their cross product vanishes, thus $\hat{D}X = \partial X-g\hat{A}\times X = \partial X$. Since $X_ {\mu}$ has only $\varphi$ component, the term $X_ {\mu}\times X_ {\nu}$ also vanishes. Some calculation shows  that the first equation of motion beocmes $LHS=0$ and $RHS=0$, it is satisfired trivially. 

Regarding the second equation of motion, since $\mathcal{C}$ and $X$ both depends on $\varphi$ only, consequently $H_ {\mu \nu}=0$ and $X_ {\mu \nu}=0$. The EoM simplifies to

$$
\hat{D}_ {\mu}(\partial_ {\mu}\vec{X}_ {\nu}-\partial_ {\nu}\vec{X}_ {\mu}) =0.
$$

Define $T_ {\mu \nu}=\partial_ {\mu}\vec{X}_ {\nu}-\partial_ {\nu}\vec{X}_ {\mu}$, then the non-zero components are 

$$
\begin{align*}
T_ {t\varphi} &= -i\omega\frac{nf}{g} e^{-i(\omega t-kz)}T^{3}, \\
T_ {r\varphi} &= \frac{nf'}{g} e^{-i(\omega t-kz)}T^{3}, \\
T_ {z\varphi} &= ik \frac{nf}{g} e^{-i(\omega t-kz)}T^{3}.
\end{align*}
$$

where $T^{3}=\frac{1}{2}\sigma^{3}$ is the group generator. Since they are all proportional to $T^{3}$ direction, again $\hat{D}_ {\mu}{T^{\mu}}_ {\nu}$ beocmes $\nabla_ {\mu}{T^{\mu}}_ {\nu}$, where we have written $\partial_ {\mu}$ to the covariant derivative $\nabla_ {\mu}$ since we will work with polar coordinates. The divergence is $\nabla_ {\mu}T^{\mu \nu}=\frac{1}{\sqrt{\left\lvert g \right\rvert}} \partial_ {\mu}(\sqrt{\left\lvert g \right\rvert}T^{\mu \nu}) + \Gamma_ {\mu \rho}^{\nu}T^{\mu \rho}$, we get 

$$
\hat{D}_ {\mu}T^{\mu \nu} = \nabla_ {\mu} T^{\mu \nu} = \frac{1}{r} \partial_ r (r T^{r\varphi}) + \partial_ z T^{z\varphi} + \partial_ t T^{t\varphi} = 0,
$$

where the indices are raised by $g^{\mu \nu} = \left( 1,-1,-\frac{1}{r^{2}} ,-1 \right)$ corresponding to $x=(t,r,\varphi,z)$:

$$
\begin{align*}
T^{r\varphi} &= \frac{1}{r^{2}} T_ {r\varphi} =\frac{nf'}{gr^{2}} e^{-i(\omega t-kz)}T^{3}\\
T^{z\varphi} &= \frac{1}{r^{2}} T_ {z\varphi} = ik \frac{nf}{gr^{2}} e^{-i(\omega t-kz)}T^{3}\\
T^{t\varphi} &= \frac{1}{r^{2}}  T_ {t\varphi} = i\omega\frac{nf}{gr^{2}} e^{-i(\omega t-kz)}T^{3}
\end{align*}
$$

Substitute these expressions back into the divergence equation and multiply by a factor of $r^{2}$, we obtain the equation of motion for $f(r)$:

$$
\boxed{
f''- \frac{1}{r} f'+(\omega^{2}-k^{2})f =0.
} 
$$

Define $\omega^{2}-k^{2}=:m^{2}$ and introduce the dimensionless parameter $x=mr$, the original equations becomes 

$$
\frac{d^{2}f(x)}{dx^{2}} - \frac{1}{x} \frac{df(x)}{dx}+f(x)=0,
$$

which is a linear equation.

- - -

As a double check, let's take the ansatz into the Lagrangian and derive the equation of motion from variational principal directly. Both $\hat{A}_ \mu$ and $\vec{X}_ \mu$ align exactly along the constant $T_ 3$ color axis, and because they are parallel in color space, their internal cross products vanish identically, i.e. $\hat{A}_ \mu \times \vec{X}_ \nu = 0$ and $\vec{X}_ \mu \times \vec{X}_ \nu = 0$, which reduces the covariant derivative to a standard partial derivative $\hat{D}_ \mu \vec{X}_ \nu = \partial_ \mu \vec{X}_ \nu$), greatly simplifies  the lagrangian. The action becomes 

$$
\mathcal{L} = -\frac{1}{2} (\partial_ \mu X_ \nu - \partial_ \nu X_ \mu)(\partial^\mu X^\nu - \partial^\nu X^\mu)^{\dagger}
$$

With the help of quantities defined before, we get the following result:

$$
\begin{align*}
\left\lvert F_{\mu\nu} \right\rvert ^2 &= 2 \left( g^{rr}g^{\varphi\varphi} \left\lvert F_ {r\varphi} \right\rvert^2 + g^{tt}g^{\varphi\varphi} \left\lvert F_{t\varphi} \right\rvert^2 + g^{zz}g^{\varphi\varphi} \left\lvert F_{z\varphi} \right\rvert^2 \right) \\
&= \frac{2n^2}{g^2 r^2} \left( (f'(r))^2 - \omega^2 (f(r))^2 + k^2 (f(r))^2 \right)
\end{align*}
$$

Hence the action in cylindrical coordinates reads

$$
S =\int d^4x \sqrt{-g} \mathcal{L} = \int dr \, L_{\text{eff}}, \quad  L_{\text{eff}} = -\frac{1}{r} (f'(r))^2 + \frac{\omega^2 - k^2}{r} (f(r))^2 .
$$

The Euler-Lagrangian equation reads

$$
\frac{d}{dr} \left( -\frac{2}{r} f'(r) \right) = \frac{2}{r^2} f'(r) - \frac{2}{r} f''(r)
$$

which simplifies to our previous result:

$$
f''(r) - \frac{1}{r} f'(r) + (\omega^2 - k^2) f(r) = 0.
$$

- - -

Define the substitution $f(r) = r g(r)$, the first derivative is $f'(r) = g(r) + r g'(r)$. The second derivative is $f''(r) = 2g'(r) + r g''(r)$. Substituting these into the original equation yields:

$$
2g'(r) + r g''(r) - \frac{1}{r}[g(r) + r g'(r)] + (\omega^2 - k^2) r g(r) = 0
$$

which simplifies to

$$
r^2 g''(r) + r g'(r) + \left(m^{2}r^2 - 1\right) g(r) = 0, \quad  m^{2} := \omega^2 - k^2.
$$

This is the parametric Bessel equation of the first order. To solve it, define a dimensionless parameter $x:=\mathrm{mr}$, then the equation becomes 

$$
x^2 \frac{d^2g}{dx^2} + x \frac{dg}{dx} + (x^2 - 1) g(x) = 0
$$

which is the standard Bessel differential equation of order 1. Next we discuss two different situations, 1) $\omega^{2}-k^{2}>0$, which implies that $m=\sqrt{\omega^{2}-k^{2}}$ is real; 2) $\omega^{2}-k^{2}<0$, which implies that $m=\sqrt{\omega^{2}-k^{2}}$ is pure imaginary. 

- - -

$\omega^{2}-k^{2}>0$: The general analytical solution is a linear combination of the Bessel function of the first kind $J_ 1(x)$ and the Bessel function of the second kind $Y_ 1(x)$:

$$
g(x) = C_ 1 J_ 1(x) + C_ 2 Y_ 1(x)\implies f(r) = C_ {1}rJ_ {1}(mr) + C_ {2} r Y_ {1}(mr).
$$

The asymptotic behavior of $rJ_ {1},rY_ {1}$ are as follows:

- $rJ_ 1(mr) \sim \frac{mr^{2}}{2}$ at zero and $r J_ 1(mr) \sim \sqrt{\frac{2r}{\pi m}} \cos\left(mr - \frac{3\pi}{4}\right)$ at infinity;
-  $r Y_ 1(mr) \sim -\frac{2}{\pi m}$(constant) at zero and $r Y_ 1(mr) \sim \sqrt{\frac{2r}{\pi m}} \sin\left(mr - \frac{3\pi}{4}\right)$ at inifnity.

*Both of them diverges as $\sqrt{r}$ at $r\to\infty$. It is mathematically impossible to satisfy the boundary condition that $f(\infty)=0$ when $\omega>0$.*

- - -

$\omega^{2}-k^{2}=0$: 

Setting $\omega = 0$ and $k = 0$ reduces the effective mass parameter to zero. The radial differential equation simplifies to:

$$
f''(r) - \frac{1}{r} f'(r) = 0
$$

We can solve this exact analytical equation. Let $v(r) = f'(r)$. The equation becomes a first-order separable differential equation:

$$
v'(r) = \frac{1}{r} v(r)
$$

Integrating both sides yields $\ln\vert{}v\vert{} = \ln\vert{}r\vert{} + c$, which gives $v(r) = C_ {1} r$. Integrate a second time to find the profile function $f(r)$:

$$
f(r) = \frac{1}{2} C_ 1 r^2 + C_ 2.
$$

Now apply the spatial boundary conditions $f(0) = 1$ requires setting the constant $C_ {2} = 1$. The function becomes $f(r) = \frac{1}{2}C_ {1} r^2+1$. On the other hand, the second boundary condition $f(\infty) = 0$ can not be satified, for evaluating our function as $r \to \infty$ gives a second order divergence, it is mathematically impossible to satisfy this condition unless $C_ {1} = 0$.

This mathematical contradiction might be due to *the lack of non-linear interactions needed to stabilize the soliton solution*. In the Abelian Higgs theory, gauge singularities manifest as string-like magnetic vortex tubes. Constructing these physical objects requires a complex scalar field undergoing spontaneous symmetry breaking to form the required vacuum manifold.


- - -

$\omega^{2}-k^{2}<0$: Now $m$ is pure imaginary. The equation transforms into the modified Bessel equation. The solution utilizes the modified Bessel functions of the first kind $I_ 1$ and the second kind $K_ 1$:

$$
f(r) = r [C_ 1 I_ 1(\left\lvert m \right\rvert r) + C_ 2 K_ 1(\left\lvert m \right\rvert r)].
$$

The asymptotic behavior of $r I_ {1}(\left\lvert m \right\rvert r),r K_ {1}( \left\lvert m \right\rvert r)$ are as follows:

- $r I_ 1(\left\lvert m \right\rvert r) \sim \frac{\left\lvert m \right\rvert }{2} r^2$ at origin and $r I_ 1(\left\lvert m \right\rvert r) \sim \sqrt{\frac{r}{2\pi \left\lvert m \right\rvert }} e^{\left\lvert m \right\rvert r}$ at infinity.
-  $r K_ 1(\left\lvert m \right\rvert r) \sim \frac{1}{\left\lvert m \right\rvert }$ at zero and $r K_ 1(\left\lvert m \right\rvert r) \sim \sqrt{\frac{\pi r}{2\left\lvert m \right\rvert }} e^{-\left\lvert m \right\rvert r}$.

In summary, it seems that no solution could satisfy the boundary condition $f(0)=0$ and $f(\infty)=1$. However, **in the case $\omega^{2}-k^{2}<0$, the solution proportional to $K_ {1}$ could satisfy the opposite boundary condition: $f(0)=1$ and $f(\infty)=0$.** It seems to be the only plasuble solution with given ansatz. The plot of $K_ {1}$ is given below, by courtesy of Liping:

![[a17735e23943fa78c92e895aa3c90a06.png]]

- - -

**The Energy Functional of Vortex and Derrick-like Theorem**

Recall that the total gauge field is decomposed into 1)restricted Abelian background ($\mathcal{A}_ \mu + \mathcal{C}_ \mu$) and 2) the valence fluctuation ($X_ \mu$) maintain orthogonal dynamics in color space. Next we give the expression of energy functional in terms of these fields. Then we will derive the energy functional with the aforementioned vortex ansatz, in terms of the profile function $f(r)$. At last we will discuss the stability of permitted vortex solutions with correct boundary condition. 

Recall that the extended Yang-Mills Lagrangian density separates the Abelian field strength from the non-Abelian covariant derivatives:
 
$$
\mathcal{L}_ {\text{ECD}} = -\frac{1}{4}\left[ (f_ {\mu\nu} + H_ {\mu\nu} + X_ {\mu\nu})^2 + (\hat{D}_ \mu \vec{X}_ \nu - \hat{D}_ \nu \vec{X}_ \mu)^2 \right]
$$

Because the restricted fields and valence fluctuations are orthogonal, the total energy functional $E = \int d^3x \, \mathcal{H}$ is the spatial integral of the squared electric ($E_ i = F_ {0i}$) and magnetic ($B_ i = \frac{1}{2}\epsilon_ {ijk}F_ {jk}$) field components for both sectors:

$$
E = \int d^3x \left[ \frac{1}{2} (f_ {0i} + H_ {0i} + X_ {0i})^2 + \frac{1}{4} (f_ {ij} + H_ {ij} + X_ {ij})^2 + \frac{1}{2} (\hat{D}_ 0 \vec{X}_ i - \hat{D}_ i \vec{X}_ 0)^2 + \frac{1}{4} (\hat{D}_ i \vec{X}_ j - \hat{D}_ j \vec{X}_ i)^2 \right].
$$

Applying the vortex ansatz simplifies the energy functional. It's most convenient to go to the Lagrangian $\mathcal{L}_ {ECD}$ rather than energy. 

The ansatz sets $f=0$, meaning the abelian Maxwell potential $\mathcal{A}_ \mu$ is zero, yielding $f_ {\mu\nu} = 0$. The unit vector $\hat{n} = (\cos n\varphi, \sin n\varphi, 0)^T$ depends exclusively on the azimuthal angle $\varphi$ hence as we have shown before that $H_ {\mu\nu} = 0$. The valence field $\vec{X}_ \mu$ is constructed to be strictly proportional to $\mathcal{C}_ \mu = -\frac{1}{g}\hat{n} \times d\hat{n}$. Because they align in color space, their cross product is zero, making the fluctuation tensor $X_{\mu\nu} = 0$ (recall that $X_ {\mu \nu} \mathfrak{n} := -ig [X_ {\mu},X_ {\nu}]$). Also, with $\mathcal{C}_ \mu \times \vec{X}_ \nu = 0$, the gauge covariant derivative reduces to partial derivative. The valence field possesses only an azimuthal component:

$$
X_ \varphi = \frac{n f(r)}{g} e^{-i(\omega t - kz)} T^{3}
$$

The non-zero components of the field strength tensor, denote it by $G_{\mu\nu} := \partial_\mu X_\nu - \partial_\nu X_\mu$, has the following nonzero components:

$$
\begin{align}
G_ {t\varphi} &= \partial_ t X_ \varphi = -i\omega X_ \varphi\\ 
G_ {r\varphi} &= \partial_ r X_ \varphi = \frac{n}{g} f'(r) e^{-i(\omega t - kz)} T^{3} \\
G_ {z\varphi} &= \partial_ z X_ \varphi = ik X_ \varphi
\end{align}
$$

In cylindrical coordinates we raise the spatial indices using (note the change of a minus sign in comparison to Minkowsky metric) $g^{rr} = 1$, $g^{zz} = 1$, and $g^{\varphi\varphi} = \frac{1}{r^2}$. Similar to the electromagnetic case, the physical energy density is $\mathcal{H} = \frac{1}{2} \vert{}E\vert{}^2 + \frac{1}{2} \vert{}B\vert{}^2$  where $E_ i := G_ {0i}$ and $B_ i = \frac{1}{2}\epsilon_ {ijk}G_ {jk}$, thus

$$
\begin{align}
\mathcal{H} &= \frac{1}{2} \left( g^{\varphi\varphi} \left\lvert G_ {t\varphi} \right\rvert ^2 + g^{rr} g^{\varphi\varphi} \left\lvert G_ {r\varphi} \right\rvert ^2 + g^{zz} g^{\varphi\varphi} \left\lvert G_ {z\varphi} \right\rvert ^2 \right) \\ 
            &= \frac{1}{2r^{2}} \left(  \left\lvert \omega X_ {\varphi} \right\rvert ^2 + \left\lvert \frac{n}{g}f' \right\rvert ^2 + \left\lvert kX_ {\varphi} \right\rvert ^2 \right) ,
\end{align}
$$

Substituting the radial profile function $f(r)$ we have

$$\mathcal{H} = \frac{n^2}{2 g^2} \frac{1}{r^2} \left[ (f'(r))^2 + (\omega^2 + k^2) f^{2}(r)\right]$$

To obtain the total energy functional, integrate this density over the invariant cylindrical volume element $d^3x = r dr d\varphi dz$. Integrating out the angular coordinate $\varphi$, we  get the energy density in z-slice:

$$
\boxed{
E =\int dz \, \mathcal{E}, \quad  \mathcal{E} =  \frac{\pi n^2}{g^2} \int dr \frac{1}{r} \left[ (f'(r))^2 + (\omega^2 + k^2) f^2(r) \right].
} 
$$

Given a solution $f(r)$ to the equation of motion, which is *linear*, the rescaled function $\lambda f(r)$ is also a solution. The energy density of $\lambda f$ is simply $\mathcal{E}[\lambda f]=\lambda^{2}\mathcal{E}[f]$, hense we can decrease the energy all the way to $\lambda=0$, unless the value of $\lambda$ is fixed by some boundary condition, such ad $f(0)=1$. Without such boundary conditions the solution is not stable. 

On the other hand, let's consider a space-rescale of the solution, the vortex gets fatter or smaller while other conditions are fixed. **This transformation preserves the boundary condition.** Define $f_ {\lambda}(r):=f(\lambda x)$, define $r'=\lambda r$ then the energy deisity reads

$$
\mathcal{E}[f_ {\lambda}(x)] = \frac{\pi n^{2}}{g^{2}} \int_ {0}^{\infty} dr' \, \frac{1}{r'}\left[ \lambda^{2}\left( \frac{df(r')}{dr'} \right)^{2} + (\omega^{2}+k^{2}) f^{2}(r') \right] .  
$$

Apparently the energy decreases as $\lambda$ decreases, all the way down to $\lambda=0$ and $\mathcal{E}=\frac{\pi n^{2}}{g^{2}} \int_ {0}^{\infty} dr' \, \frac{1}{r'}\left[ (\omega^{2}+k^{2}) f^{2}(r') \right]$, which is zero if $\omega=k=0$. *The solution is again unstable, it will grow fatter and fatter!*

- - -

As a possible remedy, let's try to introduce time dependence to the vector field $\hat{n}$. The idea is that:
1. Introduce the time dependence;
2. Keep $\mathcal{C}=-f(r)X$ so that the boundary condition is clean.

Define $\Phi(\varphi,t):=n\varphi-\omega t$, let $\hat{n}=(\cos \Phi,\sin \Phi,0)^{T}$. Then the $\mathcal{C}$ field reads

$$
\mathcal{C}_ {\mu} = - \frac{1}{g} \hat{n} \times  d\hat{n} = -\frac{n}{g} \hat{e}_ {3} d\varphi + \frac{\omega}{g} \hat{e}_ {3} dt.
$$

It is still in $\hat{e}_ {3}$ direction, but with $t$-component now. Assume $X=-f(r)\mathcal{C}$ as usual. The field strength reduces to (as before) $F=dA-ig A\wedge A$ where $A=\mathcal{C}+X=(1-f(r))\mathcal{C}$. Since $\mathcal{C}$ does not depend on any coordinates really, we have $d\mathcal{C}=0$, and $\mathcal{C}\wedge\mathcal{C}=0$. Thus 

$$
F= \frac{f'(r)}{g} (-ndr\wedge d\varphi+\omega dr\wedge dt)T^{3}.
$$

The action is 

$$
S = - \frac{1}{4} \int  \,F\wedge \star F,
$$

thus we need to know $\star dr\wedge d\varphi$ and $\star dr\wedge dt$ in cylindrical coordinage. Using the definition $\omega \wedge\star \omega=\left\langle \omega,\omega \right\rangle d\text{Vol}$, where $d\text{Vol}=rdt\wedge dr\wedge d\varphi \wedge dz$, we have $\star dr\wedge d\varphi=\frac{1}{r} dt\wedge dz$ and $\star dt \wedge dr=-rd\varphi \wedge dz$. Hencd 

$$
S = \int dtdz \, \mathcal{L}_ {\text{eff}},\quad  \mathcal{L}_ {\text{eff}} = \int dr \, \frac{\pi f'^{2}}{2rg^{2}}(\omega^{2}r^{2}-n^{2}).  
$$

The Euler-Lagrange equation from $\mathcal{L}_ {\text{eff}}$ reads 

$$
\frac{d}{dr} \left[ r f'(r) \left( \omega^2 - \frac{n^2}{r^2} \right) \right] = 0
$$

**which is still a linear equation of motion.** It has solutions of form

$$
f(r) = \frac{C_ {1}}{\omega^{2}} \ln \left\lvert r^{2}\omega^{2}-n^{2} \right\rvert +C_ {2}.
$$

*This ansatz does not seem to work.*

- - -

Another ansatz is to introduce an $r$-dependence to $\hat{n}$. By introducing the radial profile $h(r)$ into the topology field $\hat{n}$, we mignt be able to restore the non-abelian self-interactions required to stabilize the vortex. Define $\Phi(\varphi,t,z) := n\varphi - \omega t + kz$, and modified direction field is $\hat{n} = (h(r)\cos\Phi, h(r)\sin\Phi, \sqrt{1-h(r)^2})$. **It seems to be a promising approach to introduce non-linear, stabalizing interaction. What do you think?**
