(classical-thermodynamics:potentials)=
# Thermodynamics potentials

In this section, principles and the mathematical formalism of classical thermodynamics are reviewed.

## First principle

For an extensive system

$$d E = T \, d S + \mathbf{F} \cdot d \mathbf{X} \ ,$$

being $E$ the internal energy, $T$ temperature, $S$ entropy, $\mathbf{F}$ generalized force, $\mathbf{X}$ generalized displacement.

Following Gibbs' formulation, internal energy $E$ can be written as a function of a limited set of independent state variables,

$$E(S, \mathbf{X}) \ .$$

Internal energy $E$, entropy $S$ and the generalized displacement $\mathbf{X}$ are **extensive** physical quantities, and thus (**thus?**) the derivatives

$$T := \left.\dfrac{\partial S}{\partial E}\right|_{\mathbf{X}} \quad , \quad \mathbf{F} := \left.\dfrac{\partial E}{\partial \mathbf{X}}\right|_S$$

are **intensive** quantities. A discussion about the difference between the concept of *additivity* and *extensivity*[^additivity-extensivity].
Beside being extensive, internal energy in classical thermodynamics is an homogeneous function[^SE-e-homogeneous] of order 1 of its arguments, namely

$$E(a \, S, a \, \mathbf{X}) = a \, E(S, \mathbf{X}) \ .$$

**Euler's theorem for homogeneous functions** holds.

```{prf:theorem} Euler's theorem for homogeneous functions
Let $f(x_i)$ and homogeneous function of order $m$, i.e.

$$f(a \, x_i) = a^m \, f(x_i) \ .$$ (eq:homogeneous-fun:def)

It follows that 

$$f(x_k) = m \, x_i \, \dfrac{\partial f}{\partial x_i}(x_k) \ .$$

```
Proof immediately follows, evaluating the derivative of {eq}`eq:homogeneous-fun:def` w.r.t. $a$, and evaluating for $a = 1$, i.e.

$$x_i \, \dfrac{\partial f}{\partial x_i} (a \, x_k) = m \, a^{m-1} \, f(x_k) \ ,$$

and for $a = 1$,

$$f(x_k) = x_i \, \dfrac{\partial f}{\partial x_i} (x_k)\ .$$

[^additivity-extensivity]: [H.Touchette, When is a quantity additive, and when is it extensive?](https://arxiv.org/pdf/cond-mat/0201134)
[^SE-e-homogeneous]:  [https://physics.stackexchange.com/q/677855](https://physics.stackexchange.com/q/677855)

Thus, internal energy can be written as

$$E(S, \mathbf{X}) = T \, S + \mathbf{F} \cdot \mathbf{X} \ .$$ 

### First principle for different systems

- Single-component fluid, $E(S, V, N)$

   $$d E = T \, d S - P \, d V + \mu \, d N$$

- Multi-component fluid, $E(S, V, N_k)$

   $$d E = T \, dS - P \, d V + \mu_k \, d N_k$$

   where the change of number of particles (or moles, it depends on the description - anyway a non-dimensional number) $d N_k$ is governed by the stoichiometric ratios of the reactions occurring in the system.

- Single-component solid, $E(S, \mathbf{X})$

   $$d E = T \, dS + \mathbf{F} \cdot d \mathbf{X}$$

### First principle for specific quantities

First principle and thermodynamics can be writtenin terms of specific quantites, usually either for unit volume or for unit mass.

#### First principle per unit mass

All the extensive quantites are written as the product of the mass of the system $M$ and its density, namely

$$E = M  e \quad , \quad S = M  s \quad , \quad \mathbf{X} = M \mathbf{x} \ ,$$

and, using the product rule for differential $d E = d (M e) = dM \, e + M \, de$, first principle can be written as

$$0 = d M \underbrace{\left( e - T s - \mathbf{F} \cdot \mathbf{x} \right)}_{= 0} + M \left( d e - T ds - \mathbf{F} \cdot d \mathbf{x} \right) \ .$$

The first term is identically zero, since it's the expression of the internal energy divided by $M$. Being $M > 0$, the second term gives the first principle per unit mass

$$d e = T ds + \mathbf{F} \cdot d \mathbf{x} \ .$$

##### Different systems

- Single-component fluid; 

   $$V = M \dfrac{1}{\rho} \quad , \quad N = M \dfrac{1}{m} \ , $$

   being $\rho$ the mass density and $m$ the mass of a particle (or mole, it depends on the description) of the medium; $m$ is **constant**. First principle becomes

   $$0 = d M \underbrace{\left( e - T s + \dfrac{P}{\rho} - \dfrac{\mu}{m} \right)}_{= 0} + M \left( d e - T ds - \dfrac{P}{\rho^2} d\rho \right) \ ,$$

  and thus

   $$de = T ds + \dfrac{P}{\rho^2} d \rho \ .$$

- Multi-component fluid

   $$V = M \dfrac{1}{\rho} \quad , \quad N_k = M_k \dfrac{1}{m}_k = M \dfrac{M_k}{M} \dfrac{1}{m_k} = M \dfrac{1}{m_k} \dfrac{\rho_k}{\rho} = M \dfrac{1}{m_k} w_k \ , $$

   being $\rho$ the mass density and $m$ the mass of a particle (or mole, it depends on the description) of the $k^{th}$ substance; $m_k$ is **constant**. The first principle becomes

   $$0 = d M \underbrace{\left( e - T s + \dfrac{P}{\rho} - \dfrac{\mu_k}{m_k} w_k \dfrac{}{} \right)}_{= 0} + M \left[ d e - T ds - \dfrac{P}{\rho^2} d\rho - \dfrac{\mu_k}{m_k} d w_k \right] \ ,$$

  and thus

   $$de = T ds + \dfrac{P}{\rho^2} d \rho + \dfrac{\mu_k}{m_k} d w_k\ .$$

- Single-component solid 

   $$\text{\textbf{todo}}$$


#### First principle per unit volume

All the extensive quantites are written as the product of the mass of the system $M$ and its density, namely

$$E = V  \mathcal{E} \quad , \quad S = M  \mathcal{S} \quad , \quad \mathbf{X} = M \symbf{\chi} \ ,$$

and, using the product rule for differential $d E = d (V \mathcal{E}) = dV \, \mathcal{E} + V \, d\mathcal{E}$, first principle can be written as

$$0 = d V \underbrace{\left( \mathcal{E} - T \mathcal{S} - \mathbf{F} \cdot \symbf{\chi} \right)}_{= 0} + V \left( d \mathcal{E} - T d \mathcal{S} - \mathbf{F} \cdot d \symbf{\chi} \right) \ .$$

The first term is identically zero, since it's the expression of the internal energy divided by $V$. Being $V > 0$, the second term gives the first principle per unit volume

$$d \mathcal{E} = T d\mathcal{S} + \mathbf{F} \cdot d \symbf{\chi} \ .$$


##### Different systems

- Single-component fluid; 

   $$V = V \cdot 1 \quad , \quad N = V \dfrac{M}{V} \dfrac{1}{m} = V \dfrac{\rho}{m} \ , $$

   being $\rho$ the mass density and $m$ the mass of a particle (or mole, it depends on the description) of the medium; $m$ is **constant**. First principle becomes

   $$0 = d V \underbrace{\left( \mathcal{E} - T \mathcal{S} + P - \mu \dfrac{\rho}{m} \right)}_{= 0} + V \left( d \mathcal{E} - T d\mathcal{S} + 0 - \frac{\mu}{m} \, d \rho  \right) \ ,$$

  and thus

   $$d \mathcal{E} = T d \mathcal{S} + \dfrac{\mu}{m} d \rho \ .$$

   This latter formulation is consistent with the principle per unit mass. Volume density can be written as the product of mass density and the mass density of the physical quantity of interest, namely $\mathcal{E} = \rho e$

  $$\begin{aligned}
    0 & = - d( \rho e ) + T d (\rho s) + \frac{\mu}{m} d \rho = \\
      & = d \rho \left( - e + T s + \frac{\mu}{m} \right) - \rho \left( d e + T d s \right) = \\
      & = d \rho \underbrace{\left( - e - \dfrac{P}{\rho} + T s + \frac{\mu}{m} \right)}_{\text{def. of $e$}} + \rho \underbrace{\left( - d e + \dfrac{P}{\rho^2} d \rho + T d s \right)}_{1^{st} \text{ pr. per unit mass}} \ .
  \end{aligned}$$

- Multi-component fluid

   $$\text{\textbf{todo}}$$

- Single-component solid 

   $$\text{\textbf{todo}}$$


## Potentials - specific quantities

Here mechanical $\mathbf{X}_m$ and non-mechanical $\mathbf{X}_n$ generalized forces and displacements are recognized to define enthaply and Gibbs' free energy later.

$$e(s, \mathbf{x}) = e \left( \frac{S}{M}, \frac{\mathbf{X}}{M} \right) = \frac{1}{M} E\left( \frac{S}{M}, \frac{\mathbf{X}}{M} \right) \qquad \text{\textbf{todo check}} $$

**Internal energy, $e(s, \mathbf{x})$.**

$$d e = T ds + \mathbf{F} \cdot d \mathbf{x}$$

**Helmholtz free energy, $f(T, \mathbf{x}) = e - T s$.**

$$\begin{aligned}
  d f 
  & = de - T d s - s d T= \\
  & =- s d T + \mathbf{F} \cdot d \mathbf{x} \ .
\end{aligned}$$

**Enthaply, $h(T, \mathbf{F}_m, \mathbf{x}_n) = e - \mathbf{F}_m \cdot \mathbf{x}_m$.**

$$\begin{aligned}
  d h 
  & = de - d \mathbf{F}_m \cdot \mathbf{x}_m - \mathbf{F}_m \cdot d \mathbf{x}_m = \\
  & = T d s - \mathbf{x}_m \cdot d \mathbf{F}_m + \mathbf{F}_n \cdot d \mathbf{x}_n \ .
\end{aligned}$$

**Gibbs' free energy, $g(T, \mathbf{F}_m, \mathbf{x}_n) = h - T s = e - \mathbf{F}_m \cdot \mathbf{x}_m - T s = f - \mathbf{F}_m \cdot \mathbf{x}_m = \mathbf{F}_n \cdot \mathbf{x}_n$.**

$$\begin{aligned}
  d g 
  & = dh - T ds - s dT = \\
  & = - s  dT - \mathbf{x}_m \cdot d \mathbf{F}_m + \mathbf{F}_n \cdot d \mathbf{x}_n = \\
  & = \mathbf{x}_n \cdot d \mathbf{F}_n + \mathbf{F}_n \cdot d \mathbf{x}_n \ .
\end{aligned}$$



**Partial derivatives of potentials.**

$$\begin{aligned}
 T & = \quad \left.\frac{\partial e}{\partial s}\right|_{\mathbf{x}} && = \quad \left.\frac{\partial h}{\partial s}\right|_{\mathbf{F}_m,\mathbf{x}_n} \\
 s & =     - \left.\frac{\partial f}{\partial T}\right|_{\mathbf{x}} && =     - \left.\frac{\partial g}{\partial T}\right|_{\mathbf{F}_m,\mathbf{x}_n} \\
 \mathbf{F}_m & = \quad \left.\frac{\partial e}{\partial \mathbf{x}_m}\right|_{s,\mathbf{x}_n} && = \quad \left.\frac{\partial f}{\partial \mathbf{x}_m}\right|_{T,\mathbf{x}_n} \\
 \mathbf{F}_n & = \quad  \left.\frac{\partial e}{\partial \mathbf{x}_n}\right|_{s,\mathbf{x}_m} && = \quad \left.\frac{\partial f}{\partial \mathbf{x}_n}\right|_{T,\mathbf{x}_m} && = \quad  \left.\frac{\partial h}{\partial \mathbf{x}_n}\right|_{s,\mathbf{F}_m} && = \quad \left.\frac{\partial g}{\partial \mathbf{x}_n}\right|_{T,\mathbf{F}_m} \\
 \mathbf{x}_m & = -\left.\frac{\partial h}{\partial \mathbf{F}_m}\right|_{s,\mathbf{x}_n} && =- \left.\frac{\partial g}{\partial \mathbf{F}_m}\right|_{T,\mathbf{x}_n}\\
\end{aligned}$$


**Maxwell's relations.**

$$\begin{aligned}
 \left.\dfrac{\partial T}{\partial x_k}\right|_{s, x_{j \ne k}}    & = \ \ \left.\dfrac{\partial F_i}{\partial s}\right|_{x_k} && \qquad
 \left.\dfrac{\partial F_i}{\partial x_k}\right|_{s, x_{j \ne k}}  & = \ \ \left.\dfrac{\partial F_k}{\partial x_i}\right|_{s, x_{j \ne i}} \\
-\left.\dfrac{\partial s}{\partial x_i}\right|_{T} & = \ \ \left.\dfrac{\partial F_k}{\partial T}\right|_{x_k} && \qquad
 \left.\dfrac{\partial F_i}{\partial x_k}\right|_{T, x_{j \ne k}}  & = \ \ \left.\dfrac{\partial F_k}{\partial x_i}\right|_{T, x_{j \ne i}} \\
 \left.\dfrac{\partial T}{\partial F_i}\right|_{} & = \ \ \left.\dfrac{\partial x_i}{\partial S}\right|_{} && \qquad
 \left.\dfrac{\partial F_i}{\partial x_k}\right|_{s, x_{j \ne k}}  & = \ \ \left.\dfrac{\partial F_k}{\partial x_i}\right|_{s, x_{j \ne i}} \\
 \left.\dfrac{\partial S}{\partial F_i}\right|_{} & = \ \ \left.\dfrac{\partial x_i}{\partial T}\right|_{} && \qquad
 \left.\dfrac{\partial F_i}{\partial x_k}\right|_{s, x_{j \ne k}}  & = \ \ \left.\dfrac{\partial F_k}{\partial x_i}\right|_{s, x_{j \ne i}} \\
\end{aligned}$$

e

$$\begin{cases}
 \dfrac{\partial F_i}{\partial x_j} & =  \dfrac{\partial F_j}{\partial x_i} \\
 \dfrac{\partial x_i}{\partial F_j} & =  \dfrac{\partial x_j}{\partial F_i} \\
\end{cases}$$


<!--
**Derivate parziali dei potenziali come definizione di variabili termodinamiche.** Osservando i differenziali dei potenziali termodinamici, si possono riconoscere che le variabili termodinamiche $T$, $S$, $\mathbf{F}$, $\mathbf{x}$ possono essere scritte come derivate parziali dei potenziali termodinamici,

$$\begin{aligned}
 T & = \quad \frac{\partial E}{\partial S}\Big|_{\mathbf{x}} & = \quad \frac{\partial H}{\partial S}\Big|_{\mathbf{F}} \\
 S & =     - \frac{\partial F}{\partial T}\Big|_{\mathbf{x}} & =     - \frac{\partial G}{\partial T}\Big|_{\mathbf{F}} \\
 \mathbf{F} & =     - \frac{\partial E}{\partial \mathbf{x}}\Big|_{S} & = - \frac{\partial F}{\partial \mathbf{x}}\Big|_{T} \\
 \mathbf{x} & = \quad \frac{\partial H}{\partial \mathbf{F}}\Big|_{S} & = \quad \frac{\partial G}{\partial \mathbf{F}}\Big|_{T}\\
\end{aligned}$$


**Relazioni di Maxwell.** Applicando il **teorema di Schwarz** sulle derivate miste ai potenziali termodinamici, si ricavano le relazioni di Maxwell,

$$\begin{cases}
 \dfrac{\partial T}{\partial x_i} & =   - \dfrac{\partial F_i}{\partial S} \\
 \dfrac{\partial S}{\partial x_i} & = \ \ \dfrac{\partial F_i}{\partial T} \\
 \dfrac{\partial T}{\partial F_i} & = \ \ \dfrac{\partial x_i}{\partial S} \\
 \dfrac{\partial S}{\partial F_i} & =   - \dfrac{\partial x_i}{\partial T} \\
\end{cases}$$

e

$$\begin{cases}
 \dfrac{\partial F_i}{\partial x_j} & =  \dfrac{\partial F_j}{\partial x_i} \\
 \dfrac{\partial x_i}{\partial F_j} & =  \dfrac{\partial x_j}{\partial F_i} \\
\end{cases}$$
-->
