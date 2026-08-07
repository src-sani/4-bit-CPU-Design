# Accumulator v2 Documentation

## Module Name

**Accumulator v2**

---

## Purpose

The Accumulator is a 4-bit register used to temporarily store the result produced by the ALU. It acts as the primary working register of the CPU and supplies one of the operands for subsequent arithmetic and logical operations.

---

## Inputs

| Signal |  Width | Description                                        |
| ------ | -----: | -------------------------------------------------- |
| Data   | 4 bits | Data to be stored in the accumulator               |
| Load   |  1 bit | Enables writing new data into the accumulator      |
| Clock  |  1 bit | Synchronizes data storage on the active clock edge |

---

## Outputs

| Signal |  Width | Description                             |
| ------ | -----: | --------------------------------------- |
| Q      | 4 bits | Current value stored in the accumulator |

---

## Internal Architecture

The accumulator consists of:

* Four D Flip-Flops for 4-bit data storage.
* A 2:1 multiplexer before each flip-flop.
* A common **Load** signal controlling all multiplexers.
* Internal splitters used to distribute and combine the 4-bit data bus.

Operation:

* **Load = 0**

  * Each multiplexer feeds back the current flip-flop output.
  * The stored value is retained.

* **Load = 1**

  * The input data bus is selected.
  * On the active clock edge, the new 4-bit value is stored.

---

## Design Improvements from Accumulator v1

* Replaced four separate input pins with a single **4-bit Data bus**.
* Replaced four separate output pins with a single **4-bit Output bus**.
* Moved all splitters inside the module, creating a cleaner external interface.
* Reduced top-level wiring and improved readability.
* Standardized the module interface for easier CPU integration.

---

## Status

**Module Status:** Complete

**Verification:** Successfully verified for data loading and value retention.

**CPU Integration:** Ready.
