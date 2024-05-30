## Overview
This project involves the design of an analog voltmeter with overload protection, using various electronic components to ensure accurate measurement and circuit protection.

## Circuit Components

### 1. Overload Protection Circuit
- **BC558B Transistor**
  - Used to cutoff the input voltage when it exceeds 13V, protecting the main amplifier circuit.
  - Features high cutoff voltage and low saturation current.
- **LM358P**
  - Op-amp used to isolate the main circuit from the input and overload protection circuit.
- **16V Zener Diode**
  - Used to set the threshold voltage through the transistors, cutting off voltages higher than 13V to protect the main op-amp and the voltmeter panel.

### 2. Main Amplifying Circuit
- **LM358P**
  - Used as the non-inverting amplifier to amplify the input voltages according to the DC voltage.
- **Resistors (100KΩ, 50KΩ, 200KΩ)**
  - Used for range selection:
    - 100KΩ for general resistance.
    - 50KΩ for measuring the 10V range.
    - 200KΩ for measuring the 2.5V range.
- **Voltmeter Panel**
  - Indicates the measured voltage value.

### 3. Power Supply Circuit
1. **IN4001 Diodes**
   - Rectify the input AC voltage to obtain DC output voltage.
2. **2W, 400V 1μF Capacitor**
   - Reduces the voltage from 230V RMS to 34V RMS.
   - The 2W rating is to handle high current and protect components from high current.
3. **2W, 50V 1000μF Capacitor**
   - Reduces the ripple voltage of the DC output.
4. **LM7824 Voltage Regulator**
   - Regulates the voltage to a 24V DC output.
5. **2W, 1MΩ Resistor**
   - Prevents surge current from damaging the diode, voltage regulator, and other connected components.

