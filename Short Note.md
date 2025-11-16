

Hi professor Cho, 

I think I have proven that the *active* gauge transformation for $\mathcal{C}=-\frac{1}{g}\hat{n}\times \partial \hat{n}$ that you defined is equivalent to a simpler form:

$$
\mathcal{C}\to \mathcal{C'}= - \frac{1}{g}\hat{n}'\times \partial \hat{n}', \quad  \hat{n}':=\Omega \hat{n}\Omega ^{\dagger}
$$
where $\Omega=\exp(i\alpha)$ is the finite gauge transformation. The prove has something to do with the uniqueness of the solution for $\hat{D}_ {\mu}\hat{n}=0$ that is orthodox to $\hat{n}$.
Especially, I am able to show this equivalence both of infinitesimal form and finite form for a special kind of gauge transformation, that keeps $\hat{n}$ invariant:
$$
U:= e^{i k \hat{n}}, \quad  \hat{A}\to \hat{A}'=U\left( \hat{A}+\frac{i}{g}\partial \right)U^{\dagger}.
$$
In this case we have
$$
\hat{A}\to  \hat{A}' = U\left( \mathcal{A}+ \mathcal{C} + \frac{i}{g}\partial \right) U ^{\dagger} = A\mathfrak{n} + \frac{2i}{g}\mathfrak{n} U\partial \mathfrak{n} U^{\dagger} + \frac{i}{g} U \partial U^{\dagger}.
$$
where $\mathfrak{n}$ is the $\mathfrak{g}$-version of $\hat{n}$, that is $\mathfrak{n}:=\hat{n}^{i}T^{i}$, and $T^{i}$ is the generator of $SU(2)$.

Since $U = \exp ik\mathfrak{n}=\cos \frac{k}{2} \mathbb{1}_ {2}+2i\sin \frac{k}{2}\mathfrak{n}$, we have 

$$
\begin{align*}
\frac{2i}{g}\mathfrak{n} U \partial \mathfrak{n} U^{\dagger} &= \frac{2i}{g}\left( \mathfrak{n} \partial \mathfrak{n} \cos k + \frac{i}{2} \partial \mathfrak{n}  \sin k \right),\\
\frac{i}{g}U \partial U^{\dagger} &= \frac{i}{g}\left( -i\partial k\mathfrak{n} -i\partial \mathfrak{n} \sin k + 4\sin ^{2} \frac{k}{2} \,\mathfrak{n} \partial \mathfrak{n}  \right).
\end{align*}
$$

Put everything together we get that 

$$
\hat{A} \to  \hat{A}' = \left( A+\frac{\partial k}{g} \right)\mathfrak{n} + \mathcal{C},\quad  \mathcal{C}=\frac{2i}{g}\mathfrak{n} \partial \mathfrak{n} .
$$

in vector form it is just $\hat{A}'=(A+\partial k /g)\hat{n}-\frac{1}{g}\hat{n}\times \partial \hat{n}$.