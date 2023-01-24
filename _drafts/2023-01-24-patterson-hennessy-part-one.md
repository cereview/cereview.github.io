---
title:  "P&H 1: Revision Notes"
mathjax: true
layout: post
comments: true
permalink: /posts/2023/patterson-hennessy-part-one/
tag: computer architecture
---
`Following are some notes, for a computer architect in a hurry. All important concepts covered in the Patterson & Hennessy's on Computer Organization and Design (RISC-V) edition are covered below. Leave a comment, if you find more interesting topics to add to these notes.`

### Instructions in ISA

RISC-V instructions are fixed in number of operands. Requiring everyinstruction to keep exactly three operands conforms to the philosophy of *keeping hardware simple*. Variable number of operands in instructions in ISA are more complicated to implement in hardware.

### Principles:
1. SIMPLICITY FAVORS REGULARITY : keep ISA instructions regular and fixed.
2. SMALLER IS FASTER: number of registers in the processor, keep it less.

RISC-V is available as 32-bit and 64-bit architectures.
32-bit is a word.
64-bit is called doubleword.

RISC-V $$ \rightarrow $$ 32 registers of size 64 bits, named as `[x0 ... x31]`

Less registers $$ \rightarrow $$ faster performance.  Why? large number of registers may increase the clock cycle simply because it takes electronic signals longer when they must travel farther. Note that, this is not an absolute rule, RISC-V has 32 registers, but having 31 registers does not necessarily mean faster processor. It is a tradeoff and the goal is to *keep clock cycle fast*.

If we need more than 32 registers in the processor, the number of bits required in the ISA will increase.

Effective use of registers is critical to program's performance.

Compiler associates program variables to registers. Temporary registers when splitting one expression into many instructions, are also automatically assigned by the compiler.

### Main Memory. Why?
