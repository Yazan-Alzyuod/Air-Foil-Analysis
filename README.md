# Air-Foil-Analysis
# 2D Computational Fluid Dynamics (CFD) Analysis of an Airfoil ✈️

## 📌 Project Overview
This project performs a two-dimensional external flow analysis on an airfoil geometry using **Ansys Fluent**. The objective is to determine the aerodynamic performance parameters—specifically the **Lift Coefficient ($C_L$)** and **Drag Coefficient ($C_D$)**—under simulated flow conditions. This analysis is crucial for evaluating the efficiency and performance of the profile in aerial or hydrodynamic applications.

## ⚙️ Simulation Setup and Methodology

### 1. Geometry and Profile
* **Geometry:** 2D Airfoil Profile.
* **Coordinate Data:** The profile was defined using the coordinates provided in `Airfoil_Coordinates.txt` (originally `New Text Document.txt`). This allows for high-fidelity reproduction of the wing shape.

### 2. Meshing
* **Mesh Size:** 76,680 Cells, 115,782 Faces.
* **Refinement Strategy:** A C-grid or similar structured/unstructured mesh was used. **Inflation Layers** were applied to the airfoil surface to accurately resolve the boundary layer, which is critical for calculating skin friction drag and flow separation. 

### 3. Solver Settings
* **Solver Type:** Pressure-Based, Steady-State.
* **Fluid Medium:** Air (Compressible/Incompressible based on speed).
* **Turbulence Model:** **SST k-omega** model, which is highly recommended for aerospace applications due to its superior performance in regions of adverse pressure gradients and separation.

### 4. Boundary Conditions
* **Inlet:** Velocity Inlet (or similar far-field condition).
* **Outlet:** Pressure Outlet.
* **Airfoil Wall:** No-slip condition.

## 📊 Results & Analysis

### 🔍 Key Findings
The simulation successfully converged after 126 iterations, with all residuals meeting the convergence criteria (0.001 for continuity and velocity).

| Parameter | Value | Unit |
| :--- | :--- | :--- |
| **Lift Force** | -0.06440 | N |
| **Drag Force** | 0.68723 | N |
| **Lift Coefficient ($C_L$)** | **-0.01168** | - |
| **Drag Coefficient ($C_D$)** | **0.12467** | - |
| **L/D Ratio** | -0.0937 | - |

The negative lift coefficient suggests the airfoil may be at a **negative angle of attack** or an unconventional (non-lifting) configuration, resulting in net downward force under the current flow conditions.


## 🚀 Repository Contents
* `Project.wbpj`: Ansys Workbench Project file.
* `Case.cas`: Fluent case file (containing mesh and setup).
* `Data.dat`: Fluent data file (containing solution results).
* `Airfoil_Coordinates.txt`: The geometry definition file.
* `Ansys_Fluent_Simulation_Report_Air_foil.pdf`: The detailed simulation report.

---
## 👨‍💻 Author
**Yazan Alzyuod**
* **Mechanical Engineer**
* 📧 [yqlasem@gmail.com](mailto:yqlasem@gmail.com)
* 🔗 [LinkedIn Profile](https://www.linkedin.com/in/yazan-alzyuod)
* 💻 [GitHub Profile](https://github.com/Yazan-Alzyuod)
* 📞 00962775327776
