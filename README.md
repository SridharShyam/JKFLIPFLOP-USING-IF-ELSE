# JKFLIPFLOP-USING-IF-ELSE

**AIM:** 

To implement  JK flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**JK Flip-Flop**

JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/a649c30b-232b-4558-b188-fd6c09845180)


This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/c4360742-e8a8-4937-b089-c46c0433f9a3)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/6c275261-a6d5-4c37-a3a7-1e88ca11c4cd)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/5174f41b-0ce0-4329-a372-6d1943ea6673)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

## Procedure:
### Step-1:
Go to quartus software.
### Step-2:
Set new environment.
### Step-3:
Type the code to implement SR flipflop using verilog and validating their functionality using their functional tables.
### Step-4:
Run the program.
### Step-5:
Give inputs in the waveform table .
### Step-6:
Run the program.

**PROGRAM**
```
Program for flipflops and verify its truth table in quartus using Verilog programming.
Developed by: SHYAM S
RegisterNumber: 212223240156
module SR_FF(q,q_bar,s,r,clk,reset);
input s,r,clk,reset;
output reg q;
output q_bar;
always@(posedge clk) begin
if(!reset)
	q<=0;
else
begin
	case ({s,r})
		2'b00: q<=q;
		2'b01: q<=1'b0;
		2'b10: q<=1'b1;
		2'b11: q<=1'bx;
		default: q<=q;
		endcase
	end
end
assign q_bar=~q;
endmodule
```

**RTL LOGIC FOR FLIPFLOPS**

![image](https://github.com/SridharShyam/JKFLIPFLOP-USING-IF-ELSE/assets/144871368/9d9def0f-13ff-42b7-a839-be3ae7ef471c)

**TIMING DIGRAMS FOR FLIP FLOPS**

![image](https://github.com/SridharShyam/JKFLIPFLOP-USING-IF-ELSE/assets/144871368/4e65e559-72b0-48ec-99f9-83c472886411)

**RESULT**
Thus, the program code is successfully runned and executed.
