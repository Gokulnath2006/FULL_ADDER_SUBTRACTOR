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

Full Adder

![437919745-bf0a7383-16c4-40b4-89f5-7f1a37a976ee](https://github.com/user-attachments/assets/1b1be712-fcc7-42bc-b2a2-bb412c4d0972)

Full Subtractor

![437920294-b6626bf9-62da-4a22-86ac-6e41daf3dd29](https://github.com/user-attachments/assets/fdff2b6e-5c7f-46c9-afc0-4ff8d26905ab)

**Procedure**

Full Adder:
1.Open Quartus II and create a new project.
2.Use schematic design entry to draw the full adder circuit. 
3.The circuit consists of XOR, AND, and OR gates. 
4.Compile the design, verify its functionality through simulation. 
5.Implement the design on the target device and program it.

Full Subtractor: 
1.Follow the same steps as for the full adder. 
2.Draw the full subtractor circuit using schematic design. 
3.The circuit includes XOR, AND, OR gates to perform subtraction. 
4.Compile, simulate, implement, and program the design similarly to the full adder.

**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: Gokul Nath R
RegisterNumber: 212224230077
```
Full Adder: 

module ex(a,b,cin,sum,carry);
input a,b,cin;
output sum, carry;
assign sum=(a^b^cin);
assign carry=((a&b)|(b&cin)|(cin&a));
endmodule

Full Subtractor:

module ex2(a,b,bin,borr,diff);
input a,b,bin;
output diff, borr;
assign diff=(a^b^bin);
assign borr=((~a&b)|(b&bin)|(bin&~a));
endmodule
```


**RTL Schematic**

Full-Adder
![436615545-5162ba9f-c163-4f15-a3e8-cd332e4e65d7](https://github.com/user-attachments/assets/9feea9c0-452d-4f61-bb66-d0076f90be3f)

Full-Subtractor
![image](https://github.com/user-attachments/assets/a7fb07d3-c4cf-441f-adb6-4ffe9bb1370e)

**Output Timing Waveform**

Full-Adder
![436616282-ff749d6c-e583-4b61-96a5-5ed686eaede6](https://github.com/user-attachments/assets/e96c014a-44d5-4d97-9e3a-ce3841dada74)

Full-Subtractor
![436616526-ca2f3407-0524-48cd-9952-8df9faf8c5a7](https://github.com/user-attachments/assets/9ce00729-c0d7-4155-b9b6-f3d9ee1156b3)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



