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

**Program:
```
module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^c);
assign carry= ( (a & b)| ( cin &(a ^ b ));
endmodule

module fs(a,b,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b )));
endmodule
```
Developed by: Nidishkumar S
RegisterNumber:24002777
*/

**RTL Schematic**
![WhatsApp Image 2024-12-03 at 13 44 58_7b892a4e](https://github.com/user-attachments/assets/95f934b7-5582-44d7-be45-50fd4845cb6b)

![WhatsApp Image 2024-12-03 at 13 58 27_c7bd3292](https://github.com/user-attachments/assets/bf27c1ba-c228-4961-b981-e70ec7f93ea4)

**Output Timing Waveform**
![WhatsApp Image 2024-12-03 at 13 47 45_f798fdbe](https://github.com/user-attachments/assets/1e94acf1-3dda-45fd-b460-5ab7c8afc20f)

![WhatsApp Image 2024-12-03 at 13 58 43_29dabf44](https://github.com/user-attachments/assets/3b474805-ef94-445e-9417-9b2b22ec34db)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



