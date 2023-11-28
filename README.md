# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167910294-bb550548-b1dc-4cba-9044-31d9037d476b.png)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167910648-ced88e69-869c-42e2-9718-a285a3902446.png)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167908180-5fc9d589-1cb5-41f5-b2c8-927e04f5f387.png)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167908214-25b30a54-db20-4bcb-9385-5f93a1982a09.png)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![image](https://user-images.githubusercontent.com/36288975/167908342-e03f0cbb-5958-43bb-b74a-5e3ec2341675.png)

![image](https://user-images.githubusercontent.com/36288975/167910325-aeef0739-0a54-40e2-bebd-6f5fa0cad10e.png)



Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D



![image](https://user-images.githubusercontent.com/36288975/167908850-d39d07ba-7f9d-490a-b9f2-274e189fd047.png)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.
![image](https://user-images.githubusercontent.com/36288975/167910378-d2d984a7-2815-4d17-8c41-ee4bdf59ec24.png) 

 
This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167908575-59c35afb-50d3-46a2-888c-47478a3179d5.png)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

![image](https://user-images.githubusercontent.com/36288975/167908664-c854ffe9-0bd3-44c2-bfa6-e53928181c69.png)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 
 ![image](https://user-images.githubusercontent.com/36288975/167908688-fa93c3e9-8323-4864-947d-c11d163d5a90.png)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167911534-5f3c445d-bc68-46e2-9a9c-7efce5febc60.png)



This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167909015-53aa9450-3f28-4202-887a-79d88228f8a0.png)

From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure
/* write all the steps invloved */



### PROGRAM 
/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: Maha Vidya J P
RegisterNumber:  23013441
*/

## Code

## SR Flipflop

![Screenshot 2023-11-28 210614](https://github.com/Mahavidyajp/Experiment--05-Implementation-of-flipflops-using-verilog/assets/144870914/f55cb8b8-711b-4fb1-a628-73447f7efc1a)

## D Flipflop

![Screenshot 2023-11-28 210623](https://github.com/Mahavidyajp/Experiment--05-Implementation-of-flipflops-using-verilog/assets/144870914/814d9eb9-2c25-4730-9447-6e6566f5f41e)

## JK Flipflop

![Screenshot 2023-11-28 210634](https://github.com/Mahavidyajp/Experiment--05-Implementation-of-flipflops-using-verilog/assets/144870914/391059d8-9174-46e6-bea6-5d27073810a5)

## T Flipflop

![Screenshot 2023-11-28 210643](https://github.com/Mahavidyajp/Experiment--05-Implementation-of-flipflops-using-verilog/assets/144870914/f125d6a2-e70f-47a3-8687-3b33373ab1c7)

## RTL Logic for Flipflop

## SR Flipflop

![Screenshot 2023-11-28 210658](https://github.com/Mahavidyajp/Experiment--05-Implementation-of-flipflops-using-verilog/assets/144870914/7f415a94-6ef1-4d3f-9952-94864811d0c3)

## D Flipflop

![Screenshot 2023-11-28 210707](https://github.com/Mahavidyajp/Experiment--05-Implementation-of-flipflops-using-verilog/assets/144870914/2184d9db-5395-44d7-b4cb-a99c4d080af3)

## JK Flipflop

![Screenshot 2023-11-28 210718](https://github.com/Mahavidyajp/Experiment--05-Implementation-of-flipflops-using-verilog/assets/144870914/60a3d298-3527-40fd-8c66-0ef5da2f5695)

## T Flipflop

![Screenshot 2023-11-28 210728](https://github.com/Mahavidyajp/Experiment--05-Implementation-of-flipflops-using-verilog/assets/144870914/1abef4c4-fd26-4fea-a71d-80d4b37968d5)

## Timing Diagram

## SR Flipflop

![Screenshot 2023-11-28 210746](https://github.com/Mahavidyajp/Experiment--05-Implementation-of-flipflops-using-verilog/assets/144870914/0478c4fb-0965-4b51-9aaa-2362ada70e18)

## D Flipflop

![Screenshot 2023-11-28 210804](https://github.com/Mahavidyajp/Experiment--05-Implementation-of-flipflops-using-verilog/assets/144870914/250a8548-3f1d-4c47-8e67-31cd5fae8ffd)

## JK Flipflop

![Screenshot 2023-11-28 210823](https://github.com/Mahavidyajp/Experiment--05-Implementation-of-flipflops-using-verilog/assets/144870914/608504d1-1e3b-4c93-9009-b753822910b1)

## T Flipflop

![Screenshot 2023-11-28 210842](https://github.com/Mahavidyajp/Experiment--05-Implementation-of-flipflops-using-verilog/assets/144870914/52fffdc8-3660-4efa-9633-808a6735a785)

### RESULTS 

Successfully implemented all the flipflops using verilog and validating their functionality using their functional tables.
