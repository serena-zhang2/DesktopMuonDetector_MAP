# Desktop Muon Detector – Data Simulation and Analysis

After building desktop muon detector (2022), this project acquires the data from the detector and performs basic data parsing and visualization. It demonstrates a full mini-pipeline from raw measurement generation to structured analysis and exploratory plots.

## Overview

The program generates synthetic detector measurements that mimic the output of a simple muon detection setup. Each measurement includes event counts, timing information, sensor readings, and environmental conditions. The data is written to a text file, read back into Python, parsed into structured lists, and visualized using histograms.

While the data in this implementation is simulated, the structure mirrors how real detector data would be logged and analyzed.

## Data Fields

Each line in the data file represents a single measurement and contains:

- **Muon count** – number of detected events
- **Time stamp** – time offset of the measurement
- **ADC value** – raw analog-to-digital converter output
- **Voltage** – detector voltage (simplified from ADC conversion)
- **Measurement deadtime** – detector recovery time
- **Temperature (°C)** – ambient temperature during measurement

## Program Workflow

1. **Data Generation**  
   Randomized measurement values are generated to simulate detector output and written to a text file.

2. **Data Ingestion**  
   The file is read line by line, parsed, and converted into structured Python lists for analysis.

3. **Data Organization**  
   Each measurement variable is separated into its own list to support independent analysis.

4. **Visualization**  
   Histograms are produced for each variable to inspect distributions and basic behavior.

## Tools and Libraries

- Python
- NumPy
- Matplotlib
- File I/O

## Notes

- This project focuses on data handling, structure, and visualization rather than physical detector calibration.
- The voltage value is used directly rather than derived from ADC conversion for simplicity.
- The program is intended as a demonstration of data analysis workflow rather than a production detector system.

