(physics-hs:thermodynamics:foundation:principles:second)=
# Second Law of Thermodynamics - Clausius Statement

The Clausius statement of the second law of thermodynamics can be formulated quite naturally using the formalism introduced. There are two other famous statements of the second law of thermodynamics, the Planck and Kelvin statements, which will be presented in the context of heat engines.

(physics-hs:thermodynamics:foundation:principles:second:simple)=
## Simple Systems
The elementary variation of entropy $d S$ of a simple closed system at uniform temperature $T$ is greater than or equal to the ratio of the elementary heat flux introduced into the system and the temperature of the system itself,
  
  $$dS = \underbrace{\dfrac{\delta^+ D}{T}}_{\ge 0} + \dfrac{\delta Q^{ext}}{T} \ge \dfrac{\delta Q^{ext}}{T} \ .$$

This is the Clausius statement of the second law of thermodynamics for simple systems with uniform temperature.

(physics-hs:thermodynamics:principles:second:composite)=
## Composite Discrete Systems
**todo** definition of a composite system. Heat conduction occurs between subsystems.

Entropy in classical thermodynamics is an extensive physical quantity: the entropy of a system composed of $N$ simple subsystems is the sum of the entropies of the subsystems,

$$S = \sum_{n=1:N} S_n \ .$$

The entropy balance of a single subsystem that exchanges heat with the other subsystems and the external environment is written as

  $$\begin{aligned}
    dS_i & = \dfrac{\delta Q^{ext,i}_i}{T_i} + \dfrac{\delta^+ D_i}{T_i} = \\
         & = \dfrac{\delta Q^{ext}_i}{T_i} + \dfrac{\sum_{k \ne i} \delta Q_{ik}}{T_i} + \dfrac{\delta^+ D_i}{T_i} \ge \\
         & \ge \dfrac{\delta Q^{ext}_i}{T_i} + \dfrac{\sum_{k \ne i} \delta Q_{ik}}{T_i} \ . 
  \end{aligned}$$

The entropy balance of the entire system is obtained by summing the entropy balances of the individual subsystems,

  $$\begin{aligned}
    dS & = \sum_i d S_i \ge \\
       & \ge \sum_i \left\{ \dfrac{\delta Q^{ext}_i}{T_i} + \dfrac{\sum_{k \ne i} \delta Q_{ik}}{T_i} \right\} = \\
       & = \sum_i \dfrac{\delta Q^{ext}_i}{T_i} + \underbrace{\sum_{\left\{i,k\right\}} \delta Q_{ik} \left( \dfrac{1}{T_i} - \dfrac{1}{T_k} \right)}_{\ge 0} \ge \\
       & \ge \sum_i \dfrac{\delta Q^{ext}_i}{T_i} \ . 
  \end{aligned}$$

Using the relation that represents the natural tendency of heat transfer "from a system at a higher temperature to a system at a lower temperature,"

$$\delta Q_{ik} \left( \dfrac{1}{T_i} - \dfrac{1}{T_k} \right) \ge 0 \ .$$

**todo** *add reference to the natural tendency in heat transfer*

(physics-hs:thermodynamics:principles:second:universe)=
## Increase of Entropy in the Universe
If we consider the universe as the closed and isolated system (but is this true? Who knows? Maybe it's reasonable for now, but many things that seem reasonable today might be nonsense in a few years) consisting of a system of interest $sys$ and the external environment $env$.

The variation of entropy in the universe is the sum of the variation in the system and in the external environment. We denote by $\delta Q_{sys,env}$ the heat flux which, if positive, increases the energy of the system and decreases that of the external environment. Assuming that the two subsystems are internally homogeneous,

$$\begin{aligned}
d S^{univ} & = d S^{sys} + d S^{env} = \\
           & = \dfrac{\delta Q_{sys,env}}{T^{sys}} + \dfrac{\delta Q_{env,sys}}{T^{env}} = \\
           & = \dfrac{\delta Q_{sys,env}}{T^{sys}} - \dfrac{\delta Q_{sys,env}}{T^{env}} = \\
           & = \delta Q_{sys,env} \left( \dfrac{1}{T^{sys}} - \dfrac{1}{T^{env}} \right) \ge 0 \ ,
\end{aligned}$$

we obtain the relation

$$dS^{univ} \ge 0 \ ,$$

which predicts the "non-decrease" of the entropy of the universe.

(physics-hs:thermodynamics:principles:second:continuum)=
## Composite Continuous Systems





