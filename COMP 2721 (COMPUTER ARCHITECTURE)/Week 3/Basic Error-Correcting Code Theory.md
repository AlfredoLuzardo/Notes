
**Error-correcting code:**
- Use for detecting and (possibly) correcting errors in words

**Errors**
- Some errors are correctable
- Some errors are undetectable because it looks correct
- NOT ALL ERRORS ARE CREATED EQUALLY

**Data Word** (aka memory word): 
- the raw data word we want to protect and store without errors

**Codeword**:
- the data word, with **extra bits added into it**. 
	- The extra bits are called parity bits, check bits, or redundant bits. 
	- These extra bits are what allow us to detect/correct errors

Hamming Code is an official protocol for error detection and correction

**Code**:
- A set of words that we agree are valid (like a dictionary)


QUIZ QUESTION:
	00000000
	11111111
	
	0
	1

- Why is top code which is less efficient better than the bottom two word vocabulary.
	- The more different the words are, the more errors it requires to transform one valid word to another by mistake. If you make a mistake in the bottom code, you cannot tell whether it was a mistake or not.

Worst Cases:
- 50% mark
- More than 50%
- 100% error

Tradeoff:
- **Clarity** versus **Efficiency**
- To get clearer words, we need longer words with lots of differences between them

Valid and Intended are different

**Hamming Distance**:
- The **minimum** number of bits different between **any** two valid words in a code

- Differences between its closes words
	- e.g. Code A has 8 bit differences between its closest words

- A code with a Hamming Distance of **h** bits can **detect** up to **less than h** bit errors (anything but h amount of errors).

- A code with Hamming Distance of **h** bits can **correct** up to **less than h/2** bit errors (not equal to h/2).

- WE WANT LARGE GAPS BETWEEN VALID CODEWORDS
- WE WANT A LARGE HAMMING DISTANCE

| **HD** | **ED (# bit errors detectable)** | **EC (# bit errors correctable)** |
| ------ | -------------------------------- | --------------------------------- |
| H      | Up to H-1                        | Less than H/2                     |
| 1      | Code B: 0                        | 0                                 |
| 8      | Up to 7 bits (this is code A)    | Up to 3                           |

