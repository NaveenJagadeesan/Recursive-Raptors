# Recursive-Raptors

# Thermal-Protection Solver & 3D Visualization  

---

## Overview
This project couples an **1-D multi-layer heat-conduction solver** with an **interactive OpenGL viewer** to predict and visualise insulation-thickness requirements for a humanoid robot submerged in 900 K molten metal. The code base is entirely **modern C++17** and cross-platform.

* **Solver.** Tridiagonal BTCS discretisation solved with a Thomas algorithm, using the harmonic mean of \(k\) at material interfaces to enforce flux continuity.  
* **Viewer.** GLFW + GLAD renderer that loads an OBJ mesh, maps insulation thickness to a colour-map, and supports face / wireframe / material modes, cut-plane slider, and smooth mouse pan / zoom / rotate .  
* **Validation.** Matches analytical trends and reproduces presentation results (e.g., average thickness 41.6 cm for 7 h soak).  
* **Performance.** Full 7-hour mission solved in **< 2 s**

---

