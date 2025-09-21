let $a,a^{\dagger}$ be ladder operators in quantum mechanics, satisfying the commutation relation $[a^{\dagger},a]=1$. The Baker-Campbell-Harsdorf formula says that

$$
e^{A+B} = e^{A}e^{B}e^{-1/2 [A,B]}
$$

if $[A,B]$ commutes with both $A$ and $B$. If we apply it to $a^{\dagger},a$, we get 

$$
e^{a^{\dagger}-a} = e^{a^{\dagger}} e^{a}e^{-1/2 [a^{\dagger},a]} = e^{a^{\dagger}}e^{a}e^{1/2}.
$$

If we apply it to the ground state $\left\lvert 0 \right\rangle$, then the right hand side is 

$$
e^{a^{\dagger}}e^{a}e^{1/2}\left\lvert 0 \right\rangle =0
$$

since $a$ annihilates the vacuum, but the left hand side is $e^{a^{\dagger}-a}\left\lvert 0 \right\rangle\neq 0$. where did I do wrong?