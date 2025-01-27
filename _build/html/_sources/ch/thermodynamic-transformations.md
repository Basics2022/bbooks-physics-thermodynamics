<!--
```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```
-->

(classical-thermodynamics:transformations)=
# Thermodynamic transformations and thermomechanical systems


(classical-thermodynamics:transformations:turbine)=
## Turbine

[Integral balance equations](https://basics2022.github.io/bbooks-physics-continuum-mechanics/ch/continuum/balance-primary-integral.html#integral-balance-equations-for-arbitrary-domains-arbitrary-description) for the operating fluid in the inner volume $v_t$ of a turbine read

$$\begin{cases}
  \dfrac{d}{dt} \displaystyle\int_{v_t} \rho + \oint_{\partial v_t} \rho ( \vec{u} - \vec{u}_b ) \cdot \hat{n} = 0  \\
  \dfrac{d}{dt} \displaystyle\int_{v_t} \rho \vec{u} + \oint_{\partial v_t} \rho \vec{u} ( \vec{u} - \vec{u}_b ) \cdot \hat{n} = \int_{v_t} \rho \vec{g} + \oint_{\partial v_t} \vec{t}_{\hat{n}}  \\
  \dfrac{d}{dt} \displaystyle\int_{v_t} \rho \vec{r} \times \vec{u} + \dots \\
  \dfrac{d}{dt} \displaystyle\int_{v_t} \rho e^t + \oint_{\partial v_t} \rho e^t ( \vec{u} - \vec{u}_b ) \cdot \hat{n} = \int_{v_t} \rho \vec{g} \cdot \vec{u} + \oint_{\partial v_t} \vec{t}_{\hat{n}} \cdot \vec{u} - \oint_{\partial v_t} \vec{q} \cdot \hat{n} + \int_{v_t} \rho r \ .
\end{cases}$$

For a Newtoninan fluid, stress vector can be written as the sum of a pressure and viscous contribution,

$$\vec{t}_{\hat{n}} = - p \hat{n} + \vec{s}_{\hat{n}} \ .$$

The boundary of the geometrical domain $\partial v_t$ can be represented as the union of the intake manifold $s_{in}$, exhaust manifold $s_{out}$, the steady solid boundary $s_{sta}$ (stator,...), and rotatin solid boundary $s_{rot}$ (rotor), here neglecting fuel intake (it can be considered as well, nothing changes radically). There's no mass flux thourgh solid walls, i.e. $(\vec{u}-\vec{u}_b) \cdot \hat{n}|_{s_{sta}, s_{rot}} = 0$. As a first approximation, volume force is considered negligible, $\vec{g} = \vec{0}$, heat transfer is considered negligible as well, $\vec{q} = \vec{0}$, $r = 0$ (and thus material particles undergo adiabatic transformations), and viscous stress is considered negligible at inflow and outflow, $\vec{s}_{\hat{n}}|_{s_{in}, s_{out}} = \vec{0}$, or $\vec{t}_{\hat{n}}|_{s_{in}, s_{out}} = - p \hat{n}|_{s_{in}, s_{out}}$. With all these assumptions, and further assuming steady regime $\frac{d}{dt} \equiv 0$, mass and total energy balance equations become

$$\begin{cases}
  \displaystyle\int_{s_{in}} \rho ( \vec{v} - \vec{v}_b ) \cdot \hat{n} + \int_{s_{in}} \rho ( \vec{v} - \vec{v}_b ) \cdot \hat{n} = 0 \\ 
  \displaystyle\int_{s_{in}} \rho e^t ( \vec{u} - \vec{u}_b ) \cdot \hat{n} + \int_{s_{out}} \rho e^t ( \vec{u} - \vec{u}_b ) \cdot \hat{n} = - \int_{s_{in}} p \hat{n} \cdot \vec{v} - \int_{s_{out}} p \hat{n} \cdot \vec{v} + \int_{s_{rot}} \vec{t}_{\hat{n}} \cdot \vec{v} \ .
\end{cases}$$

Mass balance equation reduces to equality of inflow and outflow mass flux: mass is not created or destroyed in classical mechanics, and can't accumulate in the volume in steady conditions. If $\vec{v}_b \cdot \hat{n} = 0$ (or other conditions to make the following manipulation of the total energy equation), total energy equation can be written in terms of fluxes of total enthaply $h^t := e^t + \frac{P}{\rho}$,

$$  \displaystyle\int_{s_{in}} \rho h^t \vec{u} \cdot \hat{n} + \int_{s_{out}} \rho e^t ( \vec{u} - \vec{u}_b ) \cdot \hat{n} = \int_{s_{rot}} \vec{t}_{\hat{n}} \cdot \vec{v} \ ,
$$

i.e. the **total power done on the fluid by the turbine**[^turbine-power], $\int_{s_{rot}} \vec{t}_{\hat{n}} \cdot \hat{n}$,


[^turbine-power]: This contribution is the total power done by the turbine on the fluid, being the integral over the moving interface between the media of the dot product of the velocity of the material points and the stress acting *on the fluid*. Total power transferred from the turbine to the fluid could be written as the integral over the whole interface surface, namely $s_{sta} \cup s_{rot}$, but the power contribution of the stator is identically zero, being $\vec{v}|_{s_{sta}} = \vec{0}$.


(classical-thermodynamics:transformations:compressor)=
## Compressor




