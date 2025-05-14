# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER

**AIM:**

To implement  SISO Shift Register using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**SISO shift Register**

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

![image](https://github.com/naavaneetha/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/154305477/e81c4072-37f9-46c6-8145-566764b74c3a)

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next.
Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.

**Procedure**

1.Declare a Verilog module named EXP11 with input ports clk, rst, sin, and an output port q.

2.Declare input ports: clk for the clock signal, rst for the reset signal, and sin for the input signal. Also, declare the output port q as a 4-bit vector representing the state of flip-flops.

3.Declare an internal register q as a 4-bit vector to store the state of the flip-flops.

4.Create an always block that triggers on the positive edge of both the clock (clk) and the reset signal (rst), containing the following steps:

5.If the reset signal is asserted (rst), assign q to 4'b0000 to reset all flip-flops to 0.

6.If the reset signal is not asserted, assign the value of sin to the first flip-flop (q[0]) and shift the values of q to the right.

**PROGRAM**

Developed by: JONATHAN RHENIUS S

RegisterNumber: 212224050016

```
module ex10(clk, sin, q);
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

![442644387-0733b824-3d74-4a9d-8ef3-9cde60a622e7](https://github.com/user-attachments/assets/80b52909-3798-4ff4-9053-0f46b593a2c0)

**TIMING DIGRAMS FOR SISO Shift Register**

![442644559-631b1f35-2317-4662-bc1e-9fcaafc65e59](https://github.com/user-attachments/assets/7de4e634-735a-489d-8b76-87bda1ff04a8)

**RESULTS**

Thus implemented a SISO Shift Register using verilog and validated their functionality using their functional tables.
Thus,SISO Shift Register using verilog and validating their functionality using their functional tables has successful execution of the program.
