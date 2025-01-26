<!--
```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```
-->

(classical-thermodynamics:coefficients)=
# Thermodynamic coefficients

In this section different related to first derivatives of thermodynamic state variables are introduced and discussed for different systems.

## Thermodynamic coefficients of a single-component fluid

For a 1-component fluid with constant composition, the first principle reads

$$de = T ds - P dv = T ds + \frac{P}{\rho^2} d \rho \ .$$

**Heat capacity.**

$$c_x := T \dfrac{\partial s}{\partial T}\Big|_x$$

For fluid systems, usually heat capacity at constant pressure or constant density are the most used.

**Thermal expansion coefficients.**

$$\alpha_x := \dfrac{1}{v} \dfrac{\partial v}{\partial T}\Big|_x = - \dfrac{1}{\rho} \dfrac{\partial \rho}{\partial T}\Big|_x$$

For fluid systems, usually thermal expansion coefficent at constant pressure is the most used.

**Compressibility coefficients.**

$$\beta_x := - \dfrac{1}{v} \dfrac{\partial v}{\partial P}\Big|_x = \dfrac{1}{\rho} \dfrac{\partial \rho}{\partial P}\Big|_x$$

For fluid systems, usually compressibility coefficent at constant temperature or entropy are the most used.


## Thermodynamic equilibrium

Here thermodynamic equilibrium is discussed for a single-component fluid, for which the first principle reads

$$d e = T ds - P dv = T ds + \frac{P}{\rho^2} d \rho \ .$$

First conditions on energy, $e(s, \rho)$, as a function of entropy and density then the equivalent conditions on entropy $s(e, \rho)$, as a function of energy and density are discussed.

### Conditions on energy

Thermodynamic equilibrium implies conditions on the second order term in series expansion of the function $e(s, \rho)$ (**todo** *why? Spend few words. Use Landau as a reference if needed*)

$$\begin{aligned}
  e(s+ds, \rho+d\rho) 
  & = e(s, \rho) + \partial_s e|_{\rho} (s,\rho) d \rho + \partial_\rho e|_{s} (s, \rho) ds + \\
  & + \dfrac{1}{2} \left[ \partial_{ss} e|_{\rho}(s,\rho) ds^2 + 2 \partial_{s\rho} e(s, \rho) ds d\rho + \partial_{\rho \rho} e(s, \rho) d \rho^2 \right] \ .
\end{aligned}$$

The equilibrium energy must be a *minimum* (**todo** check the function that must be a *minimum*, since $\partial_s e|_{\rho} = T$,... and $T$ not zero, and thus it can be a minimum!): the second order term must be positive for any increment of independent physical variables $d \rho$, $d s$, i.e.

$$\dfrac{1}{2} \left[ \partial_{ss} e|_{\rho} ds^2 + 2 \partial_{s\rho} e ds d\rho + \partial_{\rho \rho} e|_{s} d \rho^2 \right] $$

is a positive-definite quadratic form, i.e. the Hessian

$$\begin{bmatrix} \partial_{ss} e|_{\rho} & \partial_{s \rho} e \\ \partial_{s \rho } e & \partial_{\rho \rho} e|_{s} \end{bmatrix} $$

is definite positive, and thus teh following conditions must hold

$$\begin{cases}
  \partial_{ss} e|_{\rho} > 0 \\
  \partial_{ss} e|_{\rho} \partial_{\rho \rho} e|_{s} - \left( \partial_{s \rho} e \right)^2 < 0
\end{cases}$$

### Conditions on entropy

Using $e$, $\rho$ as independent thermodynamic state variables, and the entropy $s(e, \rho)$ it can be proved that the condition on $e(s, \rho)$ for the thermodynamic equilibrium implies that $s(e, \rho)$ is a *maxiumum* (**todo** *check the meaning of maximum here*), and thus

$$\dfrac{1}{2} \left[ \partial_{ee} s|_{\rho} de^2 + 2 \partial_{e\rho} s de d\rho + \partial_{\rho \rho} s|_{e} d \rho^2 \right] $$

is a positive-definite quadratic form, i.e. the Hessian

$$\begin{bmatrix} \partial_{ee} s|_{\rho} & \partial_{e \rho} s \\ \partial_{e \rho } s & \partial_{\rho \rho} s|_{e} \end{bmatrix} $$

is definite positive, and thus teh following conditions must hold

$$\begin{cases}
  \partial_{ee} s|_{\rho} < 0 \\
  \partial_{ee} s|_{\rho} \partial_{\rho \rho} s|_{e} - \left( \partial_{e \rho} s \right)^2 < 0
\end{cases}$$

```{dropdown} Relation between partial derivatives of $e(s,\rho)$ and $s(e,\rho)$

The relation

$$e = e_{s \rho}(s_{e \rho}(e, \rho), \rho) \ ,$$

provides the link between the two representations, having written $e_{s,\rho}()$, $s_{e,\rho}()$ the functions with the arguent indicated as indices. This relation contains only $e$, $\rho$ as independent variables. All the required relations are evaluated computing partial derivatives of this relation.

**First-order derivatives.** It can be proved that

$$\begin{aligned}
  \partial_e s |_{\rho} & = \dfrac{1}{\partial_s e |_{\rho}} \\
  \partial_{\rho} s |_e & = - \dfrac{\partial_{\rho} e |_{s}}{\partial_s e |_{\rho}} \\
\end{aligned}$$


**Second-order derivatives.** It can be proved that

$$\begin{aligned}
  \partial_{ee}       s|_{\rho} & = - \dfrac{1}{\left( \partial_s e|_{\rho} \right)^3} \partial_{ss} e |_{\rho} \\
  \partial_{e\rho}    s         & =   \dfrac{\partial_{\rho} e|_s}{\left( \partial_s e|_{\rho} \right)^3} \partial_{ss} e |_{\rho} - \dfrac{\partial_{s \rho} e}{(\partial_s e|_{\rho})^2} \\
  \partial_{\rho\rho} s|_{e}    & = - \dfrac{1}{\left( \partial_s e|_{\rho} \right)^3} \left[ \left( -\frac{\partial_\rho e_s}{\partial_s e|_\rho} \right)^2 \partial_{ss} e |_{\rho} + 2 \left(-\frac{\partial_\rho e_s}{\partial_s e|_\rho}\right) \partial_{s \rho} e + \partial_{\rho \rho} e|_s  \right] \\
\end{aligned}$$

```

```{dropdown} Equivalence of conditions on $e(s, \rho)$ and on $s(e, \rho)$ for thermodynamic equilibrium

Exploiting first condition on partial derivatives of $e(s,\rho)$, the first condition on the partial derivatives of $s(e,\rho)$ is

$$\partial_{ee} s|_{\rho} = - \dfrac{1}{\left( \partial_s e|_{\rho} \right)^3} \partial_{ss} e |_{\rho} = - \dfrac{1}{T^3} \partial_{ss} e |_{\rho}< 0 $$

since $T > 0$ and $\partial_{ss} e|_{\rho} > 0$.

Second condition for derivatives of $s(e, \rho)$ is

$$\begin{aligned}
  \partial_{\rho \rho} s|_{e} \partial_{ee} s |_{\rho} - \left( \partial_{\rho s} e \right)^2 
  & = \dots \\
  & = \frac{1}{T^4} \left[ \partial_{ss} e|_{\rho} \partial_{\rho \rho} e|_{s} - \left( \partial_{s \rho} e \right)^2  \right] < 0 \ .
\end{aligned} $$

```


<!--
<br>
**Relazioni tra coefficienti.**
<br>
-->
