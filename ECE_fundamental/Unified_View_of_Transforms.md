# Unified View of Laplace Transform, Fourier Transform, Z-Transform, and the RLC Circuit

## Overview of the Three Major Transforms

| Transform | Domain | Time Range | Definition | Kernel | Variable | Use Case |
|-----------|--------|------------|------------|---------|----------|-----------|
| Laplace | Continuous | t ≥ 0 | <img src="https://latex.codecogs.com/svg.latex?F(s)=\int_0^\infty%20f(t)e^{-st}dt"/> | <img src="https://latex.codecogs.com/svg.latex?e^{-st}"/> | <img src="https://latex.codecogs.com/svg.latex?s=\sigma+j\omega"/> | Unified transient and frequency response |
| Fourier | Continuous | -∞ < t < ∞ | <img src="https://latex.codecogs.com/svg.latex?F(j\omega)=\int_{-\infty}^{\infty}f(t)e^{-j\omega%20t}dt"/> | <img src="https://latex.codecogs.com/svg.latex?e^{-j\omega%20t}"/> | <img src="https://latex.codecogs.com/svg.latex?j\omega"/> | Frequency spectrum analysis |
| Z | Discrete | n ≥ 0 | <img src="https://latex.codecogs.com/svg.latex?X(z)=\sum_{n=0}^{\infty}x[n]z^{-n}"/> | <img src="https://latex.codecogs.com/svg.latex?z^{-n}"/> | <img src="https://latex.codecogs.com/svg.latex?z=re^{j\omega}"/> | DSP & digital filters |

**Key Relationships:**
- Fourier Transform is a special case of Laplace Transform when <img src="https://latex.codecogs.com/svg.latex?\sigma=0"/>
- Discrete Fourier Transform is a special case of Z-transform on the unit circle (<img src="https://latex.codecogs.com/svg.latex?z=e^{j\omega}"/>)

## Introduction

This document provides a unified perspective on the fundamental transforms in electrical engineering and their relationship with RLC circuits.

## Table of Contents
1. [Laplace Transform](#laplace-transform)
2. [Fourier Transform](#fourier-transform)
3. [Z-Transform](#z-transform)
4. [RLC Circuit Analysis](#rlc-circuit-analysis)
5. [Connections and Relationships](#connections-and-relationships)

## Laplace Transform

The Laplace transform is defined as:

<img src="https://latex.codecogs.com/svg.latex?F(s)=\int_0^\infty%20f(t)e^{-st}dt"/>

## Fourier Transform

The Fourier transform is defined as:

<img src="https://latex.codecogs.com/svg.latex?F(j\omega)=\int_{-\infty}^{\infty}f(t)e^{-j\omega%20t}dt"/>

## Z-Transform

The Z-transform is defined as:

<img src="https://latex.codecogs.com/svg.latex?X(z)=\sum_{n=0}^{\infty}x[n]z^{-n}"/>

## RLC Circuit Analysis

### RLC Circuit (Series):
\[
v_{in}(t) = R i(t) + L \frac{di(t)}{dt} + \frac{1}{C} \int i(t) dt
\]

### 📍 Laplace Domain:
Apply Laplace Transform:
\[
V_{in}(s) = I(s) \left(R + sL + \frac{1}{sC}\right) \Rightarrow H(s) = \frac{I(s)}{V_{in}(s)}
\]

- Pole-zero structure tells us about **system behavior & stability**
- Set \( s = j\omega \) to get **frequency response**

### 🌊 Fourier Domain:
Assume sinusoidal input:
\[
v_{in}(t) = V_0 \cos(\omega t) \Rightarrow H(j\omega)
\]

- Capacitor: \( \frac{1}{j\omega C} \)  
- Inductor: \( j\omega L \)

Useful for **Bode plots, resonance, filtering**

### 🧮 Z-Domain:
Discretize the RLC system using Tustin/backward difference:
- \( \frac{di}{dt} \approx \frac{i[n] - i[n-1]}{T} \)
- \( \int i dt \approx T \sum i[n] \)

Leads to:
\[
V_{in}(z) = I(z) \cdot Z_{equiv}(z)
\]
Used for **digital simulation, embedded control**

## Connections and Relationships

## References
