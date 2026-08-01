# 4-bit Register File Version 0.1

## Overview

Implementation of a 4-bit register and register file for CPU data storage and transfer operations.

## 4-bit Register

### Description

A 4-bit register stores binary data using four D flip-flops. It supports controlled data loading using a load enable signal.

### Inputs

* D[3:0]
* Clock
* Load Enable

### Outputs

* Q[3:0]

### Features

* 4-bit data storage
* Clock synchronized operation
* Load enable control

---

# Register File

## Description

A register file containing four 4-bit registers with controlled read and write operations using decoders and a shared bus.

## Registers

* R0
* R1
* R2
* R3

## Inputs

* Data Input[3:0]
* Clock
* Write Enable
* Write Select[1:0]
* Read Enable
* Read Select[1:0]

## Outputs

* Data Output[3:0]

## Architecture

* Four 4-bit registers
* Shared 4-bit bus
* Read Selection Decoder
* Write Selection Decoder
* Tri-state buffers for bus control

## Operations Supported

### Write Operation

* Selects a destination register using Write Select
* Stores input data on the clock edge

### Read Operation

* Selects a source register using Read Select
* Places register data on the output bus

## Tool Used

Logisim Evolution
