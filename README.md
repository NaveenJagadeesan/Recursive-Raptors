# Recursive-Raptors

# Thermal-Protection Solver & 3D Visualization  

# Authors

Nishi Mishra — matrix math & solver derivation
Hassan Niaz — Thomas-algorithm heat-solver implementation

Layan Samandar — OBJ scaling, thickness parsing, mass calc
Parina Patel — OBJ scaling, thickness parsing, mass calc

Bihao Zhang — Visualization - GUI, thickness plots, color Map, CMakeLists, Error Handling
Naveen Jagadeesan — Visualization - GUI Interactive Viewer, Rendering the thickness plots in the viewer, Color Map, Error Handling


---

## Overview
This project couples an **1-D multi-layer heat-conduction solver** with an **interactive OpenGL viewer** to predict and visualise insulation-thickness requirements for a humanoid robot submerged in 900 K molten metal. The code base is entirely **modern C++17** and cross-platform.

* **Solver.** Tridiagonal BTCS discretisation solved with a Thomas algorithm, using the harmonic mean of \(k\) at material interfaces to enforce flux continuity.  
* **Viewer.** GLFW + GLAD renderer that loads an OBJ mesh, maps insulation thickness to a colour-map, and supports face / wireframe / material modes, cut-plane slider, and smooth mouse pan / zoom / rotate .  
* **Validation.** Matches analytical trends and reproduces presentation results (e.g., average thickness 41.6 cm for 7 h soak).  
* **Performance.** Full 7-hour mission solved in **< 2 s**

---
## Folder layout
Thermal Protection Solver/
├─ assets/ # Icons, fonts, shaders
├─ csv/ # Thickness profiles etc.
├─ docs/ # PDF slides, figures
├─ obj/ # Generic OBJ meshes
├─ robot/ # Humanoid OBJ + CSV bundle
├─ sphere/ # Demo sphere case
├─ libs/ # External deps (see below)
│ ├─ freeglut/ glad/ glfw/ glm/ implot/
├─ mesh_lib/ # Mesh utilities (separate CMake target)
│ ├─ mesh_lib.cpp / .h
│ ├─ mesh_oper.cpp
│ └─ mesh_vol.cpp
├─ visual_lib/glad/ # GLAD build files
├─ build/ # (generated) CMake build directory
├─ Project_3_Visual.cpp # Main viewer entry point
├─ CMakeLists.txt
README.md # ← you are here
