(physics-hs:thermodynamics:foundation:principles:gibbs-phase-rule)=
# Gibbs: Internal Energy, Phase Rule, and Multivariable Functions

Following Gibbs' work, this section introduces concepts such as [state variables](physics-hs:thermodynamics:foundation:principles:gibbs-phase-rule:state-vars) and [internal energy](physics-hs:thermodynamics:foundation:principles:gibbs-phase-rule:internal-energy), as well as the [Gibbs phase rule](physics-hs:thermodynamics:foundation:principles:gibbs-phase-rule:gibbs-phase-rule). Later, the [first law of thermodynamics is reformulated](physics-hs:thermodynamics:foundation:principles:gibbs-phase-rule:first) using the formalism introduced by Gibbs, which allows identifying the state of a system with a limited number of independent state variables and expressing the other (dependent) state variables as functions of multiple variables.

(physics-hs:thermodynamics:foundation:principles:gibbs-phase-rule:state-vars)=
## State Variables
```{prf:definition} State Variable

A state variable of a system is a physical property of the system that depends exclusively on the current state of the system.

```

```{prf:example} State Variables and Non-State Variables
State variables include temperature, pressure, internal energy, entropy, etc.
Non-state variables include work or heat exchanged by the system. **todo**

``` 

(physics-hs:thermodynamics:foundation:principles:gibbs-phase-rule:internal-energy)=
## Internal Energy
```{prf:definition} Internal Energy
The internal energy of a system is defined as the difference between the total energy and the macroscopic kinetic energy of the system,

$$E = E^{tot} - K \ .$$
```

It is possible to derive a balance for the internal energy of a closed system by subtracting the balance of kinetic energy described by the kinetic energy theorem from the balance of total energy provided by the first law of thermodynamics,

$$\begin{aligned}
  d E^{tot} & = \delta L^{ext} + \delta Q^{ext} \\
  d K       & = \delta L^{ext} + \delta L^{int} \ ,
\end{aligned}$$

The energy balance for the internal energy of a closed system then becomes

$$d E = \delta Q^{ext} - \delta L^{int} \ .$$


(physics-hs:thermodynamics:foundation:principles:gibbs-phase-rule:gibbs-phase-rule)=
## Gibbs Phase Rule
```{prf:definition} Phase
A phase is defined as a portion of a chemical-physical system characterized by uniform chemical-physical (macroscopic) properties.
```
**todo**
- Discussion of properties
- Examples: a mixture of miscible gases constitutes a single phase, in which the individual components cannot be macroscopically distinguished; immiscible liquids remain macroscopically separated and thus constitute multiple phases, in which distinct chemical compositions can be macroscopically identified;...

```{prf:proposition} Gibbs Phase Rule
The thermodynamic (equilibrium) state of a system is identified by a number $F$ of independent **intensive** state variables, determined by the **Gibbs phase rule**,

$$F = C - P + 1 + W \ ,$$

i.e., the number of independent intensive variables (or degrees of freedom), $F$, of a system is a function of the number of independent components $C$, the number of phases $P$, and the number $W$ of ways the system can manifest internal work, such as:
- internal mechanical stresses
- contribution of surface tension
- bond energy of the molecules of the components
- contribution of the electromagnetic field
```

```{dropdown} Discussion of the Gibbs Phase Rule
The equilibrium state of a system is defined by the values of the state variables, which for a non-electrically charged gas system are: temperature $T$, pressure $p$, and concentrations $C_{c,\phi}$ of the individual components $c=1:C$ in the individual phases $\phi = 1:P$ within the system.

The state of the system is thus determined by the values of the $1+W$ intensive thermodynamic variables, here $W+1=2$ ($T$, $p$), and the $C \, P$ molar or mass fractions $n_{c,\phi}$, for a total of $N \, P + W + 1$ variables.
In general, these variables are constrained by some conditions:

- $C \, (P-1)$ phase equilibrium conditions for each component, described by the equality of chemical potentials

  $$\mu_{c,\phi_1}(T,p) = \mu_{c,\phi_2}(T,p) = \dots = \mu_{c,\phi_P}(T,p)$$

- $P$ unitarity conditions of the fractions

  $$\sum_{c} n_{c,\phi} = 1$$

Thus, with $C \, P + W + 1$ variables and $P + C\, (P-1) = C \, P - C + P$ equations, we find that the problem can be determined by 

$$C \, P + W + 1 - C \, P + C - P  =  C - P + W + 1 = F \ ,$$

independent variables.
```

**todo** 
- Provide examples that clarify the definition of phase (e.g., pure solids or liquids represent phases on their own), and of independent component (e.g., chemical reactions, with no excess components, create constraints that reduce the number of independent substances, thanks to stoichiometric relationships between substances)
- Discuss the role of phase fractions of a single component and the fact that they are not state variables; example phase transition from liquid to vapor: equilibrium is determined by the value of $P$ (or $T$), and the vapor fraction is a result of other extensive variables of the system.

```{prf:example} Closed system containing a single-component (or non-reactive), single-phase, electrically neutral (or not subjected to electromagnetic field)
:class: dropdown

In a system consisting of a compressible gas, single-component and single-phase (gas phase), electrically neutral, **todo** *other?*, the only form of internal work is related to compression, $\delta L^{int,rev} = P dV$, and thus $W = 1$. Therefore, the system requires

$$F = C - P + 1 + W = 1 - 1 + 1 + 1 = 2 \ ,$$

state variables to define the system state.
```
```{prf:example} Open system containing a single-component (or non-reactive), single-phase, electrically neutral (or not subjected to electromagnetic field)
:class: dropdown

In an open system, the variation in energy of the system also depends on the variation in the amount of gas contained in it. Thus, in general, there are $W = 2$ ways to change the system's energy: by compression work or by a flow of matter into the system. Therefore, $F=3$ state variables are needed to define the system's state.
```
```{prf:example} Reactive gas mixture in a closed system
:class: dropdown

In a reactive gas mixture consisting of two compounds $A$, $B$ in equilibrium according to the equilibrium reaction

$$n_a A + n_b B \leftrightarrow n A_a B_b$$

the energy of the system depends on the mechanical compression work of the gas mixture and the quantities of the 3 compounds present in the gas. However, the variation of these compounds is not independent but determined by the equilibrium reaction. Specifically,

$$\begin{aligned}
  d n_{B} & = d n_{A} \frac{n_b}{n_a} \\
  d n_{A_a B_b} & = - d n_{A} \frac{n}{n_a} \\
\end{aligned}$$

The reaction is thus determined by a single parameter. The variation in energy of the system is thus determined by $W=2$ processes: from the compression work done on the system, and from the state of the reaction. To define the state of the system, $F=3$ independent state variables are needed, such as **todo** $T$, $P$, $n_A$? Are the chemical potentials $\mu_A$, $\mu_B$, $\mu_{A_a B_b}$ required? Are they uniquely determined?
```
```{prf:example} Single-component system during a phase transition
:class: dropdown
**First-order phase transition.** During a first-order phase transition, two phases, $P = 2$, are simultaneously present in the system. According to the Gibbs phase rule, the state of the system is determined by 

$$F = C - P + 1 + W = 1 - 2 + 1 + 1 = 1 \ ,$$

state variable.

**Critical point.** The critical point in the phase diagram of a single-component system defines the condition where three phases, $P = 3$, are simultaneously present in the system. According to the Gibbs phase rule, the state of the system is determined by $F = 0$ state variables: the state of the system at the critical point is uniquely defined, with no degrees of freedom.
```
```{prf:example} Solid
:class: dropdown

In the absence of other physical phenomena, the only form of work in a solid is related to deformation work, $\delta L^{int,rev} = \sigma_{ij} \, d \varepsilon_{ij} dV$. The strain tensor is second-order and symmetric, and therefore has 6 independent components in 3-dimensional space, so $W=6$
```
```{prf:example} Solid mixtures
:class: dropdown

- Phases in solid mixtures **todo**
```
```{prf:example} Influence of the electromagnetic field
:class: dropdown

- Electric field and magnetization **todo**
```

(physics-hs:thermodynamics:foundation:principles:gibbs-phase-rule:first)=
## First Law in terms of state variables
Internal energy is an extensive variable of a thermodynamic system. In general, it can be written as a function of extensive variables that represent the ways the system manifests its internal energy (**todo** *due to work done on it, heat transferred to the system, and its chemical composition, thus the energy contained in bonds*).

$$E(S, X_k)$$

where $ X_k $ are the state variables whose variations are associated with reversible internal work, and $ S $ is the state variable whose variation is associated with heat exchange with the external environment and internal dissipative actions. **todo** *referring to the chapter on functions and multivariable calculus*

Assuming the function $ E $ is continuous and differentiable, at least piecewise, the exact differential of internal energy can be written as a function of the increments of the independent variables:

$$
dE = \left. \dfrac{\partial E}{\partial S} \right|_{\mathbf{X}} d S + \left. \dfrac{\partial E}{\partial X_k} \right|_{S} d X_k = 
T \, d S + \sum_k F_k \, d X_k
$$

where $ F_k $ are the generalized forces associated with changes in the generalized coordinates $ X_k $, and $ T $ and $ S $ correspond to temperature and entropy as discussed further below. **todo**.

```{note}
As shown later, with this formalism, it is straightforward to express [the **second** and **third** laws of thermodynamics](physics-hs:thermodynamics:foundation:principles:gibbs-phase-rule:second) as:
- $ dS \ge \dfrac{\delta Q^{ext}}{T} $
- $ T \ge 0 $
```

The expression for the differential of internal energy can be compared with the energy balance written in terms of heat transferred to the system and internal work:

$$
dE = \delta Q^{ext} - \delta L^{int} = 
\delta Q^{ext} + \delta^+ D - \delta L^{int,rev}
$$

where the internal work $ \delta L^{int} $ is recognized as the sum of a reversible contribution and a dissipative contribution, which is never negative: $ \delta L^{int} = \delta L^{int,rev} - \delta^+ D $.

Since $ dE $ is an exact differential and $ \delta L^{int,rev} $ is a reversible contribution, it follows that the sum of the two non-reversible contributions, $ \delta U := \delta Q^{ext} + \delta^+ D $, is a reversible contribution. Comparing the two expressions for the differential of internal energy, we can associate reversible internal work with the sum of works formed as the product of generalized forces $ F_k $ and changes in the state variables $ X_k $, and the term $ \delta U $ with the product $ T \, dS $:

$$
\begin{cases}
  -\delta L^{int,rev} &= \sum_k F_k \, d X_k \\
  \delta U &= T \, dS
\end{cases}
$$

```{dropdown} Temperature, $ T $, and entropy, $ S $

In the absence of external work done on the system, and in the absence of dissipation $ \delta^+ D = 0 $, we get:

$$
dE^{tot} = dE = \delta Q^{ext}
$$

$$
dS = \frac{\delta Q^{ext}}{T}
$$

Consider a closed and isolated system made of two subsystems in equilibrium, which can exchange heat but not work.

The total energy of the system is constant, $ E = E_1 + E_2 $. If the two subsystems are not initially at the same temperature, we observe a heat flow from the hotter system to the colder one, which satisfies the inequality:

$$
\frac{\delta Q_{12}}{T_1} + \frac{\delta Q_{21}}{T_2} \ge 0 \quad \rightarrow \quad dS_1 + dS_2 \ge 0
$$

The quantity $ S = S_1 + S_2 $ is non-decreasing.


<!--
$$E_1(T_1) + E_2(T_2) = E = \text{const}$$

$$\frac{d E_1}{d T_1} = -\frac{d E_2}{d T_2} \frac{d T_2}{d T_1}$$
-->

```

(physics-hs:thermodynamics:foundation:principles:gibbs-phase-rule:second)=
## Second and Third Laws of Thermodynamics

The formalism introduced in this section allows for a rather natural formulation of the second law and a version of the third law of thermodynamics.

This formulation of the third law of thermodynamics states that the thermodynamic temperature is always positive:

$$
T := \left.\frac{\partial E}{\partial S}\right|_{\mathbf{X}} > 0
$$

**todo** *Add some words about the significance, in terms of molecular agitation and probability*

In cases where this form or consequence of the third law of thermodynamics holds, the second law of thermodynamics is a consequence of the non-negativity of dissipation and the heat transfer mechanism, as will be discussed in more detail in the discussion of [composite systems](physics-hs:thermodynamics:principles:second:composite).

In the general case of a **simple system**, using the definition $ dS = \frac{\delta U}{T} = \frac{\delta Q^{ext} + \delta^+ D}{T} $, the non-negativity of dissipation, $ \delta^+ D \ge 0 $, implies:

$$
dS \ge \frac{\delta Q^{ext}}{T}
$$

This is an expression of the [Clausius statement of the second law of thermodynamics](physics-hs:thermodynamics:foundation:principles:second).

**todo** **oss** *The third law of thermodynamics: 1. It seems not to be a fundamental principle; 2. For some systems with limited energy, the definition of temperature $ T := \left( \frac{\partial E}{\partial S} \right) $ produces a negative temperature* **todo** *add a section on statistical mechanics?*

---

From L.E. Reichl, *A Modern Course in Statistical Physics*, with some inconsistencies **todo** *check!*

$$
\delta W = - P dV + J dL + \sigma d A + V \left( \vec{e} \cdot d \vec{p} + \vec{h} \cdot d \vec{m}\right) + \phi d q
$$

- where $ J $, $ \sigma $ are tensions per unit length and area, $ d L $, $ d A $ are changes in length or area,
- where $ \vec{e} $, $ \vec{h} $ are the electric and magnetic fields, $ \vec{p} $, $ \vec{m} $ are polarization and magnetization,
- $ \phi $ is the electric potential, and $ q $ is electric charge (for open systems, otherwise $ dq \equiv 0 $ or net charge would be created!)

```{prf:example} Closed Monocomponent Gas System
:class: dropdown

The energy of the system, $ E(S,V) $

$$
dE = T \, dS - P \, dV
$$

```

```{prf:example} Open Monocomponent Gas System
:class: dropdown

The energy of the system, $ E(S,V,N) $

$$
dE = T \, dS - P \, dV + \mu \, dN
$$

```

```{prf:example} Reactive Gas Mixture in a Closed System
:class: dropdown

The energy of the system

$$
\begin{aligned}
  dE & = T \, dS - P \, dV + \mu_k \, dN_k = \\
     & = T \, dS - P \, dV + \left( \mu_k n_k \right) dN
\end{aligned}
$$

where $ n_k $ are the stoichiometric coefficients (with sign) of the reaction, and $ N $ is a quantity that identifies the equilibrium of the reaction, such that the variation of each component can be written as $ dN_k = n_k \, dN $.

```

```{prf:example} Monocomponent Mixture During a Phase Transition
:class: dropdown

**todo** how to treat the phase fractions?

```

```{prf:example} Solid
:class: dropdown

Solid system with initial volume $ V $ under uniform stress and strain, with small deformations

$$
dE = T \, dS - V \, \sigma_{ij} \, d \varepsilon_{ij}
$$

```

```{prf:example} Solid Mixtures
:class: dropdown

**todo**
```

```{prf:example} Influence of the Magnetic Field
:class: dropdown

$$
dE = T \, dS - P \, d V + H \, dM
$$

**todo**
```

