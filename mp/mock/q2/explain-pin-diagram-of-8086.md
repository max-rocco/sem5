# Q. Explain pin diagram of 8086.

→  Intel 8086 is a 16-bit HMOS microprocessor. 
It is available in 40 pin DIP chip. 
It uses a 5V DC supply for its operation. 
The 8086 uses 20-line address bus. 
It has a 16-line data bus. 
The 20 lines of the address bus operate in multiplexed mode. 
The 16-low order address bus lines have been multiplexed with data and 4 high-order address bus lines have been multiplexed with status signals.

**Pin Diagram**

<img src="https://media.geeksforgeeks.org/wp-content/uploads/pin_diagram_of_8086-1-1.png" />

**AD0-AD15**: Address/Data bus. These are low order address bus. They are multiplexed with data. 
When AD lines are used to transmit memory address the symbol A is used instead of AD, for example A0-A15. 
When data are transmitted over AD lines the symbol D is used in place of AD, for example D0-D7, D8-D15 or D0-D15.

**A16-A19**: High order address bus. These are multiplexed with status signals.

**S2, S1, S0**: Status pins. These pins are active during T4, T1 and T2 states and is returned to passive state (1,1,1 during T3 or Tw (when ready is inactive). 
These are used by the 8288 bus controller for generating all the memory and I/O operation) access control signals. 
Any change in S2, S1, S0 during T4 indicates the beginning of a bus cycle.

**A16/S3, A17/S4, A18/S5, A19/S6**: The specified address lines are multiplexed with corresponding status signals.

**BHE’/S7**: Bus High Enable/Status. During T1 it is low. It is used to enable data onto the most significant half of data bus, D8-D15. 
8-bit device connected to upper half of the data bus use BHE (Active Low) signal. It is multiplexed with status signal S7. S7 signal is available during T2, T3 and T4.

**RD’**: This is used for read operation. It is an output signal. It is active when low.

**READY** : This is the acknowledgement from the memory or slow device that they have completed the data transfer. 
The signal made available by the devices is synchronized by the 8284A clock generator to provide ready input to the microprocessor. The signal is active high(1).

**INTR** : Interrupt Request. This is triggered input. This is sampled during the last clock cycles of each instruction for determining the availability of the request. 
If any interrupt request is found pending, the processor enters the interrupt acknowledge cycle. 
This can be internally masked after resulting the interrupt enable flag. This signal is active high(1) and has been synchronized internally.

**NMI** : Non maskable interrupt. This is an edge triggered input which results in a type II interrupt. 
A subroutine is then vectored through an interrupt vector lookup table which is located in the system memory. 
NMI is non-maskable internally by software. A transition made from low(0) to high(1) initiates the interrupt at the end of the current instruction. 
This input has been synchronized internally.

**INTA** : Interrupt acknowledge. It is active low(0) during T2, T3 and Tw of each interrupt acknowledge cycle.

**MN/MX’** : Minimum/Maximum. This pin signal indicates what mode the processor will operate in.

**RQ’/GT1′, RQ’/GT0′** : Request/Grant. 
These pins are used by local bus masters used to forc the microprocessor to release the local bus at the end of the microprocessor’s current bus cycle. 
Each of the pin is bi-directional. RQ’/GT0′ have higher priority than RQ’/GT1′.

**LOCK’** : Its an active low pin. It indicates that other system bus masters have not been allowed to gain control of the system bus while LOCK’ is active low(0). 
The LOCK signal will be active until the completion of the next instruction.

**TEST’** : This examined by a ‘WAIT’ instruction. If the TEST pin goes low(0), execution will continue, else the processor remains in an idle state. 
The input is internally synchronized during each of the clock cycle on leading edge of the clock.

**CLK** : Clock Input. The clock input provides the basic timing for processing operation and bus control activity. 
Its an asymmetric square wave with a 33% duty cycle.

**RESET** : This pin requires the microprocessor to terminate its present activity immediately. The signal must be active high(1) for at least four clock cycles.

**Vcc** : Power Supply( +5V D.C.)

**GND** : Ground

**QS1,QS0** : Queue Status.

**DT/R** : Data Transmit/Receive. This pin is required in minimum systems, that want to use an 8286 or 8287 data bus transceiver. 
The direction of data flow is controlled through the transceiver.

**DEN** : Data enable. This pin is provided as an output enable for the 8286/8287 in a minimum system which uses transceiver. 
DEN is active low(0) during each memory and input-output access and for INTA cycles.

**HOLD/HOLDA** : HOLD indicates that another master has been requesting a local bus .This is an active high(1). 
The microprocessor receiving the HOLD request will issue HLDA (high) as an acknowledgement in the middle of a T4 or T1 clock cycle.

**ALE** : Address Latch Enable. ALE is provided by the microprocessor to latch the address into the 8282 or 8283 address latch. 
It is an active high(1) pulse during T1 of any bus cycle. ALE signal is never floated, is always integer.

<hr />

Sources

- https://www.geeksforgeeks.org/pin-diagram-8086-microprocessor/
