Define $\mathfrak{n}=\hat{n}^{a}T^{a}$. Initially we have $\mathfrak{n}_ {0}=T^{3}$, the gauge-rotation changes it to $\mathfrak{n}=U\mathfrak{n}_ {0}U^{\dagger}$ (since $\mathfrak{n}$ transforms as a adjoint scalar under gauge transformation). Then $\mathfrak{n}=U(x)T^{3}U^{\dagger}(x)$. 

Correspondingly, the initial gauge field is just the vacuum $A=0$ everywhere, after the gauge transformation we have $A \to U\left( A+i\partial \right)U^{\dagger}=iU\partial U^{\dagger}$.

We have used the Cambridge convention, where the coupling $g$ is absorbed into the definition of the gauge field $A$, thus it does not appear explicitly in the expression. In this convention, in the adjoint representation, the covariant derivative is defined as 

$$
D_ {\mu} \phi = \partial_ {\mu} \phi -i [A,\phi].
$$

- - -

The gauge decomposition decomposes the gauge field into three parts:

$$
A = \hat{A} + X, \quad  \hat{A} = \mathcal{A} + \mathcal{C},
$$

where $\hat{A}$ is the solution of $D_ {\mu}\mathfrak{n}=0$. $X_ {\mu}$ is whatever the components of the gauge field. If $A$ is a pure gauge, we can show that $X_ {\mu}$ actually vanishes, so we are left with $\hat{A}$ only, then we can write $\mathcal{A}_ {\mu}=a_ {\mu} \hat{n}$ and $\mathcal{C}=-\hat{n}\times \partial \hat{n}$. Next let's show that $X_ {\mu}$ indeed vanishes.

To show $X_ {\mu}$ vanishes boils down to show that the pure gauge $A^{\text{pure}}$ itself already satisfies $D_ {\mu}\mathfrak{n}=0$, hence there is nothing left for $X_ {\mu}$. We have (I will neglect the Lorentz index from the second line, writing $\partial_ {\mu}$ as $\partial$ for simplicity)

$$
\begin{align*}
D_ {\mu}\mathfrak{n}  =& \partial_ {\mu}\mathfrak{n}  -i [A^{\text{pure}}_ {\mu},\mathfrak{n} ] \\
=& \partial(UT^{3}U^{\dagger})-i[iU\partial U^{\dagger}, UT^{3}U^{\dagger}] \\
=& \partial UT^{3}U^{\dagger}+UT^{3}\partial U^{\dagger} + U\partial U^{\dagger}UT^{3}U^{\dagger}-UT^{3}U^{\dagger}U\partial U^{^{\dagger}} \\
=& \partial UT^{3}U^{\dagger}+UT^{3}\partial U^{\dagger} - \partial UT^{3}U^{\dagger}-UT^{3}\partial U^{^{\dagger}} \\
=&0.
\end{align*}
$$


