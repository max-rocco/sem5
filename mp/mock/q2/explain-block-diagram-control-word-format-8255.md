# Q. Explain block diagram & control word format of PPI 8255.

→ Block diagram

![](https://www.eeeguide.com/wp-content/uploads/2018/08/Pin-Diagram-of-8255-Microprocessor-3.jpg)

### Data Bus Buffer:
This tri-state bi-directional buffer is used to interface the internal data bus of 8255 Pin Diagram to the system data bus. 
Input or Output instructions executed by the CPU either Read data from, or Write data into the buffer. 
Output data from the CPU to the ports or control register, and input data to the CPU from the ports or status register are all passed through the buffer.

### Control Logic:
The control logic block accepts control bus signals as well as inputs from the address bus, 
and issues commands to the individual group control blocks (Group A control and Group B control). 
It issues appropriate enabling signals to access the required data/control words or status word. The input pins for the control logic section are described here.

### Group A and Group B Controls:
Each of the Group A and Group B control blocks receives control words from the CPU and issues appropriate commands to the ports associated with it. 
The Group A control block controls Port A and PC7-PC4 while the Group B control block controls Port B and PC3-PC0.

### Port A:
This has an 8-bit latched and buffered output and an 8-bit input latch. It can be programmed in three modes: mode 0, mode 1 and mode 2.

### Port B:
This has an 8-bit data I/O latch/ buffer and an 8-bit data input buffer. It can be programmed in mode 0 and mode 1.

### Port C:
This has one 8-bit unlatched input buffer and an 8-bit output latch/buffer. 
Port C can be splitted into two parts and each can be used as control signals for ports A and B in the handshake mode. 
It can be programmed for bit set/reset operation.

## Control Word Formats
A high on the RESET pin causes all 24 lines of the three 8-bit ports to be in the input mode. 
All flip-flops are cleared and the interrupts are reset. This condition is maintained even after the RESET goes low. 
The ports of the 8255 Pin Diagram can then be programmed for any other mode by writing a single control word into the control register, when required.

### Bit Reset Mode

![](https://www.eeeguide.com/wp-content/uploads/2018/08/Pin-Diagram-of-8255-Microprocessor-5.jpg)

* The eight possible combinations of the states of bits D3 – D1 (B2 B1 B0) in the Bit Set-Reset format (BSR) determine particular bit in 
PC0 – PC7 being set or reset as per the status of bit D0. A BSR word is to be written for each bit that is to be set or reset. 
For example, if bit PC3 is to be set and bit PC4 is to be reset, the appropriate BSR words that will have to be loaded into the 
control register will be, 0XXX0111 and 0XXX1000, respectively, where x is don’t care.

* The BSR word can also be used for enabling or disabling interrupt signals generated by Port C when the 8255 Pin Diagram is programmed for Mode 1 or 2 operation. 
This is done by setting or resetting the associated bits of the interrupts. This is described in detail in next section.

### I/O Mode

![](https://www.eeeguide.com/wp-content/uploads/2018/08/Pin-Diagram-of-8255-Microprocessor-6.jpg)

The control words for both, mode definition and Bit Set –Reset are loaded into the same control register, with bit D7 used for specifying whether 
the word loaded into the control register is a mode definition word or Bit Set-Reset word. 
If D7 is high, the word is taken as a mode definition word, and if it is low, it is taken as a Bit Set-Reset word. 
The appropriate bits are set or reset depending on the type of operation desired, and loaded into the control register.

<hr />

Sources

- https://www.eeeguide.com/8255-pin-diagram/