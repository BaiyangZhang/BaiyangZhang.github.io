Alright, let us dive right into what you need. To get Gemini to draft your paper section by section with the exact academic tone, theoretical rigor, and consistency we discussed, you want prompts that enforce the proper operator formalisms, boundary conditions, and LSPT scaling without any fluff.

  

Here are the exact prompts you can use for each section:

  

### Prompt for Section I: Introduction and Passive Perspective


Draft Section I of our theoretical physics manuscript on the diagrammatic method in LSPT. 
- Tone: Rigorous, concise, objective academic prose (Phys. Rev. D style), avoiding AI clichés.
- The content, including physics focus. Each part may comprise of multiple paragraphs.
  1. Introduce the background and history of solitons, expecially scalar kinks. 
  2. Review what others have done regarding quantization of soliton states, especially kinks. Introducint the difficulties when regarding kink quantum states as coherent states, including the divergence that Sydney Coleman talk about. mention something like "It was shown that the squeezing will cure this divergence."
  3. Introduce the perturbative calculation of kinks. Review the work done on the one-loop kink mass correction. Review the mismatch between the vacuum sector and kink sector in renormalized perturbation theory. clearly highlight our novel contribution, namely the LSPT, solves this mismatch.
  4. Set the stage by explaining why studying quantum solitons beyond one loop is important, expecially for instance, the history and importance of kink mass quantum corrections. Mention that higher loop correction is also important in tackling IR divergences, meson production, or scattering amplitudes.
  5. The above discussion show that an efficient perturbative calculation tool is needed. Introduce that based on the LSPT, in this paper we introduce an efficient and easy-to-track diagrammatic method that is good for calculating the kink mass corrections and wave function correction.


### Prompt for Section II: Perturbative Field operator in kink sector

Draft Section II of our manuscript, collect and rewrite the necessary formulae from the notes, expecially the .md files.

 1. Explain vacuum polarization and why the Schrödinger picture is necessary to handle non-trivial field expectation values without the inconsistencies of the interaction picture.
 2. Define the $d+1$ dimensional scalar field $\phi(\vec{x})$ and momentum $\pi(\vec{x})$ satisfying the equal-time canonical commutation relation $[\phi(\vec{x}), \pi(\vec{y})] = i\delta^{(d)}(\vec{x}-\vec{y})$.
 3. Introduce the passive perspective: rather than changing the physical state, the unitary displacement operator $\mathcal{D}_f := \exp\{-i\pi(f)\}$ shifts the field-space origin, defining the perturbative field operator $\varphi(\vec{x}) = \mathcal{D}_f \phi(\vec{x}) \mathcal{D}_f^\dagger = \phi(\vec{x}) - f(\vec{x})$ such that $\langle \Psi | \varphi(\vec{x}) | \Psi \rangle = 0$.
 4. Contrast the broken-vacuum sector (constant $v$, plane-wave basis) with the soliton sector (spatially varying $f(x)$, Sturm-Liouville normal modes $\mathfrak{g}_k(x)$, Bogoliubov squeezing, and zero-mode collective coordinates $\phi_0, \pi_0$). 
 5. Emphasis that the kink field operator $\varphi$ is to be expanded in terms of Sturm-Liouville normal modes. There exists a matching between the perturbative field operator and the modes in which the operators are to be expanded, depending on the specific sector. A mismatch will cause computational error.



### Prompt for Section III: The $\phi^4$ Model and Hamiltonian Renormalization Conditions


Draft Section III of our manuscript, focusing on the $\phi^4$ double-well model in the kink sector.
- Tone: Rigorous and precise.
- Physics focus:
  1. Write out the explicit kink sector Hamiltonian density in terms of the kink field operator $H[\varphi, \pi]$ and decompose it into components $H_2, H_3, H_4, H_5$ ordered by powers of the coupling $g$.
  2. State the four non-perturbative Hamiltonian Renormalization Conditions (HRC): (i) $H|\Omega\rangle = 0$, (ii) $H|\vec{p}\rangle = \omega_p |\vec{p}\rangle$, (iii) orthogonal conditions ${}_0\langle \vec{p}_1 \vec{p}_2 | \vec{p}\rangle_{i\ge 2} = 0$, and (iv) the tadpole condition $\langle \Omega | \varphi | \Omega \rangle = 0$. Important: Dicsuss the reasons for choosing them.
  3. Show how the $\mathcal{O}(g)$ no-tadpole condition fixes the counterterm $\delta v_1$ and simplifies $\mathcal{H}_3(\vec{x}) = -\frac{mg}{\sqrt{2}}\varphi^3(\vec{x})$ with $A_3 = 0$.
  4. Provide the exact mode-number decomposition $H_k = \sum_n H_k^{(n)}$ sorted by net meson creation number in the plane-wave/normal-mode ladder operator basis.



### Prompt for Section IV: Diagrammatic Rules


```
Draft Section III of our manuscript, detailing the diagrammatic rules for state corrections and vertices.
- Tone: Direct, economical, and technically precise.
- Physics focus:
  1. Define the prefactors and vertex weights for $H_4$ and $H_5$ interactions.
  2. Explain the rules for reading off internal propagators and energy denominators from $-H_2^{-1}$ (vacuum sector) or $(\omega_p - H_2)^{-1}$ (one-meson sector).
  3. Explain how the 14 second-order wavefunction diagrams in $|\vec{p}\rangle_2$ are stripped of external propagators and treated as effective composite vertices.
  4. Describe the graphical representation of Jarah diagrams, where coupling order increases from right to left across vertical slices representing fixed multi-meson Fock spaces.
```

### Prompt for Section V: Renormalized Wavefunction Corrections and Soliton Sector

Plaintext

```
Draft Section IV of our manuscript, covering renormalized wavefunction corrections and mass/tension shifts.
- Tone: Rigorous and mathematically explicit.
- Physics focus:
  1. Derive the multi-meson Fock components of the vacuum state corrections up to $\mathcal{O}(g^3)$ ($|\Omega\rangle_1^{(3)}, |\Omega\rangle_2^{(4)}, |\Omega\rangle_2^{(6)}$, and $|\Omega\rangle_3^{(1)}$), and show how the disconnected vacuum bubble $(2\pi)^3\delta^3(0)$ cancels against $A_4'$.
  2. Present the one-meson wavefunction corrections and show how the $\mathcal{O}(g^2)$ condition $(\omega_p - H_2)|\vec{p}\rangle_2^{(1)} = 0$ fixes the mass renormalization counterterm $\delta m^2 = -\frac{9g^2m^2}{8\pi^2}\ln\left(\frac{\Lambda}{m}\right) + \text{finite}$.
  3. Group the third-order wavefunction components $|\vec{p}\rangle_3^{(2)}$ into reducible and irreducible diagrams to demonstrate UV divergence cancellation and fix the coupling counterterm $\frac{\delta g}{g} = -\frac{9g^2\ln\Lambda}{16\pi^2} + \text{finite}$.
  4. Apply the passive frame transformation and normal-mode decomposition to evaluate the soliton sector state coefficients $\gamma_i^{mn}$ and compute the one-loop / two-loop mass or domain wall tension corrections.
```

Whenever you are ready to feed these into Gemini or want us to refine any specific equations or derivations further, just let me know.