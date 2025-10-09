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

**Truthtable**<br>
<img width="555" height="836" alt="image" src="https://github.com/user-attachments/assets/21fbe0d8-91cf-4b6c-8da7-3427e1d47ebc" /><br>
**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/<br>
25018432<br>
i)FULL ADDER<br>
module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule<br>
ii)FULL SUBTRACTOR<br>
module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule<br>
**RTL Schematic**<br>
<img width="965" height="518" alt="image" src="https://github.com/user-attachments/assets/cdf2e1d6-b440-4709-9fd5-227f26eb7752" /><br>
<img width="920" height="449" alt="image" src="https://github.com/user-attachments/assets/f22613cf-49d5-4105-92a6-269d0c43cfaf" /><br>
**Output Timing Waveform**<br>
<img width="771" height="518" alt="image" src="https://github.com/user-attachments/assets/8ca4b909-7d0b-46cf-ac71-ec1093a48730" /><br>
<img width="952" height="467" alt="image" src="https://github.com/user-attachments/assets/32ca0927-80a0-4ce9-847e-0c3124c3e480" /><br>

**Result:** <br>
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



