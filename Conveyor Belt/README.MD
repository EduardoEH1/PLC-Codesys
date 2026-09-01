## CONVEYOR BELT ##

### DESCRIPTION ###

This project simulates a conveyor belt control system using Ladder Logic (LD) in CODESYS. The system uses Start and Stop controls with seal-in logic to operate the conveyor motor, a simulated sensor to detect and count passing pieces, and a CTU counter to track production. When the preset number of pieces is reached, the conveyor automatically stops. The counter can then be reset to prepare the system for a new cycle.

### VARIBALE DECLARATION ###
The variable declaration contains the Boolean variables used for the simulated controls and sensor signals, the conveyor motor output, the CTU counter instance, and the variables used to store the counting status and current count

<img width="333" height="235" alt="Captura de pantalla 2026-08-27 145736" src="https://github.com/user-attachments/assets/e0c6e0bb-3c95-4ac4-9558-83c547407aeb" />

### PROGRAM LOGIC (LD) ###
The Ladder Logic is divided into two networks. The first network controls the conveyor motor using Start/Stop controls, seal-in logic, and an automatic stop condition. The second network handles piece detection and counting using a CTU counter.

<img width="963" height="309" alt="Captura de pantalla 2026-08-27 145816" src="https://github.com/user-attachments/assets/7edcbae2-b877-4e2b-b13f-95e19145b3d4" />

### DEMO ###

https://github.com/user-attachments/assets/d185350d-ab32-4d2a-b2f3-21061a301bf2

### What you see in the DEMO: ###

| Step                            | What you see                                             | What it means                                                                       |
| ------------------------------- | -------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| **Extra Step — Stop & Restart** |  StartButton: TRUE → FALSE THEN StopButton: TRUE → FALSE →| Demonstrates manual stopping and restarting of the conveyor.                        |
| **1. Start Conveyor**           | StartButton: TRUE → FALSE                              | The conveyor starts and remains running through seal-in logic.                      |
| **2. Detect & Count Pieces**    | PieceSensor: TRUE → FALSE (repeat)                     | Each sensor activation represents a passing piece and increases the counter by one. |
| **3. Automatic Stop**           | PieceCount reaches PV                                  | The preset count is reached and the conveyor stops automatically.                   |
| **4. Reset Counter**            | ResetCounter: TRUE → FALSE                             | The counter returns to zero and the system is ready for a new cycle.                |

