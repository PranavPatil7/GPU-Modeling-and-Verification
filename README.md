# gpu
Modelling GPU in C/C++/Python and Verilog/SystemVerilog and verifying using UVM. 
Can take in svg files - only parses triangles as a start
 Project Objective
The goal of this project is to build and verify a simplified GPU core that emulates the behavior of real-world GPU components. It focuses on:

Modeling GPU hardware structures (execution units, register files, ALUs, etc.)

Implementing programmable control paths

Creating a UVM-based verification environment to simulate and validate functional correctness

Optimizing the testbench and simulation flows for performance

Core Components Implemented>>>

Instruction Set Simulation (ISS):

A simplified ISA (Instruction Set Architecture) is created to define how the GPU executes instructions (e.g., ADD, LOAD, STORE).

It supports programmable pipelines, just like in actual GPU execution.

Execution Unit (EU):

A small ALU was built to perform arithmetic and logic operations.

It can be extended to test fused-multiply-add (FMA) or vector processing instructions, similar to NVIDIA GPU workloads.

Register Files:

Supports multiple read and write ports to simulate parallel execution.

Implements hazard detection and bypassing.

Instruction Decoder + Control Unit:

Decodes instruction opcodes and generates control signals.

Works like a finite state machine to direct data through the datapath.

UVM-Based Verification Environment:

Agents for input stimulus generation (instruction streams).

Monitors and Scoreboards to compare expected vs. actual outputs.

Functional coverage collection across different instruction categories and operand combinations.

Random and directed test generation supported via Python or SystemVerilog constraint classes.



Key Achievements / Metrics>>>

30% reduction in simulation time achieved by:
Restructuring the UVM environment to remove redundant transactions
Improving clocking and reset synchronization within the testbench
Achieved 92%+ functional coverage, validating control signals, pipeline stages, and arithmetic correctness
Successfully verified instruction sequencing, memory access, and hazard detection for 1000+ test cases

