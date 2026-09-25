Project Description

This project implements a hierarchical digital system that displays the SUM output of a 4-bit adder on the Basys 3 board's seven-segment display. The top module combines three submodules: the 4-bit adder from Lab 2 (Ripple Carry Adder and Carry Look Ahead Adder), a 2:1 multiplexer that selects which adder's SUM output is passed forward, and a BCD-to-seven-segment decoder that converts the selected SUM value into the signals needed to drive the display. Only the SUM output is displayed; the carry-out is not shown.

Simulation

1. Open the project in Vivado.
2. Add the BCD-to-seven-segment decoder, the 4-bit adder module(s), the 2:1 multiplexer, and the top module as design sources.
3. Add the desired testbench (BCD-to-seven-segment decoder or top module) as a simulation source.
4. Set the testbench as the simulation top module.
5. Run Behavioral Simulation.
6. Verify from the waveform that each input case produces the expected decoded output: for the decoder testbench, that each 4-bit value produces the correct segment pattern; for the top module testbench, that each A, B, and CI combination produces the correct SUM value.

FPGA Implementation

1. Select the Basys 3 as the target FPGA board.
2. Select the top module as the top module for implementation.
3. Add the Basys 3 constraints file and assign the A and B inputs, CI, and the adder-select line to switches, and the decoded SUM output to the seven-segment display.
4. Run Synthesis.
5. Run Implementation.
6. Generate the Bitstream.
7. Connect and power the Basys 3.
8. Open Hardware Manager and program the FPGA with the generated bitstream.
9. Test different switch input combinations, including both adder selections, and verify that the seven-segment display matches the expected SUM output.
