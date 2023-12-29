# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
## Theory:
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.
## Logic Diagram (using nand gate) and (using nor gate):
![Screenshot 2023-11-25 210856](https://github.com/dharshan7200/Experiment--02-Implementation-of-combinational-logic-/assets/138850116/112dff2e-a385-4bc3-b729-cf51cade9356)
![image](https://github.com/dharshan7200/Experiment--02-Implementation-of-combinational-logic-/assets/138850116/78ec00f6-e5c3-47af-9e8c-05218f9324fb)
## Procedure
*Create a project with required entities.
*Create a module along with respective file name.
*Run the respective programs for the given boolean equations.
*Run the module and get the respective RTL outputs.
*Create university program(VWF) for getting timing diagram.
*Give the respective inputs for timing diagram and obtain the results.
## Program:
```
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: TAMIZHSELVAN B
RegisterNumber: 23013460
module combinational(a,b,c,d,w,x,y,z,fl,f2);
input a,b,c,d,w,x,y,z;
output fl,f2;
wire g1=((~a)&(~b)&(~c)&(~d)); 
wire g2=((a)&(~c)&(~d));
wire g3=((~b)&(c)&(~d));
wire g4=((~a)&(b)&(c)&(d)); 
wire g5=((b)&(~c)&(d));
assign fl=g1|g2|g3|g4|g5; 
wire g6=((x)&(~y)&(z));
wire g7=((~x)&(~y)&(z));
wire g8=((~w)&(x)&(y)); 
wire g9=((w)&(~x)&(y));
wire g10=((w)&(x)&(y)); 
assign f2=g6|g7|g8|g9|g10;
endmodule
```
## OUTPUT:
## RTL realization of NAND AND NOR gates:
![Screenshot 2023-11-25 211738](https://github.com/dharshan7200/Experiment--02-Implementation-of-combinational-logic-/assets/138850116/4924c21c-22b0-4dcd-ae8f-50a3a8a9cd62)
## Truthtable of NAND gate:
![image](https://github.com/dharshan7200/Experiment--02-Implementation-of-combinational-logic-/assets/138850116/c327631d-3264-43be-8096-82067ac75a60)
## Truthtable of NOR gate:
![image](https://github.com/dharshan7200/Experiment--02-Implementation-of-combinational-logic-/assets/138850116/d148d3ff-a33b-49a7-9266-9524edaaccae)
## Timing Diagram:
![image](https://github.com/dharshan7200/Experiment--02-Implementation-of-combinational-logic-/assets/138850116/b79fbc34-a5df-42fa-83d5-c5fae61a7864)
## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
