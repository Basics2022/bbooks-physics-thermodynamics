<!--
```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```
-->

(classical-thermodynamics:heat-engines)=
# Thermodynamic cycles and heat engines

**Direct and reversed thermodynamic cycles.** Direct cycles: transform heat to mechanical work. Reverset cycle: transform mechanical work to heat transfer (e.g. refrigeration/cooling - refrigerator cycles - or heating - heat pump cycles)

**Carnot cycle - reversible cycle between two constant temperatur sources.** Planck and Kelvin statements of $2^{nd}$ principle of thermodynamics. Maximum efficiency....

**Ideal models of real cycles.** Otto, Diesel, Atkinson, Stirling (ICE), Rankine, Joule-Brayton

**Principle.** Reciprocating (piston)/reactive (turbine) engines

**Circuit.** Open/close


(classical-thermodynamics:heat-engines:carnot)=
## Carnot cycle and heat engine

(classical-thermodynamics:heat-engines:carnot)=
### Second principle of thermodynamics: Planck and Kelvin statements

(classical-thermodynamics:heat-engines:real)=
## Heat engines and cycles

In this section, the idealization/model of real thermodynamic cycles performed by real-life machines are discussed.

(classical-thermodynamics:heat-engines:real:otto)=
### Otto

**Introduction.**

**Applications.**

**Thermodynamic cycle.** Reciprocating operation, with (approximately[^closed-system]) close system between intake and exhaust processes:
- $0 \rightarrow 1$ intake, approximately isobaric
- $1 \rightarrow 2$ adiabatic compression
- $2 \rightarrow 3$ combustion, approximately isochoric at TDC: **spark ignition** usually makes combustion fast enough to be modeled as an immediate process occurring at TDC; this is in contast to [Diesel engines](classical-thermodynamics:heat-engines:real:diesel), where combustion starts with self-ignition due to high temperature reached at the end of the compression
- $3 \rightarrow 4$ adiabatic expansion
- $4 \rightarrow 0$ exhaust, approximately isochoric BDC followed by isobaric

[^closed-system]: Combustion chamber is an approximately close system during a cycle between intake and exhaust, because of: 1. fuel injection, 2. leakage through the clearance between the walls of the piston and the cylinder.

(classical-thermodynamics:heat-engines:real:diesel)=
### Diesel

**Introduction.**

**Applications.**

**Thermodynamic cycle.** Reciprocating operation, with (approximately[^closed-system]) close system between intake and exhaust processes:
- $0 \rightarrow 1$ intake, approximately isobaric
- $1 \rightarrow 2$ adiabatic compression
- $2 \rightarrow 3$ combustion, approximately isobaric at TDC: **self ignition** usually triggers slower combustion if compared with [Otto engines](classical-thermodynamics:heat-engines:real:otto), that can be modeled as an isobaric transformation
- $3 \rightarrow 4$ adiabatic expansion
- $4 \rightarrow 0$ exhaust, approximately isochoric BDC followed by isobaric

(classical-thermodynamics:heat-engines:real:joule-brayton)=
### Joule-Brayton

**Introduction.** It's the reference thermodynamic cycle for **gas turbine** heat engines. These systems have continuous operation and can work both in open (jet propulsion) and close cycles (electric power generation). 

**Applications.** Joule-Brayton close cycle is used in electric power generation: heat producesd by combustion is transferred to an operating fluid(chemical power to thermal power), entnering a turbine that converts "thermal power of the fluid" into mechanical power, then converted to electric power by an electric generator. Joule-Brayton open cycle is used for jet propulsion (typically for aircraft): operating fluid is usually air, undergoing the thermodynamic cylce through the jet engine; air is compressed before entering the combustion chamber, and released after passing throught a turbine: turbine extracts the power required to drive the compressor, and "extra power" contained in the fluid is used to accelerating exhaust fluid, producing thrust. 

**Thermodynamic cycle - close cycle.** Components involved in the system are usually open systems. Steady operation of these systems is described by balance of total enthalpy flux. Kinetic energy of the fhe fluid is usually negligible if compared with internal energy and enthapy: total entalphy reduces to **enthalpy**
- $1 \rightarrow 2$ adiabatic compression
- $2 \rightarrow 3$ combustion, approximately isobaric at in combustion chamber
- $3 \rightarrow 4$ adiabatic expansion
- $4 \rightarrow 1$ isobaric cooling

**Thermodynamic cycle - open cycle.** Components involved in the system are usually open systems. Steady operation of these systems is described by balance of **total enthalpy** flux. Kinetic energy of the fhe fluid is usually **not** negligible if compared with internal energy and enthapy
- $0 \rightarrow 1$ adiabatic compression in free air before or at the engine intake
- $1 \rightarrow 2$ adiabatic compression in compressor
- $2 \rightarrow 3$ combustion, approximately isobaric at in combustion chamber
- $3 \rightarrow 4$ adiabatic expansion in turbine
- $4 \rightarrow 5$ adiabatic expansion in the nozzle

(classical-thermodynamics:heat-engines:real:rankine)=
### Rankine

**Introduction.**

**Application.**

**Thermodynamic cycle.**

(classical-thermodynamics:heat-engines:systems)=
## Applications

(classical-thermodynamics:heat-engines:systems:engine)=
### Mechanical power
(classical-thermodynamics:heat-engines:systems:power-generation)=
### Power generation
(classical-thermodynamics:heat-engines:systems:heat-pump-refrigeration)=
### Heat pump and/or refrigeration


<!--
Le macchine termiche sono sistemi che sfruttano scambi di calore per produrre lavoro (**macchine dirette**, come i motori a combustione) o lavoro per scambiare calore da sistemi freddi a sistemi più caldi (**macchine inverse**, come i frigoriferi).

Di solito, le macchine termiche sfruttano un fluido di lavoro. Le macchine a fluido possono essere un sistema aperto (es. motori aeronautici) o chiuso (circuiti delle centrali elettriche e di frigoriferi), o un sistema che è aperto solo in alcune fasi (es. nei motori alternativi, la camera di combustione è un sistema aperto solo durante le fasi di aspirazione e scarico, se si trascurano le perdite).

**Macchine ideali.** *Macchina ideale di Carnot; efficienza massima; enunciati di Planck e Kelvin del secondo principio della termodinamica.*

**Macchine reali.** *Cicli ideali: Otto, Diesel, Rankine, Joule-Brayton,...;*
-->
