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

**FULL ADDER:**
![318405960-7116d2bf-8e90-4e96-bfd5-d62af11a317a](https://github.com/Harsetha/FULL_ADDER_SUBTRACTOR/assets/149985878/bf991c76-3514-49ba-a639-9f05f9f223ab)


**FULL SUBTRACTOR:**
![318405667-33d8ba16-9169-40b0-8696-3bb8e5c3a0b7](https://github.com/Harsetha/FULL_ADDER_SUBTRACTOR/assets/149985878/8c8ef1a4-f72f-4bf5-b5c3-44e79137e955)



**Procedure**

Write the detailed procedure here

~~~
**Full Adder:**
1.Open Quartus II and create a new project.
2.Use schematic design entry to draw the full adder circuit. 
3.The circuit consists of XOR, AND, and OR gates. 
4.Compile the design, verify its functionality through simulation. 
5.Implement the design on the target device and program it.

**Full Subtractor:** 
1.Follow the same steps as for the full adder. 
2.Draw the full subtractor circuit using schematic design. 
3.The circuit includes XOR, AND, OR gates to perform subtraction. 
4.Compile, simulate, implement, and program the design similarly to the full adder.
~~~

**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

~~~
module EX04(a,b,c,sum,carry,BO,DIFF);
input a,b,c;
output sum,carry,BO,DIFF;

//FULL ADDER
assign sum = a^b^c;
assign carry = (a&b) | (b&c) | (a&c);
wire a0;
not (a0,a);

//FULL SUBTRACTOR
assign DIFF = a^b^c;
assign BO = (a0&b) | (b&c) | (a0&c);
endmodule

Developed by: HARSETHA J
RegisterNumber: 212223220032
~~~

*/



**RTL Schematic**

![328942316-e9367f12-3106-4725-a02e-344208308090](https://github.com/Harsetha/FULL_ADDER_SUBTRACTOR/assets/149985878/5d384cfb-d609-4d66-8528-8b9f5bf2c509)

**Output Timing Waveform**

![328942629-69b5d850-ba92-48c8-9eaa-3765ec2bb3a7](https://github.com/Harsetha/FULL_ADDER_SUBTRACTOR/assets/149985878/c9883618-4181-4182-83ec-818b7b1a3c44)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



