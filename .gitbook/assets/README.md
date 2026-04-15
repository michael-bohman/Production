# Software Programming Instructions 
These instructions identify the process for programming production-ready software into ILS hardware (Hw#: 23122).

1. Update *program-23122.bat* with required programming settings.  Variables to modify/verify are located at the top of the file and include:
	- ipeCmd: Location of the IPE tool on the users computer.
    - pgmDev: The programming device used.  Common programmer types are:
        - ICD4: The Microchip In-Circuit Debugger (ICD) - 4th generation.
        - RICE: The Microchip REAL ICE programmer.
        - PK3: The Microchip PICkit3 programmer.
		- PK4: The Microchip PICkit4 programmer.
2. Connect Microchip programmer between PC and pic32-6xIls board.
3. Connect pic32-6xIls USB power.
4. Double-click *program-23122.bat*.