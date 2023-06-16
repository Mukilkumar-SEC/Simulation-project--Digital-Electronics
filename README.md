# Design and simulate mod 12 synchronous upcounter with T flip flop using Verilog.

## AIM:
To Design and simulate mod 12 synchronous upcounter with T flip flop using Verilog.

## Equipments Required:
1. Hardware – PCs, Cyclone II , USB flasher
2. Software – Quartus prime

## THEORY:
The counter is a digital sequential circuit and here it is a 4 bit counter, which simply means it can count from 0 to 15 and vice versa based upon the direction of counting (up/down). 

The counter (“count“) value will be evaluated at every positive (rising) edge of the clock (“clk“) cycle.
The Counter will be set to Zero when “reset” input is at logic high.
The counter will be loaded with “data” input when the “load” signal is at logic high. Otherwise, it will count up or down.
The counter will count up when the “up_down” signal is logic high, otherwise count down

Since we know that binary count sequences follow a pattern of octave (factor of 2) frequency division, and that J-K flip-flop multivibrators set up for the “toggle” mode are capable of performing this type of frequency division, we can envision a circuit made up of several J-K flip-flops, cascaded to produce four bits of output.
The main problem facing us is to determine how to connect these flip-flops together so that they toggle at the right times to produce the proper binary sequence.
Examine the following binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1:
Binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1.


## LOGIC DIAGRAM
![240555551-3e2addc4-d769-4d8a-bb22-0fd84bc81cf7](https://github.com/Mukilkumar-SEC/Simulation-project--Digital-Electronics/assets/119559663/331eabc8-140d-4e91-9bfa-b55bbaa27d5e)

## PROCEDURE:
1.Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.

## PROGRAM:
```
Design and simulate mod 12 synchronous upcounter with T flip flop using Verilog.
Developed by:  MUKIL KUMAR V
RegisterNumber: 212222230087
module project,clk,q,qbar);
input t,clk;
output q,qbar;
reg q,qbar;
always @(posedge clk)
begin 
q<=(t&~q)|(~t&q);
qbar<=~q;
end
endmodule
```





## NETLIST DIAGRAM :
##### RTL realization:
![240555551-3e2addc4-d769-4d8a-bb22-0fd84bc81cf7](https://github.com/Mukilkumar-SEC/Simulation-project--Digital-Electronics/assets/119559663/172bfaba-8e9f-4445-a56a-2a5a6cd5fb9d)






## TIMING DIAGRAM :
![240556624-cbd70e07-f80f-4ac2-8310-cac2841e9678](https://github.com/Mukilkumar-SEC/Simulation-project--Digital-Electronics/assets/119559663/81a29f95-24f6-4e16-9995-2e9b52173748)






## RESULT :
Thus the Design and simulation of mod 12 synchronous upcounter with T flip flop using Verilog is successfully completed


## REFERENCE :
https://www.scrsdgibd.com/document/21400435234634/upcounterss
