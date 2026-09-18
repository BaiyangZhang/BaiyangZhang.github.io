

  

The topological magnetic field strength is defined as $H_{\mu\nu} = -\frac{1}{g} \hat{n} \cdot (\partial_\mu \hat{n} \times \partial_\nu \hat{n})$. Evaluating this cross product with your specific ansatz yields:

  

$$H_{\mu\nu} = -\frac{1}{g} \frac{h(r) h'(r)}{\sqrt{1-h(r)^2}} (\delta_{\mu r} \partial_\nu \Phi - \delta_{\nu r} \partial_\mu \Phi)$$

The total gauge field is $A_\mu = (1 - f(r)) \mathcal{C}_\mu$. Because $\mathcal{C}_\mu$ now contains orthogonal color components driven by $h(r)$, the cross product $\mathcal{C}_\mu \times \mathcal{C}_\nu$ no longer vanishes. It directly relates to the topological field strength via the identity $\mathcal{C}_\mu \times \mathcal{C}_\nu = -\frac{1}{g} H_{\mu\nu} \hat{n}$.

  

Substituting this relation into the full Yang-Mills field strength tensor $F_{\mu\nu} = \partial_\mu A_\nu - \partial_\nu A_\mu - ig [A_\mu, A_\nu]$ produces a remarkably clean decomposition:

  

$$F_{\mu\nu} = -f'(r) (\delta_{\mu r} \mathcal{C}_\nu - \delta_{\nu r} \mathcal{C}_\mu) + (1-f(r)^2) H_{\mu\nu} \hat{n}$$

### 2. The Effective Action

To find the Lagrangian density $\mathcal{L} = -\frac{1}{4} F_{\mu\nu} F^{\mu\nu}$, we square the field strength tensor. Because the restricted potential $\mathcal{C}_\mu$ is strictly orthogonal to $\hat{n}$, all cross terms between the two parts vanish perfectly.

  

Let $E(r) = \partial_\mu \Phi \partial^\mu \Phi = \omega^2 - k^2 - \frac{n^2}{r^2}$. Contracting the indices using the cylindrical metric gives the effective Lagrangian density:

  

$$\mathcal{L}_{\text{eff}} = \frac{h^2}{2g^2} E(r) \left[ (f')^2 + \frac{(h')^2 (1-f^2)^2}{1-h^2} \right]$$

To obtain the one-dimensional effective action, we multiply this density by the invariant radial integration measure $r$:

  

$$S_{\text{eff}} = \int dr \, L_{\text{1D}}, \quad L_{\text{1D}} = \frac{r E(r) h^2}{2g^2} \left[ (f')^2 + \frac{(h')^2 (1-f^2)^2}{1-h^2} \right]$$

Notice how the $(1-f^2)^2$ term appears natively here. This generates the exact non-linear confining potential required for topological stability.

  

### 3. The Coupled Equations of Motion

We treat $L_{\text{1D}}$ as an effective Lagrangian to find the Euler-Lagrange equations for both profile functions.

  

**Equation of motion for $f(r)$:**

Evaluate the derivatives of $L_{\text{1D}}$ with respect to $f$ and $f'$ to find:

  

$$\frac{d}{dr} \left( r E(r) h^2 f' \right) + \frac{2 r E(r) h^2 (h')^2 f (1-f^2)}{1-h^2} = 0$$

**Equation of motion for $h(r)$:**

Evaluate the derivatives of $L_{\text{1D}}$ with respect to $h$ and $h'$ to find:

  

$$\frac{d}{dr} \left( \frac{r E(r) h^2 h' (1-f^2)^2}{1-h^2} \right) - r E(r) h \left[ (f')^2 + \frac{(h')^2 (1-f^2)^2}{(1-h^2)^2} \right] = 0$$

These coupled, non-linear differential equations dictate the full behavior of the stable vortex string. The next logical step is establishing the proper boundary conditions for $h(r)$ at $r=0$ and $r \to \infty$ to guarantee finite energy. Would you like to map out the asymptotic behavior for these specific boundaries next?


- - -

We find the physical magnetic field vector components in cylindrical coordinates by applying the metric scale factor $1/r$:

- **Longitudinal component:** $B_z = \frac{1}{r} F_{r\varphi} = \frac{n}{gr} f'(r) e^{i(kz-\omega t)} T^{3}$

- **Radial component:** $B_r = -\frac{1}{r} F_{z\varphi} = -i k \frac{n}{gr} f(r) e^{i(kz-\omega t)} T^{3}$

- **Azimuthal component:** $B_\varphi = 0$