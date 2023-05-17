### Experiment--04-Implementation-of-combinational-logic-using-universal-gates
Implementation of combinational logic using universal-gates
 
### AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate
### Equipments Required:
### Hardware – PCs, Cyclone II , USB flasher
### Software – Quartus prime


### Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. 

### Using NAND gates
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

### Logic Diagram

Using NOR gates
NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

### Logic Diagram
### Procedure
### Program:
/*
Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming.
Developed by: Vishwa Rathinam S
RegisterNumber:  2122211240063

```
module exp4(a,b,c,d,w,x,y,z,fl,f2);
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
endmodule-0p-
```
*/


### Output:
### RTL realization of NAND and NOR gates:
![e1](https://github.com/Vishwarathinam/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/95266350/79dbc872-dc79-487e-a762-c10a27d6f654)

### Truth Table of NAND gate:
![img1](https://github.com/Vishwarathinam/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/95266350/82838256-efe4-476e-bc19-f727e3db522f)

### Truth Table of NOR gate:
![img 2](https://github.com/Vishwarathinam/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/95266350/acd52217-b0d2-4e98-8c86-c49f47bcbe82)

### Timing Diagram:
![vish](https://github.com/Vishwarathinam/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/95266350/a632314e-4ee9-436c-9013-6394eb7fbdad)

### Result:
Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
