# DIGITAL-FIR-FILTER-
COMPANY: CODETECH IT SOLUTIONS 
NAME: AVULA BHUVANA PREETHI
INTERN ID: CT08DN1058
DOMAIN : VLSI
DURIATION: 8 WEEKS
MENTOR: NEELA SANTOSH

As part of my Codetech project, I designed and simulated a Digital FIR (Finite Impulse Response) Filter using Verilog HDL. The objective of this task was to understand how digital filters work and implement a working model that can process discrete-time input signals with fixed coefficients. FIR filters are widely used in digital signal processing to filter out unwanted frequencies or smooth signals. This project helped me gain hands-on experience in digital filter design, hardware description, and waveform simulation.

Filter Concept and Design
A FIR filter is a type of digital filter whose output depends only on current and previous input samples, multiplied by fixed coefficients. The mathematical expression for an FIR filter output is:

In my design, I implemented a 4-tap FIR filter, which means it uses the current input and the last 3 inputs. I chose the coefficients as:
These coefficients represent a simple low-pass filter.
Verilog Implementation
The Verilog code consists of two modules:
fir_filter.v: This is the main FIR filter module. It accepts an 8-bit signed input (x_in) and produces a 16-bit signed output (y_out). It includes registers to store previous input values and performs the multiply-accumulate operation on every clock cycle. The output is updated continuously based on the most recent four inputs.
tb_fir_filter.v: This is the testbench used to simulate the FIR filter. It generates a clock signal, applies a series of input values (like 1, 2, 3, 4, etc.), and observes the output. It also includes waveform dump commands to save the simulation data into a .vcd file for viewing in GTKWave.
Simulation and Output
I used Icarus Verilog and GTKWave to simulate the design. The testbench applied sample inputs and I observed the filter output using the waveform viewer. The output values matched the expected results calculated using the FIR formula. For example, when the inputs were 1, 2, 3, and 4, the output became:
y=1×4+2×3+3×2+4×1=20
As new inputs were applied, the filter continued updating its output in real time.
Performance and Learning
The filter processes one input per clock cycle.
It takes 4 cycles to "fill the pipeline" and start giving meaningful output.The implementation uses basic Verilog constructs and is efficient for FPGA synthesis.
This project gave me practical experience in writing synthesizable Verilog, understanding signal delay in filters, and using waveform tools for debugging. It also improved my grasp of how digital systems handle real-time signal processing.
In conclusion, I successfully designed and simulated a working FIR filter using Verilog as part of my Codetech assignment. I understood the internal architecture of digital filters, verified functionality through simulation, and analyzed performance — fulfilling all deliverables of the task.

