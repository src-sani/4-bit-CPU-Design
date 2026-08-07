# Instruction Register v2

## Changes from Version 1

* Replaced separate input/output connections with **8-bit input and output buses**.
* Added internal splitters to distribute the 8-bit input across the two 4-bit registers.
* Maintained the existing **two 4-bit register architecture**:

  * Upper 4 bits → Opcode
  * Lower 4 bits → Operand
* Combined the outputs of both 4-bit registers into a single 8-bit output bus.
* Kept separate 4-bit Opcode and Operand outputs for CPU integration.
* No functional changes were made.

**Status:** Ready for CPU integration.
