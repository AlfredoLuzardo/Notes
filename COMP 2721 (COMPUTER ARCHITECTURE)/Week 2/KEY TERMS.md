
**Definitions**:
- **Clock**: Anything that can be turned on or off
- **Clock Cycle:** 
	- Time it takes for the clock to turn on and off
	- e.g. 100 MHz bus frequency: 100 million cycles per second; 100 x 10^6
	- **Period** = 1/frequency; 1/1M = 1 microsecond = 10^-6
	- 1GHz = 1,000,000,000 cycles/second; corresponds to 1/1,000,000,000th second/cycle (1 ns)
- **1 GHz cpu**:
	- 1 billion rising and falling edges per second
	- 1 rising edge per nanosecond
	- Possible we could start one instruction each nanosecond


![[Pasted image 20240919091255.png]]
**SPECIAL PURPOSE REGISTERS:**

**PC**:
- **Program Counter**: Holds the main memory address of the next instruction to be fetched, decoded and executed (FDE).
**IR**:
- **Instruction Register**: Holds the current-executing instruction

Page 63-65 wish list (How to speed up instruction execution)
- **All instructions should be directly executed by hardware**: complex and expensive
- **Issue instructions as fast/often as possible**: physics limits, complex, expensive
- **only LOAD and STORE instructions should reference main memory**: cannot avoid going to main memory
- **Provide lots of registers**: expensive
GOAL: PREVENT CPU FROM STARVING

**RISC VS CISC ARCHITECTURES**
Reduced Instruction Set Computer (RISC):
- fewer and simpler instructions
Complex Instruction Set Computer (CISC):
- more and more complex instructions: e.g. implement the most common instructions directly in hardware (no interpretation required), even the complex ones

Our computer is a mix: mostly RISC with some CISC

CISC: attempts to minimize number of instructions per program, sacrificing the number of cycles per instruction. 
RISC: does the opposite, reducing the cycles per instruction at the cost of the number of instructions per program


**INTERPRETER**:
- Any software program (aka VM) that FDE the instructions of another program.
- The output of this is another program that is simpler to run.
- But this process takes time
- This is cheaper than having hardware run the original (more complex, higher level) program and it is cheaper than having hardware do the conversion (interpretation)