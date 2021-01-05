# Q. Explain operating modes of 8253 with timing diagram.

→ 8253/54 can be operated in 6 different modes.

### Mode 0 ─ Interrupt on Terminal Count

* It is used to generate an interrupt to the microprocessor after a certain interval.
* Initially the output is low after the mode is set. The output remains LOW after the count value is loaded into the counter.
* The process of decrementing the counter continues till the terminal count is reached, i.e., 
the count become zero and the output goes HIGH and will remain high until it reloads a new count.
* The GATE signal is high for normal counting. When GATE goes low, counting is terminated and the current count is latched till the GATE goes high again.

### Mode 1 – Programmable One Shot

* It can be used as a mono stable multi-vibrator.
* The gate input is used as a trigger input in this mode.
* The output remains high until the count is loaded and a trigger is applied.

### Mode 2 – Rate Generator

* The output is normally high after initialization.
* Whenever the count becomes zero, another low pulse is generated at the output and the counter will be reloaded.

### Mode 3 – Square Wave Generator

* This mode is similar to Mode 2 except the output remains low for half of the timer period and high for the other half of the period.

### Mode 4 − Software Triggered Mode

* In this mode, the output will remain high until the timer has counted to zero, at which point the output will pulse low and then go high again.
* The count is latched when the GATE signal goes LOW.
* On the terminal count, the output goes low for one clock cycle then goes HIGH. This low pulse can be used as a strobe.

### Mode 5 – Hardware Triggered Mode

* This mode generates a strobe in response to an externally generated signal.
* This mode is similar to mode 4 except that the counting is initiated by a signal at the gate input, which means it is hardware triggered instead of software triggered.
* After it is initialized, the output goes high.
* When the terminal count is reached, the output goes low for one clock cycle.
