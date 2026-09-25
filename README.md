# Basic-Buck-Converter-PCB

This repository contains the full design, simulation, documentation, and PCB layout for a compact buck (step‑down) DC‑DC converter. It is intended as a small, practical companion board to a more advanced isolated flyback converter, providing a simple, efficient, and well‑documented reference design for low‑voltage power conversion.

The project includes LTspice simulations, KiCad schematic + PCB, design calculations, and live testing and wiring. 
🔧 Project Overview

The board will take a DC input and step it down to low‑voltage output using a synchronous switching topology. 

Design Focuses: 

* Compact PCB footprint
* Good efficiency across a wide input range
* Clean documentation and reproducible calculations
* Practical testability (scope points, connectors, PG indicator)

Recruiter‑friendly presentation on GitHub

🎯 Target Electrical Specifications
* Parameter	Target
* Input Voltage	7–24 V DC
* Output Voltage	5 V (adjustable via feedback divider)
* Output Current	1–2 A depending on regulator choice
* Switching Frequency	500 kHz – 2 MHz (IC‑dependent)
* Duty Cycle ≈ 0.42
* Output Ripple	≤ 50 mVpp
* Inductor Ripple	20–40% of Iout


These values will be refined once the LTspice schematic is finalised.

📐 LTspice Simulations Included

The following was simulated fully in LTspice: 

* Output voltage regulation
* Output ripple measurement
* Inductor current ripple
* Switch node waveform
* Startup behaviour
* Load step response
* Line step response
* Efficiency vs load sweep

## Repository Structure

```text
├── docs/                               # General Documentation 
│   └── testreport.docx                 # Lab Test Report
├── kicad/                              # KiCAD Project Files 
│   ├── Buck Converter.kicad_pcb        # PCB Board File 
│   ├── Buck Converter.kicad_sch        # Schematic File 
│   ├── bom.csv                         # Bill of Materials
│   ├── gerber/                         # Manufacturing Files 
│   │   └── buck.zip                    # Gerber, NC Drill Files 
│   └── images/                         # 3D PCB Renders 
│       ├── buckconverterbottom.png     # Bottom Layer
│       └── buckconvertertop.png        # Top Layer 
├── ltspice/                            # Analog Simulation Files 
│   ├── models.asc                      # Component Models 
│   └── schematic.asc                   # LTspice schematic
├── testing/                            # Lab Testing
│   ├── oscilloscopeinput.png           # Input Ripple Waveforms 
│   ├── oscilloscopeoutput.png          # Output transient response waveform
│   └── testsetup.png                   # Bench Test Setup 
├── LICENSE                             # MIT Licence File 
└── README.md                           # Guidance / info 
