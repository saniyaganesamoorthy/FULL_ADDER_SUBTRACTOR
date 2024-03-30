# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by: SANIYA G 

RegisterNumber: 212223240147
```
module fulladder(a,b,c,sum,carry,BO,DIFF);
input a,b,c;
output sum,carry,BO,DIFF;
//FULL ADDER
assign sum =a^b^c;
assign carry =(a&b)|(a&c)|(b&c);
//FULL SUBTRACTOR
assign DIFF =a^b^c;
assign BO =(~a&c)|(~a&b)|(b&c);
endmodule
```
*/

**RTL Schematic**
## Full Adder:
![image](https://github.com/saniyaganesamoorthy/FULL_ADDER_SUBTRACTOR/assets/145742583/4853d65d-220a-4ebd-85c5-f2e8831c733c)

## Full Subtractor


![image](https://github.com/saniyaganesamoorthy/FULL_ADDER_SUBTRACTOR/assets/145742583/2c3646bd-f887-4889-94e0-850d67e2321f)


**Output Timing Waveform**
## Full Adder:
![image](https://github.com/saniyaganesamoorthy/FULL_ADDER_SUBTRACTOR/assets/145742583/c7266353-8c3d-4f01-9986-17d6240d0de4)

## Full Subtractor
![image](https://github.com/saniyaganesamoorthy/FULL_ADDER_SUBTRACTOR/assets/145742583/c70bde1f-4b44-4b70-89bd-04f875506dc8)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



