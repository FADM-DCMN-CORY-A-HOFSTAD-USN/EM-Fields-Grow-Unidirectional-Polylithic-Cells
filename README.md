# EM-Fields-Grow-Unidirectional-Polylithic-Cells

```
# EM-Aligned Polylithic Solar Reactor

**High-Efficiency Solution-Processed Solar Cells via Electromagnetic Molecular Alignment**

> *"Everything acts like a magnet if you push it hard enough. We are making the molecules grow straight."*

## 📖 Overview

This project aims to bridge the efficiency gap between expensive monocrystalline silicon and affordable solution-processed photovoltaics (Perovskites/OSCs). By integrating **Electromagnetic Field Alignment (EMFA)** into standard solution-coating workflows, we enforce uniform molecular orientation during the crystallization phase.

The goal: Eliminate grain boundaries and structural defects in polylithic cells to achieve monocrystalline-grade charge mobility (>22% PCE) at thin-film manufacturing costs.

## 🚀 The Core Concept

Current solution-processed cells suffer from a "mosaic" effect---randomly oriented crystal grains that trap electrons. This project builds a reactor that applies a precise external field (Magnetic or Electric) during the liquid-to-solid transition.

**The Physics:**
1.  **Liquid Phase:** Precursor solution is deposited (Blade/Slot-die). Molecules are mobile.
2.  **Field Application:** An external field (Helmholtz coil or High-Voltage Plate) exerts torque on molecular dipoles, forcing them to align parallel to the field lines.
3.  **Crystallization:** The solvent is evaporated (or anti-solvent applied) while the field holds the molecules in place ("locking" the alignment).
4.  **Result:** A defect-free, unidirectional crystalline highway for electrons.

## 📂 Repository Structure

```text
├── /docs               # Theory, field calculations, and chemistry notes
├── /hardware           # BOM and wiring diagrams for the reactor
├── /scad               # OpenSCAD source files for the reactor chassis & coil mounts
├── /firmware           # Arduino/ESP32 code for field modulation and temp control
└── README.md

```

🛠 Hardware Architecture
------------------------

The design focuses on a modular "Reactor" that fits over standard coating equipment.

| **Component** | **Function** | **Implementation** |
| --- | --- | --- |
| **Deposition Bed** | Holds the substrate; thermally controlled. | Heated aluminum bed (3D printed base). |
| **Field Generator** | Creates the uniform alignment field. | Dual Helmholtz Coils (Magnetic) or HV Plates (Electric). |
| **Gantry System** | Moves the coating blade/head. | Linear rail system (NEMA 17 steppers). |
| **Controller** | Manages field strength & motion profiles. | Microcontroller (ESP32/Arduino). |

📐 Getting Started
------------------

### Prerequisites

-   **OpenSCAD:** We use code-based 3D modeling for all structural parts. [Download Here](https://openscad.org/)

-   **Git:** For version control.

### Installation

1.  Clone the repo:

    Bash

    ```
    git clone [https://github.com/your-username/em-aligned-solar.git](https://github.com/your-username/em-aligned-solar.git)
    cd em-aligned-solar

    ```

2.  Open the main assembly:

    Bash

    ```
    openscad scad/main_assembly.scad

    ```

🗺 Roadmap
----------

1.  **Phase 1: The Chassis (Current Focus)**

    -   Design the `reactor_bed.scad` to house a standard glass substrate.

    -   Design `coil_mounts.scad` for adjustable Helmholtz coils.

    -   **Goal:** A printable frame that allows for variable field testing.

2.  **Phase 2: Field Simulation**

    -   Calculate required Teslas/Volts for standard Perovskite precursors.

    -   Determine power supply specs.

3.  **Phase 3: Prototype Build**

    -   Print parts, wind coils, and run initial "dry" alignment tests (using iron filings or similar visual indicators).

🤝 Contributing
---------------

We are currently following a "Prompt-to-Product" workflow. Check the Issues tab for the latest generated tasks.
