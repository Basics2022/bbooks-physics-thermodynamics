(physics-hs:thermodynamics:foundation:principles:electro-chemical)=
# Principles of Thermodynamics - Electro-chemical systems


```{dropdown} Energy balance
:open:

Total energy balance

$$d E^{tot} = \delta L^{ext} + \delta Q^{ext} \ .$$

Macroscopic kinetic energy balance (theorem, from mechanics)

$$d K = \delta L^{ext} + \delta L^{int} \ .$$

Internal energy $E := E^{tot} - K$

$$d E = - \delta L^{int} + \delta Q^{ext} \ .$$

```

```{dropdown} Internal energy, intensive and extensive variables
:open:

$$d E = - \delta L^{int,rev} + \underbrace{\delta^+ D + \delta Q^{ext}}_{=:T dS}$$

As $dE$ is a state function, and $\delta L^{int,rev}$ must be reversible by definition, the remaining terms must be reversible as well and completing the exact differential of the energy as a state function. The internal nature may have different natures, e.g. mechanical, elelctrical, magnetic, chemical

$$\delta L^{int,rev} = \delta L^{int,mech} + \delta L^{int,el} + \delta L^{int,magn} + \delta L^{int,el} + \dots$$

but all of these works can be written as the product of a intensive variable $\mathbf{F}$ of the system and the variation of a extensive variable $\mathbf{X}$, formally

$$\delta L^{int,rev} = \mathbf{F} \cdot d \mathbf{X} \ ,$$

* mechanical work
  
* electrical work, being $V$ the (uniform) electrical potential of the system, and $Q$ its electrical charge (see [Elecetrostatic energy: systems with uniform potential](https://basics2022.github.io/bbooks-physics-electromagnetism/ch/regimes-electrostatics.html#systems-with-uniform-potential))

  $$- V d Q$$

* chemical work, with $\mu_i$ the molar chemical potential $i$ of the substance (the amount of internal energy added to the system by a change in the number of moles of the $i$ substance in the system)

   $$\mu_i d N_i$$

**todo** See and uniform the treatment in [First principle](physics-hs:thermodynamics:foundation:principles:first), [Second principle](physics-hs:thermodynamics:foundation:principles:second), [Gibbs formalization](physics-hs:thermodynamics:foundation:principles:gibbs-phase-rule), [Thermodynamic potentials](classical-thermodynamics:potentials)



```


