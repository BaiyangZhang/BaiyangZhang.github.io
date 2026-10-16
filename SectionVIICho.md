\section{Uniqueness of Abelian Decomposition} 

The Abelian decomposition plays a central role in understanding the physics of QCD. Therefore, it is important to know whether the Abelian decomposition is unique. To clarify this question, suppose we have a QCD gauge potential $\hat{A}_\mu$. The Abelian decomposition of this potential clearly depends on the Abelian direction $\hat{n}$. If we choose two different Abelian directions, we obtain two different Abelian decompositions. However, they should be gauge-equivalent since the two Abelian directions are connected by a gauge transformation. This strongly suggests that the Abelian decomposition is unique once an Abelian direction is selected.

To discuss this question in more detail, consider the Wu-Yang potential given by
\begin{gather}
\hat{A}_ {\mu} = - \frac{1}{g} \hat{r}\times \partial_ {\mu}\hat{r}
\label{wy1}
\end{gather}
Obviously with $\hat{n}=\hat{r}$ as the Abelian direction, we have the following Abelian decomposition of the Wu-Yang potential \cite{prd80,prl81,prl80}:
\begin{gather}
\hat{A}_ {\mu} = -\frac{1}{g}\hat{r}\times \partial_ {\mu}\hat{r}, \quad  \hat{X}_ {\mu} =0.
\label{wy1r}
\end{gather}
which can also be expressed under the gauge transformation $\hat{r} \rightarrow \hat{e}$ as
\begin{gather}
\hat{A}_ {\mu} = -\frac{1}{g}(1-\cos \theta)\partial_ {\mu}\varphi, \quad  \hat{X}=0.
\label{wy1e}
\end{gather}

On the other hand, because we can express the Wu-Yang monopole potential Eq.~(\ref{wy1}) as
\begin{align} 
\notag
\vec{A} _ {\mu} &= -\frac{1}{g}\hat{r}\times \partial_ {\mu}\hat{r} = \frac{1}{g}(\sin \theta \partial_ {\mu}\varphi\, \hat{\theta}-\partial_ {\mu}\theta\, \hat{\varphi}) \\\notag
&= (\sin \theta \cos \theta \sin\varphi\, \partial_ {\mu\varphi}-\cos\varphi \partial_ {\mu}\theta) \hat{e}_ {1}\\\notag
&\;\;\;\;\; + (\sin \theta \cos \theta \cos\varphi\, \partial_ {\mu\varphi} + \sin\varphi\,\partial_ {\mu}\theta)\hat{e}_ {2}\\
&\;\;\;\;\; -\sin ^{2}\theta \partial_ {\mu}\varphi \hat{e},
\label{wy2}
\end{align}
we obtain another Abelian decomposition of Eq.~(\ref{wy1}) with $\hat{n}=\hat{e}$:
\begin{align} 
\notag
\hat{A}_ {\mu} &= -\frac{1}{g} \sin ^{2}\theta \partial_ {\mu}\varphi \hat{e}, \\
\notag
\vec{X} &= \frac{1}{g} \Big[ (\sin \varphi \partial_\mu \theta +\sin \theta \cos \theta
\cos \varphi \partial_\mu \varphi)~\hat{e}_1 \\
&\;\;\;\;\; -(\cos \varphi \partial_\mu \theta -\sin \theta \cos \theta \sin \varphi \partial_\mu \varphi )~\hat{e}_2 \Big], 
\end{align}
or equivalently,
\begin{align} 
\notag
\hat{A}_ {\mu} &= - \frac{1}{g} \sin ^{2}\theta \partial_ {\mu}\varphi~\hat{e}, \\
\notag
\vec{X} &= \frac{1}{g} (\sin \theta \cos \theta \partial_ {\mu}~\hat{e}'_ {1}-\partial_ {\mu} \theta \hat{e}'_ {2}),
\label{wy2e}
\end{align} 
where 
$$
\begin{pmatrix}
\hat{e}'_ {1} \\
\hat{e}'_ {2}
\end{pmatrix}
=
\begin{pmatrix}
\cos\varphi & \sin \varphi \\
-\sin\varphi  & \cos\varphi
\end{pmatrix}
\begin{pmatrix}
\hat{e}_ {1} \\
\hat{e}_ {2}
\end{pmatrix}.
$$
Moreover, changing the basis $(\hat{e}_1',\hat{e}_2',\hat{e})$ to $(\hat{\theta},\hat{\varphi},\hat{r})$ (and the Abelian direction $\hat{e}$ to $\hat{r}$), we can express this Abelian decomposition gauge-equivalently as
\begin{align} 
\notag
\hat{A}_ {\mu} &= -\frac{1}{g} \cos \theta(1-\cos \theta)\partial_ {\mu}\varphi~\hat{r}-\frac{1}{g}\hat{r}\times \partial_ {\mu}\hat{r}, \\
\vec{X} &= \frac{1}{g}(\sin \theta \cos \theta \partial_ {\mu}\varphi~\hat{\theta}-\partial_ {\mu}\theta~\hat{\varphi}).
\label{wy2r}
\end{align}
Apparently, the two Abelian decompositions Eq.~(\ref{wy1r}) and Eq.~(\ref{wy2r}) fixed by the same Abelian direction $\hat{n}=\hat{r}$ are not just different, but appear gauge-inequivalent. Similarly, the two Abelian decompositions Eq.~(\ref{wy1e}) and Eq.~(\ref{wy2e}) fixed by the same Abelian direction $\hat{e}$ also appear different and gauge-inequivalent. If so, we have two different Abelian decompositions of Eq.~(\ref{wy1}) for the same Abelian direction $\hat{n}$. 

Moreover, because both Eq.~(\ref{wy1r}) and Eq.~(\ref{wy2r}) originate from the same Wu-Yang potential, they should both be solutions of QCD. To show that Eq.~(\ref{wy1r}) is a solution of QCD, we only need to solve the first equation of Eq.~(\ref{ecdeq3}). However, to show that Eq.~(\ref{wy2r}) is a solution of QCD, we need both equations of Eq.~(\ref{ecdeq3}). Thus, they satisfy different sets of equations, which implies that they are different solutions.

This is puzzling because it contradicts our intuition that the Abelian decomposition is uniquely determined once the Abelian direction is chosen. What is going on here?

To claim that the Abelian decomposition is unique once an Abelian direction is selected, we must show that the decompositions Eq.~(\ref{wy1r}) and Eq.~(\ref{wy1e}) are at least gauge-equivalent to Eq.~(\ref{wy2r}) and Eq.~(\ref{wy2e}). Clearly, they are not gauge-equivalent under the active gauge transformation given by Eq.~(\ref{agt0}). However, remember that with the Abelian decomposition, we have two types of gauge transformations: the classical (active) gauge transformation described by Eq.~(\ref{agt0}) and the quantum (passive) gauge transformation described by Eq.~(\ref{pgt0}). 

In the quantum gauge transformation, $\hat{n}=0$. This means that even after selecting the Abelian direction $\hat{n}$, we retain the full quantum gauge degrees of freedom, under which the two decompositions Eq.~(\ref{wy1r}) and Eq.~(\ref{wy1e}) can be transformed into Eq.~(\ref{wy2r}) and Eq.~(\ref{wy2e}). This should be clear because any two gauge potentials can be connected to each other by a gauge transformation, classical or quantum. This shows that two different Abelian decompositions may not be gauge-equivalent under classical gauge transformations, yet remain gauge-equivalent under quantum gauge transformations. 

This exercise teaches us an important lesson: two apparently different Abelian decompositions can actually describe the same configuration. We must keep this observation in mind when discussing the gauge equivalence of the Abelian decomposition in QCD.