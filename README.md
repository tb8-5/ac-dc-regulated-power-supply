# AC-DC Regulated Power Supply

This project focused on building and characterizing regulated AC-DC power supply circuits. The lab used half-wave and full-wave rectifiers, filter capacitors, a Zener diode regulator, and an LM7805 linear regulator to convert a 12 VAC input into a more stable DC output.

The project evaluated how each circuit stage improved output stability, including ripple reduction, voltage regulation, dropout behavior, load regulation, and efficiency. Measurements were taken using an oscilloscope and digital multimeter, then compared with hand calculations and NI Multisim simulations.

## Project Overview

The goal of this project was to understand how an AC input signal can be converted into a regulated DC output through rectification, filtering, and voltage regulation.

The circuit progression started with simple diode rectifiers, then added capacitive filtering to reduce ripple. The design was then extended with Zener diode regulation and an LM7805 linear regulator to evaluate how different regulator approaches affect output voltage stability and efficiency.

## Key Skills Demonstrated

- AC-DC power conversion
- Half-wave and full-wave rectifier analysis
- Capacitive filtering and ripple reduction
- Zener diode voltage regulation
- LM7805 linear regulator characterization
- Oscilloscope and DMM measurement
- Ripple voltage and ripple frequency analysis
- Dropout voltage and load regulation testing
- Efficiency calculation
- NI Multisim circuit simulation
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

The first circuit used a single 1N4004 diode and load resistor to convert only the positive half-cycle of the AC waveform into a pulsating DC output. The diode blocked the negative half-cycle, producing a single-polarity waveform across the load.

This stage demonstrated the basic operation of diode rectification and showed why a half-wave rectifier produces a large amount of ripple when used as a DC power supply.

### 2. Half-Wave Rectifier with Filter Capacitor

A filter capacitor was added in parallel with the load resistor. The capacitor charged near the peak of the rectified waveform and discharged through the load between peaks.

Different capacitance values were tested to show how increasing capacitance reduces ripple voltage. Larger capacitors discharge more slowly, which keeps the output voltage closer to the peak value between conduction intervals.

### 3. Full-Wave Rectifier

A center-tapped transformer and two 1N4004 diodes were used to create a full-wave rectifier. Unlike the half-wave rectifier, the full-wave rectifier used both halves of the AC input waveform.

This doubled the ripple frequency from 60 Hz to 120 Hz, making the output easier to smooth with a filter capacitor.

### 4. Full-Wave Rectifier with Filter Capacitor

A filter capacitor was added to the full-wave rectifier. Since the capacitor was refreshed twice per AC cycle, the full-wave rectifier produced a smoother DC output than the half-wave rectifier with the same load.

A design challenge was used to reduce ripple to approximately 1 V peak-to-peak or less. Hand calculations predicted the needed capacitance, and oscilloscope measurements were used to verify the results.

### 5. Zener Diode Regulator

A Zener diode regulator was added to the filtered full-wave rectifier circuit to hold the load voltage near 5.1 V. The Zener regulator improved voltage stability, but it was inefficient because excess voltage and current were dissipated as heat through the resistor and diode.

The measured Zener regulator efficiency was approximately 3.1%.

### 6. LM7805 Linear Regulator

The Zener regulator was replaced with an LM7805 linear regulator to produce a regulated 5 V output. The LM7805 provided stronger voltage stability and better load regulation than the Zener regulator.

The regulator maintained an output near 5 V under different load conditions. Efficiency was still limited because the regulator dissipated excess input voltage as heat, but the LM7805 performed better than the Zener regulator under heavier load conditions.

Measured LM7805 efficiency values included approximately 6.94% for a 1 kΩ load and 19.8% for a 100 Ω load.

## Key Results

- Built and tested half-wave and full-wave rectifier circuits.
- Verified that full-wave rectification reduces ripple compared to half-wave rectification.
- Demonstrated that increasing filter capacitance reduces ripple voltage.
- Used ripple voltage equations to estimate capacitor values for target ripple levels.
- Compared oscilloscope waveforms with NI Multisim simulations.
- Built and tested both Zener diode and LM7805 voltage regulation stages.
- Measured regulator output voltage, ripple, dropout behavior, and efficiency.
- Confirmed that the LM7805 provided a more stable regulated 5 V output than the Zener regulator.

## What I Learned

This project showed how each stage of a regulated power supply improves output quality. The rectifier converts AC into pulsating DC, the capacitor reduces ripple, and the regulator stabilizes the voltage under changing load conditions.

The lab also showed the tradeoff between regulation and efficiency. Both the Zener diode and LM7805 regulator improved output stability, but both dissipated excess power as heat. The LM7805 provided stronger regulation and better efficiency under heavier load conditions, but still demonstrated the efficiency limitations of linear regulation.

## Full Writeup

[View the full PDF writeup](ECE%202201%20LAB%202.pdf)

## Contributors

- Teremun Beard
- Perry Flagg

## Repository Maintainer

Teremun Beard  
Electrical and Computer Engineering  
Worcester Polytechnic Institute
