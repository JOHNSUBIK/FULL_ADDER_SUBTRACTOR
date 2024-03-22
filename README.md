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
Full_adder
![313682716-0b18ce6a-ab4d-42f7-aff3-e6422eb679df](https://github.com/Hezron-lix/FULL_ADDER_SUBTRACTOR/assets/139331337/081ddba5-c4a4-4e59-b7ec-f0bca74e533a)

Full_subtractor
![313682752-c874805b-a6bc-430e-97ce-77aa6b706b66](https://github.com/Hezron-lix/FULL_ADDER_SUBTRACTOR/assets/139331337/07276c8a-6060-4194-8294-a822c948800a)

**Procedure**

## Full Adder:
1.Open Quartus II and create a new project.
2.Use schematic design entry to draw the full adder circuit. 
3.The circuit consists of XOR, AND, and OR gates. 
4.Compile the design, verify its functionality through simulation. 
5.Implement the design on the target device and program it.

## Full Subtractor: 
1.Follow the same steps as for the full adder. 
2.Draw the full subtractor circuit using schematic design. 
3.The circuit includes XOR, AND, OR gates to perform subtraction. 
4.Compile, simulate, implement, and program the design similarly to the full adder.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
## Full_adder
```
module fulladd_top(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
wire w1,w2,w3,w4;       
xor(w1,a,b);
xor(sum,w1,cin);        

and(w2,a,b);
and(w3,b,cin);
and(w4,cin,a);

or(carry,w2,w3,w4);
endmodule
```

## Full_subtractor
```
module fullsub_top(a,b,Bin,BO,DIFF);
input a,b,Bin;
output BO,DIFF;
assign DIFF = a ^ b ^ Bin;
  assign BO = (a & b) | ((a ^ b) & Bin);
endmodule
```
Developed by: JOHN PAUL J
RegisterNumber: 21222320093
*/

**RTL Schematic**

![313683672-711ef60b-64a8-4ae0-88db-d56af7d28291](https://github.com/Hezron-lix/FULL_ADDER_SUBTRACTOR/assets/139331337/bb5d6aba-b187-46b7-857d-617ac2d3ea89)

**Output Timing Waveform**
Full_adder
![313683969-1ebe8851-dd84-47c0-a6e2-040e73a61d8e](https://github.com/Hezron-lix/FULL_ADDER_SUBTRACTOR/assets/139331337/7ac86948-5e35-41f6-ab82-89d86938f436)


Full_subtractor
![313684102-32788124-8d44-469f-a1a2-92375eb05afb](https://github.com/Hezron-lix/FULL_ADDER_SUBTRACTOR/assets/139331337/47370fa6-6ee8-4273-bd2b-8e3f5eeb6c3b)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



