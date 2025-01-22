(classical-thermodynamics:potentials)=
# Thermodynamics potentials

Starting from the 
Partendo dall'espressione incrementale del primo principio della termodinamica è possivile definire altre funzioni delle variabili di stato (**TODO** *Ruolo della trasformata di Legendre*), chiamati **potenziali termodinamici**

**Energia interna.** $E(\mathbf{x}, S)$

$$d E = - \mathbf{F} \cdot d \mathbf{x} + T dS$$

**Energia libera di Helmholtz.** $F(\mathbf{x}, T) := E - T S$

$$\begin{aligned}
d F & = d E - T dS - S dT = \\
    & = - \mathbf{F} \cdot d \mathbf{x} + T dS - T dS - S dT = \\
    & = - \mathbf{F} \cdot d \mathbf{x} - S dT 
\end{aligned}$$

**Entalpia.** $H(\mathbf{F}, S) := E + \mathbf{F} \cdot \mathbf{x}$

$$\begin{aligned}
d H & = d E + \mathbf{F} \cdot d \mathbf{x} + \mathbf{x} \cdot d \mathbf{F} = \\
    & = - \mathbf{F} \cdot d \mathbf{x} + T dS + \mathbf{F} \cdot d \mathbf{x} + \mathbf{x} \cdot d \mathbf{F}= \\
    & = \ \mathbf{x} \cdot d \mathbf{F} + T dS 
\end{aligned}$$

**Energia libera di Gibbs.** $G(\mathbf{F}, T) := H - T S$

$$\begin{aligned}
d G & = d H - T dS - S dT = \\
    & = \ \mathbf{x} \cdot d \mathbf{F} + T dS - T dS - S dT = \\
    & = \ \mathbf{x} \cdot d \mathbf{F} - S dT 
\end{aligned}$$

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
