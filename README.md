b# FULL_ADDER_SUBTRACTOR

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
![Screenshot 2024-12-27 131305](https://github.com/user-attachments/assets/f2687425-622f-4427-8980-323a7032d6af)


**Procedure**

Write the detailed procedure here
1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: Prathiksha .R RegisterNumber: 24900337*/
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
**RTL Schematic**

![Screenshot 2025-01-05 140724](https://github.com/user-attachments/assets/cc476308-c633-4d7b-b7ff-8b808f86f02a)
![Screenshot 2025-01-05 140728](https://github.com/user-attachments/assets/914ec701-fa00-4afb-b1c5-18c71131186b)


**Output Timing Waveform**
![Screenshot 2025-01-05 140745](https://github.com/user-attachments/assets/f89512e7-1a91-460a-9bfa-42de90a8747f)

![Screenshot 2025-01-05 140751](https://github.com/user-attachments/assets/800ebf05-af55-4436-a628-703d7ae3ea64)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



