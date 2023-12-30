Developed by: GOKUL SACHIN K
Refrence number:23004843

## Experiment--05-Implementation-of-flipflops-using-verilog
## AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
## HARDWARE REQUIRED: – PC, Cyclone II , USB flasher
## SOFTWARE REQUIRED: Quartus prime
## THEORY
SR Flip-Flop SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://github.com/vksachin2018/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149366019/92231b31-441b-46fa-9887-5d0b4bd6f58a)


This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of SR flip-flop.

![image](https://github.com/vksachin2018/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149366019/20bec932-a650-47a2-934a-bb2eb46b7507)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop. Present Inputs Present State Next State

![image](https://github.com/vksachin2018/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149366019/70755256-69aa-4ee5-9403-70c56516941c)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://github.com/vksachin2018/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149366019/ff67a1e7-5a18-4089-ac5c-fa481f73f904)


The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)

## D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop.

![image](https://github.com/vksachin2018/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149366019/62ba308f-38b2-41eb-b0dd-6923854f127d)


Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

![image](https://github.com/vksachin2018/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149366019/19d9583c-da1c-4753-931f-68f9cba6d9c1)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

## JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

![image](https://github.com/vksachin2018/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149366019/b7f6de52-afa1-4b84-b62c-db249cb730a5)


This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.
![image](https://github.com/vksachin2018/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149366019/a7aea625-f4fe-46aa-92d4-0379b4455c58)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State

![image](https://github.com/vksachin2018/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149366019/3a0c9641-9fbe-4222-b01f-49c5cfe15516)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://github.com/vksachin2018/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149366019/598f9bd7-6b67-46e4-a400-652c0867a818)


The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

## T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://github.com/vksachin2018/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149366019/b5cdf54f-897c-42d4-ad32-e00866058bca)


This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop. The following table shows the state table of T flip-flop.

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop. Inputs Present State Next State

![image](https://github.com/vksachin2018/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149366019/44efa94f-b147-436d-a333-6a05339b3739)


From the above characteristic table, we can directly write the next state equation as Q(t+1)=T′Q(t)+TQ(t)′ ⇒Q(t+1)=T⊕Q(t)

Procedure
1.Using nand gates and wires construct sr flip flop. 2.Repeat same steps to construct JK,D,T flipflops. 3.Find Rtl logic and timing diagram for all flipflops. 4.end the program

## PROGRAM
SR Flip-Flop: module SR_flipflop(S,R,clk,Q,Qbar); input S,R,clk; output Q,Qbar; wire X,Y; nand (X,S,clk); nand (Y,R,clk); nand (Q,X,Qbar); nand (Qbar,Y,Q); endmodule

D Flip-Flop: module D_flipflop(D,clk,Q,Qbar); input D,clk; output Q,Qbar; assign Dbar=~D; wire X,Y; nand (X,D,clk); nand (Y,Dbar,clk); nand (Q,X,Qbar); nand (Qbar,Y,Q); endmodule

JK Flip-Flop: module JK_flipflop(J,K,clk,Q,Qbar); input J,K,clk; output Q,Qbar; wire X,Y; nand (X,J,clk,Qbar); nand (Y,K,clk,Q); nand (Q,X,Qbar); nand (Qbar,Y,Q); endmodule

T Flip-Flop: module T_flipflopo(T,clk,Q,Qbar); input T,clk; output Q,Qbar; wire S,R; nand (S,T,clk,Qbar); nand (R,T,clk,Q); nand (Q,S,Qbar); nand (Qbar,R,Q); endmodule

## RTL LOGIC FOR FLIPFLOPS
SR Flip-Flop:
![image](https://github.com/vksachin2018/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149366019/fabe28da-bcc8-46e3-bf1d-201d51ed08b0)



D Flip-Flop:
![image](https://github.com/vksachin2018/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149366019/8d5f6f75-c6ad-4b26-97fc-96067c6cc7f3)



JK Flip-Flop:
![image](https://github.com/vksachin2018/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149366019/9bfd0798-e334-4dbd-b35b-e454cad3fed1)



T Flip-Flop:
![image](https://github.com/vksachin2018/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149366019/6a256e80-9522-450c-af46-b0a31345b7a1)




##TIMING DIGRAMS FOR FLIP FLOPS
SR Flip-Flop:

![image](https://github.com/vksachin2018/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149366019/1c10251f-86c8-49dc-9e05-a457017af976)


## D Flip-Flop:


JK Flip-Flop:

![image](https://github.com/vksachin2018/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149366019/6dde2593-db4c-4f8d-8da2-ea87ca454fd8)


T Flip-Flop
![image](https://github.com/vksachin2018/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149366019/3b8c16ce-5308-4f03-924c-f27ee1bdd669)

## RESULTS
Thus implementation of SR, JK, D and T flipflops using nand gates are done sucessfully.


