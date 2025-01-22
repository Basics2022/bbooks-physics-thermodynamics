(physics-hs:thermodynamics:principles)=
# Principles of Thermodynamics

In this chapter, the principles of classical thermodynamics, along with the relevant concepts and mathematical formalism, are introduced. 
The principles of thermodynamics are presented for **closed systems**, and subsequently extended to open systems.

<!--
Recalling that classical thermodynamics provides a macroscopic averaged description of the microscopic dynamics of systems composed of many elementary components, the microscopic level of detail can be used to give meaning to the thermodynamic variables used in the macroscopic description.
-->

- The [**principle of conservation of mass - Lavoisier's principle**](physics-hs:thermodynamics:foundation:principles:lavoisier), valid in classical mechanics and summarized by the formula *"nothing is created, nothing is destroyed, but everything is transformed"*, states that in a closed system, the mass is constant,

  $$d M = 0 \ .$$

- The [**first law of thermodynamics**](physics-hs:thermodynamics:foundation:principles:first) provides the general form of the *total* energy balance of a closed system, recognizing the work done by external forces $\delta L^{ext}$ and the heat $\delta Q^{ext}$ exchanged between the system and the external environment as the causes of the variation of the total energy of the system.

  $$d E^{tot} = \delta L^{ext} + \delta Q^{ext} \ .$$

- The work of **Gibbs** provides [**the necessary concepts and a rigorous mathematical formalization**](physics-hs:thermodynamics:foundation:principles:gibbs-phase-rule) of classical thermodynamics. The concepts of internal energy, state variables, and Gibbs' phase rule are introduced; additionally, some [phase diagrams](physics-hs:thermodynamics:foundation:principles:phase-diagrams) for representing the state of a system and thermodynamic transformations are presented, which will be used in subsequent chapters.

- The [**second law of thermodynamics**](physics-hs:thermodynamics:foundation:principles:second) describes natural tendencies: the dissipation of macroscopic mechanical energy and the transfer of heat from a hot body to a cold body, in a principle expressible in terms of **entropy**,

  $$d S \ge \frac{\delta Q}{T} \ .$$

- Finally, the balance of physical quantities for [**open systems**](physics-hs:thermodynamics:foundation:principles:open) is derived by modifying the balance equations for closed systems, introducing terms for the **flux of physical quantities due to the transport of matter** across the system's boundary.

<!--
<span style="color:red">Organize this for presentation! The contents are divided into subsequent sections.</span>

In this section, the fundamental principles of classical thermodynamics are presented. **todo**

**Principle of conservation of mass.**
In the context of classical physics, the mass of a closed system is constant.

**First law of thermodynamics - total energy balance.**
The first law of thermodynamics represents the total energy balance for a closed system (**todo** *references to open and closed systems*),

  $$d E^{tot} = \delta L^{ext} + \delta Q^{ext} \ .$$
  
  Using the kinetic energy theorem (**todo** reference to mechanics), $dK = \delta L^{ext} + \delta L^{int}$, and the definition of internal energy as the difference between total energy and macroscopic kinetic energy, $E := E^{tot} - K$,
  
  $$d E = - \delta L^{int} + \delta Q^{ext} \ .$$

**Gibbs' phase rule.**
The internal energy can be written as a state function, $E(S, X_k)$, **todo** with independent variables ...

$$\begin{aligned}
dE & = \left(\dfrac{\partial E}{\partial S}\right)_{\mathbf{X}} d S 
     + \left(\dfrac{\partial E}{\partial X_k}\right)_{S} d X_k  = \\
   & = T \, d S + \sum_k F_k \, d X_k
\end{aligned}$$

The variation of internal energy with respect to the variable $S$ corresponds to the temperature,

$$T = \left(\dfrac{\partial E}{\partial S}\right)_{\mathbf{X}} \ge 0 \ .$$


**Second law of thermodynamics - irreversibility.**

- Second law for simple systems **todo** *uniform temperature*

  $$\begin{aligned}
    dE & = \delta Q^{ext} - \delta L^{int} = \\
       & = \underbrace{\delta Q^{ext} + \delta^+ D}_{\delta U} - \delta L^{int, rev} = \\
  \end{aligned}$$
  
  $$\begin{cases}
  -\delta L^{int,rev} & = \displaystyle\sum_k F_k \, d X_k \\
  \delta U            & = T \, dS
  \end{cases}$$
-->

