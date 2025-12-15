# D_FLIPFLOP
AIM:

To implement D flipflop using verilog and validating their functionality using their functional tables

SOFTWARE REQUIRED:

Quartus prime

THEORY

D Flip-Flop

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

<img width="648" height="331" alt="image" src="https://github.com/user-attachments/assets/e6e52397-7c44-4e94-958b-1fbde0e2e30a" />

This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop.

<img width="372" height="139" alt="image" src="https://github.com/user-attachments/assets/194eeead-6e36-44d5-bf43-39bf405b4f6f" />

Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

<img width="383" height="203" alt="image" src="https://github.com/user-attachments/assets/dd4994bd-1f2b-415c-a392-f819dabc4c1c" />

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

#Procedure

Procedure to design D Flip-Flop (5 lines):

Identify the inputs D (Data), Clock, and outputs Q, Q̅.

Use an SR flip-flop and connect S = D and R = D̅.

Ensure the flip-flop samples the input only on the active clock edge.

Implement the logic using gates or HDL to avoid invalid input conditions.

Verify that the output Q follows D at each clock pulse through simulation.


#PROGRAM
```
// D Flip-Flop (with async reset)
module d_ff (
    input  wire clk, rst, D,
    output reg  Q
);
    always @(posedge clk or posedge rst) begin
        if (rst)
            Q <= 1'b0;   // Reset
        else
            Q <= D;      // Capture D at clock edge
    end
endmodule

```

Developed by: VANATHI T
RegisterNumber: 25013590

RTL LOGIC FOR FLIPFLOPS


<img width="1920" height="1020" alt="Screenshot 2025-12-15 170559" src="https://github.com/user-attachments/assets/c6429035-cc89-4672-a3be-ed7bd09c30c4" />

TIMING DIGRAMS FOR FLIP FLOPS

#RESULTS:
 Implemented D flipflop using verilog and validating their functionality using their functional tables

