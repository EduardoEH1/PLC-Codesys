## Tank Filling and Draining System ##

### DESCRIPTION ###
This project simulates an automated tank filling and draining system using Ladder Logic (LD) in CODESYS. The system automatically fills a tank until a high-level sensor is reached, waits for a preset time, and then drains the tank until the low-level sensor is activated. Start/Stop controls, level sensors, timers, and sequential logic are used to control the complete process.

### VARIBALE DECLARATION ###
The variable declaration contains the simulated Start/Stop controls, high and low level sensors, inlet and outlet valve outputs, process stage variables, and the TON timer used for the waiting stage. It also includes a TIME variable to track the elapsed timer value.

<img width="293" height="286" alt="Captura de pantalla 2026-08-31 172228" src="https://github.com/user-attachments/assets/0c52093e-5eed-4b0b-8317-29cccb59f670" />



### PROGRAM LOGIC (LD) ###
The Ladder Logic is divided into seven networks. The first network controls the Start/Stop operation and keeps the cycle active using seal-in logic. The following networks control the filling stage, inlet valve, waiting stage, and TON timer. The final networks control the draining stage and stop the process when the low-level sensor is reached.

<img width="940" height="543" alt="Captura de pantalla 2026-08-31 172531" src="https://github.com/user-attachments/assets/11300ac6-a77d-4f09-a35a-1ee94b8cd673" />



### DEMO ###

https://github.com/user-attachments/assets/8257a87d-4654-4e7e-a1a0-de45153e648b

