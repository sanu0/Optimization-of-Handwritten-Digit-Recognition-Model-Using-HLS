# Efficient Handwritten Digit Recognition Model Optimization Using HLS

## Project Overview
This project focuses on optimizing a Convolutional Neural Network (CNN) for handwritten digit recognition (MNIST dataset) using High-Level Synthesis (HLS) for FPGA deployment. The goal is to minimize latency and resource utilization by converting a Keras model to C with `keras2c` and applying various optimization techniques using Vivado HLS.

## Goals
- Convert the CNN model from Keras to C for compatibility with FPGA hardware.
- Utilize Vivado HLS to synthesize the model, applying optimization techniques to reduce latency and resource usage.
- Achieve efficient and faster execution on FPGA platforms by leveraging advanced optimizations like pipelining, loop unrolling, and loop tiling.

## Technologies Used
- **Keras**: For building the initial CNN model.
- **keras2c**: To convert the Keras model into C code for HLS synthesis.
- **Vivado HLS**: For synthesizing the C code into FPGA-compatible HDL and optimizing performance with pragma directives.

## Optimizations Applied
- **Loop Pipelining**: Reduces the initiation interval of loops to improve throughput.
- **Loop Unrolling**: Unrolls loops to increase parallelism and reduce loop overhead.
- **Code Motion**: Moves computations outside loops to minimize redundant calculations.
- **Loop Tiling**: Enhances data locality by breaking down loops into smaller chunks.

## Results Achieved
- **Latency Reduction**: Reduced latency by 98%, from 24,825,534 clock cycles (unoptimized) to 135,764 clock cycles (optimized).
- **Resource Utilization**: Achieved significant improvements in FPGA resource usage:
  - **LUT (Look-Up Tables)**: Improved by up to 75%
  - **FF (Flip-Flops)**: Improved by up to 75%
  - **DSP (Digital Signal Processing units)**: Reduced usage while maintaining performance
  - **BRAM (Block RAM)**: Reduced usage significantly

## Comparison with HLS4ML
- Demonstrated superior performance and resource efficiency compared to the HLS4ML-generated models, showcasing optimized usage of LUTs, FFs, DSPs, and BRAM in FPGA.

