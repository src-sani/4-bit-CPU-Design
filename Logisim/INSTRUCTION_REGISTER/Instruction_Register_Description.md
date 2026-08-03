# Instruction Register (IR)

## Overview

The Instruction Register is used to store the current instruction fetched from memory before it is decoded and executed by the Control Unit.

In our CPU, the instruction size is 8 bits and is divided into:

```
[ Opcode ][ Operand ]
   4 bits    4 bits
```

* Bits 7-4 → Opcode
* Bits 3-0 → Operand

---

## Components Used

* Two 4-bit Registers
* Clock signal
* IR Load control signal

The two 4-bit registers together form an 8-bit Instruction Register.

---

## Architecture

```
8-bit Instruction Input

[7:4] ------------> Opcode Register

[3:0] ------------> Operand Register
```

Both registers share the same clock and load signal so that the complete instruction is stored at the same time.

---

## Working

When IR Load is enabled:

* The instruction input is stored into the registers on the clock edge.
* The upper 4 bits are stored as the opcode.
* The lower 4 bits are stored as the operand.

Example:

```
Input: 1010 0011

Opcode  = 1010
Operand = 0011
```

When IR Load is disabled:

* The previously stored instruction remains unchanged.

---

## Testing

The Instruction Register was tested for:

* Loading a new instruction
* Holding the previous instruction when load is disabled
* Reloading with a new instruction

All tests passed successfully.

---

## Status

Instruction Register: Completed ✅
