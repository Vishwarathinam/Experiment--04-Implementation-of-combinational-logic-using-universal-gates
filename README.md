### Experiment--02-Implementation-of-combinational-logic-using-universal-gates
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
Using NAND Operation:


module combine1(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R;
assign P = C&(~B)&(~A);
assign Q = D&(~C)&(~A);
assign R = (~C)&B&(~A);
assign F = (~P&~Q&~R);
endmodule

Using NOR Operation:

module combine2(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R,S;
assign P = C&(~B)&A;
assign Q = D&(~C)&A;
assign R = C&(~B)&A;
assign S = ~(P|Q|R);
assign F = ~S;
endmodule
```
*/


### Output:
### NAND:

### RTL:
![RTL](https://user-images.githubusercontent.com/95266350/231412582-15f82f50-a843-4f70-a373-ed6a096743c3.jpg)

### Truth Table:
![TRUTH1](https://user-images.githubusercontent.com/95266350/231413838-bc35330c-5736-41d5-9379-fe82b2ea6eba.jpg)

### Timing Diagram:
![TIMINGNAND](https://user-images.githubusercontent.com/95266350/231412814-0a595fd0-c497-46b3-9d2c-57db7a45e310.jpg)

### NOR:

### RTL:
![RTLNOR](https://user-images.githubusercontent.com/95266350/231413454-7e202a7b-6d48-414d-b40e-172adae4ad0c.jpg)

### Truth Table:
![TRUTHNOR](https://user-images.githubusercontent.com/95266350/231413616-e6abab28-04ea-4f58-9c19-52b7de59b8aa.jpg)

### Timing Diagram:
![timingnor](https://user-images.githubusercontent.com/95266350/231413755-8c903f2f-0377-4d6c-b03d-5703393fa8c0.jpg)

## Result:
Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
