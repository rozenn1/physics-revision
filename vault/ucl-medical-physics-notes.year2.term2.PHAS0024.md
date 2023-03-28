---
id: w560luji87m7oylc1t7hipt
title: PHAS0024
desc: ''
updated: 1679997964162
created: 1676999169204
---

# Statistical Physics of Matter

***

# 1 The Four Laws of Themodynamics
## 1.1 State Variables

State variables specify the condition (**state**) of a system without reference to the path taken to get there.
-	Extensive state variables scale with the amount of material in the system ($E$, $V$, $N$) 
-	Intensive state variables remain the same ($T$, $p$, $\mu$)

($Q$ and $W$ are process variables)


## 1.2 The zeroth and first laws

Zeroth law of thermodynamics: If two systems are each in thermal contact with a third system, then they are in equilibrium with each other. Hence, an intensive state variable $T$ may be defined to describe whether two systems are in equilibrium.
$$
\textrm{if }T_A=T_C\textrm{ and }T_B=T_C\textrm{, then }T_A=T_B
$$

First law of thermodynamics: There is a system property $E$ which is conserved for an isolated system.
$$
\textrm{d}E=\textrm{d}Q+\textrm{d}W=\textrm{d}Q-p\textrm{d}V
$$
$$
\Delta E=Q+W
$$


## 1.3 Entropy of an ideal gas

$$
\begin{array}{ll}
pV=Nk_BT & E=\dfrac{1}{2}Nm\langle v^2\rangle \\[12pt]
pV=\dfrac{1}{3}Nm\langle v^2\rangle & E=\dfrac{3}{2}Nk_BT
\end{array}
$$

In **quasistatic** conditions, where temperature remains constant upon addition of heat,
$$
\textrm{d}S=\left(\dfrac{\textrm{d}Q}{T}\right)_q
$$
which for the monatomic ideal gas takes the form
$$
S(p,V,N)=Nk_B\ln\left(\dfrac{p^{3/2}}{V^{5/2}}{C(N)}\right)
$$
$$
S(p,V,N)=Nk_B\ln\left(\dfrac{(k_BT)^{3/2}}{\hat{c}N/V}\right)\quad C(N)=\hat{c}N^{5/2}
$$


## 1.4 The second law

Clausius statement: Heat cannot flow spontaneously from a colder to a warmer body.

There is a state variable entropy $S$, which for an isolated system, either grows (*irreversible transformations*) or is conserved (*reversible transformations*).
$$
\Rightarrow \textrm{d}S\geq 0
$$

Kelvin statement: no device operating on a cycle may produce work from a *single thermal reservoir*.
$$
\eta=\dfrac{W}{Q_A}\leq 1-\dfrac{T_B}{T_A}=\dfrac{T_A-T_B}{T_A}
$$


## 1.5 The third law

The entropy of a system at zero temperature is an absolute constant that does not depend on any other thermodynamic variable.
$$
\textrm{if }T\rightarrow 0\textrm{ then }S\rightarrow S_0
$$
where usually, $S_0=0$.

***

# 2. Free Energy and Entropy
## 2.1 The fundamental relation of thermodynamics

Rewrite the first law $\textrm{d}E=\textrm{d}Q+\textrm{d}W$ in terms of state variables only - we know that $\textrm{d}W=-p\textrm{d}V$ and from the relation between entropy and heat change $\textrm{d}S=(\textrm{d}Q/T)_q\:\Rightarrow\:\textrm{d}Q=T\textrm{d}S$
$$
\therefore\textrm{d}E=T\textrm{d}S-p\textrm{d}V+\mu\textrm{d}N
$$
which is the **fundamental relation of thermodynamics**.
$$
\textrm{d}E=\underbrace{\left(\dfrac{\partial E}{\partial S}\right)_{V, N}}_{=\;T}\textrm{d}S+\underbrace{\left(\dfrac{\partial E}{\partial V}\right)_{S, N}}_{=\;-p}\textrm{d}V+\underbrace{\left(\dfrac{\partial E}{\partial N}\right)_{S, V}}_{=\;\mu}\textrm{d}N
$$
We may define the *intensive* state variables temperature, pressure and chemical potential $\mu$ as partial derivatives of energy with respect to the *extensive* state variables entropy, volume and number of particles. Each pair are called *conjugate* thermodynamic variables.
$$
T=\left(\dfrac{\partial E}{\partial S}\right)_{V, N},\quad p=\left(\dfrac{\partial E}{\partial V}\right)_{S, N},\quad\mu=\left(\dfrac{\partial E}{\partial N}\right)_{S, V}
$$


## 2.2 Equilibrium via minimisation of energy

Consider a marble in a 1D potential well.
$$
E_{pot}=\dfrac{1}{2}C(x-x_0)^2
$$
The equilibrium position $x_{eq}$ **minimises** $E_{pot}$.
$$
\left.\dfrac{\textrm{d}E_{pot}(x)}{\textrm{d}x}\right|_{x=x_{eq}}=0\quad\Rightarrow\quad x_{eq}=x_0
$$

Minimise $E$ while imposing $\textrm{d}S=\textrm{d}V=\textrm{d}N=0$:
$$
\textrm{d}S_{total}=\textrm{d}S+\textrm{d}S_{env}=0-\dfrac{\textrm{d}Q}{T_{env}}\quad\Rightarrow\quad\textrm{d}S_{total}=-\dfrac{\textrm{d}Q}{T_{env}}
$$
$$
\textrm{d}E=\textrm{d}Q=-T_{env}\textrm{d}S_{total}\leq 0
$$

Therefore, minimisation of energy corresponds to maximisation of entropy for a system at constant $S$, $V$, and $N$. When such a system reaches equilibrium, there is no longer any net heat exchange with the environment ($\textrm{d}Q=0$).


## 2.3 Legendre transformations and thermodynamic potentials

To define a potential that can be a function of independent state variables $T$, $V$, $N$ instead of $S$, $V$, $N$, we consider the quantity
$$
F=E-TS=E-\left(\dfrac{\partial E}{\partial S}\right)_{V, N}S
$$
where we subtract the entropy $S$ multiplied by its conjugate $T=\left(\dfrac{\partial E}{\partial S}\right)_{V, N}$ to change variables from $S$ to $T$ dependence - a *Legendre transformation*.

This leads to 
$$
\textrm{d}F=-S\textrm{d}T-p\textrm{d}V+\mu\textrm{d}N
$$
demonstrating that $F=F(T,V,N)$. $F$ is called the Helmholtz free energy.

**Legendre transform**
$$
f(x,y,z,\dots)\rightarrow g(x',y,z,\dots)
$$
$$
g=f-\left(\dfrac{\partial f}{\partial x}\right)_{y,z,\dots}\cdot x=f=x'\cdot x
$$
where $x'$ is the conjugate of $x$.

![A table of thermodynamic potentials](/assets/images/2023-03-02-18-38-06.png){max-width: 450px, display: block, margin: 0 auto}


## 2.4 The ideal classical gas subject to gravity

Consider a room full of air molecules that are subject to gravity.
$$
E_1=\frac{3}{2}k_BT+mgh
$$
Why aren't all particles at $h=0$ to minimise their energy?

Consider the air to be a classical ideal gas at constant temperature $T$
$$
p=n_Vk_BT\quad\Rightarrow\quad\dfrac{\textrm{d}p}{\textrm{d}h}=\left(\dfrac{\textrm{d}n_V}{\textrm{d}h}\right)k_BT
$$
$$
\dfrac{\textrm{d}p}{\textrm{d}h}=\dfrac{1}{\mathcal{A}}\dfrac{\textrm{d}f}{\textrm{d}h}
$$
$$
=\dfrac{1}{\mathcal{A}}\dfrac{\textrm{d}}{\textrm{d}h}\left[-(mg)\times(n_V\mathcal{A}\textrm{d}h)\right]=-mgn_V
$$
Comparing both expressions,
$$
\dfrac{\textrm{d}n_V}{\textrm{d}h}=\left(-\dfrac{mgh}{k_BT}\right)n_V\:\Rightarrow\:n_V(h)=n_0e^{-\beta mgh}=\tilde{n}_0e^{-\beta E_1(h)}
$$
which leads to an exponential Boltzmann (canonical) distribution.

![Illustration of the effect of gravity on an ideal gas predicted by the canonical Boltzmann disribution.](/assets/images/2023-03-02-18-40-57.png){max-width: 450px, display: block, margin: 0 auto}


This leads to the identification of $F=E-Tk_B\ln\Omega$ as the Helmholtz free energy that must be minimised ($\Omega$ is the number of quantised lattice sites that a particle can occupy), which is valid if we identify $S=k_B\ln\Omega$, which is **Boltzmann's definition of entropy**.

***

# 3 Core concepts of statistical mechanics
## 3.1 Microstates, macrostates and microstate multiplicity

- Microstate $\Omega_i$ : description of a system in exactly specified "fine-grained" variables. Due to the principle of *a priori* equal probabilities, each microstate has an equal probability of occurring. (E.g. for 2 distinguishable dice, the microstate (3,5))

The whole set of dynamical variables of a system is referred to as *"phase space"*.

- Macrostate: collection of system microstates with a common property. (E.g. for 2 distinguishable dice, the macrostate that the sum is 7)


## 3.2 Boltzmann entropy and the second law

Consider two identical systems with volume $V$, number of particles $N=1$, entropy $S$, and number of microstates $\Omega$. The combined system $V_1+V_2$ contains $\Omega^2$ microstates, as for each single microstate in the first volume, there are $\Omega$ in the second.

![](/assets/images/2023-03-02-21-53-04.png){max-width: 450px, display: block, margin: 0 auto}

**Boltzmann entropy**
$$
S=k_B\ln\Omega
$$
where $k_B$ is Boltzmann's constant.


## 3.3 The microcanonical distribution

A closed, isolated system is known as a **microcanonical ensemble**, where each microstate is equally likely.
$$
P(\textrm{macrostate})=\dfrac{\Omega(\textrm{macrostate})}{\Omega_{\textrm{total}}}
$$

## 3.4 The canonical distribution

A system in contact with a large thermal reservoir at temperature $T$, containing a fixed number of particles $N$ is known as a **canonical ensemble**.

**The Boltzmann (canonical) distribution**
$$
P(i)=\dfrac{e^{-\beta E_i}}{Z}\quad\textrm{where}\quad Z=\sum_je^{-\beta E_j}
$$
and considering that multiple microstates can have the same energy,
$$
P(E)=\dfrac{\Omega(E)e^{-\beta E}}{Z}\quad\textrm{where}\quad Z=\sum_E\Omega(E)e^{-\beta E}
$$
May also be written
$$
\begin{align}
P(E)&=\dfrac{\Omega(E)e^{-\beta E}}{Z}=\dfrac{e^{-\beta(E-Tk_B\ln\Omega(E))}}{Z} \\
&=\dfrac{e^{-\beta F(E)}}{Z}
\end{align}
$$
where $F=E-TS$ is the Helmholtz free enrgy.


## 3.5 The grand canonical distribution

The **grand canonical distribution** can exchange both energy and particles with a large reservoir at temperature $T$ and chemical potential $\mu$.
$$
P(E,N)=\dfrac{\Omega(E,N)e^{-\beta(E-\mu N)}}{Z_G}
$$
$$
Z_G=\sum_{E,N}\Omega(E,N)e^{-\beta(E-\mu N)}
$$
which can equivalently be written in terms of the Grand potential $\Phi$
$$
\begin{align}
P(E,N)&=\dfrac{\Omega(E,N)e^{-\beta(E-\mu N)}}{Z_G}=\dfrac{e^{-\beta(E-Tk_B\ln\Omega(E,N)-\mu N)}}{Z_G} \\
&=\dfrac{e^{-\beta\Phi(E,N)}}{Z_G}
\end{align}
$$

![Summary of characteristics of statistical ensembles.](/assets/images/2023-03-02-22-25-20.png){max-width: 550px, display: block, margin: 0 auto}

***

# 4 Statistical mechanics in action
## 4.1 Microcanonical ensemble and microstate enumeration

[Stars and bars (combinatorics) - Wikipedia](https://en.wikipedia.org/wiki/Stars_and_bars_(combinatorics))

Consider $Q$ identical items distributed over $N$ boxes as $Q$ stars ($*$) and $N-1$ bars ($\,|\,$) that can be arranged into $\Omega(Q,N)$ distinguishable configurations.
$$
**|***|**
$$
$$
\Omega(Q,N)=\dfrac{(Q+N-1)!}{Q!(N-1)!}
$$

The possible numbers of items in each box can be represented as an $(N-1)$-dimension *phase space* (since total number of particles $Q$ is known).

![](/assets/images/2023-03-03-19-09-29.png){max-width: 250px, display: block, margin: 0 auto}

### Mean and standard deviation

For a state variable $A$, relevant statistical properties are
$$
\langle A\rangle=\sum_iA_iP_i
$$
$$
\sigma^2=\langle A^2\rangle-\langle A\rangle^2
$$

### The Stirling approximation

To deal with factorials of large numbers, use the Stirling approximation
$$
\ln m!\approx m\ln m-m\quad\textrm{for }\:m\gg1
$$

## 4.2 Quantum harmonic oscillator

Consider a single quantum oscillator that is part of a large system of $N_{\textrm{tot}}$ quantum oscillators containing $Q_{\textrm{tot}}$ quanta of energy. Each state has its own distinguishable (non-degenerate) energy $E_q$, and the system is described by the **canonical distribution**.
$$
\begin{align}
\langle E\rangle&=\sum_{q=0}^{Q_{\textrm{tot}}}E_q\,P(E_q)=\dfrac{1}{Z}\sum_{q=0}^{Q_{\textrm{tot}}}E_q\,e^{-\beta E_q} \\
&=-\dfrac{1}{Z}\sum_{q=0}^{Q_{\textrm{tot}}}\dfrac{\partial e^{-\beta E_q}}{\partial\beta}=-\dfrac{1}{Z}\dfrac{\partial Z}{\partial\beta}
\end{align}
$$
$$
\therefore\langle E\rangle=-\dfrac{1}{Z}\dfrac{\partial Z}{\partial\beta}=-\dfrac{\partial\ln Z}{\partial\beta}
$$
So $\langle E\rangle$ can be determined by only knowing the partition function.

For a quantum harmonic oscillator, $E_q=\left(\dfrac{1}{2}+q\right)\hbar\omega$
$$
Z=e^{-\beta\frac{1}{2}\hbar\omega}\cdot\sum_{q=0}^{\infty}e^{-\beta q\hbar\omega}=\dfrac{e^{-\frac{1}{2}\beta\hbar\omega}}{1-e^{-\beta\hbar\omega}}
$$
$$
Z=\dfrac{1}{2\sinh\left(\frac{1}{2}\beta\hbar\omega\right)}
$$
$$
\langle E\rangle=-\dfrac{1}{Z}\dfrac{\partial Z}{\partial\beta}=\dfrac{\frac{1}{2}\hbar\omega}{\tanh\left(\frac{1}{2}\beta\hbar\omega\right)}
$$
$$
\langle E\rangle=\begin{cases}
\frac{1}{2}\hbar\omega & \text{for }\:\beta\hbar\omega\gg1 & (\text{low }T) \\
k_BT & \text{for }\:\beta\hbar\omega\ll1 & (\text{high }T)
\end{cases}
$$
So classical behaviour is recovered at high temperatures.

![](/assets/images/2023-03-03-21-48-39.png){max-width: 350px, display: block, margin: 0 auto}

## 4.3 Classical ideal gas: the Maxwell velocity distribution

$$
P(v)\text{d}v\propto\textrm{e}^{-\beta\frac{1}{2}mv^2}\text{d}v_x\text{d}v_y\text{d}v_z
$$
Applying the canonical distribution, we find
$$
P(v)\text{d}v\propto v^2\textrm{e}^{-\beta\frac{1}{2}mv^2}
$$

## 4.4 The equipartition theorem

If energy is described in terms of $n$ independent phase space variables $x_j$, then each term $\alpha_jx_j^2$ in the energy (*degrees of freedom*) contributes a total of $\frac{1}{2}k_BT$ to the total average canonical energy at temperature $T$.
$$
Z=\prod_{j=1}^n\int_{-\infty}^{\infty}\textrm{e}^{-\beta\alpha_j x_j^2}\:\textrm{d}x_j
$$
$$
\langle E\rangle=-\dfrac{\partial\ln Z}{\partial\beta}=\dfrac{n}{2}k_BT
$$

## 4.5 Heat capacities
$$
C_V=\left(\dfrac{\partial E}{\partial T}\right)_V=\dfrac{3}{2}Nk_B
$$
$$
C_p=\dfrac{5}{2}Nk_B
$$

## 4.6 Two-level systems in thermal equilibrium

Only two possible states $\pm\Delta$ in thermal equilibrium, apply canonical distribution.

*e.g.* Split energy levels due to a magnetic field $E_{m_s}=-m_s\mu_BB=-m_s\Delta$
$$
\langle m_s\rangle=\tanh\beta\Delta
$$
![](/assets/images/2023-03-12-12-49-29.png){max-width: 350px, display: block, margin: 0 auto}

## 4.7 Grand canonical ensemble: Vacancies in crystals

Number of vacancies in a lattice site $N=1$ or $N=0$. If having a vacancy has an energy cost of $E_v$, then
$$
Z_G=1+\textrm{e}^{-\beta(E_v-\mu)}\quad\Rightarrow\quad
\langle N\rangle=\dfrac{1}{\textrm{e}^{\beta(E_v-\mu)}+1}
$$
Useful relations:
$$
\begin{array}{l}
\langle E\rangle=-\dfrac{\partial\ln Z}{\partial\beta} \\
\langle E\rangle-\mu\langle N\rangle=-\dfrac{\partial\ln Z_G}{\partial\beta} \\
\langle N\rangle=\dfrac{1}{\beta}\dfrac{\partial\ln Z_G}{\partial\mu}
\end{array}
$$

***

# 5 Probability and entropy
## 5.1 The thermodynamic limit

Statistical physics describes systems in terms of average properties.
$$
P(E)=\dfrac{\Omega(E,N)e^{-\beta E}}{Z}
$$
Defining $E^*$ as the energy with the highest probability, a Gaussian distributions with standard deviation $\sigma$,
$$
\dfrac{\sigma}{E^*}\propto\sqrt{\dfrac{1}{N}}
$$
Which justifies the 'mean variables' approach for high number of particles $N$.

## 5.2 Gibbs entropy

$$
S_G=-k_B\sum_jP_j\ln P_j
$$
where $P_j$ is the probability of a certain microstate $j$ occurring.

### Canonical distribution
$$
-k_BT\ln Z=\langle E\rangle-TS_G=F
$$

### Grand canonical distribution
$$
-k_BT\ln Z_G=\langle E\rangle-TS_G-\mu\langle N\rangle=\Phi
$$

## 5.3 Shannon entropy: Quantifying information

Let $N$ be the length of a message written using symbols $j$. The number of possible different messages is
$$
\dfrac{N!}{\prod_j(P_jN)!}
$$
if the message is also written in bits, this is equal to $2^{NS_I}$, where $S_I$ is the number of bits per symbol.

This leads to the **Shannon entropy** $S_I$, which represents the minimum number of bits per symbol needed to convey a message without loss of information
$$
S_I=-\sum_jP_j\log_2P_j=-K\sum_jP_j\ln P_j
$$
with $K=(\ln2)^{-1}$ for base-2 encoding.

Both the Gibbs and Shannon entropy lead to an interpretation of entropy as a measure of *uncertainty* in a system.

The microcanonical, canonical, and grand canonical distributions can be derived from the maximisation of the probabilistic form of entropy. 

*E.g.* For the microcanonical distribution:
$$
\dfrac{\partial}{\partial P_j}\biggl(\underbrace{-\sum_jP_j\ln P_j}_{S_I}-\lambda\underbrace{\biggl(\sum_iP_i-1\biggr)}_{\textrm{constraint}}\biggr)=0
$$
where $\lambda$ a Lagrange multiplier.

***

# 6 Quantum gases
## 6.1 Energetics of a quantum gas

A quantum gas can be considered as quantum particles in a box.
$$
-\dfrac{\hbar^2}{2m}\dfrac{\textrm{d}^2\psi_{n_x}(x)}{\textrm{d}x^2}=\epsilon_{n_x}\psi_{n_x}(x)
$$
$$
\Rightarrow\:\psi_{n_x}(x)\propto\sin(k_xx)\quad n_x=1,2,3,\dots
$$
$$
k_x=\dfrac{2\pi}{\lambda_x}=\dfrac{\pi n_x}{L}\quad\Rightarrow\quad\epsilon_{n_x}=\dfrac{\hbar^2k_x^2}{2m}=\dfrac{h^2n_x^2}{8mL^2}
$$
In 3D:
$$
\epsilon_{n_xn_yn_z}=\dfrac{\hbar^2}{2m}(k_x^2+k_y^2+k_z^2)=\dfrac{h^2}{8mL^2}(n_x^2+n_y^2+n_z^2)
$$
> Quantum states can be considered as point spanning a 3D "k-space" with separation $\Delta k=\pi/L$

![](/assets/images/2023-03-12-13-50-57.png){max-width: 200px, display: block, float: right, margin: 10px}
$$
\textbf{k}=(k_x,k_y,k_z)
$$
Every state (point) has **Spin degeneracy**
$$
(2S+1)
$$
The density of states $\rho(k)\textrm{d}k$ in 3D is
$$
\rho(k)\textrm{d}k=(2S+1)\dfrac{Vk^2}{2\pi^2}\textrm{d}k
$$
- $\rho(k)\textrm{d}k$ is the number of states between $k$ and $k+\textrm{d}k$
- $g(\epsilon)\textrm{d}\epsilon$ is the number of states between $\epsilon$ and $\epsilon+\textrm{d}\epsilon$
$$
\rho(k)\textrm{d}k=g(\epsilon)\textrm{d}\epsilon
$$

## 6.2 One-particle partition function $Z_1$
$$
g(\epsilon)=\rho(k)\dfrac{\textrm{d}k}{\textrm{d}\epsilon}
$$
$$
g(\epsilon)=\dfrac{(2S+1)V}{(2\pi)^2}\left(\dfrac{2m}{\hbar^2}\right)^{3/2}\sqrt{\epsilon}
$$
$Z_1$ is the partition function for a single quantum particle in a box.
$$
Z_1=\int_0^\infty\rho(k)\textrm{e}^{-\beta\epsilon_k}\textrm{d}k=\int_0^\infty g(\epsilon)\textrm{e}^{-\beta\epsilon}\textrm{d}\epsilon
$$
$$
\therefore Z_1=(2S+1)\,\dfrac{V}{\lambda_{th}^3}
$$
$$
\:\lambda_{th}=\dfrac{h}{\sqrt{2\pi mk_BT}}
$$
where $\lambda_{th}$ is the **thermal de Broglie wavelength**. It describes the "length scale" limiting the concentration of particles in a box.

## 6.3 Grand canonical partition function of a single quantum level $Z_G^{(\epsilon)}$
Single quantum level of energy $\epsilon$ with temperature $T$ and chemical potential $\mu$.

In quantum physics, particles are **indistinguishable** when exchanged
$$
\psi(r_1,r_2,\dots)=\textrm{e}^{i\phi}\psi(r_2,r_1,\dots)
$$
$$
\textrm{e}^{2i\phi}=1\quad\Rightarrow\quad\textrm{e}^{i\phi}=\begin{cases}+1&\textrm{symmetric}\\-1&\textrm{antisymmetric}\end{cases}
$$
- **Bosons** are symmetric with respect to the exchange of two particles $(\textrm{e}^{i\phi}=1)$, therefore multiple particles are allowed to be in the same state. Bosons have integer spin.
- **Fermions** are antisymmetric with respect to the exchange of two particles $(\textrm{e}^{i\phi}=-1)$, so only one particle is allowed per state (Pauli exchange principle). Fermions have half-integer spin.
$$
Z_G^{(\epsilon)}=\sum_{N=0}^{N=N_{\text{max}}}\text{e}^{-\beta(\epsilon-\mu)N}\qquad N_{\text{max}}=\begin{cases}1&\text{for fermions}\\\infty&\text{for bosons}\end{cases}
$$
$$
\langle N\rangle^{(\epsilon)}_{\text{bosons}}=\dfrac{1}{\beta}\dfrac{\partial\ln Z_G^{(\epsilon)}}{\partial\mu}=\dfrac{1}{\text{e}^{\beta(\epsilon-\mu)}-1}\quad\text{Bose-Einstein statistics}
$$
$$
\langle N\rangle^{(\epsilon)}_{\text{fermions}}=\dfrac{1}{\beta}\dfrac{\partial\ln Z_G^{(\epsilon)}}{\partial\mu}=\dfrac{1}{\text{e}^{\beta(\epsilon-\mu)}+1}\quad\text{Fermi-Dirac statistics}
$$
![](/assets/images/2023-03-12-16-32-30.png){max-width: 300px, display: block, margin: 0 auto}

## 6.4 Grand canonical partition function for all quantum states $Z_G$

Can be written as product of partition functions of each energy state, assuming that each quantum state is independent.
$$
Z_G=\prod_\epsilon\bigl(Z_G^{(\epsilon)}\bigr)^{\Omega(\epsilon)}
$$
$$
\begin{align}
\ln Z_G&=\sum_\epsilon\Omega(\epsilon)\ln Z_G^{(\epsilon)}=\sum_\epsilon\dfrac{\Omega(\epsilon)}{\Delta\epsilon}\ln Z_G^{(\epsilon)}\Delta\epsilon \\
&\approx\int_0^\infty g(\epsilon)\ln Z_G^{(\epsilon)}\text{d}\epsilon
\end{align}
$$
$$
\ln Z_G=\dfrac{(2S+1)V}{(2\pi)^2}\left(\dfrac{2m}{\hbar^2}\right)^{3/2}\int_0^\infty\sqrt\epsilon\ln\left(1\mp\text{e}^{-\beta(\epsilon-\mu)}\right)\text{d}\epsilon
$$
for bosons $(-)$ and for fermions $(+)$.

## 6.5 Canonical partition function for a quantum gas of $N$ particles $Z_N$
$$
\begin{align}
Z_G&=\sum_{E,N}\Omega(E,N)\text{e}^{-\beta(E-\mu n)} \\
&=\sum_N\text{e}^{\beta\mu N}\sum_E\Omega(E,N)\text{e}^{-\beta E}=\sum_N\text{e}^{-\beta E}Z_N
\end{align}
$$

## 6.6 The entropy and pressure of a quantum gas

Entropy of a quantum gas can be derived from the expression for Gibbs entropy.
$$
S_G=\dfrac{\langle E\rangle}{T}-\dfrac{\mu\langle N\rangle}{T}+k_B\ln Z_G
$$
$$
\langle E\rangle-\mu\langle N\rangle=-\dfrac{\partial\ln Z_G}{\partial\beta}=\int_0^\infty g(\epsilon)(\epsilon-\mu)\langle N\rangle^{(\epsilon)}\text{d}\epsilon
$$
using $\langle E\rangle^{(\epsilon)}=\epsilon\langle N\rangle^{(\epsilon)}$.
$$
\langle N\rangle=\dfrac{1}{\beta}\dfrac{\partial\ln Z_G}{\partial\mu}=\int_0^\infty g(\epsilon)\langle N\rangle^{(\epsilon)}
$$
So entropy can be calculated by substituting the correct expressions for $g(\epsilon)$ and mean number of particles per energy level $\langle N\rangle^{(\epsilon)}$.

**Pressure** can also be calculated
$$
p=-\left(\dfrac{\partial\Phi}{\partial V}\right)_{T,\mu}=\dfrac{1}{\beta}\left(\dfrac{\partial\ln Z_G}{\partial V}\right)_{T,\mu}=\dots=\dfrac{2}{3}\dfrac{\langle E\rangle}{V}
$$
which agrees with thermodynamics of an ideal classical gas, although quantum effects become apparent at $\;T\rightarrow0$.

## 6.7 The classical limit of a quantum gas and Sackur-Tetrode entropy

In the classical limit, $T$ is high, occupancy of each energy state is very small such that quantum effects (such as Pauli exclusion principle) are negligible, and $\langle N\rangle^{(\epsilon)}$ is the same for bosons and fermions.
$$
\ln Z_G^{(\epsilon)}\simeq\ln(1+\text{e}^{-\beta(\epsilon-\mu)})\approx\text{e}^{-\beta(\epsilon-\mu)}
$$
$$
\ln Z_G=\int_0^\infty g(\epsilon)\text{e}^{-\beta(\epsilon-\mu)}\text{d}\epsilon=Z_1\text{e}^{\beta\mu}
$$
$$
Z_G=\exp(\text{e}^{\beta\mu}Z_1)=\sum_{n=0}^\infty\text{e}^{\beta\mu N}\dfrac{Z_1^N}{N!}
$$
$$
\Rightarrow\quad Z_N=\dfrac{Z_1^N}{N!}=\dfrac{1}{N!}\left(\dfrac{V(2S+1)}{\lambda_{th}^3}\right)^N
$$
($N!$ factor is due to the $N$ indistinguishable particles)
$$
\langle E\rangle=-\dfrac{\partial\ln Z_N}{\partial\beta}=\dfrac{3}{2}Nk_BT\qquad\text{where }\:\lambda_{th}=\sqrt{\dfrac{\beta h^2}{2\pi m}}
$$
Use $\;S=\frac{\langle E\rangle-\langle F\rangle}{T}=\frac{3}{2}Nk_B+k_B\ln Z_N$ and Stirling approximation

Recall from classical thermodynamics $S(T,V,N)=Nk_B\ln\left(\dfrac{(k_BT)^{3/2}}{\tilde{c}\,(N/V)}\right)$

**Sackur-Tertrode entropy** 
$$
S=Nk_B\ln\left(\dfrac{(2S+1)\text{e}^{5/2}V}{\lambda_{th}^3N}\right)
$$
$$
S=Nk_B\ln\left(\dfrac{(2S+1)\text{e}^{5/2}(2\pi mk_BT)^{3/2}}{(N/V)h^3}\right)
$$
$\lambda_{th}$ is the limit of "fine-graining" in entropy.

Condition fopr quantum behaviour: for particle density to become comparable or larger to quantum density
$$
n\gtrsim n_q=\lambda_{th}^{-3}
$$
$$
\lambda_{th}=\sqrt{\dfrac{\beta h^2}{2\pi m}}
$$

***

# 7 Quantum behaviour of Boson gases
## 7.1 Light as a boson gas - Ultraviolet catastrophe

Consider light as bosonic particles in a box (photons), with
$$
\omega=\dfrac{2\pi c}{\lambda}=kc
$$
![The two orthogonal polarisations of light can be considered as an additional degree of freedom for photons instead of spin degeneracy](/assets/images/2023-03-16-13-25-55.png){max-width: 250px, float: right, margin: 10px}
$$
\rho(k)=2\times\dfrac{Vk^2}{2\pi^2}
$$
due to the the two polarisations of light.

$$
g(\omega)=\rho(k)\dfrac{\text{d}k}{\text{d}\omega}=\dfrac{1}{c}\rho(k)=\dfrac{V}{\pi^2c^3}\omega^2
$$

Calculating energy density
$$
\left.\dfrac{\langle E\rangle}{V}\right|_{\text{classical}}\propto\sum_{n=1}^{\infty}k_BT\approx k_BT\int_0^\infty g(\omega)\text{d}\omega\propto\int_0^\infty\omega^2\text{d}\omega\rightarrow\infty
$$
Energy density diverges at high frequency $\Longrightarrow$ **The Ultraviolet catastrophe**

Solution proposed by Planck: light is discretised (**quantised**) with $E_j=\hbar\omega j$
$$
\begin{align}
\ln Z&=\int_0^\infty g(\omega)\ln(Z^{(\omega)})\text{d}\omega \\
&=\int_0^\infty g(\omega)\ln(\sum_{j=0}^\infty\text{e}^{-\beta\hbar\omega j})\text{d}\omega
\end{align}
$$
Using $\sum_{j=0}^\infty x^j=\dfrac{1}{1-x}\quad\text{for }|x|\lt 1$
$$
\ln Z=-\int_0^\infty\underbrace{g(\omega)}_{\frac{V}{\pi^2c^3}\omega^2}\ln(1-\text{e}^{-\beta\hbar\omega})\text{d}\omega
$$
$$
\dfrac{\langle E\rangle}{V}=-\dfrac{1}{V}\dfrac{\partial\ln Z}{\partial\beta}=\int_0^\infty\underbrace{\dfrac{\hbar}{\pi^2c^3}\dfrac{\omega^3}{\text{e}^{\beta\hbar\omega}-1}}_{\equiv u(\omega)}\text{d}\omega
$$
where $u(\omega)$ is the Planck energy spectrum.

![The black-body spectrum in SI units at three different temperatures. The position of the maximum scales linearly with T (Wien’s law), and the area under the curves scales with T to the power 4 (Stefan-Boltzmann law).](/assets/images/2023-03-20-15-21-38.png){max-width: 350px, display: block, margin: 0 auto}

The expression for energy confirms that photons can be considered a boson gas. 

### Wien's law
Solve for frequency which has maximum intensity $\left.\dfrac{\text{d}u}{\text{d}\omega}\right|_{\omega=\omega_\text{max}}$
$$
\omega_\text{max}\approx2.821\dfrac{k_BT}{\hbar}
$$

## 7.2 Stefan-Boltzmann law and the greenhouse effect

### 7.2.1 Stefan-Boltzmann law
$$
\dfrac{\langle E\rangle}{V}=\dfrac{4}{c}\sigma T^4
$$
where we have definied the Stefan-Boltzmann constant as
$$
\sigma=\dfrac{\pi^2k_B^4}{60c^2\hbar^3}=5.67\times10^{-8}\:\text{Wm}^{-2}\text{K}^{-4}
$$

A black body radiator can be considered a volume containing black body radiation emitting through a hole.

![Profile view of the element of area dA and of the particle velocity v, where |v| is the speed of light c. The spherical polar coordinate θ defines the angle between the normal to dA and the velocity v. The normal to the surface, represented as a dashed line in the drawing, defines the z-axis](/assets/images/2023-03-20-15-35-36.png){max-width: 300px, display: block, margin: 0 auto}

Number of particles incident per unit time on $\text{d}A$:
$$
\dfrac{c}{4\pi}n(\omega)\text{d}\omega\int_{-\pi}^\pi\text{d}\phi\int_0^{\pi/2}\sin\theta\cos\theta\,\text{d}\theta=\dfrac{c}{4}n(\omega)\,\text{d}\omega
$$
Multiply by energy per photon and integrate
$$
\Phi=\dfrac{c}{4}\int_0^\infty\hbar\omega n(\omega)\,\text{d}\omega=\dfrac{c}{4}\dfrac{\langle E\rangle}{V}=\dfrac{c}{4}\dfrac{4}{c}\sigma T^4
$$

#### Stefan-Boltzmann law
$$
\Phi=\sigma T^4
$$
Where $\Phi$ is flux (energy incident per unit area)

### 7.2.2 The greenhouse effect
![Simplified depiction of energy exchanges between the Sun, the Earth’s surface and the atmosphere.](/assets/images/2023-03-20-18-11-17.png){max-width: 350px, display: block, margin: 0 auto}

Incident radiation from the Sun on the Earth
$$
\sigma T_\odot^4\dfrac{4\pi R_\odot^2}{4\pi d^2}\approx1.37\times103\text{Wm}^{−2}
$$
which is divided by 4 after averaging over the whole surface area of the Earth $(4\pi R_{\text{Earth}}^2/\pi R_{\text{Earth}}^2)$

1. Atmosphere and Earth reflect radiation, and $(1-a_T)\approx70%$ solar radiation goes to Earth's surface
2. The atmosphere absorbs all of the emitted radiation from the Earth $(\sigma T_S^4)$
3. Atmosphere emits radiation both to Earth and to space $(2\sigma T_A^4)$
4. Can find estimate of Earth's surface temperature

## 7.3 Phonons and the heat capacity of solids

Oscillations of atoms in a solid lattice can be considered bosons: **phonons**.

First consider atoms in a solid as 1D chains of N coupled atoms connected by hookean springs.
$$
\text{For }\:1\leq j\leq N\::\:m\ddot\psi_j=-C_L\left(\psi_j-\psi_{j-1}\right)-C_L\left(\psi_j-\psi_{j+1}\right)
$$
$$
\psi_j(t)=\xi\text{e}^{\text{i}(\kappa j-\omega t)}
$$
Yields dispersion relation
$$
-m\omega^2=-4C_L\sin^2\left(\dfrac{\kappa}{2}\right)
$$

Set periodic boundary condition:
$$
x_{j+N}=x_j\quad\forall j\quad\Rightarrow\text{e}^{\text{i}\kappa N}=1,\qquad\kappa=z\dfrac{2\pi}{N}\quad z\in\mathbb{Z}
$$
This leads to $N$ independent solutions, which can be extended to $3N$ oscillatory modes (two transverse and one longitudinal) in 3D. We can ignore the discretisation of $N$ when $x\gg a$
$$
\psi(x,t)=\xi\text{e}^{\text{i}(kx-\omega t)}
$$
where $kx=kaj=\kappa j$. This shows that $\psi$ represents propagating waves.

Dispersion relation is $\omega=kv$ (same as for light) for the large wavelength approximation.

$$
g(\omega)=\dfrac{V\omega^2}{2\pi^2}\left(\dfrac{2}{v_T^3}+\dfrac{1}{v_L^3}\right)=\dfrac{3V\omega^2}{2\pi^2v_s^3}
$$
where average speed of sound $v_s$ is defined by $3v_S^{-3}=2v_T^{-3}+v_L^{-3}$, taking into account longitudinal and transverse components.

Compared with light, an important difference is that the total number of modes (phonons) is capped to $3N\quad\Rightarrow\quad$ Introduce (artificial) **Debye cut-off frequency**
$$
3N=\int_0^{\omega_D}g(\omega)\,\text{d}\omega=\dfrac{V\omega_D^3}{2\pi^2v_s^3}
$$
$$
\therefore\omega_D=v_s\left(6\pi^2n\right)^{1/3}
$$
where $n=N/V$ is particle density.

Keeping the zero-point energy $E_j=(\frac{1}{2}+j)\hbar\omega$
$$
\begin{align}
\ln Z&=\int_0^{\omega_D}g(\omega)\ln Z^{(\omega)}\,\text{d}\omega \\
&=\int_0^{\omega_D}g(\omega)\ln\left(\text{e}^{-\frac{1}{2}\beta\hbar\omega}\sum_{j=0}^\infty\text{e}^{-\beta\hbar\omega j}\right)\text{d}\omega
\end{align}
$$
Then calculate heat capacity $C_V$
$$
C_V=\dfrac{\partial\langle E\rangle}{\partial T}\quad\text{with}\quad\langle E\rangle=-\dfrac{\partial\ln Z}{\partial\beta}
$$

Heat capacity of solids at low temperature limit:
$$
\Rightarrow\:C_V\approx\dfrac{12\pi^4}{5}Nk_B\left(\dfrac{T}{T_D}\right)^3
$$
where $T_D=\hbar\omega_D/k_B$ is the Debye temperature.

## 7.4 Bose-Einstein condensation

If $(\epsilon-\mu)\rightarrow0^+$, the occupancy of the ground state tends to $0$. This behaviour is called **Bose-Einstein condensation**.

When temperatur goes to zero, any physical system will have a highly populated ground state.
$$
n=\dfrac{\langle N\rangle}{V}=\dfrac{(2s+1)}{(2\pi)^2}\left(\dfrac{2m}{\beta\hbar^2}\right)^{3/2}\int_0^\infty\dfrac{\sqrt{\beta\epsilon}}{\text{e}^{\beta(\epsilon-\mu)}-1}\text{d}(\beta\epsilon)=\dfrac{2(2s+1)}{\sqrt{\pi}}n_q\int_0^\infty\dfrac{\sqrt{x}}{\text{e}^{-\beta\mu}\text{e}^x-1}
$$
where quantum density $n_q=\lambda_{th}^{-3}$ and $x=\beta\epsilon$

We find that particle density obeys
$$
n\leq n_{\text{max}}\approx(2s+1)n_q2.612\neq\infty
$$
Reason for discrepancy: the integral approximation of a sum over *discrete states*, which does not hold when $T\rightarrow0^+$

Define a new particle density
$$
n=\begin{cases}
\langle N\rangle/V&\text{for }n\leq n_{\text{max}} \\
n_0+n_{\max}&\text{for }n\gt n_{\text{max}}
\end{cases}
$$
This results in the proportio of particles in the ground state
$$
\dfrac{\langle N\rangle_0}{\langle N\rangle}=1-\dfrac{n_\text{max}}{n}=1-\left(\dfrac{T}{T_c}\right)^{3/2}
$$
where $T_c$ is *critical temperature*

#### Bose-Einstein condensation
When a finite fraction of particles is in the ground state, leading to effects such as superfluidity (zero viscosity) and superconductivity due to macroscopic numbers of particles being in the same quantum state.

![The proportion of particles occupying the ground state versus the temperature (in units of the critical temperature Tc)](/assets/images/2023-03-21-17-19-01.png){max-width: 350px, display: block, margin: 0 auto}


***

# 8 Quantum behaviour of Fermi gases
## 8.1 The Fermi energy
$$
f(\epsilon)=\langle N\rangle^{(\epsilon)}=\dfrac{1}{\text{e}^{\beta(\epsilon-\mu)}+1}=\begin{cases}1&\text{for}\;\epsilon\lt\mu\\0&\text{for}\;\epsilon\gt\mu\end{cases}\quad\beta\rightarrow\infty
$$
As $T\rightarrow0$, $f(\epsilon)$ can be approximated as a step function $\Rightarrow$ **degenerate Fermi gas approximation**.

![Fermi-Dirac function for different values of beta](/assets/images/2023-03-26-13-00-59.png){max-width: 350px, display: block, margin: 0 auto}

The **Fermi Energy** $\epsilon_F$ is defined as the chemical potential $\mu$ when $\beta\rightarrow\infty$
$$
\langle N\rangle=\lim_{\beta\rightarrow\infty}\int_0^\infty g(\epsilon)f(\epsilon)\,\text{d}\epsilon=\int_0^{\epsilon_F}g(\epsilon)\,\text{d}\epsilon
$$
Subsitituting the density of states for a particle in a box, we find
$$
\epsilon_F\propto n^{2/3}
$$

Average energy of a degenerate Fermi gas
$$
\langle E\rangle=\lim_{\beta\rightarrow\infty}\int_0^\infty\epsilon\,g(\epsilon)f(\epsilon)\,\text{d}\epsilon=\int_0^{\epsilon_F}\epsilon\,g(\epsilon)\,\text{d}\epsilon
$$
$$
\Rightarrow\;\langle E\rangle\propto\epsilon_F^{5/2}
$$

#### Pressure of a Fermi gas
$$
p=\dfrac{2}{3}\dfrac{\langle E\rangle}{V}=\dfrac{2}{3}\dfrac{3}{5}n\epsilon_F=\dfrac{\hbar^2}{5m}\left(3\pi^2\right)^{2/3}n^{5/3}
$$
So pressure of a Fermi gas is **non-zero** in the limit $T\rightarrow\infty$, which is a consequence of quantum behaviour (of Fermi-Dirac statistics).

## 8.2 Stars as Fermi gases
### 8.2.1 Collapse to white dwarf
Consider a simplified model of a star, consisting of protons, neutrons, and electrons (spin $1/2$) forming a Fermi gas.

![Assuming that only the inward gravitational force and the outward pressure are at work in the gas, a star is in hydrostatic equilibrium](/assets/images/2023-03-27-21-51-28.png){width: 200px, float: right, margin: 20px}

Assuming a "core" and a "shell" $\text{d}r$ exerting gravitational force on each other
$$
\text{d}F(r)=-\dfrac{GM_1M_2}{r^2}=-G\dfrac{(4\pi)^2}{3}\rho^2r^3\text{d}r
$$
As a pressure 
$$
\text{d}p(r)\equiv-\dfrac{\text{d}F(r)}{4\pi r^2}
$$
$$
p_G=\int_0^R\text{d}p(r)=\int_0^RG\dfrac{4\pi}{3}\rho^2r\text{d}r=G\dfrac{2\pi}{3}\rho^2R^2
$$
where density $\rho=\dfrac{M}{\frac{4}{3}\pi R^3}$
$$
\therefore\quad p_G=\dfrac{3}{8\pi}\dfrac{GM^2}{R^4}
$$
This gravitational pressure $p_G$ is what drives stars to collapse.

It is opposed by the Fermi pressure
$$
p_F=\dfrac{\hbar^2}{5m_e}(3\pi^2)^{2/3}n^{5/3}=\dfrac{\hbar^2}{5m_e}(3\pi^2)^{2/3}{\dfrac{M/m_n}{\frac{4}{3}\pi R^3}}^{5/3}
$$
Electron mass $m_e$ is used as the lightest Fermions exert the largest contribution to the Fermi pressure.
$$
p_G=p_F
$$
Setting the gravitational pressure equal to the Fermi pressure and rearranging leads to the radius of a **white dwarf**
$$
R_D=\dfrac{2}{5}\left(\dfrac{9\pi}{4}\right)^{2/3}\dfrac{\hbar^2}{GM^{1/3}m_n^{5/3}m_e}
$$

(e.g. for Sun, $R_D\approx R_\odot/77\approx R_\text{earth}$)

### 8.2.2 Relativistic effects - neutron stars
Flaw in argument - as $n$ increases, $\epsilon_F$ increases and becomes comparable to $m_ec^2$, so relativistic effects cannot be ignored.
$$
\epsilon=\dfrac{\hbar^2k^2}{2m_e}=\dfrac{p_e^2}{2m_e}\quad\underrightarrow{\text{relativistic}}\quad\epsilon^2=m_e^2c^4+p_e^2c^4
$$
Ultrarelativistic case $\quad\epsilon^2\approx p_e^2c^2\quad\Rightarrow\quad\epsilon=\hbar k\cdot c$, so $g(\epsilon)\propto\epsilon^2\quad$ (instead of $\sqrt\epsilon$)

Now radius terms cancel out when equating gravitational and Fermi pressure - leads to **Chandrasekhar mass** instead
$$
M_{\text{CHANDR.}}\approx\dfrac{3}{2}\dfrac{\sqrt{\pi}}{2^{2/3}}\left(\dfrac{\hbar c}{G}\right)^{3/2}m_n^{-2}
$$
which is similar to $M_\odot$ of the Sun.

- If mass of star $\gt M_{\text{CHANDR.}}$ then the star continues to collapse - fermi pressure is provided by (non-relativistic) protons, and a **neutron star** or pulsar is formed.
Neutron stars are very dense - $\sim10^{30}\text{kg}$ in $R\simeq4\text{km}$

What if star continues collapsing and protons become relativistic? Black hole if $R$ falls below Schwartzchild radius $R_S=2GM_s/c^2$

## 8.3 Electrons in metals and the Wiedermann-Franz law
Conduction electrons in a metal can be treated a non-interacting particles with an effective mass $m^*$

Define a Fermi temperature 
$$
T_F=\dfrac{\epsilon_F}{k_B}=\dfrac{\left(3\pi^2\right)^{2/3}\hbar^2n^{2/3}}{k_B2m^*}
$$
For typical metals, $T_F\gg300\text{K}$, which justifies treating the conduction electrons as a Fermi gas.
$$
m^*\textbf{a}=-e\textbf{E}+\textbf{F}_\textbf{friction}
$$
$$
n^*\left(\dfrac{\text{d}\textbf{v}}{\text{d}t}+\dfrac{\textbf{v}}{\tau}\right)=-e\textbf{E}
$$
where we have written drag force as $\textbf{F}_\textbf{friction}=-m^*\textbf{v}/\tau$

Since current is constant, $\text{d}\textbf{v}/\text{d}t=0$
$$
\textbf{v}=-\dfrac{\textbf{E}e\tau}{m^*}
$$
Current density $\textbf{J}=\sigma\textbf{E}=-ne\textbf{v}$, where $\sigma$ is conductivity.
$$
\sigma=\dfrac{ne^2\tau}{m^*}
$$
Define heat conductivity $\alpha$ via heat flux $\Phi=-\alpha\nabla T$
$$
\alpha=\dfrac{1}{3}\bar{v}^2\tau\dfrac{C_V}{V}
$$
where $\bar{v}$ is the average velocity of the electrons.

Taking up heat is equivalent to increasing energy, so only electrons near fermi level (within $k_BT$) contribute to the heat capacity.

Clasically, we expect $C\sim k_BN$, so if only $k_BT/\epsilon_F=T/T_F$ of particles contribute
$$
C\sim k_BN\dfrac{T}{T_F}\quad\Rightarrow\quad C_V\approx\dfrac{\pi^2}{2}k_BN\dfrac{T}{T_F}
$$

#### Wiedermann-Franz law
$$
\dfrac{\alpha}{\sigma}=\dfrac{\pi^2}{3}\dfrac{k_B^2}{e^2}T=LT
$$
Lorentz number $L\approx2.45\times10^{-8}\text{ W}\Omega\text{K}^{-2}$
$$
\therefore\quad\dfrac{\alpha}{\sigma}=LT
$$
Note that this is only true if the dominant heat conduction contribution is due to conduction electrons (not lattice vibrations)

## 8.4 Semiconductors
### 8.4.1 Intrinsic semiconductors
Consider a two-band model of a semiconductor. There are periodic potentials, the lower one being the valence band and the pper one being the conductance band. The minimum separation between them is known as the band gap.

![Simplified two-band structure of a semiconductor, showing the energy epsilon as a function of the wave number k.](/assets/images/2023-03-28-10-34-46.png){max-width: 350px, display: block, margin: 0 auto}

Define the energy of the conductance band as
$$
\epsilon_G+\dfrac{\hbar^2k^2}{2m_e^*}
$$
and the energy of the valence band as $-\dfrac{\hbar^2k^2}{2m_h^*}$
The density of electrons in the conduction band and of holes (missing electrons) in the valence band can be calculated using
$$
n=\dfrac{1}{V}\int_0^\infty g_0(\epsilon)f(\epsilon)\text{d}\epsilon
$$
and using the appropriate limits and expressions for density of state $g_0(\epsilon)$. Remember that $f_h(\epsilon_h)=1-f_e(\epsilon)$ where $\epsilon_h=-\epsilon$
$$
g_0(\epsilon)=\begin{cases}\dfrac{V}{2\pi^2}\left(\dfrac{2m_e^*}{\hbar^2}\right)^{3/2}\sqrt{\epsilon-\epsilon_G}&\quad\epsilon\geq\epsilon_G\\0&\quad0\leq\epsilon\lt\epsilon_G\\\dfrac{V}{2\pi^2}\left(\dfrac{2m_h^*}{\hbar^2}\right)^{3/2}\sqrt{-\epsilon}&\quad\epsilon\lt0\end{cases}
$$

![Density of levels and Fermi-Dirac distribution for an intrinsic, two-band semiconductor. The density of valence and conduction bands are portrayed with different concavities to emphasise that the effective masses m∗h and m∗e may be different from each other.](/assets/images/2023-03-28-10-44-13.png){max-width: 350px, display: block, margin: 0 auto}

Thermal fluctuations can cause the excitation of electrons and creation of holes.

### 8.4.2 Extrinsic semiconductors (doping)
A more practical way of modulating the conductivity of semiconductors is by shifting the chemical potential $\mu$ by adding/removing electrons. This is known as **doping**.
$$
g(\epsilon)=g_0(\epsilon)+n_AV\delta(\epsilon-\epsilon_A)+n_DV\delta(\epsilon-\epsilon_G+\epsilon_D)
$$
This creates "extra states" within the band gap, increasing the conductivity of the semiconductor.

If donor/acceptor energy levels are near edges of band gap and $k_BT$ is small (all electrons/holes can be attributed to doping), then it can be approximated that
$$
n\approx n_D^+\qquad p\approx n_A^-
$$
Charge neutrality $n+n_A^-=p+n_D^+$

Assuming that all dopants are ionised, a semiconductor with many donors and many conduction electrons $(n\approx n_D-n_A)$ is described as $n$*-type* while a semiconductor with many acceptors and many holes $(p\approx n_A-n_D)$ is described as $p$*-type*

In electronics, $p-n$ juctions can be used in diodes and transistors to identify two distinct "digital" states.