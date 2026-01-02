#  Traffic Light Control System

This project is a **Smart Traffic Light Control System** designed using the DMC8 microprocessor architecture. Hardware and software integration is implemented on the Deeds Simulator.

##  Key Features

* **Dual CPU Architecture:** 4-Bit Handshaking communication between Master and Slave processors.
* **Hardware Optimized Wiring:** Pedestrian lights are integrated into the vehicle lights using hardware logic gates (Hardware Logic) to reduce software overhead. This optimizes both the code line count and port usage.
* **Polling-Based Control:** Instant response time is ensured using high-frequency "Software Polling" instead of interrupts.
* **Night Mode (Safety Mode):** A physical switch instantly triggers the system to enter "Yellow Flashing" mode.
* **Right-Turn Logic:** When vehicles have a green light, the pedestrian crossing on their right-turn path is automatically prioritized.

##  Technologies Used

* **Language:** DMC8 Assembly Language
* **Simulation:** Deeds Simulator
* **Hardware:** DMC8 CPU, PIO, 7-Segment Display, Traffic Light Modules

##  How to Run the Project

To simulate this project on your machine, follow these steps:

1.  **Install Deeds:** Ensure that [Deeds Simulator](https://www.digitalelectronicsdeeds.com/downloads.html#) is installed.
2.  **Open the Circuit:**
    * Launch `Deeds - Digital Circuit Simulator`.
    * Go to **File > Open** and select the circuit file located in: `src/TrafficLights.pbs` (or whatever you named your pbs file).
    * *The project is designed to open with all codes pre-loaded and ready to run.*
3.  **Verify Code Loading (If needed):**
    * Typically, the code loads automatically. However, if the processors appear empty or throw a "File not found" error:
    * **Double-click** (Left Click) on the **Master CPU** component.
    * In the opened window, locate the **"Source Code"** tab or "Load" button.    
    * Select/Load the `src/Master.mc8` file provided in the project folder.
    * *(Repeat this step for the **Slave CPU** using `src/Slave.mc8` if applicable).*
4.  **Start Simulation:**
    * Click the **Start Animation(F9)** button on the Deeds toolbar.
    * **Initialize System:** The system will not start automatically. Toggle the **RESET Switch** to position `1` (High) to begin the main loop.
    * **Interact with the System:**
        * **Pedestrian Buttons:** Press the directional buttons to trigger the traffic light change sequence.
        * **Night Mode:** Toggle the Night Mode switch to activate the "Flashing Yellow" safety state (and toggle back to resume normal operation).

##  File Structure

* `src/`: Assembly source codes and circuit file.
* `images/`: Circuit diagrams and simulation screenshots.
* `ProjectReport.pdf`: Detailed project documentation and analysis.