# Q. Explain the architecture of the Pentium processor.

→ The Pentium family of processors originated from the 80486 microprocessor.
The term 'Pentium processor' refers to a family of microprocessors that share a common architecture and instruction set.
It runs at a clock frequency of either 60 or 66 MHz and has 3.1 million transistors.
Some of the features of Pentium architecture are:

- Complex Instruction Set Computer (CISC) architecture with Reduced Instruction Set Computer (RISC) performance.
- 64-Bit Bus
- Upward code compatibility.
- Pentium processor uses Superscalar architecture and hence can issue multiple instructions per cycle.
- Multiple Instruction Issue (MII) capability.
- Pentium processor executes instructions in five stages.
  This staging, or pipelining, allows the processor to overlap multiple instructions so that it takes less time to execute two instructions in a row.
- The Pentium processor fetches the branch target instruction before it executes the branch instruction.
- The Pentium processor has two separate 8-kilobyte (KB) caches on chip, one for instructions and one for data.
  It allows the Pentium processor to fetch data and instructions from the cache simultaneously.
- When data is modified, only the data in the cache is changed.
  Memory data is changed only when the Pentium processor replaces the modified data in the cache with a different set of data
- The Pentium processor has been optimized to run critical instructions in fewer clock cycles than the 80486 processor.

**Architecture**

![](https://i.imgur.com/7CQ1Vhk.png)

**Operating Modes**

→ The Pentium processor has two primary operating modes:

**Protected Mode** - In this mode all instructions and architectural features are available, providing the highest performance and capability.
This is the recommended mode that all new applications and operating systems should target.

**Real-Address Mode** - This mode provides the programming environment of the Intel 8086 processor, with a few extensions.
Reset initialization places the processor in real mode where, with a single instruction, it can switch to protected mode.

**Pipeline**

The Pentium's basic integer pipeline is five stages long, with the stages broken down as follows:

1. Pre-fetch/Fetch: Instructions are fetched from the instruction cache and aligned in pre-fetch buffers for decoding.
2. Decode1: Instructions are decoded into the Pentium's internal instruction format. Branch prediction also takes place at this stage.
3. Decode2: Same as above, and microcode ROM kicks in here, if necessary. Also, address computations take place at this stage.
4. Execute: The integer hardware executes the instruction.
5. Write-back: The results of the computation are written back to the register file.

![](https://i.imgur.com/87q2Zz4.png)
