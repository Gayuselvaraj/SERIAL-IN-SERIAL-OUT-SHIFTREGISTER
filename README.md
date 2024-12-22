# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER

**AIM:**

To implement  SISO Shift Register using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime



**SISO shift Register**

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

![image](https://github.com/naavaneetha/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/154305477/e81c4072-37f9-46c6-8145-566764b74c3a)

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next.
Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.


**Truth table**


![397931311-e7b4048d-4adb-4e05-960c-5555d4dd6e0c](https://github.com/user-attachments/assets/9d5398fa-dd8e-4aa3-b5df-758347a65563)


![397931311-e7b4048d-4adb-4e05-960c-5555d4dd6e0c](https://github.com/user-attachments/assets/a8968095-ffda-4872-a981-3186ca61e4a4)



**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram


**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming.

Developed by:Gayathri s

RegisterNumber:24900444

```
module EXP10(clk, sin, q);
input clk;
input sin;
output [3:0] q;
reg [3:0] q;
always @(posedge clk)
begin
q[0] <= sin;
q[1] <= q[0];
q[2] <= q[1];
q[3] <= q[2];
end
endmodule
```

**RTL LOGIC FOR SISO Shift Register**
![394711045-603e4450-99a7-496e-a165-2abc5cc18434](https://github.com/user-attachments/assets/893c498b-8d14-4bfe-814f-0cb152b85b1c)


**TIMING DIAGRAMS FOR SISO Shift Register**
![394711075-d6b2a832-4d30-49d8-b73c-0a106391f46a](https://github.com/user-attachments/assets/ed076d76-31a5-4936-a296-fc4b17818814)


**RESULT**

Thus SISO Shift Register is implemented using verilog and their functionality using their functional tables is validated.
