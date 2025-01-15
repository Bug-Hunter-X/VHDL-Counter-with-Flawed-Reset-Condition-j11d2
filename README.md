# VHDL Counter with Flawed Reset Condition

This repository demonstrates a common error in VHDL code: an incomplete reset condition in a counter.

## Bug Description

The `buggy_counter.vhdl` file contains a counter that only resets when it reaches its maximum value (15).  A proper reset should occur regardless of the current count value.  This leads to unexpected behavior if a reset signal is asserted while the counter is less than 15.

## Solution

The `fixed_counter.vhdl` file provides a corrected version. The reset condition is improved to unconditionally reset the counter when `rst` is high. 

## How to Run

Simulate both `buggy_counter.vhdl` and `fixed_counter.vhdl` using your preferred VHDL simulator (e.g., ModelSim, GHDL) to observe the difference in behavior.