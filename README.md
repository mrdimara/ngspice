# ngspice — Power Conversion Simulation (Open Source)

A collection of ngspice netlists, KiCad custom symbols, subcircuit models, and MATLAB/Gnuplot post-processing scripts for simulating power conversion circuits with non-ideal component behaviour.

Developed as part of coursework on **Design and Simulation of Power Conversion using Open Source Tools**, with a focus on building reusable, well-documented simulation assets using entirely free and open-source software.

---

## Repository Structure

```
ngspice/
├── learnings/              # Annotated netlists and notes from the course
├── symbols_subckt/         # Custom KiCad symbols and ngspice subcircuit models
├── Custom.kicad_sym        # KiCad symbol library (custom components)
├── Custom.bak              # Backup of KiCad symbol library
├── fwd_lossy.data          # Simulation output — forward voltage sweep (lossy diode)
├── fwd_lossy.plt           # Gnuplot script — V-I characteristic plot
├── fwd_lossy_current.data  # Simulation output — forward current sweep
└── fwd_lossy_current.plt   # Gnuplot script — current waveform plot
```

---

## What's Inside

### `learnings/`
Step-by-step simulation exercises covering fundamental power conversion building blocks — rectifiers, converters, and switching circuits — with ngspice netlists and inline comments explaining circuit behaviour and simulation directives.

### `symbols_subckt/`
Reusable subcircuit definitions (`.subckt`) for non-ideal components such as lossy diodes, switches with on-resistance, and parasitic models. Paired with matching KiCad symbols for schematic-driven simulation workflows.

### Lossy Diode Characterisation
The root-level `.data` and `.plt` files capture the forward V-I characteristics and current response of a non-ideal diode model, demonstrating how forward voltage drop and series resistance are accounted for in circuit simulation.

---

## Tools Required

| Tool | Purpose | Install |
|------|---------|---------|
| [ngspice](https://ngspice.sourceforge.io/) | SPICE simulation engine | `sudo apt install ngspice` |
| [KiCad](https://www.kicad.org/) | Schematic capture & symbol editor | [kicad.org](https://www.kicad.org/download/) |
| [Gnuplot](http://www.gnuplot.info/) | Plot simulation output | `sudo apt install gnuplot` |
| MATLAB / Octave | Post-processing & analysis scripts | [GNU Octave](https://octave.org/) (free alternative) |

---

## Getting Started

**Clone the repository**
```bash
git clone https://github.com/mrdimara/ngspice.git
cd ngspice
```

**Run a netlist simulation**
```bash
ngspice <netlist_file>.cir
```

**Plot results with Gnuplot**
```bash
gnuplot fwd_lossy.plt
```

**Load the custom KiCad symbol library**
In KiCad → Symbol Editor → `File > Add Library` → select `Custom.kicad_sym`.

---

## Background

This repo accompanies the open-source power electronics simulation course offered by IISc Bangalore. The focus is on building circuit intuition through simulation before hardware implementation — covering diode non-idealities, switching losses, rectifier topologies, and converter dynamics, all using freely available tools.

---

## Author

**Mrdimara**
B.Tech Electrical Engineering, IIT (ISM) Dhanbad
[github.com/mrdimara](https://github.com/mrdimara)

---

## License

This repository is a public template. Feel free to fork and adapt for your own coursework or research.
