# Discrete Transistor Audio Amplifier (±18V Supply)

A fully discrete multi-stage audio power amplifier designed, simulated, and implemented without the use of integrated circuits. The system amplifies a low-level microphone signal to drive an 8Ω loudspeaker with high gain, low distortion, and stable thermal performance.

---

## Project Overview

This project demonstrates the design of a complete analog audio amplification system using discrete BJTs. It focuses on signal conditioning, voltage amplification, and power delivery using a Class-AB output stage.

The design is validated through analytical calculations, SPICE simulation (LTspice), and hardware implementation.

---

## Specifications

- Voltage Gain (Av): ≥ 500 V/V (~54 dB)
- Verified Gain: ~510 V/V
- Frequency Response: 100 Hz – 12 kHz (-3 dB)
- Output Power: ~1.5 W (continuous)
- Load: 8Ω speaker
- Input Impedance: ≥ 100 kΩ (~110 kΩ achieved)
- Supply: ±18V (power stage), +18V (preamp stages)

---

## System Architecture

Microphone → Input Buffer → Gain Stage I → Gain Stage II → Gain Stage III → Class-AB Output Stage → 8Ω Speaker

---

## Circuit Design

### Input Stage
- AC coupling for DC isolation
- High-pass filtering for low-frequency control
- Stable biasing for microphone input

### Buffer Stage
- Transistor: 2N3904
- Common collector configuration (emitter follower)
- High input impedance (~100 kΩ)
- Prevents loading of microphone source

### Voltage Gain Stages

Stage I (CE with emitter degeneration):
- Gain: ~26 V/V
- Improved linearity and stability

Stage II (CE amplifier):
- Gain: ~25 V/V
- Provides main voltage amplification

### Power Output Stage (Class AB Push-Pull)
- Transistors: TIP41C (NPN), TIP42C (PNP)
- High current drive for 8Ω load
- Reduced crossover distortion
- 0.22Ω emitter resistors for thermal stability

---

## Simulation & Validation

### Gain Test
- Input: 1 kHz sine wave (8 mV peak)
- Output: Clean ±4 V waveform
- Verified gain > 500 V/V

### Frequency Response
- Bandwidth: 100 Hz – 12 kHz
- Stable -3 dB roll-off behavior

### Output Power Test
- Maximum undistorted output: ~1.5 W
- Load: 8Ω speaker

---

## Tools & Technologies

- LTspice
- Discrete BJT Design (2N3904, TIP41C, TIP42C)
- Analog Circuit Design
- Small-Signal Modeling
- Hardware Testing

---

## Key Features

- Fully discrete analog audio amplifier
- Multi-stage gain architecture
- Class-AB efficient output stage
- Strong agreement between theory, simulation, and hardware results
- Thermal stability and low distortion design

---

## Applications

- Audio amplifier design
- Analog electronics learning project
- ECD coursework project
