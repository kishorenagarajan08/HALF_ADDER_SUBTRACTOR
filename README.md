# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB


![image](https://github.com/kishorenagarajan08/HALF_ADDER_SUBTRACTOR/assets/155753188/06ae49c5-82a8-48a9-9527-092865de1932)


Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B


 ![image](https://github.com/kishorenagarajan08/HALF_ADDER_SUBTRACTOR/assets/155753188/5efd7c20-72a7-46ed-b010-5c7d1cadc509)


Figure -02 HALF Subtractor

**Truthtable**

![image](https://github.com/kishorenagarajan08/HALF_ADDER_SUBTRACTOR/assets/155753188/39f988be-f5e6-429b-b6cf-f670cdbf8438)

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: N.kishore  RegisterNumber:212223230106

**HALF_ADDER**
````
module half_adder(a,b,sum,carry);
input a,b;
output sum,carry;
assign sum = a^b;
assign carry = a & b;
endmodule
````

**RTL Schematic**

![Screenshot 2024-04-11 174412](https://github.com/anushanirudh/HALF_ADDER_SUBTRACTOR/assets/151725737/c9aaa982-5161-4358-9284-ba2790a24179)



**Output/TIMING Waveform**


![image](https://github.com/kishorenagarajan08/HALF_ADDER_SUBTRACTOR/assets/155753188/864f93ff-0c6f-4278-b975-49a7c53cce0d)


**HALF_SUBRACTOR**

````
module half_subtracter(a,b,D,Bo);
input a,b;
output D,Bo;
// Outputs sum and carry for half adder:Outputs difference D,Borrow Bo for half subtractor assign D = a ^ b;
assign Bo = ~a & b;
endmodule
````

**RTL Schematic**


![image](https://github.com/kishorenagarajan08/HALF_ADDER_SUBTRACTOR/assets/155753188/d600d6d6-5463-41c5-bbe3-4a62bafd842c)


**Output/TIMING Waveform**


![image](https://github.com/kishorenagarajan08/HALF_ADDER_SUBTRACTOR/assets/155753188/4edc4620-c660-4d5a-8ff7-19dfc6b936a9)




**Result:**

The program code is successfully executed.
