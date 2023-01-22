# Experiment--04-Implementation-of-combinational-logic-using-universal-gates
Implementation of combinational logic using universal-gates
 
## AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. 

## Using NAND gates
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## Logic Diagram

Using NOR gates
NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

## Logic Diagram
## Procedure
## Program:
/*
Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming.
Developed by: Lokesh N
RegisterNumber:  22008481
*/
Using NANAD gate

   module exp1(a,b,c,d,f);
   
   input a,b,c,d;
   
   output f;
   
   wire p,q,r;
   
   assign p=(~c & b & a);
   
   assign q=(~d & c & ~a);
   
   assign r=(c & ~b & a);
   
   assign f=(~(~p & ~q & ~r));
   
   endmodule

Using NOR gate

   module exp2(a,b,c,d,f);
   
   input a,b,c,d;
   
   output f;
   
   wire p,q,r;
   
   assign p=( c & ~b & a);
   
   assign q=( d & ~c & a);
   
   assign r=( c & ~b & a);
   
   assign f=(~(~( p | q | r)));
   
   endmodule

## RTL realization

## Output:
Using NAND gates
## RTL
![image](https://user-images.githubusercontent.com/119393019/213904173-5958fd82-0eb9-47ad-b00d-0ecf2365e106.png)

## Timing Diagram
![image](https://user-images.githubusercontent.com/119393019/213904182-cbd28e1d-4e69-4a8c-8b01-08a8bfe9f71e.png)

## Truthtable 
![image](https://user-images.githubusercontent.com/119393019/213904381-2a3258ea-d31f-4906-87e8-b6b3b7ed7e31.png)

Using NOR gate

## RTL
![image](https://user-images.githubusercontent.com/119393019/213904366-058259af-0d64-447e-8cbc-eea9ee4ec07f.png)


## Timing diagram
![image](https://user-images.githubusercontent.com/119393019/213904356-675c8dec-8123-4b28-b91a-5ea38119567b.png)


TRuth table 
![image](https://user-images.githubusercontent.com/119393019/213904326-0b10fed3-a4f7-4c13-9cea-9941dc054c63.png)

## Result:
Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
