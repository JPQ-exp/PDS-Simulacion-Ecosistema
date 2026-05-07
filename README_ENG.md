<img width="838" height="649" alt="Simulación de ecosistema con rejilla" src="https://github.com/user-attachments/assets/102703ba-840c-4969-bddd-755b23a10f17" />


# Axiomatic Persistence: An Emergent Ecosystem Simulation

[![Python 3.x](https://img.shields.io/badge/python-3.x-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This project is an interactive implementation of a dynamic ecosystem based on the principles of **Axiomatic Persistence** and **Persistent Dynamical Systems (PDS)**.

Unlike traditional ecological simulations that impose external population limits (Top-Down), in this model, stability and **Carrying Capacity** are **emergent properties** that arise strictly from internal metabolic, spatial, and temporal constraints (Bottom-Up).

## 🚀 Key Features

- **Emergent Stability:** The equilibrium between herbivores, carnivores, and resources is not pre-programmed. It emerges from the interaction between entropic decay and adaptive efficiency.
- **Active Sensory Fields:** Agents operate under a cost function that combines attraction to food and repulsion (**fear**) toward predators using non-linear power laws.
- **Realistic Temporal Delays:** Implementation of digestion lags (**deferred metabolism**) and cognitive inertia (**sensory delay**), avoiding the "tyranny of the instantaneous."
- **Toroidal Geometry:** The simulation space is topologically a **Torus**, eliminating edge effects and allowing continuous population flows.
- **Allometric Scaling:** Physical and energetic differentiation between species. Carnivores are more massive, possess higher metabolic inertia, and require higher replication thresholds.

---

## 🛠 Recent Update: Perception and Performance Refactoring

A new logic layer has been implemented to enhance ecosystem stability and processing efficiency.

### Included Changes:

*   **Grid Optimization:** The food grid has been adjusted to **15x15**, creating a more strategic and visually clean resource environment.
*   **Selective Awareness (Herbivores):** Agents now possess "availability awareness." They only detect and move toward active (green) food patches, ignoring cells currently in the regeneration process.
*   **Fixed Vision Range (Carnivores):** Predators now have a constant vision radius of **180px**, regardless of herbivore variables, balancing the hunting dynamics.
*   **FPS Stabilization:** The simulation engine is synced to **30 FPS (33ms per cycle)**, eliminating lag and ensuring constant fluidity even with high populations.
*   **Static Resource Persistence:** Food now toggles color (Green $\leftrightarrow$ Black) instead of disappearing, allowing the observation of consumption patterns across the entire grid.

---

## 🧠 Theoretical Foundations

The simulation engine is based on two coupled flows:

1.  **Metabolic Flow ($x$):** Represents the mass of persistence. It is subject to continuous decay (entropy) and is fueled through a delayed digestion process.
2.  **Configuration Flow ($z$):** Movement dynamics in space. Agents adjust their internal state to minimize "surprise" or error relative to their viability niche.

> **Note:** *Specific equations and the formal framework of the underlying mathematical model will be detailed in a future documentation update.*

## 🛠️ Installation and Usage

### Requirements
- Python 3.x
- NumPy

### Execution
Clone the repository and run the main script:
```bash
git clone https://github.com/JPQ-exp/PDS-Simulacion-Ecosistema.git
cd PDS-Simulacion-Ecosistema
python PDS-ecosistema-tkinter.py
```

## 🎮 User Interface

The simulation includes a real-time control panel (Tkinter) to manipulate the ecosystem's universal constants:

- **Fear Radius (Sensor):** Adjusts the range of the herbivores' repulsion field.
- **Food Delay (Growth):** Controls the recovery time of resource patches (the "friction" of the environment).
- **Digestion Rate:** Modifies the speed at which stomach stock is converted into vital energy.

## 📊 Visualization
- **Cyan Spheres:** Herbivores (Fast adaptation, low mass).
- **Red Spheres:** Carnivores (Slow adaptation, high inertia).
- **Green Dots:** Resources (Available potential energy).
- **Sidebars:** Real-time population monitor.

---

## 🧬 The Axiomatic Set for Emergent Persistence

The simulation demonstrates that a stable **Non-Equilibrium Steady State (NESS)** is reached after ~40+ minutes when the following 7 constraints are present:

1.  🔘 **Torus:** Boundaryless geometry.
2.  🔘 **Grid:** Structured energy distribution.
3.  🔘 **Shelter:** Local vision and sensory asymmetry.
4.  🔘 **Direction:** Gradient flow dynamics.
5.  🔘 **Fear:** Non-linear repulsive fields.
6.  🔘 **Aging:** Mass recycling and turnover.
7.  🔘 **Delay:** Temporal friction in digestion/metabolism.

**Stability is not in the formula; it is in the structure of the constraints.** You are free to experiment and validate this emergent behavior. 🏗️

---

### Contributions
Ideas on how to extend temporal delays or introduce mutations in metabolic parameters are welcome. Feel free to open an *Issue* or submit a *Pull Request*.

**Author:** JPQ-exp  
**License:** MIT  
**Zenodo:** [http://doi.org/10.5281/zenodo.20054974](http://doi.org/10.5281/zenodo.20054974)
