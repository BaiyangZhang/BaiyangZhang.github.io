Suppose the $A,X$ vectors are expanded in basis of $\hat{n}_ {1,2,3}$ where $\hat{n}_ {3}=:\hat{n}$. That is,

$$
\hat{A} = A^{a} \hat{n}_ {a}, \quad  \vec{X}=X^{i}\hat{n}_ {i}.
$$

In the extended Lagrangian, in its original SU(2) form, the covariant terms reads

$$
 \mathcal{L}_ {\text{ECD}} = \mathrm{Tr}\,\left\lbrace (\hat{D}_ {\mu}X_ {\nu}-\hat{D}_ {\nu}X_ {\mu})^{2} +\cdots \right\rbrace 
$$

where $\hat{D}X=(\partial-i[\hat{A},-])X$. Define $\mathfrak{n}_ {a}:=\hat{n}_ {a}^{i} T^{i}$ which is just the $\hat{n}_ {a}$ vector in the basis of $T^{a}$. Substitute the first Equation, I get terms like $\mathrm{Tr}\,\left\lbrace \partial_ {\mu}\mathfrak{n} _ {a}\partial_ {\mu}\mathfrak{n_ {b}}\right\rbrace=\frac{1}{2}(\partial_ {\mu}\hat{n}_ {a})\cdot(\partial_ {\mu}\hat{n}_ {b})$. I can't get rid of it.

- - -


In SU(2), we have 

$$
F_ {\mu \nu} = \partial _ {\mu}A_ {\nu}-\partial_ {\nu}A_ {\mu} -i[A_ {\mu},A_ {\nu}]
$$

write $A=A^{a}T^{a}$, we can write 

$$
F_ {\mu \nu} = \partial_ {\mu}A_ {\nu}^{a}T^{a} -\partial_ {\nu}A_ {\mu}^{a}T^{a} + \epsilon^{ija}A_ {\mu}^{i}A_ {\nu}^{j}T^{a}
$$

so in the basis of $T^{a}$ we have $\vec{F}=\partial \vec{A}-\partial \vec{A}+\vec{A}\times \vec{A}$. But in basis of $\hat{n}_ {a}$, we have 

$$
\begin{align*}
F_ {\mu \nu} =& \partial_ {\mu}(A_ {\nu}^{a}\hat{n}_ {a}) -\partial_ {\nu} (A_ {\mu}^{a} \hat{n}_ {a} )+ \epsilon^{ija}A_ {\mu}^{i}A_ {\nu}^{j}\hat{n}_ {a}\\
=& (\partial_ {\mu}A_ {\nu}^{a}) \hat{n}_ {a} - (\partial_ {\nu}A_ {\mu}^{a}) \hat{n}_ {a} + \epsilon^{ija}A_ {\mu}^{i}A_ {\nu}^{j}\hat{n}_ {a} 
+A_ {\nu}^{a} (\partial_ {\mu}\hat{n}_ {a}) - A_ {\mu}^{a} (\partial_ {\nu}\hat{n}_ {a})
\end{align*}
$$

$$
\vec{X}=X^{a} T^{a} = X^{(i)} \hat{n}_ {i}.
$$