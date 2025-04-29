### NAME: SAMRITHA R
### REG NO: 24013637
### DATE: 22-04-2025
### Experiment no.2: IMPLEMENTATION OF BOOLEAN FUNCTION

### AIM:

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

### EQUIPMENT REQUIRED:

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

### THEORY:
Implementing Boolean functions in Verilog HDL (Hardware Description Language)
involves translating the simplified Boolean expressions into Verilog code to describe the
behavior of digital circuits. The basic building blocks in Verilog is module. The module
represent a combinationa circuit. Use logical operators (&, , ~, ^) to implement Boolean
functions directly. Use built-in gate primitives for basic functions: Use University
program VWF to verify the functionality of your Verilog modules. Create waveform and
check outputs against expected results.

### PROCEDURE:
1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.

### PROGRAM:
```
module boolean_function_minimization(a, b, c, d, w, x, y, z, f1, f2);
 input a, b, c, d, w, x, y, z;
 output f1, f2;
 wire x1, x2, x3, x4, x5, x6, x7, x8, x9, x10;
 assign x1 = (~a) & (~b) & (~c) & (~d);
 assign x2 = (a) & (~c) & (~d);
 assign x3 = (~b) & (c) & (~d);
 assign x4 = (~a) & (b) & (c) & (d);
 assign x5 = (b) & (~c) & (d);
 assign f1 = x1 | x2 | x3 | x4 | x5;
 assign x6 = (x) & (~y) & (z);
 assign x7 = (~x) & (~y) & (z);
 assign x8 = (~w) & (x) & (y);
 assign x9 = (w) & (~x) & (y);
 assign x10 = (w) & (x) & (y);
 assign f2 = x6 | x7 | x8 | x9 | x10;
 endmodule
```
### TRUTH TABLE:
![b15bfcd2-22c9-40b1-a6a8-b7c7a11a99db](https://github.com/user-attachments/assets/646037b4-07fa-44b5-bd2f-9cc4d3770c09)
### RTL REALIZATION:
![Screenshot 115406](https://github.com/user-attachments/assets/1072979e-a5bd-405f-84a2-5d8dd4b78ccc)
### Timing Diagram
![Screenshot 115326](https://github.com/user-attachments/assets/8ecf36a6-5905-44df-8457-298be0a25633)
### Result:
Thus the given logic functions are implemented using QUARTUS and their operations are verified using Verilog programming.

