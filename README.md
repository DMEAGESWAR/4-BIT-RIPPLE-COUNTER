# 4-BIT-RIPPLE-COUNTER

**AIM:**

To implement  4 Bit Ripple Counter using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 Bit Ripple Counter**

A binary ripple counter consists of a series connection of complementing flip-flops (T or JK type), with the output of each flip-flop connected to the Clock Pulse input of the next higher-order flip-flop. The flip-flop holding the least significant bit receives the incoming count pulses. The diagram of a 4-bit binary ripple counter is shown in Fig. below.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/cb4b74d4-31ab-4359-95d0-d22e67daba13)

In timing diagram Q0 is changing as soon as the negative edge of clock pulse is encountered, Q1 is changing when negative edge of Q0 is encountered(because Q0 is like clock pulse for second flip flop) and so on.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/a573a7d6-014e-4e54-93e6-e2ac9530960b)

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/85e1958a-2fc1-49bb-9a9f-d58ccbf3663c)

**Procedure**

Step 1: Initialize the Counter
Initialize the 4-bit counter with all bits set to 0 (0000).

Step 2: Receive Clock Pulse
Receive a clock pulse (CLK).

Step 3: Check Clock Pulse
If the clock pulse is 0, go to step 8.

Step 4: Toggle LSB (Q0)
Toggle the least significant bit (Q0).

Step 5: Check Q0
If Q0 is 1, go to step 6.

Step 6: Toggle Q1
Toggle the next bit (Q1).

Step 7: Repeat for Q2 and Q3
Repeat steps 5-6 for Q2 and Q3.

Step 8: Update Counter Outputs
Update the counter outputs (Q3, Q2, Q1, Q0).

Step 9: Repeat
Repeat steps 2-8 for each clock pulse.



**PROGRAM**

module exp12(
   
   input wire clk,  // Clock input
   
   output reg [3:0] count // 4-bit counter output
);



// Counter logic

always @(posedge clk) begin

   if (count == 4'b1111) // Reset when count reaches 15
   
       
       count <= 4'b0000;
   else
   
       count <= count + 1; // Increment count
end


endmodule




 Developed by:D.MEAGESWAR RegisterNumber:24900815


**RTL LOGIC FOR 4 Bit Ripple Counter**
![Screenshot 2024-12-25 154536](https://github.com/user-attachments/assets/50e32d51-33e7-4d74-ab66-48c5661d7cba)

**TIMING DIGRAMS FOR 4 Bit Ripple Counter**

![Screenshot 2024-12-25 154654](https://github.com/user-attachments/assets/e2b0f1f4-6ef1-469b-bbc2-9d654ed0ab5b)

**RESULTS**

Thus implementing 4 Bit Ripple Counter using Verilog and validating their functionality
using their functional tables is done successfully
