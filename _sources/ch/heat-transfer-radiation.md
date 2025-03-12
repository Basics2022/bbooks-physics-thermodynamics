(classical-thermodynamics:heat-transmission:radiation)=
# Radiation

<span style="color:red">check all the nomenclature/definition</span>

(classical-thermodynamics:heat-transmission:radiation:planck)=
## Planck's law

```{prf:definition} Black-body

```

**Spectral energy density** for black-body radiation

$$u_{f}(f, T) = \frac{8 \pi h f^3}{c^3} \frac{1}{e^{\frac{hf}{k_B T}} - 1}$$

Spectral energy density has the physical dimension $\frac{\text{Energy}}{\text{Volume} \times \text{Frequency}}$

**Spectral radiance** reads[^spectral-radiance] $B_f = \frac{1}{4 \pi} u_f(f,T) c$ and thus for a black-body

$$B_{f}(f, T) = \frac{2 h f^3}{c^2}\frac{1}{e^{\frac{hf}{k_B T}} - 1} \ .$$

It has physical dimension $\frac{\text{Energy}}{\text{Volume} \times \text{Frequency}} \times \text{Velocity} = \frac{\text{Power}}{\text{Area} \times \text{Frequency}}$.

[^spectral-radiance]: Show how to get this expression from the spectral energy density.

(classical-thermodynamics:heat-transmission:radiation:wien)=
## Wien's law

Wien's law states that the maximum of the spectral energy is obtained at a frequency $f^*$, whose value is proportional with the temperature of the body.

$$f^* = x^* \frac{k_B}{h} T \simeq 2.82  \frac{k_B}{h} T \ ,$$

where $x^* \simeq 2.82$ is the solution of the algebraic equation $3(1-e^x)-x=0$.

```{dropdown} Proof of Wien's law

From direct evaluation of the derivative of the spectral radiance as a function of $f$,

$$\begin{aligned}
  \partial_f B_{f}(f,T)
  & = \frac{2 h}{c^2} \left[ 3 f^2 \frac{1}{e^{\frac{hf}{k_B T}}-1} + f^3 \left(-\frac{\frac{h}{k_B T} e^{\frac{hf}{k_B T}}}{\left( e^{\frac{hf}{k_B T}} - 1 \right)^2}  \right) \right] = \\
  & = \frac{2 h f^2 e^{\frac{hf}{k_B T}}}{c^2 \left( e^{\frac{hf}{k_B T}} - 1 \right)^2} \left[ 3 \left( 1 - e^{-\frac{hf}{k_B T}} \right) - \frac{h f}{k_B T}  \right] \ .
\end{aligned}$$

Now, if $\partial_f B_{f}(f,T) = 0$ the frequency is either $f = 0$, or the solution of the nonlinear algebraic equation

$$0 = 3 \left(1 - e^{-\frac{h f}{k_B T}} \right) - \frac{hf}{k_B T} \ .$$

Defining $x := \frac{h f}{k_B T}$, this equation becomes

$$0 = 3 (1 - e^x) - x \ ,$$

whose solution $x^* \approx 2.82$ can be easily evaluated with an iterative method (or expressed in term of the Lambert's function $W$, so loved at Stanford and on Youtube: they'd probaly like to look at tabulated values, or pose). Once the solution $x^*$ of this non-dimensional equation is found, the frequency where maximum energy density occurs reads

$$f^* = \frac{k_B T}{h} x^* \simeq 2.82 \frac{k_B}{h} T \ .$$

```

(classical-thermodynamics:heat-transmission:radiation:energy-transfer)=
## Energy transfer by radiation

A list of physical quantities used to describe a radiation process follows.

- **Radiant flux**, $\Phi_e$. Physical dimension: $\text{W}$
- **Radiant intensity** $I_{e, \Omega}$ is the radiant flux per unit solid angle $\Omega$. Physical dimension: $\frac{\text{W}}{\text{sr}}$
- **Spectral radiant intensity** $I_{e, \Omega, f}$ is the radiant flux per unit solid angle per frequency of the radiation: $\frac{\text{W}}{\text{sr} \, \text{Hz}}$
- **Radiant exitance**, $M_e$ is the flux across an emispherical receiver surface, per unit surface of the source. Physical dimension $\frac{\text{W}}{\text{Area}}$

```{prf:definition} Lambert medium

A Lambert medium is defined as a medium that follows **Lambert cosine law**,

$$I_{1}(\vec{r}_{12}, \hat{n}_1) = I_{1,0} \, \hat{r}_{12} \cdot \hat{n}_1 \ ,$$

with $\vec{r}_{12} = \vec{r}_2 - \vec{r}_1$.

```

Elementary power flux of the radiation emitted by a source in $1$ through a solid angle $d \Omega_{21}$, as seen from $1$, reads

$$\begin{aligned}
  d P_{1 \rightarrow 2}
  & = I_{1}(\vec{r}_{12}, \hat{n}_1) \, d \Omega_{2/1} \\
\end{aligned}$$

The solid angle $d \Omega_{21}$ of a surface $d S_2$ as seen from a point in $\vec{r}_1$ is $d \Omega_{21} = \frac{\hat{n}_2 \cdot \vec{r}_{12}}{|\vec{r}_{12}|^3} \, dS_2$. From the expression of the elementary power flux,

$$
 d P_{1 \rightarrow 2} = I_{1}(\vec{r}_{12}, \hat{n}_1) \, \frac{\vec{r}_{12} }{|\vec{r}_{12}|^3} \cdot \hat{n}_2 \, dS_2 = \vec{s}_{12} \cdot \hat{n}_2 \, dS_2 \ ,
$$

it's possible to find the expression of the power flux density vector 

$$\vec{s}_{12} = I_{12} \frac{\vec{r}_{12}}{|\vec{r}_{12}|^3} \ .$$

For a Lambert medium then

$$\begin{aligned}
 d P_{1 \rightarrow 2}
 & = I_{1}(\vec{r}_{12}, \hat{n}_1) \, \frac{\vec{r}_{12} }{|\vec{r}_{12}|^3} \cdot \hat{n}_2 \, dS_2 = \\
 & = I_{0,1} \frac{\vec{r}_{12}}{|\vec{r}_{12}|} \cdot \hat{n}_1 \, \frac{\vec{r}_{12} }{|\vec{r}_{12}|^3} \cdot \hat{n}_2 \, dS_2 \ .
\end{aligned}$$ (power-flux:radiant-intensity)


(classical-thermodynamics:heat-transmission:radiation:stefan-boltzmann)=
### Stefan-Boltzmann law

The **radiant exitance**, $M_e^\circ$, - i.e. the total power through an emisphere emitted by a source, per unit area of the source - of a black body at temperature $T_1$ is

$$M_e^\circ = \sigma T_1^4 \ ,$$

with the **Stefan-Boltzmann constant**, $\sigma = 5.67 \cdot 10^{-8} \frac{\text{W}}{\text{m}^2 \text{K}^4}$.

```{dropdown} Total radiation and Stefan-Boltzmann constant $\ \sigma$

Integration over frequency $f \in [0, +\infty]$, and over an emisphere receiver surface (or better, over the equivalent solid angle) for a Lambert medium provide the **radiant exitance**

$$\begin{aligned}
  M_{e}^\circ = M_{1,2^{emisphere}}
  & = \frac{d P_{1 \rightarrow 2}}{d S_1} = \\
  & = \int_{f=0}^{+\infty} \int_{\Omega_{emisphere}} I_{1,0}(f) \cos \theta_{12} \, df \, d\Omega_{2/1} = \\
  & = \int_{f=0}^{+\infty}I_{1,0}(f) \, df \, \int_{\phi = 0}^{2\pi} \int_{\theta=0}^{\pi_2} \cos \theta \sin \theta \, d \theta \, d\phi \ ,
\end{aligned}$$

with the solid angle with spherical coordinates, $d\Omega_{2/1} = \sin \theta \, d \theta \, d\phi$. The geometric integral gives

$$
  \int_{\phi = 0}^{2\pi} \int_{\theta=0}^{\pi_2} \cos \theta_{} \, d \theta \, d\phi = \pi \ .
$$

For a black-body the integral over frequency gives

$$\begin{aligned}
  \int_{f = 0}^{+\infty} I_{1,0}(f) \, df
  & = \int_{f=0}^{+\infty} \frac{2 h f^3}{c^2} \frac{1}{e^{\frac{hf}{k_B T}}-1} \, df \\
  & = T^4 \frac{2 h}{c^2} \left(\frac{k_B}{h}\right)^4 \int_{u=0}^{+\infty} \frac{u^3}{e^u-1} \, du =: T^4 \frac{\sigma}{\pi} \ ,
\end{aligned}$$

i.e. it's proportional to $T^4$ with a constant of proportionality built on constants of nature, speed of light $c$, Boltzmann constant $k_B$, and Planck constant $h$. The integral is non-dimensional and its value[^stefan-boltzmann-integral] is $\frac{\pi^4}{15}$. **Stefan-Boltzmann constant** $\sigma$ is then defined as

$$\sigma := \pi \cdot \frac{2 h}{c^2} \left( \frac{k_B}{h} \right)^4 \int_{u=0}^{+\infty} \frac{u^3}{e^{u}-1} du = \frac{2 \pi^5}{15}\frac{k_B^4}{c^2 h^3} = 5.67 \cdot 10^{-8} \frac{\text{W}}{\text{m}^2 \text{K}^4} \ .$$

[^stefan-boltzmann-integral]: **todo** Evaluate it
```

Integration over a generic surface $S_2$ of the power flux emitted by a source $1$ per unit surface of the source gives

$$\begin{aligned}
  M_{12} = \frac{d P_{1 \rightarrow 2} }{d S_1} = T_1^4 \, \frac{\sigma}{\pi} \int_{S_2} \hat{n}_1 \cdot \frac{\vec{r}_{12}}{|\vec{r}_{12}|} \, \frac{\vec{r}_{12}}{|\vec{r}_{12}|^3} \cdot \hat{n}_2 \, dS_2
\end{aligned}$$

Thus the elementary power per unit surface of the source $1$ and the receiver $2$ is

$$dP_{1 \rightarrow 2} = T_1^4 \, \frac{\sigma}{\pi} \, \hat{n}_1 \cdot \frac{\vec{r}_{12}}{|\vec{r}_{12}|} \, \frac{\vec{r}_{12}}{|\vec{r}_{12}|^3} \cdot \hat{n}_2 \, dS_1 \, dS_2 $$

Comparing this expression of the power flux from source $1$ to the elementary surface $d S_2$ with the expression {eq}`power-flux:radiant-intensity` using the radiant intensity $I_{0,1}$, it immediately follows that the elementary radiant intensity $d I_{0,1}$ of the elementary surface $d S_1$ of the source reads

$$d I_{0,1} = T_1^4 \, \frac{\sigma}{\pi} \, d S_1 \ .$$

(classical-thermodynamics:heat-transmission:radiation:stefan-boltzmann:geometry)=
#### Geometry effects on radiation

The elementary power is the product of $\frac{\sigma T_1^4}{\pi}$ and a factor depending only on the geometry of the problem,

$$d G_{12} := \hat{n}_1 \cdot \frac{\vec{r}_{12}}{|\vec{r}_{12}|} \, \frac{\vec{r}_{12}}{|\vec{r}_{12}|^3} \cdot \hat{n}_2 \, dS_1 \, dS_2 \ .$$

This factor is **symmetric**, i.e. inverting the roles of the source and the receiver is irrelevant. Letting $G_{12} = \int_{S_1} \int_{S_2} dG_{12}$, if the source surface $1$ has uniform temperature $T_1$ and the receiver surface has uniform temperature $T_2$, (and assuming [emissvity](classical-thermodynamics:heat-transmission:radiation:emittivity) $\varepsilon = 1$, for black-bodies) thus the power fluxes from $1$ to $2$ and from $2$ to $1$ read

$$\begin{aligned}
  P_{1 \rightarrow 2} & = T_1^4 \frac{\sigma}{\pi} G_{12} \\
  P_{2 \rightarrow 1} & = T_2^4 \frac{\sigma}{\pi} G_{12} \ .
\end{aligned}$$

Thus the net power into surfaces $1$ and $2$ are

$$\begin{aligned}
  P_{\rightarrow 1} & = P_{2 \rightarrow 1} - P_{1 \rightarrow 2} \\
  P_{\rightarrow 2} & = P_{1 \rightarrow 2} - P_{2 \rightarrow 1} \ ,
\end{aligned}$$

so that $P_{\rightarrow 1} + P_{\rightarrow 2} = 0$.

In the limit of **small surfaces compared with their distance**, an approximate expression of the integral $\int_{S_1} \int_{S_2} d G$ allows to write the power transmitted by radiation from surface $1$ to surface $2$ as

$$\begin{aligned}
  P_{1 \rightarrow 2} = \frac{\sigma T_1^4}{\pi} G_{12} 
    = \frac{\sigma T_1^4}{\pi} A_{1, \perp \vec{r}_{12}} \Omega_{2/1}
    = \frac{\sigma T_1^4}{\pi} A_{2, \perp \vec{r}_{12}} \Omega_{1/2}
\end{aligned}$$

i.e. as the product of the radiant ... **todo** *find the right term* $\frac{\sigma T_1^4}{\pi}$, the projection of the surface $S_{1}$ in a plane orthogonal to the distance vector $\vec{r}_{12}$ and the solid angle $\Omega_{2/1}$ of the surface $2$ as seen by surface $1$, or viceversa.

```{dropdown} Proof of the small surface limit


```

(classical-thermodynamics:heat-transmission:radiation:emittivity)=
### Emissivity and coefficient of absorption

The radiation emission of a generic body differs from the radiation of a black-body. Its emittance can be written comparing its emission with that of of a black body. In general, the emission could differ as a function of the frequency of the radiation and the direction of the radiation.

...

If there's no dependence on $f$ and $\hat{r}$ - or taking the average values, neglecting the dependence on $f$ and $\hat{r}$ if using the average coefficient - the radiant exitance is

$$M_1 = \varepsilon_1 \sigma T_1^4 \ .$$

Reflection coefficient $r$ and absorbtion (or transmission) coefficient $a$ are then defined as the reflected and absorbed ratios of the incident radiation. Given incident radiation with power $P_i$, power of reflected and absorbed radiation reads

$$P_r = r \, P_i \quad , \quad P_a = a \, P_i \ .$$

and for "power balance", the sum of absorbed and reflected power must be equal to the incident power

$$P_i = P_r + P_a \ ,$$

and thus the coefficients must satistfy the following relation **check** *check the definition of the coefficients, if they should take into account the emission...*

$$1 = r + a \ .$$


```{prf:example} Energy exchange in isolated systems and relations between coefficients - **todo** **check**
:class: dropdown

Radiation transmission is assumed to be instantaneous here: this assumption holds for bodies close enough for the time $\Delta t = \frac{d_{12}}{c}$ to be small enough to be treated as zero.

A system composed of two bodies. Energy balance of a body immediately follows the first principle of thermodynamics: time derivative of energy of a system equals the net power done on the system. Here the net power equals the difference between the absorbed incoming power and the emitted power,

$$\begin{cases} 
  \dot{E}_1 = P^a_{\rightarrow 1} - P_1^e \\
  \dot{E}_2 = P^a_{\rightarrow 2} - P_2^e
\end{cases}$$

**Incoming power.** The incoming power is due to the power emitted and reflected by the other body,

$$\begin{cases}
  P_{\rightarrow 1} = P_{2}^e + r_2 P_{\rightarrow 2} \\
  P_{\rightarrow 2} = P_{1}^e + r_1 P_{\rightarrow 1} 
\end{cases}$$

From these two relations, the incoming powers can be explitly written as function of the emitted powers,

$$\begin{cases}
  P_{\rightarrow 1} = \dfrac{P_2^e + r_2 P_1^e}{1 - r_1 r_2} \\
  P_{\rightarrow 2} = \dfrac{P_1^e + r_1 P_2^e}{1 - r_1 r_2}
\end{cases}$$

**Energy balance of the system.** Energy of an isolated system is constant and thus the dime derivative of the energy is zero,

$$\begin{aligned}
  0
  & = \dot{E} = \dot{E}_1 + \dot{E}_2 = \\
  & = a_1 \dfrac{P_2^e + r_2 P_1^e}{1 - r_1 r_2} - P_1^e + a_2 \dfrac{P_1^e + r_1 P_2^e}{1 - r_1 r_2} - P_2^e = \\ 
  & = P_1 \frac{a_2 + a_1 r_2 - 1 + r_1 r_2}{1 - r_1 r_2} + P_2 \frac{a_1 + a_2 r_1 - 1 + r_1 r_2}{1 - r_1 r_2} \\ 
  & = T_1^4 \sigma \varepsilon_1 \frac{a_2 + a_1 r_2 - 1 + r_1 r_2}{1 - r_1 r_2} + T_2^4 \sigma \varepsilon_2 \frac{a_1 + a_2 r_1 - 1 + r_1 r_2}{1 - r_1 r_2} \ . 
\end{aligned}$$

If this relation must hold in any condition, for any value of the emitted powers and for any independent choice of the materials of the bodies, the coefficients must be zero

$$\begin{cases}
  a_2 + a_1 r_2 - 1 + r_1 r_2 = 0 \\
  a_1 + a_2 r_1 - 1 + r_1 r_2 = 0 \\
\end{cases}$$

Subtracting,

$$a_2 (1 - r_1) = a_1 (1 - r_2) \ ,$$

and, since the relation must hold for any choice of pair of materials, the relation $a_1 = 1 - r_1$ is found again.

**Bodies in thermal equlibrium.** If each body is in thermal equilibrium,

$$\begin{cases}
  0 = \dfrac{P_2^e + r_2 P^{e}_1}{ 1 - r_1 r_2} - P_1^e = \sigma G_{12} \dfrac{ \varepsilon_2 T_2^4 + ( r_2 - 1 + r_1 r_2 ) \varepsilon_1 T_1^4 }{ 1 - r_1 r_2 } \\
  0 = \dfrac{P_1^e + r_1 P^{e}_2}{ 1 - r_1 r_2} - P_2^e = \sigma G_{12} \dfrac{ \varepsilon_1 T_1^4 + ( r_1 - 1 + r_1 r_2 ) \varepsilon_2 T_2^4 }{ 1 - r_1 r_2 } \\
\end{cases}$$

```


#### Kirchhoff's law

For systems in thermodynamic equilibrium,...
- constant ratio of...
- $\alpha = \varepsilon$? for a system in thermal equilibrium **only**



