# ngspice-analog-simulations
# NGspice Analog Circuit Simulations

A collection of analog circuit simulations built with [NGspice](https://ngspice.sourceforge.io/), demonstrating core analog design concepts including frequency response analysis, transistor-level amplifier design, and differential signaling.

## Simulations

### 01 - RC Low-Pass Filter
**File:** `01_rc_lowpass_filter/rc_lowpass.cir`

First-order passive RC low-pass filter (R=1kΩ, C=100nF) with a cutoff frequency of ~1.59 kHz. Includes AC sweep for Bode plot (magnitude and phase) and transient analysis showing signal attenuation above the corner frequency.

### 02 - NMOS Common-Source Amplifier
**File:** `02_nmos_common_source/nmos_cs_amp.cir`

Single-stage NMOS common-source amplifier with resistive voltage-divider biasing, source degeneration resistor, and source bypass capacitor. Demonstrates DC operating point extraction, small-signal AC gain, and transient amplification of a 10 kHz input.

### 03 - CMOS Differential Pair with Current Mirror Load
**File:** `03_cmos_diff_pair/cmos_diff_pair.cir`

CMOS differential amplifier using an NMOS input pair and PMOS active current mirror load. Driven by an ideal tail current source (100 µA). Includes DC transfer characteristic sweep, AC differential gain analysis, and operating point verification.

## How to Run

Install NGspice, then:

```bash
ngspice <filename>.cir
```

Or run in batch mode:

```bash
ngspice -b <filename>.cir
```

## Tools & Environment

- **Simulator:** NGspice 43+
- **MOSFET Models:** SPICE Level 1 (educational; substitute foundry models for production use)
- **Analysis types used:** `.op`, `.ac`, `.tran`, `.dc`
