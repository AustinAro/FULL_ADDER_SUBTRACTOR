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

1.![Screenshot 2024-11-28 110533](https://github.com/user-attachments/assets/c41e00a9-3c7e-49b3-9490-e47c6d70caee)

2.![Screenshot 2024-11-28 113437](https://github.com/user-attachments/assets/ac3fab4e-87b7-496d-a10c-7c6af4f57a37)



**Procedure**

Write the detailed procedure here

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

**Program:**

1.Full Adder:
module full(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule

2.Full Subtractor:
module sub (a,b,bin,diff,bout);
input a,b,bin;
output diff,bout;
assign diff=((a^b)^bin);
assign bout=(~a & b)|(bin&~(a^b));
endmodule

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/24900653

**RTL Schematic**

1.![Screenshot 2024-11-28 110036](https://github.com/user-attachments/assets/b02246c8-7b45-4215-ab96-73dde3b53da7)

2.![Screenshot 2024-11-28 112806](https://github.com/user-attachments/assets/be349f7e-0515-4cdd-8379-5f8daa53a393)



**Output Timing Waveform**

1.![Screenshot 2024-11-28 110118](https://github.com/user-attachments/assets/ca23c3c0-a146-422f-8748-ddcf9885191f)

2.![Screenshot 2024-11-28 113008](https://github.com/user-attachments/assets/e395839b-844b-425b-a375-25adc12441e8)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



