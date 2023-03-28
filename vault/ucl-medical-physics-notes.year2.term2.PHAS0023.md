---
id: wgh08s9ib5clee31zyfmu44
title: PHAS0023
desc: Atomic and Molecular Physics
updated: 1680014176123
created: 1676488050139
---
# Atomic and Molecular Physics
***
# 1 One-electron atoms
## 1.1 One-electron systems with infinitely heavy nuclei

Consider atoms and atomic ions with *one electron* bound to a nucleus with charge $q=+Ze$.

One-electron systems can be solved using the Coulomb potential.
$$
V(r)=\dfrac{-Ze^2}{4\pi\epsilon_0r}\qquad\epsilon_0=8.85\times10^{-12}\;\textrm{Fm}^{-1}
$$

Assuming that the nucleus is infinitely heavy, the Hamiltonian is then
$$
\hat{H}=-\dfrac{\hbar^2}{2m_e}\nabla^2-\dfrac{Ze^2}{4\pi\epsilon_0r}
$$

Energy eigenvalues can be found by solving the Schrödinger equation
$$
\hat{H}\psi=E\psi
$$
$$
\Rightarrow\;E_n=-\dfrac{m_eZ^2e^4}{32\pi^2\epsilon_0^2\hbar^2n^2}
$$
$$
\begin{array}{l}
\textrm{Fine structure constant} & \alpha=\dfrac{e^2}{4\pi\epsilon_0\hbar c}=\dfrac{1}{137.036} \\
\textrm{Bohr radius} & a_0=\dfrac{4\pi\epsilon_0\hbar^2}{m_ee^2}=5.292\times10^{-11}\,\textrm{m} \\
\textrm{Rydberg constant} & \textrm{R}_{\infty}=\dfrac{\alpha^2m_ec}{2h}=1.0974\times10^7\;\textrm{m}^{-1} \\
& hc\textrm{R}_{\infty}=13.606\;\textrm{eV} \\
\end{array}
$$
$$
E=h\nu=\dfrac{hc}{\lambda}
$$

The Rydberg formula can be used to calculate emission or absorption lines
$$
\dfrac{1}{\lambda}=\textrm{R}_\infty Z^2\left(\dfrac{1}{n_f^2}-\dfrac{1}{n_i^2}\right)
$$

When $n$ is large, the Rydberg formula can be differentiated to find specific transition energies.
$$
\dfrac{\Delta E}{hc}=\dfrac{R_X}{n^3}
$$

## 1.2 Mass Corrections

Taking into account the finite mass of the proton, the corrected Rydberg constant is
$$
R_\textrm{X}=R_\infty\dfrac{\mu_\textrm{X}}{m_e}Z^2
$$

Where reduced mass is
$$
\mu=\dfrac{m_1m_2}{m_1+m_2}
$$

The Bohr radius $a_0$ must also be adjusted
$$
a_\textrm{X}=a_0\dfrac{m_e}{\mu_\textrm{X}}\dfrac{1}{Z}
$$

## 1.3 Parity

Parity operator
$$
\hat{P}f(r)=f(-r)
$$

The parity of $\text{e}^{im_l\phi}$ is given by $(-1)^{m_l}$
<br>The parity of $P_{l}^{m_l}(\cos\theta)$ is given by $(-1)^{l-m_l}$
$$
\Rightarrow\;\hat{P}\,Y_{lm}=(-1)^{l}Y_{lm}
$$

1. if $f(-r)=f(r)\quad\Rightarrow\quad f(r)$ has *even* parity
2. if $f(-r)=-f(r)\quad\Rightarrow\quad f(r)$ has *odd* parity

## 1.4 Spectroscopic notation

![](/assets/images/2023-02-22-18-01-17.png){max-width: 300px, display: block, margin: 0 auto}

For higher $n$ or higher $l$, the electron is on average further away
from the nucleus. Low $l$ subshells are more "core-penetrating".
$$
\langle r\rangle=\dfrac{a_H}{2}\left[3n^2-l(l+1)\right]
$$

## 1.5 Energy level degeneracy

$$
\dfrac{E_n}{hc}=-\dfrac{\textrm{R}_\textrm{M}}{n^2}
$$

The total number of degenerate states with the same energy in a
one-electron system is
$$
\sum_{l=0}^{n-1}(2l+1)=n^2
$$
(or $2n^2$ when including spin)

- $m$-degeneracy: The $m$-degeneracy of the eigenstates in a one-electron 
atom is a feature of a central potential, i.e. $V = V(r)$
- $l$-degeneracy: The $l$-degeneracy of the eigenstates in a one-electron
atom is a characteristic of a potential, such as the Coulomb potential,
that depends on $1/r$. It is removed if the $1/r$-dependence of the potential is
modified.

## 1.6 Electron spin

The electron has the intrinsic property spin $s$, which is analogous to
angular momentum $l$.
$$
\left[\hat{S}^2,\hat{S}_z\right]=0
$$
$$
\hat{S}^2\chi_{s,m_s}=s(s+1)\hbar^2\chi_{s,m_s}\quad s=1/2
$$
$$
\hat{S}_z\chi_{s,m_s}=m_{s}\hbar\chi_{s,m_s}\quad m_s=\pm 1/2
$$
$$
\Psi_{n,l,m_l,s,m_s}(r,\theta,\phi)=
\underbrace{R_{n,l}(r)\,Y_{l,m_l}(\theta,\phi)}_\textrm{Space}\;
\underbrace{\chi_{s,m_s}}_\textrm{Spin}
$$

## 1.7 Selection rules for transitions between energy levels

Transitions between different eigenstates due to emission or absorption of photons 
must follow *selection rules*. In a one-electron atom:

- $\Delta n\;=\;$ any value
- $\Delta l\;=\;\pm 1$ to conserve angular momentum
- $\Delta s\;=\;0,\pm 1$

***
# 2 Multi-electron atoms
## 2.1 Hamiltonian for many-electron atoms

The Hamiltonian for an atom with $N$ electrons, assuming an infinitely
heavy nucleus, has the form:
$$
\hat{H}(r_1,r_2,r_3,\dots,r_N)=
\underbrace{\sum_{i=1}^{N}\left\{-\dfrac{\hbar^2}{2m_e}\nabla^2_i
-\dfrac{Ze^2}{4\pi\epsilon_0r_i}\right\}}
_\textrm{Sum of single-electron Hamiltonians}
+\underbrace{\sum_{i=1}^{N}\sum_{j\gt i}^{N}
\dfrac{e^2}{4\pi\epsilon_0r_ij}}
_\textrm{Electron-electron repulsion}
$$

This cannot be solved analytically due to the exact positions of the
electrons being unknown, but the single-electron contributions can be
separated using approximations.

## 2.2 Approximate solutions to the N-electron atom

### Approximation 1: Independent particle model

In this model, the electron-electron repulsion is first ignored, leaving
only the sum of individual Hamiltonians, such that
$$
E=E_1+E_2+E_3+\dots+E_N
$$

This is a very crude approximation, which assumes that the electrons are
much more strongly bound than they actually are. The neglected interactions
are then added to the result. E.g. for Helium:
$$
a_{He}(1s)\simeq\dfrac{a_0}{Z}=\dfrac{a_0}{2}
$$

Assuming electrons are on opposite sides of the atom, an approximation for
the repulsion energy can be calculated and added to the independent particle result.

Electron-electron interactions are very significant, so this method will only work 
for Helium (and only if the repulsion is "manually" added to the result).

### Approximation 2: Central field approximation

This approximation instead introduces a central potential $V_C(r_i)$ to the Hamiltonian.
$$
\hat{H}(r_1,r_2,r_3,\dots,r_N)=\sum_i\hat{h}(r_i)
$$
$$
\hat{h}(r_i)=-\dfrac{\hbar^2}{2m_e}\nabla^2-\dfrac{Ze^2}{4\pi\epsilon_0r_i}+V_C(r_i)
$$
where
$$
V_C(r_i)=\left\langle\dfrac{e^2}{4\pi\epsilon_0r_ij}\right\rangle_{j\neq i}
$$

The central field approximation is most applicable for alkali metal atoms with one outer
shell valence electron, or Rydberg atoms with one highly excited electron. In these cases,
the effective $Z_{\text{core}}=+1$

### Approximation 3: Quantum defect $\Delta_{nl}$

Within the central field proximation, the eigenenergies of the outer electron can be
expressed as
$$
\dfrac{E_{nl}}{hc}=-\dfrac{R_M}{(n-\Delta_{nl})^2}
$$
$$
R_M=R_\infty\dfrac{\mu_M}{m_e}Z_{\text{core}}^2
$$
where $Z_{\text{core}}$ is the effective charge that the outer electron experiences.

$\Delta_{nl}$ is larger for lower $l$ states, as these are more core-penetrating, and
is slightly smaller for large $n$ states.

![Quantum defects for the low-n triplet states of He.](/assets/images/2023-02-22-18-05-44.png){max-width: 350px, display: block, margin: 0 auto}

## 2.3 Indistinguishable particles and the Pauli principle

In quantum mechanics, many particles such as electrons or photons are indistinguishable, leading to the condition
$$
|\psi(1,2)|^2=|\psi(2,1)|^2
$$
Which can be satisfied in two ways
1. Symmetric:$\quad\psi(1,2)=\psi(2,1)$
2. Antisymmetric:$\quad\psi(1,2)=-\psi(2,1)$

Any allowed wavefunction must be either symmetric or antisymmetric with respect to the exchange of two particles.

### The Pauli Principle

Wolfgang Pauli postulated that two electrons cannot occupy the same quantum state: the Pauli exclusion principle.

This leads to the observation that any total wavefunction **must be antisymmetrical** with respect to exchange of identical Fermions, and symmetric with respect to the exchange of identical Bosons.

A generalised two-electron wavefunction fulfilling the Pauli principle has the form
$$
\begin{array}{ll}
\psi(1,2) & =\dfrac{1}{\sqrt{2}}\left[\phi_A(1)\phi_B(2)-\phi_A(2)\phi_B(1)\right] \\
& =-\psi(2,1) \\ \end{array}
$$

## 2.4 Effect of the Pauli Principle on atomic structure

### 2.4.1 Spin wavefunctions
$$
\Psi(1,2)=\Psi(r_1,r_2)\chi(\sigma_1,\sigma_2)=-\Psi(r_2,r_1)\chi(\sigma_2,\sigma_1)
$$
For an individual electron wavefunction,
$$
s=\dfrac{1}{2}
$$
$$
\begin{array}{ll}
\textrm{Spin up} & \textrm{Spin down} \\
m_s=+\dfrac{1}{2} & m_s=-\dfrac{1}{2} \\
\hat{S}_z\alpha=+\dfrac{1}{2}\hbar\alpha & \hat{S}_z\beta=\dfrac{1}{2}\hbar\beta \\
\end{array}
$$
Calculating total spin quantum number for two electrons
$$
\vec{S}=\vec{s}_1+\vec{s}_2
$$
Total spin number 
$$
S=|s_1-s_2|,\dots,|s_1+s_2|
$$

Consider separately the $S=0$ and $S=1$ cases:
- $S=0$: When $S=0$, $M_S=0$

  Because there is only one value of $M_S$, this is known as a **singlet spin state**.

  $M_S=0$: Antisymmetric form of each electron having different spin.

  $$
  \chi^S=\dfrac{1}{\sqrt{2}}\left[\alpha(1)\beta(2)-\alpha(2)\beta(1)\right]
  $$

- $S=1$: When $S=1$, $M_S=-1,0,+1$

  Because there are three values of $M_S$, this is known as a **triplet spin state**.

  $M_S=+1$: Spins of electrons both parallel to z-axis.
  $$
  \chi^T=\alpha(1)\alpha(2)
  $$

  $M_S=-1$: Spins of electrons both antiparallel to z-axis.
  $$
  \chi^T=\beta(1)\beta(2)
  $$

  $M_S=0$: Two above wavefunctions are symmetric, so this must also be symmetric.
  Symmetric form of each electron having different spin.
  $$
  \chi^T=\dfrac{1}{\sqrt{2}}\left[\alpha(1)\beta(2)+\alpha(2)\beta(1)\right]
  $$

### 2.4.2 He atom wavefunctions

The symmetric/antisymmetric spacial wavefunction for helium is
$$
\Phi_{\pm}(r_1,r_2)=
\dfrac{1}{\sqrt{2}}\left[\phi_i(r_1)\phi_j(r_2)\pm\phi_i(r_2)\phi_j(r_1)\right]
$$
where, due to the Pauli principle:

![Spin and Space wavefunctions must have opposite symmetries so that the total wavefunction is antisymmetric.](/assets/images/2023-02-26-16-58-46.png){max-width: 400px, display: block, margin: 0 auto}

When the Helium is in its ground state, $\phi_i=\phi_j=\phi_{1s}$, so only the symmetric form of the space wavefunction is allowed, and to satisfy the Pauli principle, the spin wavefunction **must** be in the **antisymmetric singlet** form.

Excited states of Helium where the electrons occupy *different* orbitals, like the 1s2s configuration for example, can be either singlet or triplet states.

### Spin Multiplicity

Any value of $S$ has $(2S+1)$ associated values of $M_S$. This quantity $(2S+1)$ is known as the **spin multiplicity**.

## 2.5 The Exchange Interaction

Considering $r_1=r_2$ for the spacial part of the triplet state wavefunction, gives a value of zero for the antisymmetric spacial wavefunction, meaning that the electrons avoid each other, reducing screening.

As a result, the electrons are more strongly bound to the nucleus (lower in energy) in the triplet state than in the singlet state, where there is a non-zero probability of finding the electrons close together.

![Energy splitting between the 1s2s singlet and triplet states of He that results from the Exchange Interaction. Triplet S=1 state is lower in energy.](/assets/images/2023-02-26-17-11-10.png){max-width: 300px, display: block, margin: 0 auto}

This energy shift resulting from the Pauli principle suggests an interaction between electrons which depends on their spins: the **Exchange Interaction**.

Consider the Coulomb repulsion due to the electron charges
$$
V_\textrm{rep}=\dfrac{e^2}{4\pi\epsilon_0 r_{12}}=C\dfrac{1}{r_{12}}
$$
So the electron-electron repulsion depends directly on:
$$
\left\langle\dfrac{1}{r_{12}}\right\rangle=\int\int\psi^*(1,2)\dfrac{1}{r_{12}}\psi(1,2)\;\textrm{d}V\,\textrm{d}\sigma
$$
which, for the **singlet** state results in
$$
\left\langle\dfrac{1}{r_{12}}\right\rangle=J+K
$$
and for the **triplet** state,
$$
\left\langle\dfrac{1}{r_{12}}\right\rangle=J-K
$$
where $J$ is the Coulomb Integral, which represents the repulsion between the electron clouds, and $K$ is the Exchange Integral, from the energy shift due to the Pauli Principle. 

This confirms that the triplet state is **more strongly bound** and has **lower energy**.

## 2.6 Electronic configurations

There are $(2l+1)$ values of $m_l$ for each $l$, and there are $2s+1=2$ values of $m_s$. Each $nl$ orbital can hold up to $2(2l+1)$ electrons.

Shells containing $2n^2$ electrons are said to be *closed* and shells containing $\lt2n^2$ electrons are said to to be *open*. Electrons in open shells are optically active.

### 2.6.1 Combined terms $L$ and $S$

The **term symbol** is
$$
^{2S+1}L_J
$$

The many-electron Hamiltonian does not commute with the individual electron orbital angular momentum operators $\hat{l}_i$, meaning that $l_i$ is no longer a good quantum number for a many-electron system.

Use total orbital angular momentum and total spin quantum numbers instead. For two non-equivalent electrons:
$$
\begin{array}{ll}
\hat{L}=\sum_i\hat{l}_i&L=|l_1-l_2|,\dots,|l_1+l_2|\\
\hat{S}=\sum_i\hat{s}_i&S=|s_1-s_2|,\dots,|s_1+s_2|
\end{array}
$$

$^1S\quad^3P\quad^1D\quad$ only are allowed as whole wavefunction must be antisymmetric.

$\hat{L}$ and $\hat{S}$ are equal to zero for closed shells.

For equivalent electrons with the same $n$ and $l$, $m_l$ or $m_s$ values must be different.

### 2.6.2 Hund's rules

1. **For a given electronic configuration the term with the highest spin multiplicity (largest $S$), is lowest in energy**

  Due to spin-spin interactions - high $S$ states have parallel aligned spins (e.g. triplet state) so electrons cannot be in same position and repulsion force is reduced so energy is lower (more tightly bound). Also spin-down is higher energy.

2. **For a particular value of $S$ in a given electronic configuration, the term with the highest total orbital angular momentum (largest $L$) is lowest in energy**

  Large $L$ classically means "orbiting in same direction" - electrons less likely to be in same position so have lower energy.

3. **Outer shell $\lt$ half-filled: lowest $J$ has lowest energy**
  
  **Outer shell $\gt$ half-filled: lowest $J$ has highest energy**

  **Outer shell is exactly half-full: no multiplet energy splitting**

  Due to $L-S$ coupling (Hund's rule 3 breaks down after $J-J$ coupling)

## 2.7 Spin-orbit interaction ($L-S$ coupling) and fine structure

Bohr model: energy is dependent on $n$ only. This is not true due to the effects of **Fine structure**.

Can be described using perturbation theory by modifying the Hamiltonian
$$
\hat{H}=\hat{H}_0+\hat{H}_{SO}\qquad\hat{H}_{SO}\propto\hat{L}\cdot\hat{S}
$$

Reason for Spin-orbit coupling: Electron "sees" nucleus rotating around it, which generated magnetic field $B$. This interacts with electron magnetic moment $\mu_s$
$$
\hat{H}_{SO}=-\hat{\mu}_S\hat{B}
$$

Using Biot-Savart law to estimate $B$
$$
I=\dfrac{e}{2\pi mr^2}\quad\Rightarrow\:B=\dfrac{\mu_0I}{Zr}=\dfrac{e}{4\pi\epsilon_0m_ec^2r^3}l
$$
$$
\mu=IA=\dfrac{-e}{2\pi mr^2}\cdot\pi r^2=\dfrac{-e}{2m_e}l\Rightarrow \mu=-\mu_Bm_l
$$
where $\mu_B=9.274\times10^{-24}\;J/T$ is the **Bohr magneton**.

**Spin magnetic moment** $\mu_s$ has an extra factor due to relativistic Dirac equation.
$$
\therefore\mu_s=-g_e\mu_Bm_s\qquad\text{where }g_e=2, m_s=\pm1/2
$$
There is an extra factor of $1/2$ called Thomas Precession (due to relativistic effects).
$$
\hat{H}_{SO}=-\dfrac{1}{2}\mu_s\cdot B=\dfrac{-Ze^2}{4\pi\epsilon_0m_e^2e^2r^3}\hat{l}\cdot\hat{s}
$$
$$
\left\langle\dfrac{1}{r^3}\right\rangle=\dfrac{Z^3}{n^3a_M^3l(l+\frac{1}{2})(l+1)}
$$
which can be used to find $H_{SO}\propto Z^4/n^3$, for given $n$ increases rapidly with $Z$, but reduces as charge distribution becomes spread out at high $n$.

### Spin-orbit coupling formula
$$
H_{SO}=hc\,A(L,S)\hat{L}\cdot\hat{S}
$$
where $A(L,S)=-\dfrac{1}{hc}\dfrac{e}{2m_e^2c^2\hbar^2r}\dfrac{\text{d}\phi}{\text{d}r}$

$M_L$ and $M_S$ are bad quantum numbers after spin-orbit coupling: use $M_J$
$$
\hat{J}=\hat{L}+\hat{S}\qquad\Rightarrow\:\hat{L}\cdot\hat{S}=\dfrac{1}{2}\left[\hat{J}^2-\hat{L}^2-\hat{S}^2\right]
$$
$$
\hat{J}^2=J(J-1)\hbar^2
$$
Which can be rearranged to
$$
\dfrac{\Delta E_{SO}}{hc}=\dfrac{A_{\text{fs}}}{2}\bigl[J(J+1)-L(L+1)-S(S+1)\bigr]
$$

$J$ taked values $J=|L-S|,\dots,|L+S|$ in steps of $1$

### Landé interval rule
$$
\Delta E_{SO}(J)-\Delta E_{SO}(J-1)=hc\,A(L,S)J
$$

![Energy level structure in the ground sate configurations of the group IV elements.](/assets/images/2023-03-15-20-02-09.png){max-width: 400px, display: block, margin: 0 auto}

## 2.8 $J-J$ coupling and hyperfine structure

Protons and neutrons are *fermions* with spin $1/2$, so the nucleus has a total nuclear spin vector $\hat{I}$.
$$
\vec{\mu}_I=g_N\mu_N\dfrac{\vec{I}}{\hbar}\qquad\text{where}\:\mu_N=\dfrac{m_e}{m_p}\mu_B=\dfrac{e\hbar}{2m_p}
$$
$\mu_N$ is known as *nuclear magneton* and $g_N$ is *nuclear spin g-factor*$*.

Hyperfine structure depends on the interaction between the nuclear magnetic moment with the total electron angular momentum and the total electron spin magnetic moment
$$
\Delta E_{HFS}\propto\vec{I}\cdot\vec{J}\quad\text{and}\quad\Delta E_{HFS}\propto\vec{I}\cdot\vec{S}
$$

Total angular momentum quantum number $F$ takes into account nuclear spin.
$$
\vec{F}=\vec{J}+\vec{I}\qquad F=|J-I|,\dots,|J+I|\:\text{in steps of 1}
$$
$$
\dfrac{\Delta E_{\text{hfs}}}{hc}=\dfrac{B}{2}\left[F(F+1)-J(J+1)-I(I+1)\right]
$$

Note that for hydrogen, $F=1$ is triplet state, $F=0$ is singlet state.

***

# 3 Atomic Spectra

## 3.1 Selection rules for electric dipole transitions

There are **selection rules** for different types of transitions. For a pure electric dipole transition in a one-electron atom:
$$
\begin{align}
&\Delta l=\pm1\quad\text{(Conservation of momentum)}\\
&\Delta s=0\\
&\Delta m_l=0,\pm1
\end{align}
$$
And the term parity $(-1)^{\sum l_i}$ must change. If there is strong spin-orbit interaction, $\Delta j=0,\pm1$ but $j=0$ cannot go to $j\neq0$

This is due to the interaction between the electric dipole $V_{\text{dip}}=-\vec\mu\cdot\vec E$ with the Hamiltonian $\hat H_{\text{tot}}=\hat H_0-\hat\mu\cdot\hat E$

Fermi's Golden rule: Transition probability is
$$
P_{if}=\left|\int\Psi_f^*V_{\text{dip}}\Psi_i\text{d}\tau\right|^2
$$

For electric dipole transitions in **multi-electron** atoms:
- Rigorous selection rule (strong)
$$
\begin{align}
&\Delta J=0,\pm1\quad\text{but not}\quad J=0\text{ to }J'=0 \\
&\Delta M_J=0,\pm1 \\
&\text{Parity must change}
\end{align}
$$

- And transitions are weak unless:
$$
\begin{align}
&\Delta S=0 \\
&\Delta L=0,\pm1\quad\text{but not}\quad L=0\text{ to }L'=0
\end{align}
$$

## 3.2 Two-level systems and rates of photon emission and absorption

![An ideal two-level system with the energy difference, ∆E21, between the two levels, 1 and 2, as indicated.](/assets/images/2023-03-22-16-25-48.png){max-width: 300px, display: block, margin: 0 auto}

1. Absorption
  $$
  \nu+|1\rangle\rightarrow|2\rangle
  $$
  $$
  \Gamma_{\text{abs}}\propto N_1U(\nu_{12})
  $$
  where $N_1$ is number of available atoms in $E_1$, and $U(\nu_{12})$ is energy density of the electromagnetic field.

2. Spontaneous emission
  $$
  |2\rangle\rightarrow|1\rangle+\nu
  $$
  $$
  \Gamma_{\text{se}}\propto N_2
  $$
  Due to vacuum fluctuations.

3. Stimulated emission
  $$
  \nu+|2\rangle\rightarrow|1\rangle+2\nu
  $$
  $$
  \Gamma_{\text{stim}}\propto N_2U(\nu_{21})
  $$
  Excited state is driven to decay by absorbing photon, and two **coherent** photons are emitted.

### 3.2.1 Two-level rate equations
$$
\dfrac{\text{d}N_1}{\text{d}t}=-C\Gamma_{\text{abs}}+A\Gamma_{\text{spon}}+B\Gamma_{\text{stim}}
$$
$$
\dfrac{\text{d}N_2}{\text{d}t}=+C\Gamma_{\text{abs}}-A\Gamma_{\text{spon}}-B\Gamma_{\text{stim}}
$$

At equilibrium, $\dfrac{\text{d}N_1}{\text{d}t}=\dfrac{\text{d}N_2}{\text{d}t}=0$
$$
\Rightarrow\quad\dfrac{N_1}{N_2}=\dfrac{A+BU(\nu_{12})}{CU(\nu_{12})}
$$
When the system is in *thermal* equilibrium, $\dfrac{N_1}{N_2}=\text{e}^{h\nu_{12}/k_BT}$ where $h\nu_{12}=E_2-E_1$

Using the Planck formula for blackbody radiation,
$$
U(\nu_{12})=\dfrac{8\pi\nu_{12}^2}{c^3}\dfrac{h\nu_{12}}{\text{e}^{h\nu_{12}/k_BT}-1}
$$
and rearranging, we find
$$
C=B
$$
$$
A=\dfrac{8\pi h\nu_{12}^3}{c^3}B
$$

$A$ is the Einstein $A$ coefficient for spontaneous emission, $B$ is the Einstein $B$ coefficient for stimulated emission.

Using Fermi's golden rule,
$$
B=\dfrac{2\pi}{3\hbar^2}\left(\dfrac{1}{4\pi\epsilon_0}\right)\left|\int\Psi_2^*\,\hat{\vec\mu}\,\Psi_1\,\text{d}\tau\right|^2
$$
where $\hat{\vec\mu}=e\hat{z}$

### 3.2.2 Excited state lifetimes

In a two-level system $\Gamma_\text{spon}=A_{12}$, and lifetime $\tau_\text{spon}=1/\Gamma_\text{spon}$

In a multi-level system, $\Gamma_i=\sum_f A_{if}$ so lifetime is $\tau_i=1/\Gamma_i$

### 3.2.3 Heisenberg time-energy uncertainty relation
$$
\Delta E\Delta t\geq\dfrac{\hbar}{2}
$$
This means that transutions with a short lifetimes will have large spectral widths, and that transitions with longer lifetimes (more uncertainty in exact decay time) will have more precisely defined energy with small spectral width.

### 3.2.4 Metastable states
If spontaneous decay of an excited state is forbidden by selection rules, the excited state is said to be *metastable*.

These states can only decay by higher-order processes (magnetic dipole transitions, electric quadrupole transitions, the emission of two photons), leading  to very long lifetimes.

## 3.3 Laser cooling
Uses light to remove energy from atoms, cooling and trapping them. This is useful for precision measurements of transition frequencies.
$$
\dfrac{1}{2}Mv^2=\dfrac{1}{2}k_BT\qquad\text{in 1D}
$$
(so momentum depends on temperature)

1. Atom $(p=Mv)$ is excited by photon $(p=h/\lambda)$ such that the new momentum is $p'=p-h/\lambda$
2. Atom emits photon **spontaneously** in a random direction
3. This reduces the atom's momentum in 1 direction

Note that for 3D cooling, 6 lasers are needed.

The incident photon must be resonant with the transition, and must take into account the Doppler effect
$$
\dfrac{\Delta\lambda}{\lambda}=\pm\dfrac{v_\text{atom}}{c}
$$
$v_\text{atom}$ changes as the atom cools, so the laser must be de-tuned in a time-varying way (*chirping*).

The final absorption causes the atom to recoil in a specific direction with a final minimum speed
$$
v_\text{min}=\dfrac{p_\lambda}{M_\text{atom}}=\dfrac{h}{\lambda M_\text{atom}}
$$

Wait ~2 lifetimes per cycle to avoid stimulated emission, as this does not have random direction (no cooling effect). Generally, circularly polarised light is use to get only $\Delta m_s=+1$ not $-1$ to avoid stimulated emission.

Alkali metals are easiest to cool as they have only 1 outer electron. But metastable systems like positronium or uranium cannot be laser cooled because they do not live long enough.

***

# 4 Atoms in magnetic and electric fields - Zeeman effect and Stark effect
## 4.1 Zeeman effect - Atoms in external magnetic fields
### 4.1.1 Weak field - Normal Zeeman effect $S=0$
Normal Zeeman effect occurs when $S=0$, e.g. group 2 atoms. Magnetic moment will be entirely due to orbital effect $l$. Assuming magnetic field is only is $z$-direction,
$$
\hat\mu_L=-\dfrac{\mu_B}{\hbar}\hat{L}
$$
$$
V_B=-\hat\mu_L\cdot\hat B=\dfrac{\mu_B}{\hbar}L_zB_z
$$
Resulting Zeeman energy shift
$$
\Delta E_B=\int\psi_0^*V_B\psi_0\text{d}\tau
$$
$$
\therefore\;\Delta E_B=\mu_BM_LB_z
$$
provided that the wavefunctions are normalised.

When $S=0$, each term $L$ is split into $2L+1$ sublevels by a weak magnetic field, where splitting depends linearly on field strength $B_z$.

![The Zeeman effect in the absence of spin, i.e., when S = 0, in (a) the n 1P term, and (b) the n 1D term in He.](/assets/images/2023-03-26-17-37-40.png){max-width: 400px, display: block, margin: 0 auto}

Due to transition rules, $\Delta l=\pm1$ and $\Delta M_L=0,\pm1$, so each spectral line is split into **three** components.

![Schematic diagrams (a) indicating the electric dipole allowed transitions between Zeeman sublevels when S = 0, and (b) the corresponding spectral intensity distributions.](/assets/images/2023-03-26-17-44-21.png){max-width: 400px, display: block, margin: 0 auto}

### 4.1.2 Weak field - Anomalous Zeeman effect $S\neq0$
When $S\neq0$, magnetic dipole associated with electron spin and orital angular momentum must be accounted for. Field is still weak, i.e. $\Delta E_B\lt\Delta E_{LS}$, so $L$ and $S$ are still coupled and only quantum number $J$ is well-defined.
$$
\vec J=\vec L+\vec S
$$
$$
\begin{align}
V_B&=-\mu_zB_z=-\left(\mu_z^{(l)}+\mu_z^{(s)}\right)B_z\\
&=\left\langle\hat L_z+g_s\hat S_z\right\rangle\dfrac{\mu_B}{\hbar}B_z\qquad(g_s=2)\\
&=\dfrac{\mu_B}{\hbar}B_z(\hat J_z+\hat S)
\end{align}
$$
Considering $J$ as the vector sum of $L$ and $S$, it can be derived that
$$
\Rightarrow\;\Delta E=-\mu_zB_z=g_j\mu_BB_zm_j
$$
where
$$
g_j=1+\dfrac{J(J+1)+S(S+1)-L(L+1)}{2J(J+1)}
$$
is known as the *Landé g-factor*.

The anomalous Zeeman effect is linear with $B_z$ as long as the field is weak.

![The weak-field Zeeman effect in the 2 2P1/2 and 2 2P3/2 levels of the H atom. In zero magnetic field the two levels are separated in energy by the spin-orbit splitting ∆ESO.](/assets/images/2023-03-26-18-00-49.png){max-width: 400px, display: block, margin: 0 auto}

Selection rules require that $\Delta J=0,\pm1$ and $\Delta M_J=0,\pm1$, giving rise to spectra of two pairs of equally spaced lines separated by a larger interval.

![Schematic diagrams (a) indicating the electric dipole allowed transitions between Zeeman sublevels when S , 0 in the Na atom, and (b) the corresponding spectral intensity distributions.](/assets/images/2023-03-26-18-01-24.png){max-width: 400px, display: block, margin: 0 auto}

### 4.1.3 Strong field - Paschen-Back effect
Strong field regime (*Paschen-Back regime*) applies when
$$
V_B\gg\hat H_{SO}
$$
$$
\Delta E_B\gg\Delta E_{SO}
$$
$\vec L$ and $\vec S$ decouple and precess **independently** about the magnetic field. $J$ is no longer a good quantum number.
$$
\therefore\;\Delta E=\mu_BB_z(M_L+2M_S)
$$
Which is a very large splitting compared to the Zeeman effect.

![Schematic diagram of the changes in atomic energy level structure when S is not 0 in weak and strong magnetic fields. The red arrows indicate the electric dipole allowed transitions in the Paschen-Back regime.](/assets/images/2023-03-26-18-08-16.png){max-width: 400px, display: block, margin: 0 auto}

The selection rules that apply here are $\Delta S=0$ and $\Delta M_L=0,\pm1$

## 4.2 Stark effect - Atoms in external electric fields
Electric dipole moment $\vec\mu_\text{elec}=-e\vec r$ has potential energy $V_F=-\vec\mu_\text{elec}\cdot\vec F$

![The electric dipole moment, µelec, associated with two charges separated by a distance r](/assets/images/2023-03-26-18-55-47.png){max-width: 400px, display: block, margin: 0 auto}

If $\vec F=F_z$,
$$
V_F=eF_zz
$$

### 4.2.1 Weak field - Quadratic Stark effect
Weak filed regime occurs when Stark shifts are small compared to energy differences between unpertubed states with different $n$.
$$
V_F\ll\dfrac{e^2}{4\pi\epsilon_0r}
$$

Energy levels with different $l$ that are **non-degenarate** in energy with states that differ from it by one $l$ exhibit small **quadratic** Stark shifts, e.g. $H$ or $\text{Li}$ in $1s$ or $2s$ state.

The atom has no intrinsic $\mu_\text{elec}$, so
$$
\vec\mu_\text{induced}=\alpha\vec F
$$
where $\alpha$ is *electric dipole polarisability*.

Using perturbation theory,
$$
\Delta E_F=-\dfrac{1}{2}\alpha F_z^2
$$

![The quadratic Stark effect in the 1 2S1/2 ground state of the H atom](/assets/images/2023-03-26-19-21-05.png){max-width: 400px, display: block, margin: 0 auto}

The quadratic stark effect generally *lowers* the enrgy of an isolated non-degenerate energy level.

### 4.2.2 Weak field - Linear Stark effect
In the weak filed regime, energy levels with different $l$ that are **degenarate** in energy at the same $n$ exhibit **linear** Stark shifts, e.g. $\text{He}^+$ or $\text{Li}^{2+}$.

There is an **intrinsic dipole moment**, and using pertubation theory, $\Delta E_F\propto F_z$.

"Pure" states are mixed according to selection rules $\Delta l=\pm1$ and $\Delta m_l=0$

![The linear Stark effect in the n = 2 states in the H atom.](/assets/images/2023-03-26-19-32-54.png){max-width: 400px, display: block, margin: 0 auto}

It either increases or decreases the enrgy depending on whether the intrinsic electric dipole is antiparallel or parallel to $F_z$ respectively.

### 4.2.3 Strong field - Electric field ionisation
In strong electric fields, $V_F$ significantly mofifies the Coulomb potential $V_C$.
$$
V_F\gg\dfrac{e^2}{4\pi\epsilon_0r}
$$
$$
V(z)=V_C(z)+V_{F_z}=-\dfrac{e^2}{4\pi\epsilon_0z}+eF_zz
$$
As a result, a "saddle point" is formed which causes the atom to become **ionised**.
$$
z_\text{saddle}=\sqrt{\dfrac{e}{4\pi\epsilon_0F_z}}
$$
$$
F_\text{ionisation}\propto\dfrac{1}{n^4}
$$

![The pure Coulomb potential, VC, experienced by the electron in the H atom (dashed black curve), with the positions of excited states with high values of n indicated. The potential that results when this potential is modified by an external electric field F = −Fz is indicated by the continuous red curve.](/assets/images/2023-03-26-19-41-46.png){max-width: 350px, display: block, margin: 0 auto}

***

# 5 Diatomic molecules
## 5.1 Introduction - Molecular Schrödinger equation
$$
\hat H\Psi(R_1,R_2,\dots,R_N;r_1,r_2,\dots,r_i)=E\Psi(R_1,R_2,\dots,R_N;r_1,r_2,\dots,r_i)
$$
where $R_N$ are the nuclear coordinates and $r_i$ are the electronic coordinates.

Constructing the Hamiltonian,
$$
\hat H=\sum_N\left[-\dfrac{\hbar^2}{2M_N}\nabla_N^2\right]+\sum_i\left[-\dfrac{\hbar^2}{2m_e}\nabla_i^2\right]+V(R_N;r_i)
$$
where $V(R_N;r_i)$ is the sum of electron-electron, electron-nucleus and nucleus-nucleus Coulomb interactions.

## 5.2 Born-Oppenheimer Approximaton
> The **Born-Oppenheimer approximation** states that due to nuclei being much heavier and slower than electrons, the electronic motion can be considered to be independent of the nuclear motion, and only dependent on the instantaneous nuclear position $R$.

1. Electronic Schrödinger equation $H_{el}(r;R)\psi_{el}(r;R)=E_{el}(R)\psi_{el}(r;R)$
2. Nuclear Schrödinger equation $[\hat H_N(R)+E_{el}(R)]\psi_N(R)=E\psi_N(R)$

Solve the Schrödinger equation for a fixed internuclear separation, and repeat for many values of $R$.

![The dependence of the electronic energy of H2 molecule on the distance between the H atoms R. Blue crosses show energies calculated at particular fixed separations between the nuclei.](/assets/images/2023-03-28-11-27-23.png){max-width: 350px, display: block, margin: 0 auto}

## 5.3 Molecular hydrogen ion ${H_2}^+
### 5.3.1 ${H_2}^+$ Wavefunctions
Molecular orbitals can be considered a linear combination of atomic orbitals (LCAO)
$$
\psi_{el}=c_11s_A+c_21s_B
$$
Due to inversion symmetry, $c_1^2=c_2^2\;\Rightarrow\;c_1=\pm c_2$, giving a symmetric (bonding) and antisymmetric (antibonding) wavefunction.
$$
\begin{align}\text{symmetric}&\equiv\text{gerade}\\\text{antisymmetric}&\equiv\text{ungerade}\end{align}
$$

Overlap integral $S=S_{AB}=S_{BA}=\left\langle 1s_A\middle|1s_B\right\rangle$

Variational method: minimise energy
$$
E_{el}=\dfrac{\left\langle\psi_{el}\middle|\hat H_{el}\middle|\psi_{el}\right\rangle}{\left\langle\psi_{el}\middle|\psi_{el}\right\rangle}
$$
$$
\dfrac{\partial E_{el}}{\partial c_1}=0\qquad\dfrac{\partial E_{el}}{\partial c_2}=0
$$
leads to a secular determinant that must be set equal to zero.

### 5.3.2 ${H_2}^+$ Energies
Solve secular determinant, here using symmetry $S_{AB}=S_{BA}$ and $H_{AB}=H_{BA}$ (where $H_{AB}=\left\langle 1s_A\middle|\hat H_{el}\middle|1s_B \right\rangle$). Since individual atomic orbitals are normalised, $S_{AA}=S_{BB}=1$. Atomic orbitals (AOs) are the same, so $H_{AA}=H_{BB}$.
$$
\Rightarrow\quad E_{el}^\pm(R)=\dfrac{H_{AA}\pm H_{AB}}{1\pm S}
$$
Using the expression for the Hamiltonian in atomic units
$$
\hat H_{el}=-\dfrac{\nabla^2}{2}-\dfrac{1}{r_A}-\dfrac{1}{r_B}+\dfrac{1}{R}
$$
$$
\therefore E_{el}^\pm(R)=E_{1s}+\dfrac{1}{R}-\dfrac{J(R)\pm K(R)}{1\pm S(R)}
$$
where $J$ is coulomb integral and $K$ is exchange integral (charge density in overlap)

To find more states, combine more AOs.

## 5.4 Hydrogen molecule $H_2$
### 5.4.1 $H_2$ electronic wavefunctions
Hartree-Fock approximation: electrons interact (with average charge density) but move independently (no correlation).

Accounting for the electrons' spins
$$
\psi^{S,T}=\psi(\vec R,\vec r_i)\chi^{S,T}=\dfrac{1}{\sqrt2}\left[\phi_{1s_A}(1)\phi_{1s_B}(2)\pm\phi_{1s_A}(2)\phi_{1s_B}(1)\right]\chi^{S,T}
$$
Where $-$ is for the triplet state (antisymmetric) and $+$ is for the singlet state (symmetric). Due to Pauli principle, total wavefunction must be antisymmetric with respect to two electrons.

Determine energies $E_{el}=\dfrac{\left\langle\psi^{S,T}\middle|\hat H_{elec}\middle|\psi^{S,T}\right\rangle}{\left\langle\psi^{S,T}\middle|\psi^{S,T}\right\rangle}$ using the Hamiltonian for $H_2$

The resulting expression includes single-electron Coulomb and exchange integrals and two-electron integrals.

![Gerade, ψS, and ungerade, ψT, electronic potential energy functions for the ground states of the neutral hydrogen molecule H2. The dashed curves represent the results obtained using the procedure described above, while the continuous curves are the results of exact calculations.](/assets/images/2023-03-28-13-09-23.png){max-width: 350px, display: block, margin: 0 auto}

How to improve?
- Add more terms to the AO basis
- Vary exponents in hydrogen-like AOs instead of just varying $c_i$
- Use more sophisticated AOs like elliptical coordinates

### 5.4.2 Molecular orbitals
![Schematic diagram of the singlet (bonding), and triplet (antibonding) orbitals of H2 at large large internuclear separation (outer energy levels) and at R = Re.](/assets/images/2023-03-28-13-11-07.png){max-width: 350px, display: block, margin: 0 auto}

Similar to $H_2^+$, $H_2$ has bonding and antibonding states.

### 5.4.3 Taking into account $e^--e^-$ correlation
Repulsion between electrons of opposite spin must also be taken into account - this decreases the total energy of the molecule.

## 5.5 Heteronuclear diatomic molecules
### 5.5.1 Chemical bond formation
Note that only valence electrons (from open shells) contribute to bonding.

Generally, MOs of heteronuclear molecules must be formed from AOs of different energies as the atoms constituting it are too different. Only orbitals of similar energy can be combined using LCAO.

In an ionic bond, the electron goes to the species with the **highest ionisation potential**.

### 5.5.2 Molecular dipole moment and electronegativity
$$
\mu=Q\times d=\delta\times d
$$
Ability to attract electrons is **electronegativity**
Usually electronegativity $\lt 0.5$ is non-polar covalent, between $0.5$ and $1.9$ is polar covalent, and $\gt 2$ is ionic.

### 5.5.3 Ionic bond and hapooning mechanism
$$
\dfrac{e^2}{R_\text{transfer}}=|\Delta H_I|-|\Delta H_{EA}|
$$
In the harpooning mechanism, the adiabatic approximation breaks because the electronic wavefunction changes greatly over a small $R$.

## 5.6 Nuclear motion
### 5.6.1 Solving for nuclear motion
A molecule with $N$ nuclei has $3N$ degrees of freedom
1. Translational motion: 3 d.o.f. in three dimensions
2. Vibrational motion: $3N-6$ vibrational modes for a non-linear molecule or $3N-5$ modes for a linear molecule
3. Rotational motion: 3 rotational degrees of freedom (or 2 distinct rotational d.o.f.s for a linear molecule)
$$
[\hat T_N(R)+U(R)]\psi_N(R)=E\psi_N(R)
$$
Using CM spherical polar coordinates $\hat T_N=-\dfrac{1}{2M_{TOT}}\nabla_{CM}^2-\dfrac{1}{2\mu}\nabla_\text{internal}^2$
Can separate into translatinal motion and internal motion, which in turn consistes of electric-vibrational and rotational components.
$$
\Psi=\psi_{el}(r,R)\psi_{vib}(R)\psi_{rot}(\theta,\phi)\psi_{trans}(R_{CM})
$$
$$
E_{TOT}=E_{el}+E_{vib}+E_{rot}+E_{trans}
$$
Generally, $E_{el}\lt E_{vib}\lt E_{trans}\lt E_{rot}$

### 5.6.2 Vibration
Harmonic approximation: $U(R)\approx U(R_e)+\dfrac{1}{2}kx^2\qquad x=R-R_e$
$$
E_{\nu}=\hbar\sqrt{\dfrac{k}{\mu}}\left(\nu+\dfrac{1}{2}\right)
$$
Fundamental vibrational angular frequency $\omega_0=\sqrt{\dfrac{k}{\mu_{AB}}}$

The reduced mass $\mu_{AB}$ results in the isotope effect: different frequency for different isotopologues.

The vibrational ground state $\nu=0$ has non-zero energy, this is known as the *zero-point energy* of the oscillator.

Dissociation energy is difference between depth of potential well and zero-point energy
$$
D_0=D_e-\dfrac{1}{2}\hbar\omega_0
$$
Selection rule $\Delta\nu=\pm1$

Strength of vibrational band depends on derivative of dipole moment with distance. So homonuclear molecules with $\mu=0$ and zero derivative of dipole moment have no electric dipole vibrational absorption spectra.

Real vibrational spectra have broadening of line shape due to sample's solvent affecting the potential energy surface.

#### Anharmonism in molecules
Real potential is not harmonic and is better approximated by the Morse potential.

![Schematic diagram of the Morse (continuous lines/curve) and harmonic oscillator (dashed lines/curve) potentials with their associated energy level structure.](/assets/images/2023-03-28-14-25-15.png){max-width: 350px, display: block, margin: 0 auto}

Second order anharmonicity correction
$$
E_{vib}=\hbar\omega_0(\nu+\dfrac{1}{2})-\hbar\omega_0x_e(\nu+\dfrac{1}{2})^2
$$
$x_e$ is anharmonicity constant (usually small, 0.01-0.02)

Effective frequency $\omega_{osc}=\omega_0\left[1-x_e(\nu+\dfrac{1}{2})\right]$

Anharmonicity relaxes the $\Delta\nu=\pm1$ rule, allowing (weakly) the existence of **overtones** ($|\Delta\nu|\neq1$). Each overtone can have **"hot bands"** at high temperature, originating from initial levels above the ground state, although these have very small intensity. $\Delta\nu=0$ is also allowed, and leads to pure rotational transitions.

- Overtones in vibrational spectra are equidistant in wavenumber with exponential intensity decrease
- At room temperature, hot bands can be neglected/are very small
- $\omega_e$ and $x_e$ are determined experimentally. Is data close to harmonic approximation?

### 5.6.3 Rotation
Rigid rotor model $R\approx R_e$ for rotation

Kinetic energy $KE=\frac{1}{2}I\omega^2$ and degeneracy of each energy state is $g_J=(2J+1)$ (Rotational wavefunction = Spherical harmonics)
$$
E_{rot}=\dfrac{\hbar^2J(J+1)}{2\mu R_e^2}
$$
Momemt of inertia in rigid rotor $I_e=\mu_{AB}R_e^2$
$$
\therefore E_{rot}=B(J(J+1))\qquad\text{where }B=\dfrac{\hbar^2}{2I_e}
$$
$E_{rot}\propto \omega_{rot}$

Selection rules: Molecules must have a permanent dipole moment, and $\Delta J=\pm1$ (pure vibrational transitions are forbidden)

Rotational spectra consists of equidistant lines at multiples of $2B$ **except** for the forbidden pure vibrational line.

Intensites governed by Boltzmann distribution
$$
N_J\sim(2J+1)\exp\left(\dfrac{-BJ(J+1)}{k_BT}\right)
$$

#### Centrifugal distortion
Introduce a second-order correction
$$
E_J^{(2)}=-D_\nu J^2(J+1)^2
$$
and adjust $B$ for higher internuclear separation due to high $\nu$, perturbation theory:
$$
B_\nu=\int_0^\infty F^*(R)\dfrac{\hbar^2}{2\mu_{AB}R^2}F(R)\text{d}R
$$
approximate: $B_\nu=B_e-\alpha_e(\nu+\dfrac{1}{2})$ where $\alpha_e$ is vibrational-rotational constant
$$
\therefore E_J=B_\nu J(J+1)-D_\nu J^2(J+1)^2
$$
where $D_\nu$ is usually very small.

## 5.7 Total energy of a diatomic molecule
Under the harmonic approximation (bottom of potential well, low temperature), and the rigid rotor approximation when $J$ is small (no centrifugal distortion), the total energy of a diatomic molecule is
$$
E_{AB}=V(R_e)+B_eJ(J+1)+\hbar\sqrt{\dfrac{k}{\mu_{AB}}}(\nu+\dfrac{1}{2})
$$
where $B_e=\dfrac{\hbar}{4\pi c\mu R_e^2}$

Applying the anharmonic oscillator and centrifugal distortion corrections to the second order, **total internal energy of a diatomic molecule** is
$$
\dfrac{E_{\nu Jm}}{hc}=D_e+\omega_0\left[1-x_e(\nu+\dfrac{1}{2})\right](\nu+\dfrac{1}{2})+B_\nu J(J+1)-D_cJ^2(J+1)^2
$$
where centrifugal distortion coefficient $D_e=\dfrac{\hbar^3}{4\pi ck\mu^2R_e^6}$ and $B_\nu=B_e-\alpha_e(\nu+\dfrac{1}{2})$


## 5.8 Molecular spectra
#### Rovibronic spectrum
![P- and R- branch of rovibronic spectrum](/assets/images/2023-03-28-15-27-49.png){max-width: 350px, display: block, margin: 0 auto}
- $\Delta J=-1$ is known as P-branch (lowest wavenumber)
- $\Delta J=+1$ is known as R-branch (highest wavenumber)
- Missing line is pure vibrational

#### De-excitation mechanisms
![](/assets/images/2023-03-28-15-33-12.png){max-width: 350px, display: block, margin: 0 auto}

## 5.9 Essential equations
- Vibrational energy $\quad E_{vib}=\hbar\omega_0\left[1-x_e(\nu+\dfrac{1}{2})\right](\nu+\dfrac{1}{2})$
- Equilibrium vibrational frequency $\quad\omega_0=\sqrt{\dfrac{k}{\mu}}\quad$ depends on mass and bond strength
- Rotational energy $\quad E_J=B_\nu J(J+1)-D_\nu J^2(J+1)^2$

$B_\nu=B_e-\alpha_e(\nu+\dfrac{1}{2})$ where $B=\dfrac{\hbar}{4\pi c\mu R_e^2}$
$$
D_e=\dfrac{4B_e^3}{v^2}
$$
