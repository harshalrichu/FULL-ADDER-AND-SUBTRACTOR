## FULL-ADDER-AND-SUBTRACTOR
## AIM:
To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

## Full Adder and Full Subtractor
## Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin

Carry = AB + ACin + BCin

<img width="596" height="272" alt="image" src="https://github.com/user-attachments/assets/eb555bc6-1f0c-4e8a-b944-31ed5e8ac2dd" />


## Figure -1 FULL ADDER
## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

<img width="648" height="256" alt="image" src="https://github.com/user-attachments/assets/6d2eafff-f9e3-4a7b-b3bb-0189473e71cc" />


Diff = A ⊕ B ⊕ Bin

Borrow out = A'Bin + A'B + BBin

## Truthtable
## Procedure
1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram Write the detailed procedure here

## Program:
```


module fulladder(input A,B,Cin,output SUM,CARRY,BO,DIFF);
//nput A,B,Cin;
//output SUM,CARRY,BO,DIFF;
//Full adder logic
assign SUM=A^B^Cin;
assign CARRY=((A&B)|(B&Cin)|(A&Cin));
//Full Subtractor logic
assign DIFF=A^B^Cin;
assign BO=((~A&B)|(B&Cin)|(~A&Cin));
endmodule
```
## RTL Schematic
<img width="795" height="471" alt="image" src="https://github.com/user-attachments/assets/f56dcf68-3eb4-422f-a898-1f9b8c1258ab" />

<img width="843" height="107" alt="image" src="https://github.com/user-attachments/assets/ab32d39b-de0c-4d1b-b007-83a3f0f17ec2" />


## Result:
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.
