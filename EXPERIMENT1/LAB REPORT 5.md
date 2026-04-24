# 📡 EXPERIMENT #1 – Full Demodulation of a QPSK Signal

## 🧪 Introduction

Quadrature Phase Shift Keying (QPSK) is a bandwidth-efficient digital modulation scheme that transmits two bits per symbol. By utilizing two orthogonal carriers (sine and cosine) of the same frequency, QPSK effectively reduces the required bandwidth compared to Binary Phase Shift Keying (BPSK) for the same data rate.

This experiment focuses on the generation, transmission, and coherent demodulation of a QPSK signal using the **Emona Telecoms-Trainer 101**. It demonstrates how digital data is split, modulated, affected by channel conditions, and ultimately recovered at the receiver.

---

## 🎯 Objectives

* Demonstrate serial-to-parallel and parallel-to-serial data conversion
* Implement a mathematical model of a QPSK modulator
* Model channel effects such as noise and phase shifts
* Perform full demodulation using synchronous detection
* Analyze the effect of Signal-to-Noise Ratio (SNR) on signal recovery

---

## 🔧 Materials and Equipment

* Emona Telecoms-Trainer 101
* Oscilloscope
* Patch cords
* Signal generator modules
* Low-pass filters (LPF)

---

## 🧩 Methodology

### 🔹 Part A – Verifying Serial-to-Parallel & Parallel-to-Serial Conversion

A serial bitstream is split into two parallel streams and later recombined.

**Observation:**
The reconstructed signal matches the original but with a slight delay.

**Answer to Question 1:**
Yes, both signals are identical in sequence, but a time delay exists due to processing latency introduced by conversion blocks.

---

### 🔹 Part B – Generating a QPSK Signal

The input bitstream is divided into:

* Even bits → modulated using cosine carrier
* Odd bits → modulated using sine carrier

These two BPSK signals are summed to produce the QPSK waveform.

**Answer to Question 2:**
The signals are offset because the bitstream is split into alternating bits. Each branch carries half the data rate, doubling symbol duration while maintaining a 90° phase difference for orthogonality.

---

### 🔹 Part C – Modelling Channel Conditions

Noise and phase shifts are introduced to simulate real-world transmission effects.

**Key Insight:**

* Noise distorts amplitude
* Phase shift affects demodulation accuracy

---

### 🔹 Part D – Full Demodulation of QPSK Signal

The received signal is demodulated using:

* Product detectors
* Locally generated carriers (sine and cosine)
* Low-pass filters (LPF)

**Answer to Question 4:**
The recovered signals are the original even-bit and odd-bit streams.

**Answer to Question 5:**
Due to orthogonality, sine and cosine carriers do not interfere. The LPF isolates the intended baseband signal by filtering out high-frequency components.

**Answer to Question 7:**
Correct mapping of signals is critical. If I (in-phase) and Q (quadrature) components are swapped, the reconstructed data becomes corrupted due to incorrect bit ordering.

---

### 🔹 Part E – Observations of Channel Noise

Noise levels were varied to observe signal degradation.

**Findings:**

* At low noise levels (-20 dB), signal recovery is reliable
* At high noise levels (0 dB), errors significantly increase

---

## 📊 Results and Discussion

The experiment successfully demonstrated:

* Accurate generation of QPSK signals using orthogonal carriers
* Effective recovery of transmitted data through coherent demodulation
* Sensitivity of QPSK systems to phase synchronization
* Direct relationship between SNR and Bit Error Rate (BER)

Even minor phase mismatches introduced noticeable cross-talk between channels, confirming the importance of synchronization in practical systems.

---

## 📘 Learnings

* QPSK improves bandwidth efficiency by transmitting two bits per symbol
* Orthogonality (90° phase shift) is essential for channel separation
* Carrier synchronization is critical for accurate demodulation
* Digital communication systems can tolerate small noise levels but degrade rapidly under high noise conditions

---

## ✅ Conclusion

This experiment validated the complete QPSK communication process—from data splitting and modulation to transmission and demodulation. The Emona Telecoms-Trainer effectively demonstrated theoretical concepts in a practical setup.

It is concluded that while QPSK offers superior spectral efficiency, its performance is highly dependent on:

* Accurate carrier phase synchronization
* Favorable Signal-to-Noise Ratio (SNR)

Failure in either condition leads to increased bit errors and unreliable communication.

---

## 📁 Repository Structure

```
📦 QPSK-Lab-Report
 ┣ 📂 assets
 ┃ ┣ 📜 EX5_PARTA.jpg
 ┃ ┣ 📜 EX5_PARTB.jpg
 ┃ ┣ 📜 EX5_PARTC.jpg
 ┃ ┣ 📜 EX5_PARTD.jpg
 ┃ ┗ 📜 EX5_PARTE.jpg
 ┣ 📜 README.md
```

---

## 👩‍💻 Author

**Marygrace Lapid**
Electronics Engineering Student

---


⭐ *If this helped you, feel free to star the repository!*
