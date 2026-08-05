# RAM Module (16 × 8-bit)

## Overview
The RAM module provides temporary data storage for the CPU. It consists of 16 memory locations, each capable of storing 8 bits of data, giving a total storage capacity of 16 bytes (128 bits).

## Specifications
- Memory Organization: 16 × 8-bit
- Total Capacity: 16 Bytes (128 bits)
- Address Width: 4 bits
- Data Width: 8 bits

## Inputs
- Data In (8-bit): Data to be written into memory.
- Address (4-bit): Selects one of the 16 memory locations.
- Write Enable (1-bit): Enables writing to the selected memory location.
- Read Enable (1-bit): Enables the memory output.
- Clock: Stores data on the active clock edge when Write Enable is active.

## Outputs
- Data Out (8-bit): Outputs the data stored at the selected memory location when Read Enable is enabled.

## Internal Design
- Sixteen 8-bit registers arranged in a 4 × 4 layout.
- A 4-to-16 decoder selects the register to be written.
- All registers share a common 8-bit data input bus.
- A 16-to-1 multiplexer selects the output of the addressed register.
- The multiplexer is controlled by the Address input and enabled using the Read Enable signal.

## Operation
### Write Operation
1. Place the target address on the Address bus.
2. Place the data on the Data In bus.
3. Set Write Enable HIGH.
4. Apply a clock pulse.
5. The selected register stores the data.

### Read Operation
1. Place the desired address on the Address bus.
2. Set Read Enable HIGH.
3. The multiplexer routes the selected register's contents to Data Out.

## Testing Performed
- Basic write and read
- Multiple address storage
- Memory overwrite
- Data hold with Write Enable disabled
- Address isolation
- Verification of all 16 memory locations
- Read Enable verification

## Result
The module successfully stores and retrieves data from all 16 memory locations. Write and read operations function correctly, and the Read Enable signal properly controls the memory output.