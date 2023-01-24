---
title:  "P&H 1: Revision Notes"
mathjax: true
layout: post
comments: true
permalink: /posts/2023/patterson-hennessy-part-one/
tag: computer architecture
---
`Following are some notes, if you are already familiar with computer architecture design principles and want a refresher. Most important concepts covered in the Patterson and Hennessy book on Computer Organization and Design (RISC-V) edition is covered below.`<br>

### Instructions in ISA

RISC-V instructions are fixed in number of operands. Requiring everyinstruction to keep exactly three operands conforms to the philosophy of *keeping hardware simple*. Variable number of operands in instructions in ISA are more complicated to implement in hardware.

### Principles:
1. SIMPLICITY FAVORS REGULARITY : keep ISA instructions regular and fixed.
2. SMALLER IS FASTER: number of registers in the processor, keep it less.

RISC-V is available as 32-bit and 64-bit architectures.<br>
32-bit is a word.<br>
64-bit is called doubleword.<br>

RISC-V $\rarrow$ 32 registers of size 64 bits, named as `[x0 ... x31]` <br>
Less registers $\rarrow$ faster performance.  Why? large number of registers may increase the clock cycle simply because it takes electronic signals longer when they must travel farther. Note that, this is not an absolute rule, RISC-V has 32 registers, but having 31 registers does not necessarily mean faster processor. It is a tradeoff and the goal is to *keep clock cycle fast*.<br>
If we need more than 32 registers in the processor, the number of bits required in the ISA will increase.<br>
Effective use of registers is critical to program's performance.<br>

Compiler associates program variables to registers. Temporary registers when splitting one expression into many instructions, are also automatically assigned by the compiler.<br>

### Main Memory. Why?
