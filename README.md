# Dispersion-Compensation
# Dispersion Compensation

## Objective
Design and simulate a fiber optic system using dispersion-compensating fiber to reduce chromatic dispersion.

## Theory
Dispersion-compensating fiber (DCF) provides an optical medium with a relatively large negative chromatic dispersion factor \(D(\lambda)\) at the operating wavelength.  

If a transmission fiber of length \(L_{TF}\) is connected in series with a DCF of length \(L_{DCF}\), then the total chromatic dispersion is given by:

\[
\Delta D_t(\lambda) = D_{TF}(\lambda) \cdot L_{TF} + D_{DCF}(\lambda) \cdot L_{DCF} \cdot \Delta \lambda
\]

where:
- \(D_{TF}(\lambda)\) = chromatic dispersion factor for the transmission fiber  
- \(D_{DCF}(\lambda)\) = chromatic dispersion factor for the DCF  
- \(\Delta \lambda\) = transmitter spectral width  

Similarly, the total attenuation loss of the two-fiber combination is:

\[
Loss = A_{TF} \cdot L_{TF} + A_{DCF} \cdot L_{DCF}
\]

Therefore, given target values for chromatic dispersion and attenuation loss plus specifications of the transmitter, fiber, and receiver, one can determine the lengths of the transmission fiber and the DCF by solving the above two equations simultaneously.

---

## Specifications
- **Output power:** 0 dBm  
- **Spectral width:** To be determined  
- **Operating wavelength:** 1550 nm  
- **Transmitter bit rate:** 2.5 Gb/s  
- **Transmission Fiber:** Corning SMF-28  
- **DCF:** See below  
- **Receiver sensitivity:** -35 dBm  
- **System margin + coupling loss attenuation:** 6 dB  

**DCF Parameters:**  
- Chromatic dispersion factor: –200 ps/nm-km at 1550 nm  
- Attenuation: 0.5 dB/km at 1550 nm  

---

## Calculations
1. Determine the maximum allowable fiber loss  
2. Determine the maximum allowable chromatic dispersion  
3. Based on the results of (1) and (2), determine the lengths of the transmission fiber and the DCF  

---

## Layout
The main physical components of this layout are:
1. **Transmitter:** Bit sequence generator, non-return to zero (NRZ) pulse generator, and a laser  
2. **Transmission fiber**  
3. **Dispersion compensation fiber (DCF)**  
4. **Receiver:** PIN detector and electrical filter  

**Notes:**  
- The NRZ scheme is used here. The signal does not return to zero between successive 1 bits, resulting in a narrower spectral width than a return-to-zero scheme.  
- Visualizer components included:  
  - Three Optical Time Domain visualizers (at transmitter output, after transmission fiber, and at the end of DCF)  
  - One Optical Spectrum Analyzer (at transmitter output, used to estimate spectral width)  

---

## Procedure
- Adjust the laser power to obtain 0 dBm transmission output.  
- Use the optical spectrum analyzer to determine the spectral width of the signal.  
  - Expect uncertainty since the spectrum is not clean.  
  - Provide a screen capture showing markers used to determine spectral width.  
- Set appropriate fiber lengths based on pre-lab calculations.  
- Run the simulation with all parameters set according to specifications.  
- Generate screen captures for inclusion in the report.  
- Measure:  
  - Optical power at receiver input  
  - Maximum Q factor  
  - Minimum BER  
- Record:  
  - Eye diagram  
  - Optical waveforms at transmitter output, junction between fibers, and receiver input  

---

## Further Simulation and Analysis
- Set the DCF length to 0 and run the simulation again.  
- Record similar measurements for comparison.  

---

## Tabulation 
![WhatsApp Image 2026-02-07 at 2 42 40 PM](https://github.com/user-attachments/assets/b956f1f6-eb6c-45a4-9ca0-3075a2d447cb)

## Calculation

![WhatsApp Image 2026-02-07 at 2 42 39 PM](https://github.com/user-attachments/assets/ce07b8b9-e3f3-4cee-8641-cbb756d27105)



---
## Conclusions
Discuss the effectiveness of dispersion-compensating fiber and the ability of the calculations to engineer a viable system.
