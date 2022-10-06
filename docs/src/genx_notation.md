# GenX Model Notation

## Model Indices and Sets
---
|**Notation** | **Description**|
| :------------ | :-----------|
|$t \in \mathcal{T}$ | where $t$ denotes an time step and $\mathcal{T}$ is the set of time steps over which grid operations are modeled|
|$\mathcal{T}^{interior} \subseteq \mathcal{T}^{}$ | where $\mathcal{T}^{interior}$ is the set of interior timesteps in the data series|
|$\mathcal{T}^{start} \subseteq \mathcal{T}$ |  where $\mathcal{T}^{start}$ is the set of initial timesteps in the data series. $\mathcal{T}^{start}={1}$ when representing entire year as a single contiguous period; $\mathcal{T}^{start}=\{\left(m-1\right) \times \tau^{period}+1 \| m \in \mathcal{M}\}$, which corresponds to the first time step of each representative period $m \in \mathcal{M}$|
|$n \in \mathcal{N}$ | where $n$ corresponds to a contiguous time period and $\mathcal{N}$ corresponds to the set of contiguous periods of length $\tau^{period}$ that make up the input time series (e.g. load, variable renewable energy availability) to the model|
|$\mathcal{N}^{rep} \subseteq \mathcal{N}$ | where $\mathcal{N}^{rep}$ corresponds to the set of representative time periods that are selected from the set of contiguous periods $\mathcal{M}$|
|$m \in \mathcal{M}$ | where $m$ corresponds to a representative time period and $\mathcal{M}$ corresponds to the set of representative time periods indexed as per their chronological ocurrence in the set of contiguous periods spanning the input time series data, i.e. $\mathcal{N}$|
$z \in \mathcal{Z}$ | where $z$ denotes a zone and $\mathcal{Z}$ is the set of zones in the network|
|$z \rightarrow z^{\prime} \in \mathcal{B}$ |where $z \rightarrow z^{\prime}$ denotes paths for different transport routes of electricity|
|$l \in \mathcal{L}$ | where $l$ denotes a transmission line and $\mathcal{L}$ is the set of transmission lines in the network of power|
|$y \in \mathcal{G}$ | where $y$ denotes a technology and $\mathcal{G}$ is the set of available technologies in power|
|$\mathcal{H} \subseteq \mathcal{G}$ | where $\mathcal{H}$ is the subset of thermal resources in power system|
|$\mathcal{VRE} \subseteq \mathcal{G}$ | where $\mathcal{VRE}$ is the subset of curtailable Variable Renewable Energy (VRE) resources|
|$\overline{\mathcal{VRE}}_{y,z}$ | set of VRE resource bins for VRE technology type $y \in \mathcal{VRE}$ in zone $z$ |
|$\mathcal{CE} \subseteq \mathcal{G}$ | where $\mathcal{CE}$ is the subset of resources qualifying for the clean energy standard policy constraint|
|$\mathcal{UC} \subseteq \mathcal{H}$ | where $\mathcal{UC}$ is the subset of thermal resources subject to unit commitment constraints|
|$s \in \mathcal{S}$ | where $s$ denotes a segment and $\mathcal{S}$ is the set of consumers segments for price-responsive demand curtailment|
|$\mathcal{O} \subseteq \mathcal{G}$ | where $\mathcal{O}$ is the subset of storage resources excluding heat storage and hydro storage |
|$o \in \mathcal{O}$ | where $o$ denotes a storage technology in a set $\mathcal{O}$|
|$\mathcal{O}^{sym} \subseteq \mathcal{O}$ | where $\mathcal{O}^{sym}$ corresponds to the set of energy storage technologies with equal (or symmetric) charge and discharge power capacities|
|$\mathcal{O}^{asym} \subseteq \mathcal{O}$ | where $\mathcal{O}^{asym}$ corresponds to the set of energy storage technologies with independently sized (or asymmetric) charge and discharge power capacities|
|$\mathcal{O}^{LDES} \subseteq \mathcal{O}$ | where $\mathcal{O}^{LDES}$ corresponds to the set of long-duration energy storage technologies for which inter-period energy exchange is permitted when using representative periods to model annual grid operations|
$\mathcal{W} \subseteq \mathcal{G}$ | where $\mathcal{W}$ set of hydroelectric generators with water storage reservoirs|
|$\mathcal{W}^{nocap} \subseteq \mathcal{W}$ | where $\mathcal{W}^{nocap}$ is a subset of set of $ \mathcal{W}$ and represents resources with unknown reservoir capacity|
|$\mathcal{W}^{cap} \subseteq \mathcal{W}$ | where $\mathcal{W}^{cap}$ is a subset of set of $ \mathcal{W}$ and represents resources with known reservoir capacity|
|$\mathcal{MR} \subseteq \mathcal{G}$ | where $\mathcal{MR}$ set of must-run resources|
|$\mathcal{DF} \subseteq \mathcal{G}$ | where $\mathcal{DF}$ set of flexible demand resources in power an dhydrogen system|
|$\mathcal{G}_p^{ESR} \subseteq \mathcal{G}$ | where $\mathcal{G}_p^{ESR}$ is a subset of $\mathcal{G}$ that is eligible for Energy Share Requirement (ESR) policy constraint $p$|
|$p \in \mathcal{P}$ | where $p$ denotes a instance in the policy set $\mathcal{P}$|
|$\mathcal{P}^{ESR} \subseteq \mathcal{P}$ | Energy Share Requirement type policies |
|$\mathcal{P}^{CO_2} \subseteq \mathcal{P}$ | CO$_2$ emission cap policies|
|$\mathcal{P}^{CO_2}_{mass} \subseteq \mathcal{P}^{CO_2}$ | CO$_2$ emissions limit policy constraints, mass-based |
|$\mathcal{P}^{CO_2}_{load} \subseteq \mathcal{P}^{CO_2}$ | CO$_2$ emissions limit policy constraints, load emission-rate based |   
|$\mathcal{P}^{CO_2}_{gen} \subseteq \mathcal{P}^{CO_2}$ | CO$_2$ emissions limit policy constraints, generation emission-rate based |
|$\mathcal{P}^{CRM} \subseteq \mathcal{P}$ | Capacity reserve margin (CRM) type policy constraints |
|$\mathcal{P}^{MinTech} \subseteq \mathcal{P}$ | Minimum Capacity Carve-out type policy constraint |
|$\mathcal{Z}^{ESR}_{p} \subseteq \mathcal{Z}$ | set of zones eligible for ESR policy constraint $p \in \mathcal{P}^{ESR}$ |
|$\mathcal{Z}^{CRM}_{p} \subseteq \mathcal{Z}$ | set of zones that form the locational deliverable area for capacity reserve margin policy constraint $p \in \mathcal{P}^{CRM}$ |
|$\mathcal{Z}^{CO_2}_{p,mass} \subseteq \mathcal{Z}$ | set of zones are under the emission cap mass-based cap-and-trade policy constraint $p \in \mathcal{P}^{CO_2}_{mass}$ |
|$\mathcal{Z}^{CO_2}_{p,load} \subseteq \mathcal{Z}$ | set of zones are under the emission cap load emission-rate based cap-and-trade policy constraint $p \in \mathcal{P}^{CO_2}_{load}$ |
|$\mathcal{Z}^{CO_2}_{p,gen} \subseteq \mathcal{Z}$ | set of zones are under the emission cap generation emission-rate based cap-and-trade policy constraint $p \in \mathcal{P}^{CO2,gen}$ |
|$\mathcal{L}_p^{in} \subseteq \mathcal{L}$ | The subset of transmission lines entering Locational Deliverability Area of capacity reserve margin policy $p \in \mathcal{P}^{CRM}$ |
|$\mathcal{L}_p^{out} \subseteq \mathcal{L}$ | The subset of transmission lines leaving Locational Deliverability Area of capacity reserve margin policy $p \in \mathcal{P}^{CRM}$ |
|$p \in \mathcal{P}^{CO_2}_{load}$ | to set emissions target based on a CO$_2$ emission rate limit in tCO$_2$/MWh $\times$ the total demand served in each zone |
|$j \in \mathbb{J}$ |where $j$ denotes the type of truck used in hydrogen and carbon transmission and $\mathcal{J}$ is the set of all truck types|
---



## Decision Variables
---
|**Notation** | **Description**|
| :------------ | :-----------|
|$\Omega_{y,z} \in \mathbb{R}_+$ | Installed capacity of resource $y$  in zone $z$ [MWh]|
|$\Omega^{energy}_{y,z} \in \mathbb{R}_+$ | Installed energy capacity of resource $y$  in zone $z$ - only applicable for storage resources, $y \in \mathcal{O}$ [MWh]|
|$\Omega^{charge}_{y,z} \in \mathbb{R}_+$ | Installed charging power capacity of resource $y$  in zone $z$ - only applicable for storage resources, $y \in \mathcal{O}^{asym}$ [MW]|
|$\Delta_{y,z} \in \mathbb{R}_+$ | Retired capacity of technology $y$ from existing capacity in zone $z$ [MW]|
|$\Delta^{energy}_{y,z} \in \mathbb{R}_+$ | Retired energy capacity of technology $y$ from existing capacity in zone $z$ - only applicable for storage resources, $y \in \mathcal{O}$[MWh]|
|$\Delta^{charge}_{y,z} \in \mathbb{R}_+$ | Retired charging capacity of technology $y$ from existing capacity in zone $z$ - only applicable for storage resources, $y \in \mathcal{O}^{asym}$[MW]|
|$\Delta_{y,z}^{total} \in \mathbb{R}_+$ | Total installed capacity of technology $y$ in zone $z$ [MW]|
|$\Delta_{y,z}^{total,energy} \in \mathbb{R}_+$ | Total installed energy capacity of technology $y$ in zone $z$  - only applicable for storage resources, $y \in \mathcal{O}$ [MWh]|
|$\Delta_{y,z}^{total,charge} \in \mathbb{R}_+$ | Total installed charging power capacity of technology $y$ in zone $z$ - only applicable for storage resources, $y \in \mathcal{O}^{asym}$ [MW]|
|$\bigtriangleup\varphi^{max}_{l}$ | Additional transmission capacity added to line $l$ [MW] |
|$\Theta_{y,z,t} \in \mathbb{R}_+$ | Energy injected into the grid by technology $y$ at time step $t$ in zone $z$ [MWh] or hydrogen produced by technology $y$ in zone $z$ at time step $t$ [tonne-$\ce{H2}$]|
|$\Pi_{y,z,t} \in \mathbb{R}_+$ | Energy withdrawn from grid by technology $y$ at time step $t$ in zone $z$ [MWh]|
|$\Gamma_{y,z,t} \in \mathbb{R}_+$ | Stored energy level of technology $y$ at end of time step $t$ in zone $z$ [MWh]|
|$\Lambda_{s,z,t} \in \mathbb{R}_+$ | Non-served energy/curtailed demand from the price-responsive demand segment $s$ in zone $z$ at time step $t$ [MWh] |
|$l_{l,t} \in \mathbb{R}_+$ | Losses in line $l$ at time step $t$ [MWh]|
|$\varrho_{y,z,t}\in \mathbb{R}_+$ | Spillage from a reservoir technology $y$ at end of time step $t$ in zone $z$ [MWh]|
|$f_{y,z,t}\in \mathbb{R}_+$ | Frequency regulation contribution [MW] for up and down reserves from technology $y$ in zone $z$ at time $t$\footnote{Regulation reserve contribution are modeled to be symmetric, consistent with current practice in electricity markets} |
|$r_{y,z,t} \in \mathbb{R}_+$ |  Upward spinning reserves contribution [MW] from technology $y$ in zone $z$ at time $t$\footnote{we are not modeling down spinning reserves since these are usually never binding for high variable renewable energy systems}|
|$f^{charge}_{y,z,t}\in \mathbb{R}_+$ | Frequency regulation contribution [MW] for up and down reserves from charging storage technology $y$ in zone $z$ at time $t$ |
|$f^{discharge}_{y,z,t}\in \mathbb{R}_+$ | Frequency regulation contribution [MW] for up and down reserves from discharging storage technology $y$ in zone $z$ at time $t$ |
|$r^{charge}_{y,z,t} \in \mathbb{R}_+$ |  Upward spinning reserves contribution [MW] from charging storage technology $y$ in zone $z$ at time $t$|
|$r^{discharge}_{y,z,t} \in \mathbb{R}_+$ |  Upward spinning reserves contribution [MW] from discharging storage technology $y$ in zone $z$ at time $t$|
|$r^{unmet}_t \in \mathbb{R}_+$ | Shortfall in provision of upward operating spinning reserves during each time period $t \in T$ |
|$\alpha^{Contingency,Aux}_{y,z} \in \{0,1\}$ | Binary variable that is set to be 1 if the total installed capacity  $\Delta^{\text{total}}_{y,z} > 0$ for any generator $y \in \mathcal{UC}$ and zone $z$, and can be 0 otherwise |
|$\Phi_{l,t} \in \mathbb{R}_+$ | Power flow in line $l$ at time step $t$ [MWh]|
|$v_{y,z,t}$ | Commitment state of the generation cluster $y$ in zone $z$ at time $t$|
|$\mathcal{X}_{y,z,t}$ | Number of startup decisions,  of the generation cluster $y$ in zone $z$ at time $t$|
|$\zeta_{y,z,t}$ | Number of shutdown decisions,  of the generation cluster $y$ in zone $z$ at time $t$|
|$\mathcal{Q}_{o,n} \in \mathbb{R}_+$ | Inventory of storage of type $o$ at the beginning of input period $n$ [MWh]|
|$\Delta\mathcal{Q}_{o,m} \in \mathbb{R}$ | Excess storage inventory built up during representative period $m$ [MWh]|
|$ON^{+}_{l,t} \in \{0,1\}$ | Binary variable to activate positive flows on line $l$ in time $t$|
|$TransON^{+}_{l,t} \in \mathbb{R}_+$ | Variable defining maximum positive flow in line $l$ in time $t$ [MW]|
|$\varepsilon _{OUT}^{GEN}$ | Variable defining the output of hydrogen generation unit $y$ and storage device $s$ in time $t$ [tonne-$\ce{H2}$] |
|$\vartheta_{k}^{GenNewCap}$ | Installed capcaity of hydrogen generation unit $k$ [tonne-$\ce{H2}$] |
|$\vartheta_{k}^{GenRetCap}$ | Retired capcaity of hydrogen generation unit $k$ [tonne-$\ce{H2}$] |
|$\Delta_{y,z}^{total} \in \mathbb{R}_+$ | Total installed capacity of hydrogen generation technology $y$ in zone $z$ [tonne-$\ce{H2}$] |
|$\Delta_{y,z} \in \mathbb{R}_+$ | Retired capacity of hydrogen generation technology $y$ from existing capacity in zone $z$ [tonne-$\ce{H2}$]|
|$n_{s}^{size}$ | maximum quantity of demand in this segment, specified as a share of demand in each zone in each time step |
|$\rho^{min}_{y,z,t}$ | minimum rate of output from technology $y$ in zone $z$ at time step $t$ [\%] |
|$\rho^{max}_{y,z,t}$ | maximum rate of output from technology $y$ in zone $z$ at time step $t$ [\%] |
|$\tau^{advance}_{y,z}$ | advance time for flexible demand |
|$\tau^{delay}_{y,z}$ | delay time for flexible demand|
|$\eta_{y,z}^{dflex}$ | energy lossed efficiency associated with flexible demand |
|$\nu_{y,t,z}$| designates the commitment state of g2p generator cluster $h$ in zone $z$ at time $t$ |   
|$\chi_{y,t,z}$| represents number of g2p startup decisions in cluster $h$ in zone $z$ at time $t$ |   
|$\zeta_{y,t,z}$| represents number of g2p shutdown decisions in cluster $h$ in zone $z$ at time $t$ |   
|$\Theta_{h,z,t}$ | is the energy injected into the grid by technology |
|$\Delta^{\text{total}}_{h,z}$ | is the total installed capacity  |
|$\nu_{y,z,t}$ | designates the commitment state of generator cluster |
|$\chi_{y,z,t}$ | represents number of startup decisions |
|$\zeta_{y,z,t}$ | represents number of shutdown decisions |
|$\Delta^{\text{total}}_{y,z}$ | is the total installed capacity |
|$\kappa_{y,z,t}^{up/down}$ | is the maximum ramp-up or ramp-down rate as a percentage of installed capacity |
|$\rho_{y,z}^{min}$ | is the minimum stable power output per unit of installed capacity |
|$\rho_{y,z,t}^{max}$ | is the maximum available generation per unit of installed capacity |
|$\tau_{y,z}^{up/down}$ | is the minimum up or down time for units in generating cluster |
|$\epsilon^{CO_{2}}_{z,p, mass}$ | to be provided in terms of million metric tonnes |
|$\epsilon_{z,p,load}^{maxCO_2}$ | denotes the emission limit in terms on tCO$_2$/MWh |
|$\epsilon_{z,p,gen}^{maxCO_2}$ |have to buy emission allowances from the emission regulator in the region $z$ where they are located |
|$\eta_{o,z}^{discharge}$ | discharge efficiency for storage device $o$ in zone $z$ [\%] |
|$\Delta Q_{o,z,m}$ | change in storage inventory associated with representative period $m$ |
|$\tau^{period}$ | number of repeated times |
|$\Pi_{o,z,t}$ | charge rate |
|$\Theta_{o,z,t}$ | released energy or hydrogen from storage device $o$ in zone $z$ at time step $t$ |
|$r^{discharge}_{o,z,t}$ | is the contribution of storage resources to upward reserves while discharging |
|$f^{discharge}_{o,z,t}$ | is the contribution of storage resources to frequency regulation while discharging |
|$f^{charge}_{o,z,t}$ | is the contribution of storage resources to frequency regulation while charging |
|$f^{+}_{y=o,z,t}$ | is the contribution of storage resources to frequency regulation while charging |
|$\Gamma_{o,z,t}$ | stored energy level or hydrogen level in storage device $o$ in zone $z$ at time step $t$ |
|$\eta_{o,z}^{loss}$ | storage discharge efficiency of device $o$ in zone $z$ |
|$f_{o,z,t}$ | The total storage contribution to frequency regulation |
|$r_{o,z,t}$ | The total storage contribution to reserves |


## Parameters
---
|**Notation** | **Description**|
| :------------ | :-----------|
|$D_{z,t}$ | Electricity demand in zone $z$ and at time step $t$ [MWh] or hydrogen demand in zone $z$ at time step $t$ [tonne-$\ce{H2}$]|
|$\tau^{period}$ | number of time steps in each representative period $w \in \mathcal{W}^{rep}$ and each input period $w \in \mathcal{W}^{input}$|
|$\omega_{t}$ | weight of each model time step $\omega_t =1 \forall t \in T$ when modeling each time step of the year at an hourly resolution|
|$n_s^{slope}$ | Cost of non-served energy/demand curtailment for price-responsive demand segment $s$ [\$/MWh]|
|$n_s^{size}$ | Size of price-responsive demand segment $s$ as a fraction of the hourly zonal demand [%]|
|$\overline{\Omega}_{y,z}$ | Maximum capacity of technology $y$ in zone $z$ [MW]|
|$\underline{\Omega}_{y,z}$ | Minimum capacity of technology $y$ in zone $z$ [MW]|
|$\overline{\Omega}^{energy}_{y,z}$ | Maximum energy capacity of technology $y$ in zone $z$ - only applicable for storage resources, $y \in \mathcal{O}$  [MWh]|
|$\underline{\Omega}^{energy}_{y,z}$ | Minimum energy capacity of technology $y$ in zone $z$ - only applicable for storage resources, $y \in \mathcal{O}$ [MWh]|
|$\overline{\Omega}^{charge}_{y,z}$ | Maximum charging power capacity of technology $y$ in zone $z$  - only applicable for storage resources, $y \in \mathcal{O}^{asym}$ [MW]|
|$\underline{\Omega}^{charge}_{y,z}$ | Minimum charging capacity of technology $y$ in zone $z$- only applicable for storage resources, $y \in \mathcal{O}^{asym}$ [MW]|
|$\overline{\Delta}_{y,z}$ | Existing installed capacity of technology $y$ in zone $z$ [MW]|
|$\overline{\Delta^{energy}_{y,z}}$ | Existing installed energy capacity of technology $y$ in zone $z$ - only applicable for storage resources, $y \in \mathcal{O}$ [MW]|
|$\overline{\Delta^{charge}_{y,z}}$ | Existing installed charging capacity of technology $y$ in zone $z$ - only applicable for storage resources, $y \in \mathcal{O}$ [MW]|
|$\overline{\Omega}_{y,z}^{size}$ | Unit size of technology $y$ in zone $z$ [MW]|
|$\pi_{y,z}^{INVEST}$ | Investment cost (annual amortization of total construction cost) for power capacity of technology $y$ in zone $z$ [\$/MW-yr]|
|$\pi_{y,z}^{INVEST,energy}$ | Investment cost (annual amortization of total construction cost) for energy capacity of technology $y$ in zone $z$ - only applicable for storage resources, $y \in \mathcal{O}$ [\$/MWh-yr]|
|$\pi_{y,z}^{INVEST,charge}$ | Investment cost (annual amortization of total construction cost) for charging power capacity of technology $y$ in zone $z$ - only applicable for storage resources, $y \in \mathcal{O}$ [\$/MW-yr]|
|$\pi_{y,z}^{FOM}$ | Fixed O&M cost of technology $y$ in zone $z$ [\$/MW-yr]|
|$\pi_{y,z}^{FOM,energy}$ | Fixed O&M cost of energy component of technology $y$ in zone $z$ - only applicable for storage resources, $y \in \mathcal{O}$ [\$/MWh-yr]|
|$\pi_{y,z}^{FOM,charge}$ | Fixed O&M cost of charging power component of technology $y$ in zone $z$ - only applicable for storage resources, $y \in \mathcal{O}$ [\$/MW-yr]|
|$\pi_{y,z}^{VOM}$ | Variable O&M cost of technology $y$ in zone $z$ [\$/MWh]|
|$\pi_{y,z}^{VOM,charge}$ | Variable O&M cost of charging technology $y$ in zone $z$ - only applicable for storage and demand flexibility resources, $y \in \mathcal{O} \cup \mathcal{DF}$ [\$/MWh]|
|$\pi_{y,z}^{FUEL}$ | Fuel cost of technology $y$ in zone $z$ [\$/MWh]|
|$\pi_{y,z}^{START}$ | Startup cost of technology $y$ in zone $z$ [\$/startup]|
|$\upsilon^{reg}_{y,z}$ | Maximum fraction of capacity that a resource $y$ in zone $z$ can contribute to frequency regulation reserve requirements|
|$\upsilon^{rsv}_{y,z}$ | Maximum fraction of capacity that a resource $y$ in zone $z$ can contribute to upward operating (spinning) reserve requirements|
|$\pi^{Unmet}_{rsv}$ | Cost of unmet spinning reserves in [\$/MW]|
|$\epsilon^{load}_{reg}$ | Frequency regulation reserve requirement as a fraction of forecasted demand in each time step |
|$\epsilon^{vre}_{reg}$ | Frequency regulation reserve requirement as a fraction of variable renewable energy generation in each time step |
|$\epsilon^{load}_{rsv}$ | Operating (spinning) reserve requirement as a fraction of forecasted demand in each time step |
|$\epsilon^{vre}_{rsv}$ | Operating (spinning) reserve requirement as a fraction of forecasted variable renewable energy generation in each time step |
|$\epsilon_{y,z}^{CO_2}$ | CO$_2$ emissions per unit energy produced by technology $y$ in zone $z$ [metric tons/MWh]|
|$\epsilon_{y,z,p}^{MinTech}$ | Equals to 1 if a generator of technology $y$ in zone $z$ is eligible for minimum capacity carveout policy $p \in \mathcal{P}^{MinTech}$, otherwise 0|
|$REQ_p^{MinTech}$ | The minimum capacity requirement of minimum capacity carveout policy $p \in \mathcal{P}^{MinTech}$ [MW]|
|$\epsilon_{y,z,p}^{CRM}$ | Capacity derating factor of technology $y$ in zone $z$ for capacity reserve margin policy $p \in \mathcal{P}^{CRM}$ [fraction]|
|$RM_{z,p}^{CRM}$ | Reserve margin of zone $z$ of capacity reserve margin policy $p \in \mathcal{P}^{CRM}$ [fraction]|
|$\epsilon_{z,p,mass}^{CO_2}$ | Emission budget of zone $z$ under the emission cap $p \in \mathcal{P}^{CO_2}_{mass}$ [ million of metric tonnes]|
|$\epsilon_{z,p,load}^{CO_2}$ | Maximum carbon intensity of the load of zone $z$ under the emission cap $p \in \mathcal{P}^{CO_2}_{load}$ [metric tonnes/MWh]|
|$\epsilon_{z,p,gen}^{CO_2}$ | Maximum emission rate of the generation of zone $z$ under the emission cap $p \in \mathcal{P}^{CO_2}_{gen}$ [metric tonnes/MWh]|
|$\rho_{y,z}^{min}$ | Minimum stable power output per unit of installed capacity for technology $y$ in zone $z$ [%]|
|$\rho_{y,z,t}^{max}$ | Maximum available generation per unit of installed capacity during time step t for technology y in zone z [%]|
|$VREIndex_{y,z}$ | Resource bin index for VRE technology $y$ in zone $z$. $VREIndex_{y,z}=1$ for the first bin, and $VREIndex_{y,z}=0$ for remaining bins. Only defined for $y\in \mathcal{VRE}$ |
|$\varphi^{map}_{l,z}$ | Topology of the network, for line l: $\varphi^{map}_{l,z}=1$ for zone $z$ of origin, - 1 for zone $z$ of destination, 0 otherwise. |
|$\eta_{y,z}^{loss}$ | Self discharge rate per time step per unit of installed capacity for storage technology $y$ in zone $z$ [%]|
|$\eta_{y,z}^{charge}$ | Single-trip efficiency of storage charging/demand deferral for technology $y$ in zone $z$ [%]|
|$\eta_{y,z}^{discharge}$ | Single-trip efficiency of storage (and hydro reservoir) discharging/demand satisfaction for technology $y$ in zone $z$ [%]|
|$\mu_{y,z}^{stor}$ | ratio of energy capacity to discharge power capacity for storage technology (and hydro reservoir) $y$ in zone $z$ [MW/MWh]|
|$\mu_{y,z}^{\mathcal{DF}}$ | Maximum percentage of hourly demand that can be shifted by technology $y$ in zone $z$ [%]|
|$\kappa_{y,z}^{up}$ | Maximum ramp-up rate per time step as percentage of installed capacity of technology y in zone z [%/hr]|
|$\kappa_{y,z}^{down}$ | Maximum ramp-down rate per time step as percentage of installed capacity of technology y in zone z [%/hr]|
|$\tau_{y,z}^{up}$ | Minimum uptime for thermal generator type y in zone z before new shutdown [hours].|
|$\tau_{y,z}^{down}$ | Minimum downtime or thermal generator type y in zone z before new restart [hours].|
|$\tau_{y,z}^{advance}$ | maximum  time  by which flexible demand resource can  be  advanced [hours]  |
|$\tau_{y,z}^{delay}$ | maximum  time  by which flexible demand resource can  be  delayed [hours]  |
|$\eta_{y,z}^{dflex}$ | energy losses associated with shifting the flexible load [%]|
|$\mu_{p,z}^{\mathcal{RPS}}$ | share of total demand in each model zone $z \in \mathcal{RPS}^{p}$  that must be served by qualifying renewable energy resources $y \in \mathcal{G}^{RPS}_{p}$|
|$f(n)$ | Mapping each modeled period $n \in \mathcal{N}$ to corresponding representative period $w \in \mathcal{W}$|
|$\Omega^{size}_{h,z}$ | is the unit size|
|$\kappa_{h,z,t}^{up/down}$ | is the maximum ramp-up or ramp-down rate as a percentage of installed capacity|
|$\tau_{h,z}^{up/down}$ | is the minimum up or down time for units in generating cluster|
|$\Omega^{size}_{y,z}$ | is the unit size|
|$\epsilon_{y,z}^{CO_2}$ | reflects the specific $CO_2$ emission intensity in tCO$_2$/MWh associated with its operation|
|$C_{\mathrm{PIP}}^{\mathrm{c}}$ | Unit constructure costs of pipeline in hydrogen transmission [\$/(tonne-$\ce{H2}$/hour]|
|$\upsilon^{reg}_{y,z}$ | limited specified fraction of installed discharge for frequency regulation |
|$\upsilon^{rsv}_{y,z}$ | limited specified fraction of installed discharge for capacity reserve |
---