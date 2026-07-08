(classical-thermodynamics:heat-transmission:conduction)=
# Conduction

$$\begin{aligned}
  \rho c \frac{\partial T}{\partial t}
  & = - \nabla \cdot \vec{q} + \rho r \\
\end{aligned}$$

**Fourier model of heat condcution flux** wants the heat flux to be proportional to the temperature gradient, $\nabla T$. The most general expression for linear non-isotropic media reads

$$\vec{q} = - \mathbb{K} \cdot \nabla T \ ,$$

with $\mathbb{K}$ the conductivity tensor (a second-oreder (semi)definite (symmetric? **todo** *check, Onsager reciprocal relations*) positive to comply with the second principle of thermodynamics: "heat transfers energy from hot to cold regions"). The behavior of isotorpic media is described by isotropic tensors; thus[^isotropic-2nd-order] the conductivity tensor becomes $\mathbb{K}^{iso} = k \mathbb{I}$, and the heat flux reads

$$\vec{q} = - k \nabla T \ .$$

[^isotropic-2nd-order]: Isotrpic 2-nd order tensors are the identity tensor and its multiples, $\mathbb{A}^{iso} = a \mathbb{I}$. The dot product of 2-nd order identity tensor and a vector (field) gives the vector itself, $\mathbb{I} \cdot  \vec{v} = \vec{v}$.

**Differential problem.** It follows that conduction in a ... medium in region $\Omega$ for time $t \in [t_0, t_1]$ is governed by the differential problem represented by the PDE

$$\begin{aligned}
  \rho c \frac{\partial T}{\partial t}
  & = \nabla \cdot \left( k \, \nabla T \right) + \rho r \qquad \vec{r} \in \Omega \ ,
\end{aligned}$$

supplied with proper initial conditions in every point $\vec{r} \in \Omega$

$$T(\vec{r}, t_0) = T_0(\vec{r}) \qquad \vec{r} \in \Omega$$

and boundary conditions for every point on the boudary of the domain, $\vec{r} \in \partial \Omega$ for every time $t \in [t_0, t_1]$. Different boundary conditions may represent different physical processes:
- known temperature on $S_D$ (Dirichlet boundary conditions: the value of the unknown function is prescribed),

   $$T(\vec{r}, t) = T_D (\vec{r}, t) \qquad \vec{r} \in S_D$$

- known heat flux on $S_N$ (Neumann boundary conditions: the value of the directional derivative of the unknown function is prescribed, in the normal direction w.r.t. the boundary),

   $$\hat{n}(\vec{r},t) \cdot \nabla T(\vec{r}, t) = \phi_N (\vec{r}, t) \qquad \vec{r} \in S_N$$

- known value of a linear combination of the value of the unknown function and its directional derivative (Robin boundary conditions),

   $$\alpha T(\vec{r},t) + \beta \hat{n}(\vec{r},t) \cdot \nabla T(\vec{r}, t) = h(\vec{r},t) \qquad \vec{r} \in S_R$$

**todo**
- derivation of this equation from governing equations of continuum mechanics: list assumptions, thermodynamic conditions (to transform internal energy $e$ as a function of $T$)
- link to *Mathematics:Numerical methods for PDEs:Elliptic (steady) and Parabolic (unsteady) problems*

<!--
Here heat conduction is discussed either in a medium at rest,  $\vec{v} = \vec{0}$ (or equivalent state of motion, from Galileian relativity), ...**todo** *(assumption about thermodynamic state (constant $\rho$, constant $P$,...), and heat capacity...)*. The differential form of mass and internal energy equations  (**todo** *add links to governing equations in continuum mechanics*)

$$\begin{aligned}
  \partial_t \rho + \nabla \cdot \left( \rho \vec{v} \right) & = 0 \\
  \partial_t \left( \rho e \right) + \nabla \cdot \left( \rho  e \vec{v} \right) & = \mathbb{T} : \nabla \vec{v} - \nabla \cdot \vec{q} + \rho r \\
\end{aligned}$$

under the assumption $\vec{v}(\vec{r},t) = \vec{0}$ becomes

$$\begin{aligned}
  \partial_t \rho  & = 0 \qquad \rightarrowi \qquad \rho(\vec{r}, t) = \rho_0(\vec{r}) \\
  \rho_0 \partial_t e & = - \nabla \cdot \vec{q} + \rho r \\
\end{aligned}$$

The first equation implies that density at each point is constant in time. This 
-->
