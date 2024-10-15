**Mean (Average) Memory Access Time**
- The average time it takes the CPU to fetch a word from sort of memory (the fetch in the fetch-decode-execute cycle).
- Analogy:
	- Sometimes the food you want is in the fridge
	- Sometimes the food you want is at Costco
	- Sometimes the food is in between: corner store, save on foods, market etc.
	- The Mean Food Access Time is the average time it takes you to get your food
- Computer
	- CPU wants a word:
		- Sometimes the word the CPU wants is in the registers
		- Sometimes the word the CPU wants is on the hard disk drive
		- Sometimes the word the CPU wants is in between: cache(s), RAM
		- The Mean Memory Access Time is the average time it takes the CPU to get its word

A "hit" is when the requested word is found.

A "miss" is when the requested word is not found there; in this case the next level of memory is checked.

Start with a simple case: ONE level of cache, plus main memory:
- Mean Memory Access Time = **cache access time + (1 - hit rate) * main-memory access time**
	- MAT = c + (1 - h)m

