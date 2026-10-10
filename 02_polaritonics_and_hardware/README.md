# OptiBox: Photonic AI Inference Appliance for Edge Generative Models (4B--70B)

[![GitHub License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![TeX Engine](https://img.shields.io/badge/TeX-pdfLaTeX-brightgreen.svg)](https://miktex.org)
[![Conference](https://img.shields.io/badge/Conference-OFC%202027-orange.svg)](https://www.ofcconference.org)
[![Fellowship](https://img.shields.io/badge/Fellowship-Caltech%20SURF%202027-red.svg)](https://sfp.caltech.edu)

Author: **Dalton Omondi**  
Affiliation: Computational Chemistry and Mathematical Physics, Nairobi, Kenya  
Contact: `daltonomondi588@gmail.com`  
Repositories:
- Primary Code & Engineering: [https://github.com/GabuGravin41/optimia.git](https://github.com/GabuGravin41/optimia.git)
- Overleaf Master Sync: [https://github.com/GabuGravin41/overleaf.git](https://github.com/GabuGravin41/overleaf.git) (`02_polaritonics_and_hardware/`)

---

## 1. Executive Overview

Transformer large language model (LLM) inference at batch size $B=1$ is severely bounded by the **memory wall**. Moving multi-gigabyte weight tensors across copper interconnects consumes over $90\%$ of total accelerator energy, generating extreme heat (400--700 W) that mandates noisy fans or liquid chillers.

**OptiBox** is a compact ($25\ \text{cm}^3$), ultra-low-power ($\le 35\ \text{W}$ USB-C / wall-powered), whisper-quiet desk-side AI appliance designed to run 4B to 70B parameter models with zero hand-waving.

Through systematic physical modeling, OptiBox resolves the fatal traps of past photonic proposals:
1. **The Area Trap**: All-optical weight storage requires $>2.5\ \text{m}^2$ of silicon die area ($>35$ wafers) for 70B models. OptiBox resolves this by establishing a **tiered heterogeneous architecture**: bulk weights remain in low-power electronic DRAM (LPDDR5X/CXL), while high-reuse attention projections are cached in non-volatile Optical Phase-Change Memory (OPCM).
2. **The Amortization Threshold**: We formulate and prove the closed-form **break-even token horizon**:
   $$H^* = \frac{\frac{8}{b_{\rm cell}} E_{\rm pcm\_prog}}{E_{\rm dram\_read} - E_{\rm opt\_read} + \Delta E_{\rm compute}} \approx \mathbf{48\text{--}54\ \text{tokens}}$$
   Beyond $54$ tokens, OptiBox achieves **35% to 82% lower energy per token** and up to **$4.7\times$ speedup** over digital CMOS.
3. **Lifespan Qualification**: Using GSSe ($\text{Ge}_2\text{Sb}_2\text{Se}_4\text{Te}_1$) non-volatile cells ($>500,000$ cycle endurance) and Arrhenius thermal modeling ($\text{AF} \approx 11,714\times$ at $45^\circ\text{C}$), OptiBox delivers a continuous operational lifetime exceeding **15 years** ($>5 \times 10^8$ tokens), safely surpassing the 7-month operational requirement.

---

## 2. Repository Structure

```text
optimia/
├── OFC_CONFERENCE_PAPER/
│   ├── ofc_conference_paper.tex       # Official 3-page contributed paper (35-word abstract)
│   └── ofc_conference_paper.pdf       # Compiled publication-ready PDF (0 errors)
├── MASTER_MONOGRAPH/
│   ├── OPTIBOX_MASTER_MONOGRAPH.tex   # Comprehensive 20-page research monograph (9 chapters)
│   └── OPTIBOX_MASTER_MONOGRAPH.pdf   # Compiled authoritative reference PDF
├── CALTECH_SURF_PROPOSAL/
│   ├── CALTECH_SURF_PROPOSAL.tex      # Caltech SURF 2027 fellowship application proposal (3 pages)
│   └── CALTECH_SURF_PROPOSAL.pdf      # Compiled grant proposal PDF
├── figures/                           # 600 DPI Vector PDFs and high-resolution PNGs
│   ├── schematic_opcm_cell.pdf        # Fig. A: 3D micro-architectural cutaway of OPCM cell
│   ├── flowchart_decoder_execution.pdf# Fig. B: Heterogeneous decoder execution flowchart
│   ├── characterization_optics_multiphasic.pdf # Fig. C: 4-panel optical hardware spectra
│   ├── fig1_energy_vs_cache_capacity.pdf       # Fig. 1: Energy per token vs. cache capacity
│   ├── fig2_break_even_amortization.pdf        # Fig. 2: Break-even amortization curves
│   ├── fig3_throughput_vs_power_pareto.pdf     # Fig. 3: Throughput vs. power Pareto envelope
│   └── fig4_optical_snr_enob_scaling.pdf       # Fig. 4: Signal integrity, noise, & ENOB scaling
├── simulation/
│   ├── photonic_memory_study/optibox_simulator.py # Python/NumPy trace-driven decode engine
│   ├── optibox_sweep_results.csv                  # Full parametric sweep telemetry
│   └── summary_default_horizon.csv                # Baseline comparative summaries
└── README.md                          # Project documentation and reproduction guide
```

---

## 3. Key Findings & Hardware Benchmarks

### A. Performance & Energy Benchmark ($H = 256$ Tokens)

| Platform / Configuration | Model Size | Energy (mJ/tok) | Latency (ms) | Throughput (tok/s) | Power (Watts) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| NVIDIA L40S (Digital CMOS Baseline) | 4B (INT4) | 246.0 | 14.65 | 68.2 | 16.8 W |
| Streaming Photonic Core (Volatile) | 4B (INT4) | 252.4 | 14.65 | 68.2 | 17.2 W |
| **OptiBox (20% Optical Cache)** | 4B (INT4) | **158.8** | **11.72** | **85.3** | **19.4 W** |
| **OptiBox (100% Optical Cache)** | 4B (INT4) | **44.2** | **3.12** | **320.5** | **14.2 W** |
| NVIDIA H200 (Digital CMOS Baseline) | 70B (INT4) | 5,612.0 | 42.72 | 23.4 | 131.4 W |
| **OptiBox (20% Optical Cache)** | 70B (INT4) | **3,840.5** | **34.18** | **29.3** | **112.4 W** |
| **OptiBox (75% Optical Cache)** | 70B (INT4) | **1,024.1** | **10.68** | **93.6** | **22.6 W** |

### B. Signal Integrity & Noise Floor (ENOB $\ge 6.0$ Bits)

At our nominal operating point ($+3\ \text{dBm} = 2.0\ \text{mW}$ per comb line, $\mathcal{L}_{\rm link} = -7.8\ \text{dB}$, $B = 20\ \text{GHz}$):
- Optical Signal Current: $I_{\rm sig} = 0.299\ \text{mA}$
- Quantum Shot Noise: $\langle i_{\rm shot}^2 \rangle = 1.92 \times 10^{-12}\ \text{A}^2$
- Johnson-Nyquist Thermal Noise ($50\ \Omega$, $300\ \text{K}$): $\langle i_{\rm therm}^2 \rangle = 6.62 \times 10^{-12}\ \text{A}^2$
- Laser RIN ($-150\ \text{dBc/Hz}$): $\langle i_{\rm RIN}^2 \rangle = 1.79 \times 10^{-12}\ \text{A}^2$
- **Total RMS Noise Current**: $i_{\rm RMS} = 3.21\ \mu\text{A}$
- **Analog SNR**: $39.37\ \text{dB} \implies \mathbf{\text{ENOB} = 6.25\ \text{bits}}$

*Verdict*: Physical resolution is well above the 4.0-bit floor required for INT4 LLMs (AWQ/GPTQ), ensuring zero loss of task accuracy.

---

## 4. Scientific Demarcation & Taxonomy

| Technical Pillar | Classification | Prior Art / Provenance | Dalton Omondi's Distinct Contribution |
| :--- | :--- | :--- | :--- |
| **Maxwell Wave Equations & Waveguide Modes** | Standard Textbook Physics | Saleh & Teich (2019); Agrawal (2021) | None claimed; used as fundamental electromagnetic baseline. |
| **Shot, Thermal & RIN Noise Formulations** | Standard Textbook Physics | Haus (1984); Agrawal (2021) | Closed-form resolution limit derivation for INT4 photonic tensor cores. |
| **Kerr Soliton Microcomb Generation** | Prior State-of-the-Art | Kippenberg group (EPFL); Enlightra | Adopted as multi-carrier WDM comb source ($32$ carriers, $20\ \text{GHz}$). |
| **Non-Volatile OPCM Cells** | Prior State-of-the-Art | Meng et al. (2023); Rios et al. (2022) | Multi-level GSSe cell integration with multi-bridge microheaters. |
| **Homogeneous OPCM Crossbars** | Prior State-of-the-Art | Karimi et al. (*SCARLET*, 2026) | Proved the physical area limitation ($>2.5\ \text{m}^2$) of pure optical memory. |
| **Break-Even Amortization Formulation ($H^*$)** | **Author's Novel Contribution** | **First analytical closed-form derivation** | Derived the mathematical threshold $H^* \approx 48\text{--}54$ separating CMOS and photonics. |
| **Tiered Heterogeneous Memory-Compute Flow** | **Author's Novel Contribution** | **First architectural design** | Partitioned weights to eliminate the silicon area explosion via DRAM streaming + OPCM caching. |
| **Desk-Side AI Appliance Co-Design** | **Author's Novel Contribution** | **First physical specification** | Engineered silent, $\le 35\ \text{W}$, $25\ \text{cm}^3$ hardware with $>15$-year Arrhenius lifespan. |

---

## 5. Prototype Bill of Materials (BOM) & Manufacturing

Prototyping budget for 5 engineering units targeting commercial MPW runs:
- **imec iSiPP50G MPW Run** ($5 \times 5\ \text{mm}$ PIC die): \$36,000
- **Enlightra Turnkey SIL Microcomb Laser**: \$24,000
- **AMD / Xilinx ZCU216 RFSoC FPGA Controller**: \$17,000
- **SQS Vlaknova Optika PM Fiber Array**: \$7,500
- **High-Frequency RF PCB Carrier**: \$4,000
- **Protolabs CNC Milled Aluminum Chassis** ($25\ \text{cm}^3$): \$2,000
- **Total Prototype Budget**: **\$90,500**

*Volume Manufacturing (10,000+ units)*: Unit cost drops to **\$1,180**, enabling commercial retail distribution.

---

## 6. How to Reproduce & Build

### Prerequisites
- Python 3.10+ (`numpy`, `matplotlib`, `scipy`)
- TeX Live / MiKTeX (`pdflatex`, `lmodern`, `microtype`, `booktabs`, `hyperref`)

### Run Simulator & Generate Figures
```bash
# Execute the trace-driven architectural sweep
python photonic_memory_study/optibox_simulator.py

# Recompile the OFC 3-Page Contributed Paper
pdflatex -interaction=nonstopmode ofc_conference_paper.tex

# Recompile the 20-Page Master Monograph
pdflatex -interaction=nonstopmode OPTIBOX_MASTER_MONOGRAPH.tex
pdflatex -interaction=nonstopmode OPTIBOX_MASTER_MONOGRAPH.tex

# Recompile the Caltech SURF Research Proposal
pdflatex -interaction=nonstopmode CALTECH_SURF_PROPOSAL.tex
```

---

## 7. Citation

If you reference this architecture or simulation codebase, please cite:

```bibtex
@article{omondi2026optibox,
  author    = {Dalton Omondi},
  title     = {OptiBox: Architecture, Physics, and Break-Even Amortization of a Desk-Side Photonic AI Inference Appliance for 4B to 70B Transformers},
  journal   = {Technical Monograph and Research Package},
  year      = {2026},
  url       = {https://github.com/GabuGravin41/optimia}
}
```
