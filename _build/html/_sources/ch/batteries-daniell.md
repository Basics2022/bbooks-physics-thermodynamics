(electro-chemical:batteries:daniell)=
# Daniell cell

(electro-chemical:batteries:daniell:description)=
## Description

The Daniell cell consists of two separate half-cells:
* A zinc ($\text{Zn}$) electrode immersed in a zinc sulfate ($\text{ZnSO}_4$) aqueous solution, with ions $Zn^{2+}$, $SO_4^{2-}$ sully dissolved in that
* A copper ($\text{Cu}$) electrode immersed in a copper(II) sulfate ($\text{CuSO}_4$) aqueous solution, ions $Cu^{2+}$, $SO_4^{2-}$ fully dissolved in that
* A porous barrier (or salt bridge) separating the solutions to prevent rapid mixing while allowing sulfate ions ($\text{SO}_4^{2-}$) to migrate, between the 2 half-cells.

The spontanoues half-cell reactions during disharge are:
* at the anode:

  $$\text{Zn}(s) \rightleftharpoons \text{Zn}^{2+}(aq) + 2 e^-(s)$$ (eq:daniell:reaction:anode)

* at the cathode: 
  
  $$\text{Cu}^{2+}(aq) + 2 e^-(s) \rightleftharpoons \text{Cu}(s)$$ (eq:daniell:reaction:cathode)

(electro-chemical:batteries:daniell:regimes)=
## Regimes

- [Open circuit equilibrium](electro-chemical:batteries:daniell:regimes:open): chemical reactions at equilibrium, no net motion of charges through the electrolytes and the salt bridge
- [Operation under load](electro-chemical:batteries:daniell:regimes:load). Chemical kinetics reactions and diffusion process of ions may produce bottlenecks in the process, and thus overpotentials and/or losses

(electro-chemical:batteries:daniell:regimes:open)=
### Open-circuit equilibrium

**Internal energy**

$$dE = - P dV + T dS + \sum_i \mu_i d N_i + \sum_k \phi_k d Q_k$$

with $i$ spanning all the substances involved in a reaction, and $k$ all the regions with uniform electric potential,

$$\begin{aligned}
  i & \in \{ \text{Zn}, \text{Zn}^{2+}, \text{Cu}^{2+}, \text{Cu} \} \\
  k & \in \{ \text{anode}, \text{cathode}, \text{electrolytes+bridge} \}
\end{aligned}$$

Here the chemical potentials include both the energy changes associated with reaction and phase transformation.
Using the reactions {eq}`eq:daniell:reaction:anode`, {eq}`eq:daniell:reaction:cathode`, it follows (with $z = 2$, number of electrons per reacting ion)

$$\begin{aligned}
  d Q_{\text{anode}}   & = - z q d n_{\text{Zn}^{2+}} =  - z q N_{A} d N_{\text{Zn}^{2+}} = - z F d N_{\text{Zn}^{2+}} \\ 
  d Q_{\text{cathode}} & = - z q d n_{\text{Cu}^{2+}} =  - z q N_{A} d N_{\text{Cu}^{2+}} = - z F d N_{\text{Cu}^{2+}} \ , 
\end{aligned}$$

having introduced the **Faraday's constant**

$$F = q N_A = 96 485.33 \frac{\text{s} \text{A}}{\text{mol}} \ ,$$

defined as the product of the elementary charge (electron charge, but positive), and the number of Avogadro $N_A$. 

If the motion of $\text{SO}_4^{2-}$ ions through the salt bridge keeps the electrolytes electrically neutral, it's possible to write the variation of the moles of substances in the system as a function of an **extent of reaction variable**, $\xi$

$$d N_{\text{Zn}^{2+}} = d N_{\text{SO}_4^{2-}, a} = - d N_{\text{SO}_4^{2-}, c} = - dN_{\text{Cu}^{2+}} = d \xi \ .$$

If the electrolytes and the salt bridge are in an equi-potential region, then the motion of the $\text{SO}_2^{2-}$ ions doesn't influence the variation of the internal energy, that can be written as

$$\begin{aligned}
  d E
  & = - P dV + T dS + \left( \mu_{\text{Zn}^{2+}} - \mu_{\text{Zn}} - \mu_{\text{Cu}^{2+}} + \mu_{\text{Cu}} \right) d \xi - z F \phi_{a} d \xi + z F \phi_c d \xi = \\
  & = - P dV + T dS + \left[ \left( \mu_{\text{Zn}^{2+}} - \mu_{\text{Zn}} - \mu_{\text{Cu}^{2+}} + \mu_{\text{Cu}} \right) - z F \left( \phi_{a} - \phi_c \right) \right] d \xi \ .
\end{aligned}$$

**Gibbs' free energy**, $G = E + PV - TS$.

$$d G = V dP + S dT + \sum_i \mu_i dN_i - \sum_k \phi_k d Q_k$$

Equilibrium condition $d G = 0$ (see [Thermodynamic equilibrium: Gibbs's free energy](notes:equilibrium-conditions:gibbs-free-energy) **todo**) for constant $P$ and $T$ (and thus $d P = 0$, $d T = 0$), requires that the electro-chemical force must be zero, i.e.

$$0 = \mu_{\text{Zn}^{2+}} - \mu_{\text{Zn}} - \mu_{\text{Cu}^{2+}} + \mu_{\text{Cu}} - z F \left( \phi_{a} - \phi_c \right) \ .$$

Thus, the electrostatic potential at open-circuit equilibrium between the cathode (positive electrode) and the anode (negative electrode) reads

$$V_{oc} = \phi_c - \phi_a = \frac{1}{z F} \left( - \mu_{\text{Zn}^{2+}} + \mu_{\text{Zn}} + \mu_{\text{Cu}^{2+}} - \mu_{\text{Cu}} \right)$$

Introducing [Nernst equation](electro-chemicals:nernst-equation) for the chemical potentials, the open-circuit potential can be written as

$$\begin{aligned}
  V_{oc} 
  & = \frac{1}{zF} \sum_i \left\{ \text{sign}_i \mu_i + R T \ln a_i \right\} = \\
  & = \underbrace{ \frac{1}{zF} \left\{ - \mu_{\text{Zn}^{2+}}^\circ + \mu_{\text{Zn}}^\circ + \mu_{\text{Cu}^{2+}}^\circ - \mu_{\text{Cu}}^\circ \right\} }_{ = V_{oc}^\circ} + R T \ln \left( \frac{a_{\text{Cu}^{2+}} a_{\text{Zn}}}{a_{\text{Zn}^{2+}} a_{\text{Cu}}} \right) \\
  V_{oc} & = V_{oc}^\circ + R T \ln \left( \frac{a_{\text{Cu}^{2+}}}{a_{\text{Zn}^{2+}}} \right) \ ,
\end{aligned}$$

as the activity of solid phases are equal to $1$ by definition.[^activity-solid-definition] The activity of the dissolved ions are related (but not equal or proportional, as the behavior of a highly concentrated solution with charged ions deviates significantly from the ideal behavior) to the concentration of the ions at the interface close to the electrode, the regions where the reactions occur,

$$a_i = \gamma_i \frac{C_i}{C_i^\circ} \ .$$

[Debye-Huckel theory](https://en.wikipedia.org/wiki/Debye%E2%80%93H%C3%BCckel_theory) provides a model for the activity coefficient $\gamma_i$, as a function of the ionic strength of the solution.

| Ion | $\mu^\circ [\text{J}/\text{mol}]$ | $\phi$
| :--- | :---: | :---: |
| $\text{Zn}^{2+}(aq)$ | $-147.06 \cdot 10^3$ | $\phi_a =     - \frac{\mu^0_{\text{Zn}^{2+}}}{2 F} = -0.762 \, \text{V}  $ |
| $\text{Cu}^{2+}(aq)$ | $  65.49 \cdot 10^3$ | $\phi_c = \quad \frac{\mu^0_{\text{Cu}^{2+}}}{2 F} =  0.340 \, \text{V}  $ |

The standard open-circuit cell potential of a Daniell cell is $V_{oc}^\circ = \phi_c^\circ - \phi_a^\circ = 1.102 \text{V}$


[^activity-solid-definition]: By definition the standard state of a solid is chosen to be the pure solid at the system temperature and a standard pressure. From this and Nernst equation, it immediately follows that $a = 1$ for the solid in the reference condition. From a more intuitive point of view, concentration of a solid doesn't change: adding a piece of a solid medium doesn't make the atoms in the crystal more packed, and thus the chemical environment around an atom of the solid lattice doesn't change, and thus its chemical potential neither.

(electro-chemical:batteries:daniell:regimes:load)=
### Operation under loads

