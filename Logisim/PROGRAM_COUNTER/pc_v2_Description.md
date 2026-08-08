# Program Counter v2

## Changes from Version 1

* Replaced individual 4-bit connections with **4-bit buses** using internal splitters.
* Grouped the MUX inputs and flip-flop outputs into clean 4-bit buses.
* Grouped the Program Counter output into a single **4-bit output bus**.
* Kept the increment path using the current PC value and an adder to generate **PC + 1**.
* Kept the jump/load path using an external **4-bit input bus**.
* The MUX continues to select:

  * **MUX input 0:** PC + 1
  * **MUX input 1:** External jump/load address
* Rearranged the Clock and Write control pins for a cleaner module layout.
* **No functional changes were made.**

**Status:** Ready for CPU integration.
