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
![WhatsApp Image 2025-12-05 at 11 54 12 AM](https://github.com/user-attachments/assets/72d99c2a-9f9f-43b4-b3dc-d19fee9ec871)
![WhatsApp Image 2025-12-05 at 11 54 11 AM](https://github.com/user-attachments/assets/f74b974b-9e21-4c72-9776-948b76140224)

**Procedure**

Write the detailed procedure here

**Program:**
```
module full_add_sub(
    input A, B, Cin,
    input Bin,
    output Sum, Carry,
    output Diff, Borrow
);
    assign Sum   = A ^ B ^ Cin;
    assign Carry = (A & B) | (B & Cin) | (Cin & A);
    assign Diff   = A ^ B ^ Bin;
    assign Borrow = (~A & B) | (Bin & ~(A ^ B));
	 
endmodule

```
 Developed by:MONIGA.A
 RegisterNumber:25017526

**RTL Schematic**
<img width="996" height="670" alt="Screenshot 2025-12-05 114102" src="https://github.com/user-attachments/assets/56ef3417-793f-4475-a2b1-947b85bbdd81" />

**Output Timing Waveform**
<img width="1920" height="1080" alt="Screenshot (66)" src="https://github.com/user-attachments/assets/b51d796d-7b50-4727-b4b1-3f23623cd348" />

**Result:**
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



