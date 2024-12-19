# T-FLIPFLOP-POSEDGE

**AIM:**

To implement  T flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**T Flip-Flop**

T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/T-FLIPFLOP-POSEDGE/assets/154305477/458a68fe-2d08-4a9d-ac4f-7ae0480ce0bd)

 
This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop. The following table shows the state table of T flip-flop.

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop. Inputs Present State Next State

![image](https://github.com/naavaneetha/T-FLIPFLOP-POSEDGE/assets/154305477/cdd7fb32-539f-4b66-bb8d-f305a153c886)

 
From the above characteristic table, we can directly write the next state equation as Q(t+1)=T′Q(t)+TQ(t)′ ⇒Q(t+1)=T⊕Q(t)

**Procedure**

/* write all the steps invloved */

**PROGRAM**
```
module rom(addr, data_out);
 input [2:0] addr;
 output [7:0] data_out;
reg [7:0] data_out;
reg [7:0]mem [0:7];
initial
begin
mem[0]=8'b00000000;
mem[1]=8'b00000010;
mem[2]=8'b00000100;
mem[3]=8'b00001000;
mem[4]=8'b00010000;
mem[5]=8'b00100000;
mem[6]=8'b01000000;
mem[7]=8'b10000000;
end
always@(addr) begin
data_out=mem[addr];
end
endmodule
```
/* Program for flipflops and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/

**RTL LOGIC FOR FLIPFLOPS**
![Screenshot (8)](https://github.com/user-attachments/assets/864d7875-cc10-4bd9-ad3d-e535a5cbb20c)

**TIMING DIGRAMS FOR FLIP FLOPS**
![image](https://github.com/user-attachments/assets/c907a193-93b2-41ff-b849-6989ca4359b5)

**RESULTS**
Thus the OUTPUT’s of ROM and RAM are verified by synthesizing and simulating theVERILOG code
