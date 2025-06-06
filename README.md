# Analog Integrated Circuit (IC) Design
---------------------------------------------------------------------------------------

## Summer Internship course 2025
---------------------------------------------------------------------------------------
### COURSE OUTCOME
- Design of Analog ICs in the context of electronic system design
- Deriving IC specifications from the host electronic system.
- A good understanding of CMOS devices & technology.
- Proficiency in analog circuit design and analysis.
- Mastery of design tools: ngspice, xscheme, magic, netgen & Python.

### COURSE DETAIlL
***1. Introduction to an electronic system design, a plug-n-play USB-MIDI microphone.***
 - Microphone pre-amplifier and interface circuit design.
 - Select an widely available Op-Amp for the preamplifier e.g. TI OPA 344
 - Derive the important specs for the CMOS Op-Amp design.

***2. Introduction to linear circuits and passive devices***
 - Understanding passive devices (RLC) using basic EM principles.
 - Principle of linearity and superposition
 - Network analysis: KCL, KVL, node theorems, Thevenin, Norton
 - Emphasis on interfacing circuits and power transfer principle.

### SOURCES & REFFERENCES
1. MEMS mic [Datasheet](https://cdn.sparkfun.com/assets/0/5/8/b/1/SPH8878LR5H-1_Lovato_DS.pdf)
2. OP-AMP-344 [Datasheet](https://www.ti.com/lit/ds/symlink/opa344.pdf?ts=1747822666491&ref_url=https%253A%252F%252Fwww.google.com%252F)
3. Mic module [Product](https://www.sparkfun.com/sparkfun-analog-mems-microphone-breakout-sph8878lr5h-1.html)
4.  Mic module schematic [Schematic](https://cdn.sparkfun.com/assets/7/5/6/e/d/SparkFun_Analog_MEMS_Microphone_Breakout_SPH8878LR5H-1.pdf)


-------------------------------------------------------------------------------------------------------------------------------------------------------

### Day-1 
**Calculating Thevenin Equivalent of Microphone**

Key specs from the microphone [Datasheet](https://cdn.sparkfun.com/assets/0/5/8/b/1/SPH8878LR5H-1_Lovato_DS.pdf) and research:
- Sensitivty: -44 dBV/Pa
- Condition: 94 dB SPL at 1 kHz which is sound pressure of 1 Pa
- Normal voice conversation is typically 60 dB SPL
- **Vth Calculation**
  - Voice (Pa) = $10^{(60-94)/20} = 19.9\times 10^{-3} Pa$
  - Output (Vpk) = $\sqrt{2}\times V_{rms} = \sqrt{2}\times 19.9\times 10^{-3} Pa \times 10^{-44/20} = 178 \mu Vpk$
  - **$V_{out-pk} = 0.178~ mV$**
- **Rth** (from datasheet) = 380 ohms
