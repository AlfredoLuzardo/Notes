- Most Modern computers consist of two or more levels
- Machines with as many as six levels exist

![[Pasted image 20240918170722.png]]

**Digital Logic Level (Level 0)**:
- Is the machines true hardware
- Its circuits carry out the machine-language programs of level 1
- There is a level below, called the device level. Consists of transistors, the lowest level primitives for computer designers 
- **Gates**:
	- Each gate has one or more digital inputs (signals representing 0 or 1) and computes as output a simple function of these inputs, such as AND or OR
	- Built up of at most a handful of transistors
	- Small number of gates can be combined to form a 1-bit memory, which can store a 0 or 1.
		- The 1 bit memories can be combined in groups of (for example) 16, 32, or 64 to form registers
		- Each register can hold a single binary number up to some maximum.
	- Gates can also be combines to form the main computing engine itself

**Microarchitecture level (level 1)**:
- Collection of typically 8 - 32 registers
	- Form local memory and a circuit called ALU (Arithmetic Logic Unit), which is capable of performing simple arithmetic operations
- Registers are connected to ALU to form a **data path**, over which data flow 

**TOP LEVELS**
- Easier for people
- Harder for Computers
- More powerful instructions
- Smaller programs
- Slower programs (e.g. level 6 must first be converted to level 5, then 4, 3, 2, 1)

**BOTTOM LEVELS**
- Programs get larger
- Instructions get weaker (simpler): less powerful
- instructions are harder for people and easier for computers

**Having many levels**:
- good modularity
- cheap computers
- slow

**What are the advantages and disadvantages of the six-level computer, compare to a one level computer**
- Advantages:
	- Good modularity
	- Cheap Computers
- Disadvantages:
	- Slow