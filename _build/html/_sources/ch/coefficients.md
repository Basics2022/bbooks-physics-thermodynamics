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

## Relations between thermodynamic coefficients

**Relation between $c_v$ and $c_p$.**

$$c_P - c_v = T \, v \, \dfrac{\alpha_P^2}{\beta_T} \ . $$ (eq:cv-cp)

**Relation between $\beta_s$ and $\beta_T$ - 1**

$$\beta_s = \frac{c_v}{c_P} \beta_T \ .$$ (eq:beta-1)

**Relation between $\beta_s$ and $\beta_T$ - 2**

$$\beta_s - \beta_T = - \frac{v T}{c_P} \alpha_P^2 \ .$$ (eq:beta-2)

**Relation between $\beta_s$ and $\beta_T$ - 3**

$$\dfrac{1}{\beta_s} - \dfrac{1}{\beta_T} = \dfrac{T}{v c_v} \left( \partial_T P|_v \right)^2 \ .$$ (eq:beta-3)

```{dropdown} Proof of the relation between heat capacities $c_v$, $c_P$

Changing independent variables from $(T,v)$ to $(P,v)$ in the expression of entropy $s(T,v) = s(T, P(v,T))$, 

$$\begin{aligned}
  \dfrac{c_v}{T} := \left.\dfrac{\partial s}{\partial T}\right|_v 
  & = \left.\dfrac{\partial s}{\partial T}\right|_P + \left.\dfrac{\partial s}{\partial P}\right|_T \left.\dfrac{\partial P}{\partial T}\right|_v = & \qquad \text{(Maxwell $\partial_P s|_T = - \partial_T v|_P$)} \\
  & = \left.\dfrac{\partial s}{\partial T}\right|_P - \left.\dfrac{\partial v}{\partial T}\right|_P \left.\dfrac{\partial P}{\partial T}\right|_v = & \qquad \text{(relation below $\partial_T P|_v = \dots$)} \\
  & = \partial_T s|_P + \dfrac{\left( \partial_P v |_T \right)^2}{\partial_P v |_T} = & \qquad \text{(def of TD coeffs)} \\
  & = \dfrac{c_P}{T} - \dfrac{ v \alpha_P^2}{\beta_T} 
\end{aligned}$$

having exploited the relation

$$\begin{aligned}
  \left.\dfrac{\partial P}{\partial T}\right|_v 
    = \dfrac{\partial(P,v)}{\partial (T,v)} 
    = \dfrac{\partial(P,v) / \partial(T,P)}{\partial (T,v) / \partial(T,P)} 
    = - \dfrac{\partial_P v|_T}{\partial_P v|_T} \ .
\end{aligned}$$ 

```

```{dropdown} Proof of the relation between $\beta_s$ and $\beta_T$ - 1

$$\begin{aligned}
 v \beta_T & = \partial_P v |_T \\
 v \beta_s & = \partial_P v |_s 
 = \dfrac{\partial(v,s)}{\partial(P,s)} \dfrac{\partial(v,T)}{\partial(v,T)}  \dfrac{\partial(P,T)}{\partial(P,T)} 
 = \underbrace{\dfrac{\partial(P,T)}{\partial(P,s)}}_{= \dfrac{1}{\partial_T s|_P}} \underbrace{\dfrac{\partial(v,T)}{\partial(P,T)}}_{\partial_P v|_T} \underbrace{\dfrac{\partial(v,s)}{\partial(v,T)}}_{\partial_T s|_v} 
 = \dfrac{c_v}{c_P} \left( v \beta_T \right)
\end{aligned}$$

```

```{dropdown} Proof of the relation between $\beta_s$ and $\beta_T$ - 2

$$
\beta_s = \frac{c_v}{c_P} \beta_T 
  = \dfrac{\beta_T}{c_P} \left[ c_P - T v \frac{\alpha^2_P}{\beta_T} \right]
  = \beta_T - T v \frac{\alpha^2_P}{c_P} \ .
$$

```

```{dropdown} Proof of the relation between $\beta_s$ and $\beta_T$ - 3

$$\begin{aligned}
\dfrac{1}{\beta_s} = \frac{c_P}{c_v} \dfrac{1}{\beta_T}
  & = \dfrac{1}{c_v \, \beta_T} \left[ c_v + T v \frac{\alpha^2_P}{\beta_T} \right] = \\
  & = \dfrac{1}{\beta_T} \, \dfrac{1}{c_v} \left[ c_v + T v \frac{\alpha^2_P}{\beta_T} \right] = \\
  & = \dfrac{1}{\beta_T} + T v \frac{\frac{1}{v^2} (\partial_T v|_P)^2}{-\frac{1}{v} \partial_P v|_T} \frac{1}{-\frac{1}{v} \partial_P v|_T} = \\
  & = \dfrac{1}{\beta_T} + T v \left( \frac{\partial_T v|_P}{\partial_P v|_T} \right)^2
    = \dfrac{1}{\beta_T} + T v \left( \frac{\partial (v,P)}{\partial (T,P)} \frac{\partial (P,T)}{\partial (v,T)} \right)^2 = \dfrac{1}{\beta_T} + T v \left( \left.\dfrac{\partial P}{\partial T}\right|_v  \right)^2
\end{aligned}$$

```


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
