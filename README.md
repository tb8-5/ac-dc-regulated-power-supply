# AC-DC Regulated Power Supply

This project focused on designing, building, simulating, and testing diode-based AC-DC power supply circuits. The lab started with basic half-wave and full-wave rectifiers, then added capacitive filtering and voltage regulation to improve the stability of the DC output. The final stages used both a Zener diode regulator and an LM7805 linear regulator to create a more constant output voltage under different load conditions.

## Project Overview

The goal of this project was to understand how an AC signal can be converted into a regulated DC voltage using rectification, filtering, and regulation. The circuits were built and tested using a 12 VAC transformer, 1N4004 diodes, electrolytic capacitors, a Zener diode, and an LM7805 linear regulator.

Measurements were taken using an oscilloscope and digital multimeter, then compared with theoretical calculations and NI Multisim simulations.

## Key Skills Demonstrated

- AC-DC power conversion
- Half-wave and full-wave rectifier analysis
- Capacitive filtering and ripple reduction
- Zener diode voltage regulation
- LM7805 linear regulator testing
- Oscilloscope and DMM measurement
- Ripple voltage and dropout voltage analysis
- Circuit simulation using NI Multisim
- Breadboarding and hardware debugging
- Comparing theory, simulation, and measured results

## Tools and Components

### Equipment
- 12 VAC transformer
- DC power supply
- Digital multimeter
- Oscilloscope
- Function generator
- ECE lab kit

### Components
- 1N4004 diodes
- Electrolytic capacitors
- Zener diode
- LM7805 linear regulator
- Load resistors
- Sense resistor
- Breadboard and jumper wires

## Circuit Stages

### 1. Half-Wave Rectifier

The first circuit used a single 1N4004 diode and a load resistor to convert only the positive half-cycle of the AC waveform into a pulsating DC output. The negative half-cycle was blocked by the diode.

This stage demonstrated the basic behavior of diode rectification and showed that a half-wave rectifier produces a large ripple because the capacitor, when added, is only recharged once per AC cycle.

### 2. Half-Wave Rectifier with Filter Capacitor

A capacitor was placed in parallel with the load resistor to reduce ripple. The capacitor charged near the peak of the rectified waveform and discharged through the load between peaks.

Different capacitor values were tested, including 10 µF, 100 µF, and 330 µF. Increasing capacitance reduced the ripple voltage because the capacitor discharged more slowly between waveform peaks.

### 3. Full-Wave Rectifier

A center-tapped transformer and two diodes were used to create a full-wave rectifier. Unlike the half-wave rectifier, the full-wave circuit used both halves of the AC input waveform, producing two positive pulses per cycle.

This doubled the ripple frequency from 60 Hz to 120 Hz, making the output easier to smooth with a capacitor.

### 4. Full-Wave Rectifier with Filter Capacitor

A filter capacitor was added to the full-wave rectifier. Since the capacitor was refreshed twice per cycle, the full-wave design produced less ripple than the half-wave rectifier using a similar load and capacitance.

The lab included a design challenge to reduce ripple to approximately 1 V peak-to-peak or less. Calculations predicted the needed capacitance, and the measured oscilloscope results supported the theoretical relationship between capacitance and ripple voltage.

### 5. Zener Diode Regulator

A Zener diode regulator was added to the filtered full-wave rectifier circuit to hold the load voltage near 5.1 V. The output voltage became more stable, but the efficiency was low because excess voltage and current were dissipated as heat through the resistor and Zener diode.

The measured Zener regulator efficiency was approximately 3.1%.

### 6. LM7805 Linear Regulator

The Zener diode was replaced with an LM7805 linear regulator to produce a regulated 5 V output. The LM7805 provided improved voltage stability and better load regulation compared to the Zener regulator.

The regulator maintained an output near 5 V across different load conditions, though efficiency was still limited because excess input voltage was dissipated as heat.

Measured LM7805 efficiency values included approximately 6.94% for a 1 kΩ load and 19.8% for a 100 Ω load.

## Key Results

- Built and tested half-wave and full-wave rectifier circuits.
- Verified that full-wave rectification reduces ripple compared to half-wave rectification.
- Demonstrated that increasing filter capacitance reduces ripple voltage.
- Used ripple voltage equations to estimate required capacitance values.
- Compared experimental oscilloscope waveforms with NI Multisim simulations.
- Built and tested both Zener diode and LM7805 voltage regulation circuits.
- Measured regulator performance, dropout behavior, and efficiency.
- Confirmed that the LM7805 provided a more stable regulated 5 V output than the Zener regulator.

## What I Learned

This project showed how each stage of a power supply improves the quality of the output voltage. The rectifier converts AC to pulsating DC, the capacitor reduces ripple, and the regulator improves voltage stability under changing loads.

The lab also highlighted the tradeoff between voltage regulation and efficiency. While both the Zener diode and LM7805 helped stabilize the output, both dissipated excess power as heat. The LM7805 performed better than the Zener regulator, especially under heavier load conditions, but still showed the efficiency limitations of linear regulation.
