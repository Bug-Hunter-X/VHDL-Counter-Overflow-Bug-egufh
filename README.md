# VHDL Counter Overflow Bug

This repository demonstrates a common error in VHDL code: an integer counter that can overflow. The original code (`buggy_counter.vhd`) lacks a check to prevent the counter from exceeding its defined range.  The fixed version (`fixed_counter.vhd`) shows how to prevent this using a modulo operation.

## Bug Description
The `buggy_counter` entity increments its counter without any bound checking. When the counter reaches 15, the next increment will result in an overflow, leading to unpredictable behavior and potential simulation or synthesis errors.  This is a subtle bug that can be hard to detect.

## Solution
The `fixed_counter` entity addresses this issue by using a modulo operation to wrap the counter back to 0 when it reaches 15. This ensures that the counter stays within its defined range and prevents overflow.