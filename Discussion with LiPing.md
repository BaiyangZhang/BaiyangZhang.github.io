The original equation Eq.(67)  is 

$$\ddot{\alpha} + \frac{\cos\alpha}{\sin\alpha}\dot{\alpha}^2 - \frac{\cos\theta}{\sin\theta}\dot{\alpha} = 0 \quad (67)$$

Notice that the first two terms can be written as $\frac{1}{\sin\alpha}\frac{d}{d\theta}(\dot{\alpha}\sin\alpha)$, the equation becomes 

$$
\begin{align*}
& \frac{1}{\sin \alpha} \frac{d}{d\theta}(\dot{\alpha}\sin\alpha) - \frac{\cos\theta}{\sin\theta} \dot{\alpha} = 0 \\
 \implies & \frac{1}{\sin\theta} \frac{d}{d\theta}\left(\frac{\dot{\alpha}\sin\alpha}{\sin\theta}\right) - \frac{\cos}{\sin ^{2}\theta} \theta(\dot{\alpha}\sin \alpha) = 0\\
 \implies & \frac{d}{d\theta}(\dot{\alpha}\sin\alpha) - \frac{\cos\theta}{\sin\theta}(\dot{\alpha}\sin\alpha) = 0 \\\implies & \frac{d}{d\theta}\left(\frac{\dot{\alpha}\sin\alpha}{\sin\theta}\right) = 0.
\end{align*}
$$

Hence we have 

$$
\frac{\dot{\alpha}\sin\alpha}{\sin\theta} = C_ {1}.
$$

Then this ODE can be solved by the stardard method of separation of variables. We get 

$$\cos\alpha = C_1 \cos\theta - C_2.$$

The boundary condition given in Eq. (62) is $\alpha(0) = 0$ and $\alpha(\pi) = \pi$. This yields $C_ {1}-C_ {2}=1$ and $C_ {1}+C_ {2}=1$. Hence $C_ {1}=1$ and $C_ {2}=0$. The solution is

$$
\boxed{ 
\cos \alpha=\cos \theta \implies \alpha=\theta+2\pi N, \quad  N\in \mathbb{N}.
}
$$