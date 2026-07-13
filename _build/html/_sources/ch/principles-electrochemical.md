(physics:thermodynamics:foundation:principles:electro-chemical)=
# Principles of Thermodynamics - Electro-chemical systems

In this section:
- Introduction to [chemical reactions](physics:thermodynamics:foundation:principles:electro-chemical:reactions)
- [Energy balance](physics:thermodynamics:foundation:principles:electro-chemical:first-principle)
- [Law of mass action](physics:thermodynamics:foundation:principles:electro-chemical:law-of-mass-action)

In next sections:
- [Batteries](electro-chemical:batteries)


(physics:thermodynamics:foundation:principles:electro-chemical:reactions)=
## Chemical reactions

$$a A + b B \rightleftharpoons c C + d D \ ,$$

or

$$\nu_{R_i}  R_i \rightleftharpoons \nu_{P_j} P_j$$ (eq:reaction:stoichiometry)

(physics:thermodynamics:foundation:principles:electro-chemical:first-principle)=
## First principle - energy balance

```{dropdown} Energy balance

Total energy balance

$$d E^{tot} = \delta L^{ext} + \delta Q^{ext} \ .$$

Macroscopic kinetic energy balance (theorem, from mechanics)

$$d K = \delta L^{ext} + \delta L^{int} \ .$$

Internal energy $E := E^{tot} - K$

$$d E = - \delta L^{int} + \delta Q^{ext} \ .$$

```

```{dropdown} Internal energy, intensive and extensive variables

$$d E = - \delta L^{int,rev} + \underbrace{\delta^+ D + \delta Q^{ext}}_{=:T dS}$$

As $dE$ is a state function, and $\delta L^{int,rev}$ must be reversible by definition, the remaining terms must be reversible as well and completing the exact differential of the energy as a state function. The internal nature may have different natures, e.g. mechanical, elelctrical, magnetic, chemical

$$\delta L^{int,rev} = \delta L^{int,mech} + \delta L^{int,el} + \delta L^{int,magn} + \delta L^{int,el} + \dots$$

but all of these works can be written as the product of a intensive variable $\mathbf{F}$ of the system and the variation of a extensive variable $\mathbf{X}$, formally

$$\delta L^{int,rev} = \mathbf{F} \cdot d \mathbf{X} \ ,$$

* mechanical work, depends on the nature of the system. As an example, for a gas $\delta L^{int,rev} = - P d V$, or for an elastic solid $\delta L^{int,rev} = - V \sigma : d \varepsilon$
  
* electrical work, being $V$ the (uniform) electrical potential of the system, and $Q$ its electrical charge (see [Elecetrostatic energy: systems with uniform potential](https://basics2022.github.io/bbooks-physics-electromagnetism/ch/regimes-electrostatics.html#systems-with-uniform-potential))

  $$- V d Q$$

* chemical work, with $\mu_i$ the molar chemical potential $i$ of the substance (the amount of internal energy added to the system by a change in the number of moles of the $i$ substance in the system)

   $$\mu_i d N_i$$

**todo** See and uniform the treatment in [First principle](physics:thermodynamics:foundation:principles:first), [Second principle](physics:thermodynamics:foundation:principles:second), [Gibbs formalization](physics:thermodynamics:foundation:principles:gibbs-phase-rule), [Thermodynamic potentials](classical-thermodynamics:potentials)

```

Using $\mathbf{X}, S$ as independent variables, 

$$d E = \mathbf{F}(\mathbf{X}, S) \cdot d \mathbf{X} + T(\mathbf{X}, S) d S \ .$$

It the energy of the system is a order-1 homogeneous function of the extensive variables of the system, $E(\lambda \mathbf{Y}) = \lambda E(\mathbf{Y})$[^energy-extensive], Euler theorem ({prf:ref}`thm-euler`) gives

$$E = T S + \mathbf{F} \cdot \mathbf{X} \ .$$

[^energy-extensive]: Not all the systems are made by sub-systems that combine "extensively": it's likely to be impossible to write the energy of these systems as a homogeneous function of the extensive variables of the system.

Explicitly writing the number of moles of the substances of the system out fror the extensive variables $\mathbf{X}$, $\mathbf{X} \rightarrow \left( \mathbf{X}, \mathbf{N} \right)$, and the chemical potentials out from the generalized intensive variables $\mathbf{F} \rightarrow \left( \mathbf{F}, \boldsymbol\mu \right)$, the expression of the internal energy and its differential reads

$$\begin{aligned}
   E & = T S + \boldsymbol\mu \cdot \mathbf{N} + \mathbf{F} \cdot \mathbf{X} \\
  dE & = T dS + \boldsymbol\mu \cdot d\mathbf{N} + \mathbf{F} \cdot d\mathbf{X} \ .
\end{aligned}$$


(physics:thermodynamics:foundation:principles:electro-chemical:law-of-mass-action)=
## Law of Mass Action

The law of mass action states that the forward velocity $v_f$ ($R \rightarrow P$) and backward velocity $v_b$ ($R \leftarrow P$) of reaction {eq}`eq:reaction:stoichiometry` reads

$$\begin{aligned}
  v_f & := -\frac{1}{\nu_{R_k}}\frac{d [ R_k ]_f}{dt} :=  \frac{1}{\nu_{P_k}}\frac{d [ P_k ]_f}{dt} = k_f \prod_i [ R_i ]^{\alpha_{R_i}} \\ 
  v_r & :=  \frac{1}{\nu_{R_k}}\frac{d [ R_k ]_r}{dt} := -\frac{1}{\nu_{P_k}}\frac{d [ P_k ]_r}{dt} = k_r \prod_i [ P_i ]^{\alpha_{P_i}} \\ 
\end{aligned}$$

Taking $R \rightarrow P$ as the positive direction of the reaction, the velocity of the reaction is defined as $v = v_r - v_f$, and the rate of change of the concentrations thus reads

$$\begin{aligned}
  \frac{d [ R_k ]}{dt} = \frac{d [ R_k ]_f}{dt} + \frac{d [ R_k ]_r}{dt} = \nu_{R_k} \left( v_r - v_f \right) = \nu_{R_k} \, v \\ 
  \frac{d [ P_k ]}{dt} = \frac{d [ P_k ]_f}{dt} + \frac{d [ P_k ]_r}{dt} = \nu_{P_k} \left( v_f - v_r \right) = \nu_{P_k} \, v \ .
\end{aligned}$$


* **Equilibrium** is reached when $v_r = v_f$, and thus the rate of change of concentration of the substances is zero.
* **Extent of reaction** $\xi$, so that $d \xi = v dt$.

Constant $k_r$ and $k_f$ usually can be written as

$$k = A \exp \left( - \frac{E}{kT} \right) \ ,$$

being $E$ the **activation energy**, $k$ Boltzmann constant, $T$ the temperature, and $A$ a constant summarizing all the other conditions for the reaction to occur.


**References**

* https://en.wikipedia.org/wiki/Chemical_equilibrium
