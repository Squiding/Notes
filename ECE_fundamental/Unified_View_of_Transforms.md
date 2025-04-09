# 📘 Unified View of Laplace Transform, Fourier Transform, Z-Transform, and the RLC Circuit

## 🔰 Motivation: Why These Transforms?
Real-world systems (e.g., analog circuits, control systems, DSP) are input-output systems governed by differential or difference equations. Solving these equations directly is hard, especially with initial conditions. So, we apply transformations:

- **Laplace Transform**: For continuous systems, including transient and steady-state.
- **Fourier Transform**: For continuous-time frequency analysis.
- **Z-Transform**: For discrete-time systems.

---

## 🧩 Overview of the Three Major Transforms

| Transform | Domain | Time Range | Definition | Kernel | Variable | Use Case |
|----------|--------|------------|------------|--------|----------|----------|
| Laplace | Continuous | \( t \geq 0 \) | \( F(s) = \int_0^\infty f(t)e^{-st}dt \) | \( e^{-st} \) | \( s = \sigma + j\omega \) | Unified transient and frequency response |
| Fourier | Continuous | \( t \in (-\infty, \infty) \) | \( F(j\omega) = \int_{-\infty}^{\infty} f(t)e^{-j\omega t} dt \) | \( e^{-j\omega t} \) | \( \omega \) | Frequency spectrum analysis |
| Z | Discrete | \( n \geq 0 \) | \( X(z) = \sum_{n=0}^\infty x[n] z^{-n} \) | \( z^{-n} \) | \( z = re^{j\omega} \) | DSP & digital filters |

🌀 Fourier Transform is a special case of Laplace Transform when \( \sigma = 0 \)  
🌀 Discrete Fourier Transform is a special case of Z-transform on the unit circle \( z = e^{j\omega} \)

---

## ⚡ RLC Circuit Under These Transforms

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

---

## 🎯 General System Response Comparison

| Domain | Time Domain | Transform | Convolution | Algebraic Form |
|--------|-------------|-----------|-------------|----------------|
| Continuous | \( y(t) = h(t) * x(t) \) | Laplace/Fourier | \( y(t) = \int h(\tau)x(t-\tau) d\tau \) | \( Y(s) = H(s)X(s) \) |
| Discrete | \( y[n] = h[n] * x[n] \) | Z-Transform | \( y[n] = \sum h[k]x[n-k] \) | \( Y(z) = H(z)X(z) \) |

---

## 🔧 Interpreting the Frequency Variables

### ✅ Continuous:
- \( s = \sigma + j\omega \)
  - \( \omega \): Oscillation frequency
  - \( \sigma \): Exponential decay/growth
  - **Stability**: Poles must lie in the left-half plane (\( \sigma < 0 \))

### ✅ Discrete:
- \( z = r e^{j\omega} \)
  - \( r \): Magnitude (stability if \( r < 1 \))
  - \( \omega \): Digital frequency
  - **Stability**: Poles inside unit circle

---

## 🧠 Summary Table: Transform Domain View

| Domain | Time Function | Kernel | Frequency View | Stability Criterion |
|--------|---------------|--------|----------------|----------------------|
| Laplace | \( f(t) \) | \( e^{-st} \) | Set \( s = j\omega \) | Poles in LHP |
| Fourier | \( f(t) \) | \( e^{-j\omega t} \) | Entire real axis | Signal must be energy bounded |
| Z | \( x[n] \) | \( z^{-n} \) | \( z = e^{j\omega} \) | Poles in unit circle |

---

Let me know if you want visual illustrations (e.g. s-plane or z-plane plots), or RLC simulations using Python or MATLAB.
