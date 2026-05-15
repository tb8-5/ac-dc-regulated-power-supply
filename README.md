# AC-DC Regulated Power Supply

This project implements and characterizes an AC-DC regulated power supply using diode rectification, capacitive filtering, and voltage regulation. The power supply converts a 12 VAC transformer input into a more stable DC output by progressing through half-wave rectification, full-wave rectification, filter capacitors, Zener regulation, and LM7805 linear regulation.

## Project Overview

The circuit was built around the process of converting an AC input waveform into a regulated DC output. The lab began with half-wave and full-wave rectifier circuits using 1N4004 diodes. Filter capacitors were then added to reduce ripple voltage and improve output stability.

The design was extended with a Zener diode regulator and an LM7805 linear regulator to compare different methods of voltage regulation. Oscilloscope and DMM measurements were used to evaluate ripple behavior, voltage stability, load regulation, dropout behavior, and efficiency.

## Key Skills Demonstrated

- AC-DC power conversion
- Half-wave and full-wave rectifier analysis
- Diode circuit behavior
- Capacitive filtering and ripple reduction
- Zener diode voltage regulation
- LM7805 linear regulator characterization
- Oscilloscope waveform measurement
- DMM voltage and current measurement
- Ripple voltage and ripple frequency analysis
- Dropout voltage and load regulation testing
- Efficiency calculation
- NI Multisim circuit simulation
- Technical documentation

## Tools and Components

- 12 VAC transformer
- 1N4004 diodes
- Zener diode
- LM7805 linear regulator
- Electrolytic capacitors
- Load resistors
- Sense resistor
- Oscilloscope
- Digital multimeter
- Function generator
- DC power supply
- NI Multisim
- Breadboard and jumper wires

## Circuit Blocks

The AC-DC power supply was organized into six main stages:

1. **Half-wave rectifier**  
   A single 1N4004 diode allowed current to flow during the positive half-cycle of the transformer output while blocking the negative half-cycle.

2. **Half-wave rectifier with filter capacitor**  
   A capacitor was placed in parallel with the load resistor to charge near the waveform peak and discharge through the load between conduction intervals, reducing ripple.

3. **Full-wave rectifier**  
   A center-tapped transformer and two 1N4004 diodes produced two positive pulses per AC cycle, doubling the ripple frequency to 120 Hz.

4. **Full-wave rectifier with filter capacitor**  
   A filter capacitor was added to smooth the full-wave rectified output. Because the capacitor was refreshed twice per cycle, less capacitance was needed to reduce ripple compared to the half-wave design.

5. **Zener diode regulator**  
   A Zener diode regulator was added to clamp the load voltage near 5.1 V and reduce ripple. This improved voltage stability but had low efficiency because excess power was dissipated as heat.

6. **LM7805 linear regulator**  
   The Zener regulator was replaced with an LM7805 linear regulator to produce a stable 5 V output. The regulator improved load regulation and efficiency compared to the Zener circuit.

## Oscilloscope Results

### Half-Wave Rectifier with Filter Capacitor

![Half-wave rectifier with 10 uF capacitor](images/half_wave_filter_10uf.png)

This waveform shows the half-wave rectifier output with a 10 uF filter capacitor. The output has visible ripple because the capacitor only recharges once per AC cycle.

### Half-Wave Ripple Reduction

![Half-wave rectifier with 330 uF capacitor](images/half_wave_filter_330uf.png)

This waveform shows the half-wave rectifier output with a larger 330 uF capacitor. The increased capacitance reduced ripple by allowing the capacitor to discharge more slowly through the load.

### Full-Wave Rectifier with Filter Capacitor

![Full-wave rectifier with 200 uF capacitor](images/full_wave_filter_200uf.png)

This waveform shows the full-wave rectifier output with filtering. The capacitor is refreshed twice per AC cycle, reducing ripple compared to the half-wave rectifier.

### Zener Regulator Output

![Zener regulated output](images/zener_regulator_output.png)

This waveform shows the Zener regulator holding the load voltage near 5.1 V while reducing ripple compared to the unregulated rectifier output.

### LM7805 Regulated Output

![LM7805 regulated output](images/lm7805_regulated_output.png)

This waveform shows the LM7805 regulator producing a stable 5 V output under load.

## Key Results

- Built and tested half-wave and full-wave rectifier circuits.
- Verified that the half-wave rectifier blocks the negative half-cycle of the transformer output.
- Confirmed that full-wave rectification doubles the ripple frequency to 120 Hz.
- Demonstrated that increasing filter capacitance reduces ripple voltage.
- Used a 330 uF capacitor to reduce half-wave ripple to approximately 1 V peak-to-peak.
- Used two 100 uF capacitors in parallel to create 200 uF for the full-wave ripple reduction design challenge.
- Compared experimental oscilloscope waveforms with NI Multisim simulations.
- Built and tested a Zener diode regulator with an output near 5.1 V.
- Measured Zener regulator efficiency at approximately 3.1%.
- Built and tested an LM7805 linear regulator with a stable 5 V output.
- Measured LM7805 efficiency at approximately 6.94% with a 1 kΩ load and 19.8% with a 100 Ω load.
- Verified that the LM7805 provided better regulation and efficiency than the Zener regulator.

## Full Writeup

[View the full PDF writeup](writeup/ECE_2201_Lab_2_Diode_Applications.pdf)

## Contributors

- Teremun Beard
- Perry Flagg

## Repository Maintainer

Teremun Beard  
Electrical and Computer Engineering  
Worcester Polytechnic Institute
