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

FULL ADDER

<img width="429" height="395" alt="388825036-4d112be1-6902-42f6-a80f-d6ffa1814c34" src="https://github.com/user-attachments/assets/047ea97b-4e36-47aa-97ed-5f36f728b2b0" />

FULL SUBTRACTOR

<img width="438" height="393" alt="388825191-affd2a74-295b-48dc-b7c5-3e2de75db7d3" src="https://github.com/user-attachments/assets/2ff4f13f-05ca-4fb2-8bec-bcba896f0343" />


**Procedure**
Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.

**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 

Developed by: JAGAN KUMAR V

RegisterNumber: 25012671

**Full Adder**
```
module exp4(df,bo,a,b,bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=w1^bin;
assign bo=w2|w3;
endmodule
```

**FULL SUBTRACTOR**
```
module full_subtractor(diff, borrow, a, b, bin);
  output diff;
  output borrow;
  input a;
  input b;
  input bin;
  assign diff = a ^ b ^ bin;
  assign borrow = (~a & b) | (~(a ^ b) & bin);
endmodule
```
**RTL Schematic**
**FULL ADDER**

<img width="1177" height="744" alt="394118789-993f7ad7-9159-46a4-8769-48a7a7b701f3" src="https://github.com/user-attachments/assets/3bda36c5-a701-4c3e-a543-29efd30c541b" />

**FULL SUBTRACTOR**
<img width="1351" height="542" alt="394120412-5d7d76ec-1151-443f-adde-8d9412dd223b" src="https://github.com/user-attachments/assets/a120a6c1-ab3f-4995-af32-2bbda1090d3c" />


**Output Timing Waveform**

**FULL ADDER**
<img width="1920" height="1201" alt="394119650-3bc3543a-312f-4602-b767-8f7462e5c877" src="https://github.com/user-attachments/assets/f9de590b-161b-41fb-97f6-911d3df187ad" />

**FULL SUBTRACTOR**
<img width="1921" height="1201" alt="394120866-0d64db0f-5039-49e4-89e9-02676e122512" src="https://github.com/user-attachments/assets/f7715fbc-4fc9-4bec-abb4-bb0b8cb46b52" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



