(physics-hs:thermodynamics:foundation:principles:electro-chemical)=
# Principles of Thermodynamics - Electro-chemical systems


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

**todo** See and uniform the treatment in [First principle](physics-hs:thermodynamics:foundation:principles:first), [Second principle](physics-hs:thermodynamics:foundation:principles:second), [Gibbs formalization](physics-hs:thermodynamics:foundation:principles:gibbs-phase-rule), [Thermodynamic potentials](classical-thermodynamics:potentials)

```

Using $\mathbf{X}, S$ as independent variables, 

$$d E = \mathbf{F}(\mathbf{X}, S) \cdot d \mathbf{X} + T(\mathbf{X}, S) d S \ .$$

From the nature of the extensive variable, $E(\lambda \mathbf{Y}) = \lambda E(\mathbf{Y})$, Euler theorem gives

## Chemical reactions

$$a A + b B \rightleftharpoons c C + d D \ ,$$

or

$$\nu_{R_i}  R_i \rightleftharpoons \nu_{P_j} P_j$$


### Law of Mass Action

The law of mass action states that the velocity of a reaction reads

$$\begin{aligned}
  v_f & := -\frac{1}{\nu_{R_k}}\frac{d [ R_k ]_f}{dt} :=  \frac{1}{\nu_{P_k}}\frac{d [ P_k ]_f}{dt} = k_f \prod_i [ R_i ]^{\alpha_{R_i}} \\ 
  v_r & :=  \frac{1}{\nu_{R_k}}\frac{d [ R_k ]_r}{dt} := -\frac{1}{\nu_{P_k}}\frac{d [ P_k ]_r}{dt} = k_r \prod_i [ P_i ]^{\alpha_{P_i}} \\ 
\end{aligned}$$

and 

$$\begin{aligned}
  \frac{d [ R_k ]}{dt} = \frac{d [ R_k ]_f}{dt} + \frac{d [ R_k ]_r}{dt} = \nu_{R_k} \left( v_r - v_f \right) \\ 
  \frac{d [ P_k ]}{dt} = \frac{d [ P_k ]_f}{dt} + \frac{d [ P_k ]_r}{dt} = \nu_{P_k} \left( v_f - v_r \right) \\ 
\end{aligned}$$


* **Equilibrium** is reached when $v_r = v_f$, and thus the rate of change of concentration of the substances is zero.
* **Extent of reaction** $\xi$, so that $d \xi = v dt$.


**References**

* https://en.wikipedia.org/wiki/Chemical_equilibrium
