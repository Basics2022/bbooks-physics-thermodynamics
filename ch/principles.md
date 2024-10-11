```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```

(classical-thermodynamics:principles)=
# Princìpi della termodinamica

**Primo principio della termodinamica.** Il primo principio della termodinamica è il bilancio di energia totale di un sistema

$$\dot{E}^{tot} = P^{e} + \dot{Q}^{e}$$

L'energia totale di un sistema può essere scritta come la somma dell'energia cinetica macroscopica $K$ e l'energia interna $E$, una rappresentazione macroscopica dell'energia cinetica delle componenti microscopiche del sistema, attorno ai valori medi macroscopici locali,

$$E^{tot} = K + E \ .$$

Usando il teorema dell'energia cinetica *macroscopica* **[REF]** noto dalla meccanica si può ricavare

$$\begin{aligned}
  \dot{E}^{tot} & = P^{e} + \dot{Q}^e \\
  \dot{K}       & = P^{tot} = P^{e} + P^{i} \\
  \dot{E}       & = \dot{Q}^e - P^{i} 
\end{aligned}$$

Il bilancio dell'energia interna può essere scritto in forma incrementale come

$$d E = d\hspace{-0.08pt}\bar{}\hspace{0.1pt} Q^e - d\hspace{-0.08pt}\bar{}\hspace{0.1pt} L^i \ ,$$

mettendo in evidenza con la notazione che l'energia interna è una variabile di stato del sistema, a differenza degli scambi di lavoro o di calore.

 Si assume che l'energia interna del sistema può essere scritta come funzione di variabili di stato cinematiche locali $\mathbf{x}$ (che non possono contribuire all'energia cinetica macroscopica del sistema) e almeno un'altra variabile di stato additiva, qui chiamata $S$.

$$E(\mathbf{x}, S)$$

Il suo differenziale può essere scritto come

$$d E = \dfrac{\partial E}{\partial \mathbf{x}}\Big|_{S} \cdot d \mathbf{x} + \dfrac{\partial E}{\partial S}\Big|_{\mathbf{x}} \cdot d \mathbf{S}$$

Il bilancio di energia interna in forma incrementale può essere riscritto come

$$\begin{aligned}
d E & = - d\hspace{-0.08pt}\bar{}\hspace{0.1pt} L^i + d\hspace{-0.08pt}\bar{}\hspace{0.1pt} Q^e =  \\
    & = - \delta L^{i,rev} + d\hspace{-0.08pt}\bar{}\hspace{0.1pt}^+ D + d\hspace{-0.08pt}\bar{}\hspace{0.1pt} Q^e  \\
\end{aligned}$$

avendo separato nel lavoro interno il contributo delle azioni reversibili e non reversibili. In accordo con l'esperienza, si assume che il contributo al lavoro interno delle forze non reversibili è sempre positivo, $d\hspace{-0.08pt}\bar{}\hspace{0.1pt}^+ D \ge 0$: questo contributo viene chiamato **dissipazione**.

Poiché sia il differenziale dell'energia e il contributo reversibile del lavoro interno sono dei termini reversibili, allora anche la somma di dissipazione e flusso di calore deve essere un contributo reversibile, indicato con $\delta U$.

Dal confronto delle due espressioni del differenziale dell'energia interna, avendo riconosciuto il contributo reversibile del lavoro interno nel primo termine, si può scrivere

$$
  \delta L^{i,rev} = - \dfrac{\partial E}{\partial \mathbf{x}} \Big|_{S} d \mathbf{x}  \qquad , \qquad 
  \delta U         = \ \dfrac{\partial E}{\partial S} \Big|_{\mathbf{x}} d S 
$$

**Terzo principio della termodinamica: definizione e segno della temperatura.**
La temperatura viene definita come la variabile parziale dell'energia interna del sistema rispetto alla variabile di stato $S$,

$$T := \dfrac{\partial E}{\partial S}\Big|_S{} \ .$$

Il terzo principio della termodinamica postula che la temperatura sia sempre positiva.

$$T := \dfrac{\partial E}{\partial S}\Big|_S{} > 0 \ .$$

**Secondo principio della termodinamica: enunciato di Clausius.** L'enunciato di Clausis del secondo principio della termodinamica può essere formulato in accordo con l'evidenza che la dissipazione sia sempre non negativa. Infatti

$$T dS =: \partial U = \underbrace{d\hspace{-0.08pt}\bar{}\hspace{0.1pt}^+ D}_{\ge 0} + d\hspace{-0.08pt}\bar{}\hspace{0.1pt} Q^e \ge  d\hspace{-0.08pt}\bar{}\hspace{0.1pt} Q^e \ ,$$

e quindi

$$dS \ge \dfrac{d\hspace{-0.08pt}\bar{}\hspace{0.1pt} Q^e }{T} \ .$$

**Secondo principio della termodinamica per sistemi complessi e direzione dei trasferimenti di calore.**

L'esperienza evidenzia che il trasferimento di calore avviene dai corpi a temperatura maggiore a corpi a temperatura minore, ossia il flusso di calore fa aumentare l'energia interna del corpo freddo e diminuire quella del corpo caldo.

Nello scabio di calore tra due corpi $i$, $j$ a temperature $T_i$, $T_j$, questa evidenza sperimentale può essere scritta come

$$d\hspace{-0.08pt}\bar{}\hspace{0.1pt} Q_{ji} \gtreqless 0 \quad \text{se} \quad T_i \gtreqless T_j \qquad \rightarrow \qquad \dfrac{d\hspace{-0.08pt}\bar{}\hspace{0.1pt} Q_{ji}}{T_j} + \dfrac{d\hspace{-0.08pt}\bar{}\hspace{0.1pt} Q_{ij}}{T_i} \ge 0 \ ,$$

dove $d\hspace{-0.08pt}\bar{}\hspace{0.1pt} Q_{ji} = - d\hspace{-0.08pt}\bar{}\hspace{0.1pt} Q_{ij}$ è il flusso di calore dal corpo $i$ al corpo $j$, positivo se fa aumentare l'energia interna di $j$ e diminuire quella di $i$.

$$d S_i = \underbrace{\dfrac{d\hspace{-0.08pt}\bar{}\hspace{0.1pt}  D_i}{T_i}}_{\ge 0} + \dfrac{d\hspace{-0.08pt}\bar{}\hspace{0.1pt}  Q^{e,i}}{T_i} + \sum_{j \ne i} \dfrac{d\hspace{-0.08pt}\bar{}\hspace{0.1pt}  Q_{ij}}{T_i}$$

Poichè $S$ è una variabile estensiva, il valore associato all'intero sistema è uguale alla somma dei valori delle sue parti, $S = \sum_i S_i$. E' quindi possibile ricavare una relazione per l'intero sistema sommando i contributi dovuti a tutte le sue parti.

$$\begin{aligned}
  d S & = \sum_i d S_i = \\
      & = \sum_i \sum_i \dfrac{d\hspace{-0.08pt}\bar{}\hspace{0.1pt}  Q^{e,i}}{T_i} + \sum_i \sum_{j \ne i} \dfrac{d\hspace{-0.08pt}\bar{}\hspace{0.1pt}  Q_{ij}}{T_i} + \underbrace{\dfrac{d\hspace{-0.08pt}\bar{}\hspace{0.1pt}  D_i}{T_i}}_{\ge 0} = \\
      & \ge \sum_i \dfrac{d\hspace{-0.08pt}\bar{}\hspace{0.1pt}  Q^{e,i}}{T_i} + \sum_{\{i, j\}} \underbrace{\Big( \dfrac{d\hspace{-0.08pt}\bar{}\hspace{0.1pt}  Q_{ij}}{T_i} + \dfrac{d\hspace{-0.08pt}\bar{}\hspace{0.1pt}  Q_{ji}}{T_j} \Big)}_{ \ge 0 }  = \\
      & \ge \sum_i \dfrac{d\hspace{-0.08pt}\bar{}\hspace{0.1pt}  Q^{e,i}}{T_i} \ .
\end{aligned}$$

