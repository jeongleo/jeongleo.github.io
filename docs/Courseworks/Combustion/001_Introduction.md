---
title: Introduction
---

# Introduction

## 1. What is combustion
- Combustion  
    A rapid exothermic osidation process which delivers hot products.

-  Frame  
    A self-sustaining propagation of a localized combustion zone. From atomic scale perspective, a radiating plasma in which the high temperature strips some of the electrons from their nuclei.

## 2. Why combustion is important?
Combustion provide us a large fraction of energy for transportation, electricity, residential heating, commercial energy needs, and military applications.

## 3. Impacts of combustion
### 3.1. Positive impacts
- Transportation and electricity

### 3.2. Negative impacts
- Atmospheric pollution
    - Particulate pollutants: smoke, soot, fly ash, dust
    - Gaseout pollutants: SOx, NOx
- Global warming and climate change

## 4. Main Objective of combustion science and technology
1. Design safe and reliable combustion system
2. Maximize thermal efficiency and minimize fuel consumption
3. Minimize pollutant emissions and climate change/impact

## 5. Type of combustion depending on mixing of fuel and oxidizer
1. Premixed combustion  
    Fuel and oxidizer completely and homogeneously mixed before ignition  
    - the most efficient
    - the most dangerous 
    
    
    > 1. Deflagnation  
        Propagating subsonic front  
        most flames, speed ~ 10 cm/s, pressure constant across the flame front

    > 2. Detonation  
        Sueprsonic shock-induced combustion  
        flame speed ~ 1000 m/s, pressure is not constant across the flame front
    

2. Diffusion combustion (non-premixed combustion)  
    Fuel and oxidizer separately enter the combustion chamber, and simultaneously mix and burn by diffusion processes.

    - less efficient
    - less dangerous
    - more pollutants



## 6. Governing equations overview
Governing equations for a chemical system of N species reacting through M reactions

- Continuity equation (1 eqn)   

    $$ {{\partial \rho} \over {\partial t }} + {{\partial \rho u_i} \over {\partial x_i}} $$

- Species equation (N eqns (N species)) 

    $$ {{\partial \rho Y_k} \over {\partial t}} + {{\partial}\over{\partial t}} (\rho (u_i + V_{k, i}) Y_k) = \dot \omega _k \quad \text{for} \quad k=1,2,3 \dots N $$

- Momentum equation (3 eqns (vector eqn))
  
    $$ {{\partial}\over{\partial t}}(\rho u_j) + {{\partial}\over{\partial x_i}}(\rho u_i u_j) = - {{\partial p}\over{\partial x_j}} + {{\partial \tau_{ij}}\over{\partial x_i}} + \rho \sum^N_{k=1}Y_k f_{k, j} $$

- Energy equation (1 eqn (scalar eqn))

    $$ \rho c_p {{DT}\over{Dt}} = \dot\omega_T ' + {{Dp}\over{Dt}} + {{\partial}\over{\partial x_i}} \left(  {\lambda {{\partial T} \over {\partial x_i}}} \right) - \left( \rho \sum^N_{k=1}{c_{p, k} Y_k V_{k, i} } \right) {{\partial T}\over {\partial x_i}} + \tau_{ij} {{\partial u_i}\over{\partial x_j}} + \dot Q + \rho \sum^N_{k=1} Y_k f_{k, i} V_{k, i}  $$

---
and where,  

- Heat release due to combustion  

    $$ \dot \omega_T ' = - \sum^N_{k=1} (h^\circ_{f, k} + \Delta h_{s, k})\dot\omega_k $$

- Net reaction reate of species k  

    $$ \dot \omega_k = MW_k \sum^M_{j=1} {\nu_{k_j}} Q_j = MW_k \sum^M_{j=1} {\nu''_{k_j}} - {\nu'_{k_j}} $$
 
- Multi-step mechanism  

    $$ \sum^N_{k=1} \nu'_{k_j} M_k \ce{<-->[$k_{f_j}$][$k_{b_j}$]} \sum^N_{k=1} \nu''_{k_j} M_k  $$

- Forward reaction rate constant  

    $$ k_{f_j} (T) = A_{f_j} T^{\beta_j} \exp \left( {-E_{A_j} \over \bar R T} \right) = A_{f_j} T^{\beta_j} \exp \left( {-T_{A_j} \over T} \right) $$

- Backward reaction rate constant  

    $$ k_{b_j} (T) = { k_{f_j} (T) \over { \left( {p^\circ \over  \bar R T} \right)^{\sum^N_{k=1}\nu_{k_j}} \exp \left( {\Delta S^\circ_j \over \bar R} - {\Delta H^\circ_j \over \bar R T} \right) } } $$

- Equilibrium constant

    $$ K_P = \exp \left( {- \Delta G^\circ (T) \over \bar R T} \right) = {p_C^{\nu_C} p_D^{\nu_D} \over p_A^{\nu_A} p_B^{\nu_B}} = { {N_C^{\nu_C}} {N_D^{\nu_D}} \over {N_A^{\nu_A}} {N_B^{\nu_B}} }\left( P_m \over N_m \right)^{\Delta \nu} = {X_C^{\nu_C} X_D^{\nu_D} \over X_A^{\nu_A} X_B^{\nu_B}} P_m^{\Delta \nu} $$

-----