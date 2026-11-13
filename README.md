# Architecture-Aware PPA Optimization of Digital Accelerators

An experimental study of the relationship between accelerator microarchitecture and physical implementation, focusing on power, performance, area (PPA), and timing closure.

## Overview

This project investigates how architectural decisions such as resource sharing, pipelining, and parallelism influence the physical characteristics of digital hardware accelerators.

Multiple RTL implementations of equivalent computational kernels are evaluated using functional verification, synthesis, static timing analysis, and physical-design flows.

The objective is to identify architectural trade-offs and understand how logic-level optimizations translate into post-layout performance.

## Research Objectives

- Analyze the impact of microarchitecture on area, throughput, latency, and energy efficiency.
- Compare resource-shared, pipelined, and parallel datapaths.
- Investigate timing-critical paths and routing overhead.
- Evaluate architectural and physical-design optimizations under consistent implementation constraints.
- Develop reproducible methods for comparing accelerator implementations.

## Initial Design

The first experimental kernel is a four-element signed integer dot-product accelerator.

Three microarchitectures are planned:

| Architecture | Description |
|---|---|
| Sequential | Resource-shared multiply-accumulate datapath |
| Pipelined | Datapath with registered computation stages |
| Parallel | Multiple arithmetic units operating concurrently |

All implementations will be checked against a common functional specification.

## Tools and Methodology

- **RTL:** SystemVerilog
- **Verification:** Icarus Verilog, Python
- **Synthesis:** Yosys
- **Physical Design:** OpenROAD
- **Analysis:** Static timing analysis, area and power estimation

## Project Structure

```text
rtl/          RTL implementations
tb/           Verification testbenches
model/        Python reference models
scripts/      Simulation and synthesis scripts
docs/         Specifications and methodology
results/      Experimental measurements
```

## Project Status

Initial development — sequential dot-product accelerator and verification infrastructure.

Physical-design evaluation and architecture comparisons are planned.

## Future Work

- Implement pipelined and parallel architectures.
- Establish reproducible synthesis and physical-design experiments.
- Analyze architecture-dependent routing and timing effects.
- Investigate optimizations targeting energy and area efficiency.

## License

To be determined.
