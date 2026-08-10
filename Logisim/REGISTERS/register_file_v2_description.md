# Register File v2

## Changes from Version 1

* Replaced individual 4-bit input connections for each register with a **shared 4-bit Data Input bus**.
* Replaced individual register output wires with grouped **4-bit register output buses**.
* Used splitters to combine the four flip-flop outputs of each register into a single 4-bit bus.
* Reduced the number of control buffers by placing a single buffer on each register's grouped output bus instead of one buffer per flip-flop.
* Preserved the existing decoder-based write selection.
* Preserved the decoder-controlled output selection for reading a selected register.
* Maintained individual register write/read selection through the address lines.
* Kept the existing Write Enable control for controlling whether the selected register can be updated.
* Significantly reduced internal wiring and improved module readability.
* **No functional changes were made.**

**Status:** Ready for CPU integration.
