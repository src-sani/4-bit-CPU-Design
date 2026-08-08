# RAM v2

## Changes from Version 1

* Replaced the four separate address input pins with a single **4-bit Address bus**.
* Replaced the eight separate data input wires with a single **8-bit Data Input bus**.
* Replaced the eight separate output pins with a single **8-bit Data Output bus**.
* Replaced the four separate address-selection connections to the output MUX with a single **4-bit Address bus**.
* Optimized the decoder write-enable connections by grouping the 16 register enable lines into **four 4-register groups**, reducing long individual wires.
* Optimized the register output connections by grouping the outputs of every four registers before connecting them to the output MUX.
* Used internal splitters to regroup and distribute the grouped 8-bit register buses.
* Significantly reduced long and visually cluttered internal wiring.
* **No functional changes were made.**

**Status:** Ready for CPU integration.
