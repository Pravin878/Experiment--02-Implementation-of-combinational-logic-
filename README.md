# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime

 

## Program:
/*
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: pravin kumar G
RegisterNumber: 212222230109 
*/
```
module Verilog1(a,b,c,d,w,x,y,z,F1,F2);
input a,b,c,d,w,x,y,z;
output F1,F2;
wire  A1,A2,A3,A4,A5,B1,B2,B3,B4,B5;
assign A1= (~a&(~b)&(~c)&(~d));
assign A2= (a&c&(~d));
assign A3= ((~b)&c&(~d));
assign A4= (~a&b&c&d);
assign A5= (b&(~c)&d);
assign F1= A1|A2|A3|A4|A5;
assign B1= (x&(~y)&z);
assign B2= (~x&(~y)&z);
assign B3= (~w&x&y);
assign B4= (w&(~x)&y);
assign B5= (w&y&z);
assign F2= B1|B2|B3|B4|B5;
endmodule		 
```

## Output:
## RTL
![image](https://user-images.githubusercontent.com/118799555/235272644-43e084f4-fab7-493d-8e81-fa27d492f6c3.png)

## Timing Diagram
![image](https://user-images.githubusercontent.com/118799555/235272659-76a578fc-ebb2-4c0c-ab8a-965f95e0af98.png)
## truth table
![image](https://user-images.githubusercontent.com/118799555/235272680-d9598a59-a846-4071-a8df-a15b1741aeb9.png)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
