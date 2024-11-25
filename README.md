Name: SYED KASHIF S

Register Number: 24006084

EXP3: HALF ADDER AND SUBTRACTOR
Implementation-of-Half-Adder-and-Half Subtractor-circuit

AIM:

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

Equipments Required:

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

Half Adder

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/user-attachments/assets/c8ef42cb-8a6b-4f4d-9711-088fbad2db7b)


Figure -01 HALF ADDER

Half Subtractor

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.

Diff = A’B+AB’ =A ⊕ B Borrow = A’B

![image](https://github.com/user-attachments/assets/bb700b07-03ac-4a78-8a8c-4b32f23e14e3)


Figure -02 HALF Subtractor

Truthtable

Half Adder
![image](https://github.com/user-attachments/assets/0db9e8fe-2635-4642-890e-42e4a188c435)

ha truthtable

Half Subtractor
![image](https://github.com/user-attachments/assets/c5dbb06a-ae55-4a69-865f-b0a326a8df5c)


Procedure

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

Program:

Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Half Adder

module hadd(a,b,sum,cout);
input a,b;
output sum,cout;
xor g1(sum,a,b);
and g2(cout,a,b);
endmodule 
Half Subtractor

module hsub(a,b,sub,bout);
input a,b;
output sub,bout;
wire w1;
xor g1(sub,a,b);
not g2(w1,a);
and g3(bout,w1,b);
endmodule 
RTL Schematic

Half Adder
![image](https://github.com/user-attachments/assets/67a5c9ae-0b9b-47e0-aa6a-996a2f9ed31a)

Half Subtractor
![image](https://github.com/user-attachments/assets/771f4976-4780-4248-9c0a-5f11132fca55)


Output/TIMING Waveform

Half Adder

![image](https://github.com/user-attachments/assets/107f38cb-a15c-4448-8760-d0579500da98)


Half Subtractor

![image](https://github.com/user-attachments/assets/e7e10437-c74d-48a7-8c82-9564c431f019)


Result:

Thus the half adder and half subtractor circuits were successfully designed, and their truth tables were verified in Quartus using Verilog programming.
