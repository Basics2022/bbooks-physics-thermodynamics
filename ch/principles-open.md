(physics-hs:thermodynamics:foundation:principles:open)=
# Open Systems

In general, the balance equation for a physical quantity in an open system is derived from the balance of the same physical quantity for a closed system, adding the contribution of the flux terms of the desired physical quantity through the system's boundary. Thus, if the balance of the physical quantity $F$ for the closed system within volume $V_t$ can be written as

$$\dfrac{d}{dt} F_{V_t} = R^e_{V_t} \ ,$$

the balance of the same physical quantity for an open system identified by the (geometric) volume $v_t$ can be written as

$$\frac{d}{dt} F_{v_t} = R^e_{v_t} - \Phi_{\partial v_t}(f) \ , $$

where $f$ is defined as the specific quantity of $F$ per unit mass. The flux term through the boundary $\partial v_t$ can be written as the sum of the flux contributions through portions $s_{k,t}$ of the surface $\partial v_t = \cup_k s_{k,t}$,

$$\Phi_{\partial v_t}(f) = \sum_{s_{k,t}} \dot{m}_k \, f_k \ ,$$

where $\dot{m}_k = \rho_k vi^{rel}_{n,k}$ is the mass flux through the surface $s_{k,t}$, and it is assumed that the quantity $f_k$ is constant over the surface $s_{k,t}$, or that the average value over the surface has been considered.

```{note}
In case the quantity $f$ is not uniform over the domain boundary and varies continuously, the flux term can be written as the summation of infinite terms through surfaces whose area tends to zero, via a surface integral, following the definition of a Riemann integral.
```

```{note}
A balance equation of a physical quantity for an open system also includes the balance equation of the same physical quantity for a closed system as a special case where the mass flux through the domain boundary is zero, $\dot{m}_k = 0$.
```

Here, we consider the balances (integrals, global of a system) of some fundamental physical quantities in classical mechanics: mass, momentum, angular momentum, and total energy.

## Mass Balance
The mass balance, $F = M$, $f = 1$, for an open system is

$$\frac{d}{dt} M_{v_t} = - \sum_k \dot{m}_k$$

## Momentum Balance

<span style="color:red"> **todo** *reference to or from classical mechanics*</span>

## Angular Momentum Balance

<span style="color:red"> **todo** *reference to or from classical mechanics*</span>

## Total Energy Balance
The total energy balance $F = E^{tot} = E + K$, $f = e^{tot} = e + \frac{|\vec{v}|^2}{2}$,

$$\frac{d}{dt} E^{tot}_{v_t} = P^{ext}_{v_t}  + \dot{Q}^{ext}_{v_t}  - \sum_k \dot{m}_k \, e^{tot}_k \ .$$

The power of external actions $P^{ext}_{v_t}$ can be written as the sum of contributions on the surfaces of the system's boundary through which there is mass flow, and impermeable surfaces that can be used to extract work from the system. If the effects of viscous stresses on the surfaces through which there is mass flow can be neglected, the power of the actions on the system can be written as

$$\begin{aligned}
  P^{ext} & = P^{ext,mech} + P^{ext,\Phi} = \\
          & = P^{ext,mech} - \sum_{k} \dot{m}_k \frac{P_k}{\rho_k} \ , 
\end{aligned}$$

and the total energy balance of the system becomes

$$\dfrac{d}{dt} E^{tot}_{v_t} = P^{ext,mech}_{v_t} + \dot{Q}^{ext} - \sum_k \dot{m}_k h^{tot}_k \ ,$$

where the specific total enthalpy is defined as $h^{tot} = e^{tot} + \frac{P}{\rho} = e + \frac{P}{\rho} + \frac{|\vec{v}|^2}{2}$.

```{prf:example} Turbine
:label: thermodynamics:principles:open:ex:turbine
```
```{prf:example} Compressor
:label: thermodynamics:principles:open:ex:compressor
```
```{prf:example} Combustion Chamber
:label: thermodynamics:principles:open:ex:comb-chamber
```

