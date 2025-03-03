# Runge-Kutta 4th Order Method for Lake Temperature Simulation

## 📌 Overview
This project implements the **Runge-Kutta 4th Order Method (RK4)** to simulate the temperature of a lake over time using meteorological input data. The model considers factors such as **solar radiation, air temperature, air pressure, wind speed, and lake geometry** to estimate temperature changes.

## 📂 Files
- **main_script.py** - Contains the implementation of the **RK4 method** for temperature simulation.
- **input data-minlake.xlsx** - Input Excel file with meteorological data.
- **output7-data-minlake.xlsx** - Output Excel file storing computed temperature values over time.

## 🛠 Features
- **Uses Runge-Kutta 4th Order Method** for numerical approximation of temperature.
- Reads meteorological **data from an Excel file**.
- Incorporates **lake geometry and meteorological constants**.
- Saves the computed results **to an Excel file**.

## 📌 Mathematical Formulation
The model solves the differential equation for **temperature change over time (dT/dt)** using the RK4 method:

\[ dT/dt = \frac{J_{sn} + \sigma (T_{air} + 273)^4 (A + 0.031\sqrt{e_{air}})(1 - R_l) - (em \cdot \sigma \cdot (T + 273)^4) - (c_1 \cdot f_{Uw} \cdot (T - T_{air})) - (f_{Uw} \cdot (4.596 \cdot e^{(17.27T)/(237.3+T)} - e_{air}))}{1.9388 \times 10^{-8}} \]

Where:
- \( \sigma \) = **Boltzmann constant**
- \( A, R_l, em, c_1 \) = **Various coefficients**
- \( f_{Uw} \) = **Function of wind speed**
- \( J_{sn}, T_{air}, e_{air}, Uw \) = **Meteorological inputs**

## 📜 Usage
### Prerequisites
Ensure you have Python and the required dependencies installed:
```sh
pip install pandas numpy openpyxl
```

### Running the Script
1. Place the **input Excel file** in the project directory.
2. Update the script with the correct file path.
3. Run the script:
```sh
python main_script.py
```
4. The computed temperature data will be saved in **output7-data-minlake.xlsx**.

## 📊 Example Output
```
S.No.      Time       Temperature  
1          0.00       4.1234  
2          1.00       4.5678  
...
```

## 🏗 Future Improvements
- Enhance accuracy by tuning model coefficients.
- Add data visualization for better analysis.
- Implement additional numerical methods for comparison.

---
🛠 Developed by **urjoshi** | 🌊 Numerical Modeling for Lake Temperature Simulation

