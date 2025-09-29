**EXP.4 FULL_ADDER_SUBTRACTOR**

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**
## NAME : LOGU R
## REG NO : 212224230141

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
![Screenshot 2024-11-25 205106](https://github.com/user-attachments/assets/ecbc0c09-2b2f-47ce-a1a9-303012916553)
![Screenshot 2024-11-25 205632](https://github.com/user-attachments/assets/0451562c-f7b5-40b4-bffb-589452494658)

**Procedure**
```
1. Type the program in Quartus software.
2. Compile and run the program.
3. Generate the RTL schematic and save the logic diagram.
4. Create nodes for inputs and outputs to generate the timing diagram.
5. For different input combinations generate the timing diagram.
Write the detailed procedure here
```
**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
*/
```
module Full-adder(
input A,B,C,
output sum,carry);
wire w1 ,w2,w3;
assign sum=A^B^C;
assign w1=A&B;
assign w2=B&C;
assign w3=C&A;
assign carry = w1|w2|w3;
endmodule
```
```
module Full-subtractor(AB,binn,diff,borr);
inputA,Bbin;
output diff,borr;
wire w1,w2,w3,w4,w5,w6;
xor G1(Diff,A,B,bin);
and G2(w4,w1,B);
and g3(w5,w1,B);
and G4(w6,B,bin);
or G5(borr,w4,w5,w6);
endmodule
```

**RTL Schematic**
![Screenshot 2024-11-26 110321](https://github.com/user-attachments/assets/d26707a0-1149-4d18-99bc-23b079de237f)


**Output Timing Waveform**
![Screenshot 2024-11-26 110427](https://github.com/user-attachments/assets/e78b96c3-fbeb-4ec0-80b3-ba272234b813)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



