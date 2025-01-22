(classical-thermodynamics:principles)=
# Principles of Thermodynamics

This section deals with principles and Gibbs' mathematical formulation of classical thermodynamics. Principles are first introdusced for **closed systmes** and then extened to open arbitrary systems.

**First Law of Thermodynamics.** The first law of thermodynamics represents the total energy balance of a system:

$$\dot{E}^{tot} = P^{e} + \dot{Q}^{e}$$

The total energy of a system can be expressed as the sum of macroscopic kinetic energy \(K\) and internal energy \(E\), which is a macroscopic representation of the kinetic energy of the system's microscopic components around their local macroscopic mean values:

$$E^{tot} = K + E \ .$$

Using the theorem of macroscopic kinetic energy **[REF]** known from mechanics, the following can be derived:

$$\begin{aligned}
  \dot{E}^{tot} & = P^{e} + \dot{Q}^e \\
  \dot{K}       & = P^{tot} = P^{e} + P^{i} \\
  \dot{E}       & = \dot{Q}^e - P^{i} 
\end{aligned}$$

The internal energy balance can be written in incremental form as:

$$d E = d\hspace{-0.08pt}\bar{}\hspace{0.1pt} Q^e - d\hspace{-0.08pt}\bar{}\hspace{0.1pt} L^i \ ,$$

highlighting with notation that internal energy is a state variable of the system, unlike exchanges of work or heat.

It is assumed that the internal energy of the system can be written as a function of local kinematic state variables \(\mathbf{x}\) (which cannot contribute to the macroscopic kinetic energy of the system) and at least one other additive state variable, here called \(S\).

$$E(\mathbf{x}, S)$$

Its differential can be written as:

$$d E = \dfrac{\partial E}{\partial \mathbf{x}}\Big|_{S} \cdot d \mathbf{x} + \dfrac{\partial E}{\partial S}\Big|_{\mathbf{x}} \cdot d \mathbf{S}$$

The incremental internal energy balance can be rewritten as:

$$\begin{aligned}
d E & = - d\hspace{-0.08pt}\bar{}\hspace{0.1pt} L^i + d\hspace{-0.08pt}\bar{}\hspace{0.1pt} Q^e =  \\
    & = - \delta L^{i,rev} + d\hspace{-0.08pt}\bar{}\hspace{0.1pt}^+ D + d\hspace{-0.08pt}\bar{}\hspace{0.1pt} Q^e  \\
\end{aligned}$$

having separated the internal work contribution into reversible and non-reversible actions. It is assumed, in line with experience, that the contribution to internal work from non-reversible forces is always positive, \(d\hspace{-0.08pt}\bar{}\hspace{0.1pt}^+ D \ge 0\): this contribution is called **dissipation**.

Since both the energy differential and the reversible internal work contribution are reversible terms, the sum of dissipation and heat flux must also be a reversible contribution, indicated with \(\delta U\).

From the comparison of the two expressions for the internal energy differential, having recognized the reversible internal work contribution in the first term, the following can be written:

$$
  \delta L^{i,rev} = - \dfrac{\partial E}{\partial \mathbf{x}} \Big|_{S} d \mathbf{x}  \qquad , \qquad 
  \delta U         = \ \dfrac{\partial E}{\partial S} \Big|_{\mathbf{x}} d S 
$$

**Third Law of Thermodynamics: Definition and Sign of Temperature.**
Temperature is defined as the partial derivative of the system's internal energy with respect to the state variable \(S\),

$$T := \dfrac{\partial E}{\partial S}\Big|_S{} \ .$$

The third law of thermodynamics postulates that temperature is always positive:

$$T := \dfrac{\partial E}{\partial S}\Big|_S{} > 0 \ .$$

**Second Law of Thermodynamics: Clausius Statement.** The Clausius statement of the second law of thermodynamics can be formulated in accordance with the evidence that dissipation is always non-negative. Indeed:

$$T dS =: \partial U = \underbrace{d\hspace{-0.08pt}\bar{}\hspace{0.1pt}^+ D}_{\ge 0} + d\hspace{-0.08pt}\bar{}\hspace{0.1pt} Q^e \ge  d\hspace{-0.08pt}\bar{}\hspace{0.1pt} Q^e \ ,$$

and thus:

$$dS \ge \dfrac{d\hspace{-0.08pt}\bar{}\hspace{0.1pt} Q^e }{T} \ .$$

**Second Law of Thermodynamics for Complex Systems and the Direction of Heat Transfers.**

Experience shows that heat transfer occurs from bodies at higher temperatures to those at lower temperatures, meaning the heat flow increases the internal energy of the colder body and decreases that of the hotter body.

In the heat exchange between two bodies \(i\), \(j\) at temperatures \(T_i\), \(T_j\), this empirical evidence can be written as:

$$d\hspace{-0.08pt}\bar{}\hspace{0.1pt} Q_{ji} \gtreqless 0 \quad \text{if} \quad T_i \gtreqless T_j \qquad \rightarrow \qquad \dfrac{d\hspace{-0.08pt}\bar{}\hspace{0.1pt} Q_{ji}}{T_j} + \dfrac{d\hspace{-0.08pt}\bar{}\hspace{0.1pt} Q_{ij}}{T_i} \ge 0 \ ,$$

where \(d\hspace{-0.08pt}\bar{}\hspace{0.1pt} Q_{ji} = - d\hspace{-0.08pt}\bar{}\hspace{0.1pt} Q_{ij}\) is the heat flow from body \(i\) to body \(j\), positive if it increases the internal energy of \(j\) and decreases that of \(i\).

$$d S_i = \underbrace{\dfrac{d\hspace{-0.08pt}\bar{}\hspace{0.1pt}  D_i}{T_i}}_{\ge 0} + \dfrac{d\hspace{-0.08pt}\bar{}\hspace{0.1pt}  Q^{e,i}}{T_i} + \sum_{j \ne i} \dfrac{d\hspace{-0.08pt}\bar{}\hspace{0.1pt}  Q_{ij}}{T_i}$$

Since \(S\) is an extensive variable, the value associated with the entire system is equal to the sum of the values of its parts, \(S = \sum_i S_i\). Therefore, a relationship for the entire system can be derived by summing the contributions from all its parts.

$$\begin{aligned}
  d S & = \sum_i d S_i = \\
      & = \sum_i \sum_i \dfrac{d\hspace{-0.08pt}\bar{}\hspace{0.1pt}  Q^{e,i}}{T_i} + \sum_i \sum_{j \ne i} \dfrac{d\hspace{-0.08pt}\bar{}\hspace{0.1pt}  Q_{ij}}{T_i} + \underbrace{\dfrac{d\hspace{-0.08pt}\bar{}\hspace{0.1pt}  D_i}{T_i}}_{\ge 0} = \\
      & \ge \sum_i \dfrac{d\hspace{-0.08pt}\bar{}\hspace{0.1pt}  Q^{e,i}}{T_i} + \sum_{\{i, j\}} \underbrace{\Big( \dfrac{d\hspace{-0.08pt}\bar{}\hspace{0.1pt}  Q_{ij}}{T_i} + \dfrac{d\hspace{-0.08pt}\bar{}\hspace{0.1pt}  Q_{ji}}{T_j} \Big)}_{ \ge 0 }  = \\
      & \ge \sum_i \dfrac{d\hspace{-0.08pt}\bar{}\hspace{0.1pt}  Q^{e,i}}{T_i} \ .
\end{aligned}$$

